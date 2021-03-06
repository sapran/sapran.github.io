---
layout: post
title: Spectre & Meltdown
subtitle: покрокове пояснення
date: 2018-01-05
author: Vlad Styran
excerpt_separator: <!-- more -->
---

Оригінал: [https://twitter.com/gsuberland/status/948907452786933762](https://twitter.com/gsuberland/status/948907452786933762)

### Інтро

Коли процесор доходить до умовного розгалуження у коді (наприклад, "if"), він намагається передбачити, яку гілку буде обрано в програмі, перш ніж програма сама взнає результат. І він виконує цю гілку заздалегідь - ця функція процесора називається "спекулятивне виконання".
<!-- more -->

Ідея полягає в тому, що якщо процесор правильно "вгадає" вибір програми (що усі сучасні процесори роблять досить добре), він вже виконає наступний біт коду до того часу, коли фактично стане відома обрана гілка. Якщо процесор помилиться, виконання "відкотиться" назад і почне виконання правильної гілки.

Що робить процесори такими успішними в прогнозуванні умовного вибору програм, – це збереження даних про попередні операції розгалуження в так званому Буфері історії розгалужень (Branch History Buffer, BHB). По принципу: якщо певна програма обирала шлях A раніше, вона, ймовірно, обере шлях А знову, замість шляху Б, який вона ще не обирала.

Цікаво, що код виконується "спекулятивно", до того, як результат умовного розгалуження буде завершено. Це умовне розгалуження може бути критично важливим для безпеки. На щастя, процесори (в основному) досить розумні, щоб "відкотити" назад будь-які побічні ефекти спекулятивного виконання.

Але існує два важливих винятки з цього "відкочування" побічних ефектів: кеш пам'яті та сама історія розгалужень (BHB). Ці дані, як правило, не відкочуються назад, оскільки спекулятивне виконання має на меті збільшення продуктивності процесора, а відкочування кеш-пам'яті та вмісту BHB, шкодить продуктивності.

Існує три способи експлуатації цієї поведінки. У документі Spectre описано перші дві експлойти з наступними результатами:

1. Розкриття пам'яті ядра користувацькому процесу на "залізі".
2. Розкриття пам'яті ядра хоста віртуальної машини (гіпервізора) процесу в "ядрі" віртуальної машини.

### Атака #1

Перший експлойт працює, змушуючи ядро виконати деякий ретельно підготовлений зловмисником код, який містить перевірку обмежень масиву, а потім читає цей масив, причому індекс читання контролюється зловмисником. Це звучить як зухвала ідея, але це не так завдяки JIT (Just in Time compiling).

В Linux, Extended Berkley Packet Filter (eBPF) дозволяє користувачам записувати фільтри сокетів з режиму користувача, які компілюються ядром JIT, щоб ефективно фільтрувати пакети на сокеті. Подробиці неважливі, але це означає, що зловмисник може виконати код на рівні ядра.

Експлойт передбачає написання коду eBPF, який виконує наступні кроки:
1. Виділяє два масиви фіксованого розміру
2. Перевіряє наданий користувачем індекс на входження в масив 1
3. Якщо все ОК, здійснює читання масиву 1 по цьому індексу
4. Обчислює другий індекс з одного біту отриманого результату
5. Читайте  по другому індексу з масиву 2

Насправді, є ще один крок 4.5, який здійснює граничну перевірку другого індексу по читанню, але ми не маємо наміру робити читання за рамками масиву 2, тому це не має значення.

З точки зору "реального" виконання, цей код завжди обривається на кроці 2, коли/якщо користувач передає індекс за межами  масиву 1. Але якщо процесор-"провидець" припускає, що перевірка буде успішною, він спекулятивно виконає читання з-поза меж архіву на кроці 3, та продовжить виконання аж до кроку 5.

Ось що прикольно. На кроці 4 ми беремо значення, яке ми отримали читанням з-поза меж масиву (куди ми, як правило, не маємо доступу), і використовуємо один біт (b) від нього, щоб вибрати конкретну адресу пам'яті (індекс масиву) для читання. Якщо b = 0, то читаємо індекс 0x200; якщо b = 1, то читаємо індекс 0x300.

Це гарантує, що пам'ять, на яку вказує індекс 0x200 або індекс 0x300 буде закешована. Коли процесор усвідомлює, що перевірка обмежень на кроці 2 провалилася, він "відкочується" назад до цього розгалуження, щоб продовжити виконання правильної гілки. Однак дані з кроку 5 все ще знаходяться в кеші!

Потім ми можемо піти й прочитати дані в 0x200 та 0x300 та пересвідчитися, що вони кешуються, вимірюючи швидкість читання. Щойно ми взнаємо, який індекс було закешовано, ми можемо безпосередньо визначити один біт з пам'яті ядра, виходячи з вибору індексу на кроці 4.

Є деякі деталі щодо того, як необхідно підготувати кеш перед цією атакою, але всі ці речі можна проробити у циклі в процесі непривілейованого користувача, щоб здійснити повний дамп пам'яті ядра.

### Атака #2

Друга атака, описана в статті Spectre, передбачає "отруєння" історії прогнозування розгалужень, щоб змусити процесор спекулятивно виконати код за адресою, визначеною зловмисником, що призведе до подальших атак на кеш, які описані вище.

Виконавши ретельно відібрану послідовність непрямих переходів (indirect jumps), зловмисник може заповнити історію прогнозування розгалужень таким чином, що він зможе вибирати, яку гілку буде спекулятивно виконано під час виконанні непрямого переходу.

Це може бути дуже круто. Якщо я знаю, що в коді ядра є фрагмент коду, який демонструє поведінку, подібну до нашого прикладу з eBPF вище, і я знаю, яка в цього коду адреса, я можу непрямо перейти до цього коду, і процесор спекулятивно виконає його.

Якщо ви маєте досвід експлуатації вразливостей такого класу, ви, ймовірно, впізнаєте в цьому дещо подібне до ROP-гаджета (Return-Oriented Programming gadget). Ми шукаємо послідовність коду в просторі ядра, що має правильну послідовність інструкцій, щоб отримати витік інформації через кеш.

Пам'ятайте, що виконання є лише спекулятивним - процесор пізніше зрозуміє, що у мене не було привілеїв перейти до цього коду, та видасть помилку. Тому цільовий код повинен здійснювати витік даних ядра через побічні канали кешу, як і раніше.

Ви також помітите, що нам потрібно знати адресу цільового коду ядра. З KASLR (Kernel Address Space Layout Randomization) це не так просто. Цей блог Project Zero пояснює, як можна перемогти KASLR, використовуючи прогнозування розгалужень та кешування як побічний канал, тому я не буду вдаватися до опису деталей: [https://googleprojectzero.blogspot.co.uk/2018/01/reading-privileged-memory-with-side.html](https://googleprojectzero.blogspot.co.uk/2018/01/reading-privileged-memory-with-side.html)

Надзвичайно круто те, що це працює поза межами віртуальних машин. Замість традиційного непрямого переходу (наприклад, jmp eax) ми можемо використовувати команду vmcall, щоб спекулятивно виконувати код в ядрі хоста VM (гіпервізору) таким же чином, як і в  ядрі нашої ​​VM.

### Атака #3 

Нарешті, є третій підхід. Він передбачає атаку очищення та перезавантаження (flush + reload) кешу на пам'ять ядра, подібну до першого варіанту атаки, але не вимагає виконання коду в ядрі - все це можна зробити в режимі користувача.

Ідея полягає в тому, що ми намагаємося прочитати пам'ять ядра за допомогою інструкції mov, а потім виконати вторинне читання пам'яті за адресою, отриманою на основі прочитаного значення. Якщо ви думаєте, що перший mov не буде виконано, оскільки ми знаходимося в режимі користувача і не можемо читати з адреси в пам'яті ядра, ви маєте рацію.

Хитрість полягає в тому, що мікроархітектурна реалізація команди mov містить перевірку рівня привілеїв доступу до сторінки пам'яті, яка сама є інструкцією розгалуження. Процесор може спекулятивно виконувати цю гілку, як і будь-які інші.

Отже, якщо ви можете "обігнати" переривання, ви можете спекулятивно виконати якусь іншу інструкцію, яка завантажує дані в кеш на основі значення, прочитаного з пам'яті ядра. Тепер це стає кеш-атакою, подібною до попередніх трюків.

Власне, це все.

Для повної інформації я рекомендую прочитати ці два документи, а також пости Project Zero, вказані вище.

[https://spectreattack.com/spectre.pdf](https://spectreattack.com/spectre.pdf)

[https://meltdownattack.com/meltdown.pdf](https://meltdownattack.com/meltdown.pdf)

---

Від себе: #бережіться :)
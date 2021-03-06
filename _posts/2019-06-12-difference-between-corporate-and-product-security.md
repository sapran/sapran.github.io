---
layout: post
title: Різниця між корпоративною та продуктовою безпекою
date: 2019-06-12
author: Vlad Styran
excerpt_separator: <!-- more -->
---

Серед українських організацій чи не найчастіше до нас звертаються ІТ-компанії. Тому хочеться розповісти про певний накопичений досвід. Цілком можливо, він стане в нагоді іншим організаціям в цій вертикалі, а може й організаціям з інших галузей. Тому якщо у вас є знайомий CIO/CTO ІТ-фірми, покажіть йому цей текст. Він писався для нього.
<!-- more -->

Звернення ІТ-компанії приблизно в одному випадку з десяти відбувається з власної ініціативи. В решті випадків причиною такого звернення є вимога замовника чи потенційного замовника її послуг. На відміну від багатьох моїх колег, я такий підхід вважаю цілком правильним, практичним та економічно виправданим. Ці компанії пишуть код буквально на замовлення. Цей код в більшості випадків приносить вигоду замовникам та робить життя багатьох тисяч людей комфортнішим та зручнішим. Тому вимагати від ІТ-компаній піклуватися про безпеку мають право або їхні замовники, або клієнти замовників. Якийсь віртуальний Вова Стиран може звісно походити поскиглити про гнітючу картину в безпеці ПЗ, але краще б він з однодумцями відкрив локальний чаптер OWASP та зробив знання про безпеку доступними в його регіоні для тих компаній та професіоналів, яким це потрібно. Що він, власне, і робить.

Але, при цьому звернення «по безпеку» від ІТ-компаній відбуваються трохи безсистемно і тут давайте зупинимось докладніше. Причина ховається в дуалізмі поняття про безпеку в будь-якій організації, яка створює інформаційні продукти або сервіси. З одного боку, є організаційна безпека: захист інформаційних систем та мереж, охорона інтелектуальної власності, виконання вимог місцевих та міжнародних регуляторів тощо. Тобто, захист інтересів бізнесу як сутності: щоб він не збанкрутував, а його керівники не сіли у в’язницю. З іншого боку, є безпека інженерна: захист власне продуктів та сервісів від зловживань неавторизованих осіб, захист користувачів та їхніх даних від наслідків таких зловживань, а також захист бізнес-моделі як від третіх осіб, так і від авторизованих користувачів (наприклад, ліцензування ПЗ або DRM). Тобто, захист продукту діяльності бізнесу та можливості його перетворити на прибуток.

Годі й казати, що ці дві “безпеки” є досить різними областями знань. На жаль, цей факт відомий далеко на всім керівникам. Деколи це призводить до того, що за Application Security в компанії відповідають операційні ІБшники, що стаж причиною купи непорозумінь та додаткового “тертя” в стосунках ІТ та бізнесу. Трохи рідше, програмістів з продуктової розробки обтяжують операційними завданнями — оце коли розгорається справжня драма. В казці із щасливим кінцем, в обох випадках всі дійові особи зрештою досягають консенсусу та розподіляють обов’язки більш-менш органічно. В противному випадку, деколи доходить до робочих конфліктів, і тоді все залежить від дипломатичності та професіоналізму його учасників.

Щоб зробити життя керівників ІТ-фірм та їхніх підлеглих трохи простішим, я сформулюю простий алгоритм прийняття рішення щодо того, яка саме безпека потрібна організації, та як рухатися в напрямку її досягнення.

1. З’ясуйте, що ви захищаєте:

А: фірму, з усіма її активами, персоналом, фінансовими таємницями, від дій кіберзлочинців та наслідків дії законів та галузевих стандартів,
чи

Б: продукт/сервіс, який ця фірма виготовляє, від атак кіберзлочинців та зловмисних дій користувачів.

А.2. У першому випадку довіряйте виконання задачі спеціалістам з безпеки, які займаються технічним захистом інформації та організаційними заходами ІБ. Такі спеціалісти виходять, наприклад, з горнила кадрової кузні банківської системи, або з класичних ІТ-інтеграторів та дистриб’юторів. В минулому вони зазвичай працівники операційних підрозділів ІТ: системні та мережеві адміністратори. Деколи — працівники правоохоронних органів.
Ключові слова: CISSP, CISM, Information Security, Security Administration.

Б.2. У другому випадку довіряйте виконання задачі спеціалістам з безпеки програмного забезпечення. Такі спеціалісти менш поширені на ринку праці та володіють дещо іншими навичками. В минулому вони програмісти, тестувальники або ж розпочали кар’єру одразу ж в Application Security. Скоріш за все, вони беруть участь в програмах Bug Bounty у вільний час. 
Ключові слова: OSCP, OSCE, Application Security, Bug Bounty, White-Hat Hackers.

А.3. Методичних рекомендацій та галузевих стандартів (тобто вказівок, як будувати безпеку, коли не знаєш, як це робити) у першому випадку навіть занадто багато. Скоріш за все ви матимете справу із ISO 27001, SOC 2, NIST, CIS або іншим фреймворком. Беріть це до уваги, коли обираєте виконавців та керівників операційної ІБ.

Б.3. Щодо безпеки ПЗ, тут рекомендацій теж вистачає, а ось із стандартами поки що все глухо (і на мою думку це добре). Рекомендації з безпечної розробки можна шукати по ключових словах OWASP, SAMM, SDL, NIST. Керівники функцій безпечної розробки повинні мати не лише образне уявлення про ці процеси, але й вміти їх ефективно впроваджувати та вдосконалювати.

А.4. Залучення зовнішніх консультантів до технічної та організаційної ІБ може відбуватися в багатьох форматах, але зазвичай це або побудова чогось швидше, ніж ви можете це зробити самотужки, або перевірка якості ваших заходів безпеки. Аудит та консалтинг в цій галузі досить прибуткові види діяльності, якщо ви розумієте про що я. Тому тут треба бути дуже уважними на всіх стадіях формулювання та виконання проектів, адже скоуп розповзається з першого дня, а невраховані очікування можуть виявитися на завершальних стадіях.
Ключові слова: CISA, CISSP, ISO27001LA, ISO27001LI, Penetration Test, Security Audit.

Б.4. Залучення зовнішнього ресурсу до процесів безпечної розробки можливе майже на всіх стадіях побудови ПЗ за виключенням, хіба що, формулювання бізнес-ідеї. Дизайн, архітектура, планування, реалізація, тестування, міграція, підтримка, робота з інцидентами — всі ці та інші фази можуть виконуватися як власними силами, так і виноситися на аутсорс. Але є один момент: на певному етапі розвитку проекту існування власної внутрішньої функції стане набагато ефективнішим та вигіднішим. Використання послуг незалежної перевірки/тестування безпеки та ad-hoc консалтинг, скоріш за все, доведеться залишити, але в ході розробки, вдосконалення та інтеграції продукту стане актуальним власний спеціаліст з безпеки ПЗ або навіть цілий підрозділ.
Ключові слова: OWASP, OSWE, OTG, ASVS, SAMM, Application Security Assessment, Application Penetration Test.

5. Розміщення підрозділу безпеки в організаційній структурі — окрема складна та драматична тема. Багато прихильників “хороших практик” управління безпекою наполягають, що підпорядкування CISO (Chief Information Security Officer) до CIO — погана ідея, адже таким чином виникає конфлікт інтересів: ІТ-директор наполягає на доступності та продуктивності систем та сервісів, коли керівник ІБ накладає на них купу обмежень. У випадку організаційної безпеки, можливо, це твердження і є доцільним, але коли мова йде про підпорядкування безпеки до CTO в продуктовій організації — конфлікт кудись зникає, адже саме СТО зацікавлений в безпеці сервісів та продуктів, що розробляються.

Сподіваюся, ці нотатки допоможуть вам правильно зорієнтуватися в тематиці та обрати правильну стратегію. Або принаймні зекономлять трохи часу.

#Бережіться.
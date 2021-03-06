---
layout: post
title: Як хакери отримують ваші паролі
subtitle: та як цьому запобігти
date: 2016-07-17
author: Vlad Styran
---

Більшість програм, які обробляють чи зберігають цінні дані, реалізують один з методів ідентифікації користувачів. Абсолютна більшість з них використовує автентифікацію за іменем користувача та паролем, з якою знайомий кожен відвідувач інтернету. Інші методи ідентифікації користувачів можуть використовувати біометричні дані (відбиток пальця, сітківку ока, форму долоні та ін.), фізичні ключі (магнітні та смарт-картки, цифрові токени та ін.), або ж комбінацію з двох чи навіть усіх трьох факторів автентифікації.

Пропускаючи роздуми про надійність паролів як методу автентифікації, давайте одразу перейдемо до того місця, де хакери крадуть ваші паролі. Так, паролі є однією з найпопулярніших цілей кібер-злочинців з двох причин:

1. По-перше, і це очевидно, отримання вашого паролю надає будь-кому доступ до цінних даних у відповідній системі – службі електронної пошти, соціальній мережі, чи корпоративній мережі вашого роботодавця - до яких у вас є легітимний доступ. Іншими словами, всі ваші дані, накопичені до цього часу, тепер не ваші і з цим фактом доведеться жити навіть після виявлення компрометації та зміни паролю.

1. По-друге, і це для багатьох буває сюрпризом, отримавши доступ до вашого аккаунту, зловмисник може, видаючи себе за вас, використовувати довіру ваших рідних, друзів, колег та просто знайомих, для поширення шкідливих програм або нелегального вмісту. І під нелегальним вмістом я маю на увазі не DVD-ріпи чи музику в MP3, а бази даних викрадених кредитних карт та дитячу порнографію. Компрометація довіри може набувати катастрофічних масштабів для жертви та її оточення, включаючи роботодавців та бізнес-партнерів.

Отже, яким саме чином хакери можуть дізнатися ваш пароль, та наскільки складно це зробити? Забігаючи наперед, відповім на друге питання: це залежить лише від вас та адміністратора системи, до якої ви здійснюєте доступ з таким паролем. А методи отримання паролів ось такі:

### 1. Підбір пароля онлайн

Коли сервіс або програма дозволяє доступ по мережі, а в наш час інакше майже не буває, хакер може спробувати підібрати ваш пароль, знаючи ваше ім'я користувача (що зазвичай не є великою таємницею) та озброївшись списком "популярних" паролів, які були вкрадені ним або іншими хакерами в минулому. Ця процедура досить тривіальна, до того ж до послуг нападника декілька ефективних та безкоштовних інструментів її автоматизації, тому атака підбору пароля "за словником" не вимагає якихось спеціальних знань та навичок.

Отже, якщо ваш пароль ненадійний та міститься в одній з "колекцій" паролів (а їх в інтернеті чимало та більшість – безкоштовні), від підбору його захищає лише час, потрібний для здійснення атаки. Цей час залежить від швидкості роботи системи, професіоналізму її адміністратора, пропускної здатності мережі тощо. Але в одному можна бути впевненим: з часом такий пароль обов'язково зламають.

### 2. Підбір пароля оффлайн

Коли сервіс або програма містить вразливості безпеки, які дозволяють хакеру здійснити несанкціонований доступ до їхніх нутрощів (наприклад, бази даних), це може призвести до викрадення паролів користувачів у зашифрованому, або точніше хешованому вигляді. На жаль, трапляються випадки, коли паролі зберігаються в базі в чистому вигляді, тоді компрометація системи рівнозначна їх викраденню. Але про це згодом.

~~~
Plain text password:	my5uperDup3r$ecurePWD
MD5 hash (old *NIX):	eea2f7abd226770f85fbf69f836a3caf
LM hash (old Win):	AAD3B435B51404EEAAD3B435B51404EE
NTLM hash (new Win):	244936F66C0BFF1C222011AA6D41AC2F
SHA1 hash:	2c3d59e5df90826f5dde14104ecaa708544da842
SHA256 hash:	57b1c949176683545fd1f8b7e8a74ff6b08d1936da875000a0e5f5f23929d18f
~~~

Отримавши доступ до бази даних хешованих паролів, хакер починає підбирати їхні незашифровані значення. Умовно це можна уявити як перебір усіх можливих текстових рядків, їх хешування у вигляд, в якому зберігаються паролі в пограбованому сервісі, та порівняння отриманих результатів із значеннями у викраденій базі даних. Отримавши збіг хешованих даних, хакер отримує відкрите значення паролю. Звісно, в реальності цей процес трохи складніший та набагато швидший завдяки сучасним методам оптимізації. І звичайно ж в десятки мільйонів разів швидший за онлайн-підбір.

### 3. Повторне використання пароля

Не секрет, що багато користувачів використовують один пароль в декількох системах. На жаль, це поширена практика, дехто навіть скрізь використовує всього один пароль та гордо називає його "улюбленим". Погана новина в тому, що витоки баз даних паролів відбуваються щодня, після чого ці бази або стають доступними публічно, або продаються на чорному ринку. Тому знайшовши пароль користувача з логіном vpupkin@gmail.com у викраденій базі аккаунтів ВКонтакте, хакер перевірить, чи підходить він в Однокласниках, Facebook та на VPN-сервері його компанії-роботодавця.

Дізнатися про те, як часто та в яких масштабах трапляються витоки баз даних паролів, можна на веб-сайті [https://haveibeenpwned.com](https://haveibeenpwned.com). Там же можна перевірити, які з ваших паролів в інтернеті вже було скомпрометовано та підписатися на повідомлення про майбутні злами.

### 4. Викрадення або підглядання пароля

Найбільш різноманітним методом отримання наших паролів є їх викрадення з систем, в яких вони зберігаються або застосовуються. Зробити це можна порівняно просто: піддивившись як користувач вводить пароль в форму автентифікації; трохи складніше: знайшовши та використавши програмну вразливість в відповідній системі; або ж скориставшись методами соціальної інженерії для захоплення контролю над комп'ютером цілі та пошуку паролів у пам'яті та на диску комп'ютера.

В результаті хакер може заволодіти або паролем в чистому вигляді, або його хешем, який він згодом підбере оффлайн.

### 5. Відновлення пароля через email або SMS

Більшість гідних поваги інтернет-сервісів дозволяють користувачам відновити втрачений чи забутий пароль за допомогою email або номера телефону, який використовувався під час реєстрації. (Менш підковані використовують для цього відповіді на "секретні питання", які зазвичай не є такими вже й секретними). Отже, отримавши доступ до номеру телефону або, що значно легше, до електронної пошти користувача, хакер може скористатися легітимною процедурою відновлення пароля.

### 6. Перехоплення пароля по мережі

Досить популярний колись метод перехоплення пароля шляхом прослуховування мережевого трафіку став тепер менш поширеним через масову адоптацію криптографії інтернет-сервісами. Тепер майже усі популярні веб-сайти забезпечують доступ по HTTPS, причому більшість вимагає цього за замовчуванням. В таких умовах прямий перехват та аналіз мережевих пакетів стає неефективним.

{:refdef: style="text-align: center;"}
![SinffPass](/img/sniffpass.gif)
{:refdef}

Сподіваюся, мені вдалося скласти загальну картину того, як важко зберегти ваші паролі в таємниці, якщо не докладати до цього жодних зусиль. У наступному пості я розкажу про прості та надійні засоби захисту, які може використати будь-хто для збереження своїх паролів та захищених ними секретів.

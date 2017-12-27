---
layout: post
title: Месенджери та URL-посилання 
subtitle: Що відбувається, коли ви відсилаєте лінк?
date: 2016-11-22
author: Vlad Styran
excerpt_separator: <!-- more -->
---
Нещодавно в інтернеті знову набули популярності історії про шкідливі програми, які поширюються в SVG файлах, відправлених в Facebook. Ви можете дізнатися більше про цей вектор атаки та методи зловмисників в [цьому пості](https://bartblaze.blogspot.com/2016/11/nemucod-downloader-spreading-via.html), але мою увагу привернуло інше.

Як ви, напевно, знаєте, SVG це векторний графічний формат, який, по суті, є файлом XML, що містить інструкції з малювання різних зображень та, що декому може здатися дивним, може містити програмний код JavaScript. Ось приклад SVG, відкривши який в більшості сучасних браузерів, ви побачите синє коло та запустите зовнішній сценарій, на який вказує відредаговане посилання:

![SVG keylogger](/img/avakl.png)

<!-- more -->
На щастя, це спрацює лише тоді, коли в адресному рядку браузера явно вказати URL SVG-файлу, або ж якщо файл буде відкрито з диска; `<IMG SRC =` більш не працює з очевидних причин.

Отже, коли тема поширення шкідливих програм в SVG піднялася знову, цього разу в контексті недостатньої фільтрації вмісту в Facebook Messenger, я подумав про наслідки для приватності, які несе цей (мабуть що, не дуже ефективний) захід безпеки. Я гадав, що було б гарною ідеєю використати JavaScript-код в зображенні SVG, щоб перевірити, як сучасні месенджери обробляють цей формат файлів.

Після низки повідомлень, відправлених моїй дружині та колегам, я сподіваюся, що мені не заборонять використовувати месенджери, які я використав під час тестування. І, звичайно ж, у мене є чим з вами поділитися.

Гарна новина полягає в тому, що **Siganl**, **Viber**, **WhatsApp**, та **Facebook Messenger** і **Telegram** в своїх «секретних» режимах, не брешуть, стверджуючи, що шифрують повідомлення з кінця в кінець. Хоча, в разі WhatsApp і Telegram, вставлені в повідомлення URL викликали деяку активність з боку клієнта, крім цього ніхто більше не "з'явився" в журналах веб-сервера.

Погана новина в тому, що на цьому хороші новини закінчуються.

Розпочнемо з очевидного: Slack здійснює активний перегляд вмісту за посиланням для того, щоб показати його в графічному інтерфейсі. Це круто, ми всі знаємо що так і потрібно, в цьому пості я просто використаю це в якості прикладу того, як ця діяльність виглядає. Отже, коли ви відправляєте посилання, веб-сервер, що його містить, реєструє в журналі ось такий запит:

~~~
54.89.92.4 — — [21/Nov/2016:16:02:31 +0000] “GET /avakl.js HTTP/1.1” 404 152 “-” “Slackbot-LinkExpanding 1.0 (+https://api.slack.com/robots)"
~~~

Де 54.89.92.4 це, звичайно, один з інстансів Slack в Amazon AWS:

~~~
$ whois 54.89.92.4 | grep Organization
Organization: Amazon Technologies Inc. (AT-88-Z)
~~~

Давайте поглянемо, як інші месенджери поводяться з посиланнями.

Skype відправляє 6 запитів з 2 хостів, які напряму належать Microsoft. Багата компанія може собі це дозволити.

~~~
23.101.61.176 — — [21/Nov/2016:15:38:44 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “Mozilla/5.0 (Windows NT 6.1; WOW64) SkypeUriPreview Preview/0.5”
23.101.61.176 — — [21/Nov/2016:15:38:44 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “Mozilla/5.0 (Windows NT 6.1; WOW64) SkypeUriPreview Preview/0.5”
23.101.61.176 — — [21/Nov/2016:15:38:44 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “Mozilla/5.0 (Windows NT 6.1; WOW64) SkypeUriPreview Preview/0.5”
23.101.61.176 — — [21/Nov/2016:15:38:44 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “Mozilla/5.0 (Windows NT 6.1; WOW64) SkypeUriPreview Preview/0.5”
104.45.18.178 — — [21/Nov/2016:15:38:44 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “Mozilla/5.0 (Windows NT 6.1; WOW64) SkypeUriPreview Preview/0.5”
104.45.18.178 — — [21/Nov/2016:15:38:44 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “Mozilla/5.0 (Windows NT 6.1; WOW64) SkypeUriPreview Preview/0.5”
~~~

Telegram стягує картинку лише один раз, з його власної мережі.

~~~
149.154.167.163 — — [21/Nov/2016:15:35:18 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “TelegramBot (like TwitterBot)”
$ whois 149.154.167.163 | grep -E ‘^descr|^person|^address’
descr: Telegram Messenger Network
person: Nikolai Durov
address: P.O. Box 146, Road Town, Tortola, British Virgin Islands
descr: Telegram Messenger Amsterdam Network
~~~

URL, відправлений через Facebook Messenger на мобільному пристрої, викликає чотири запити.

~~~
31.13.102.98 — — [21/Nov/2016:19:44:51 +0000] “GET /avakl.svg HTTP/1.1” 206 328 “-” “facebookexternalhit/1.1 (+http://www.facebook.com/externalhit_uatext.php)"
173.252.120.119 — — [21/Nov/2016:19:44:52 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “facebookexternalhit/1.1 (+http://www.facebook.com/externalhit_uatext.php)"
173.252.123.130 — — [21/Nov/2016:19:44:53 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “facebookexternalhit/1.1 (+http://www.facebook.com/externalhit_uatext.php)"
173.252.123.129 — — [21/Nov/2016:19:45:12 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “-” “facebookexternalhit/1.1 (+http://www.facebook.com/externalhit_uatext.php)"
~~~

Facebook люб'язно пояснює свою поведінку за наданою URL.

![Facebook explanation](/img/fb_url.jpeg)

Однак, коли посилання надсилається через веб-сайт Facebook, подивіться, що відбувається:

~~~
31.13.113.194 — — [21/Nov/2016:15:11:58 +0000] “GET /avakl.svg HTTP/1.1” 206 328 “-” “facebookexternalhit/1.1”
66.220.145.243 — — [21/Nov/2016:15:12:01 +0000] “GET /avakl.svg HTTP/1.1” 200 328 “http://l.facebook.com/lsr.php?u=https%3A%2F%2F*******%2Favakl.svg&ext=1479741420&hash=AcnhtJ5F7tKqGD-kIHGSbCF0-TflNMaiR9WNCxHznoOqJw" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
66.220.145.243 — — [21/Nov/2016:15:12:01 +0000] “GET /kl.js HTTP/1.1” 200 283 “https://*******/avakl.svg" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
66.220.145.243 — — [21/Nov/2016:15:12:01 +0000] “GET /favicon.ico HTTP/1.1” 404 152 “https://*******/avakl.svg" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
66.220.145.243 — — [21/Nov/2016:15:12:03 +0000] “GET /keylogger? HTTP/1.1” 404 152 “https://*******/avakl.svg" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
66.220.145.243 — — [21/Nov/2016:15:12:04 +0000] “GET /keylogger? HTTP/1.1” 404 152 “https://*******/avakl.svg" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
66.220.145.243 — — [21/Nov/2016:15:12:05 +0000] “GET /keylogger? HTTP/1.1” 404 152 “https://*******/avakl.svg" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
66.220.145.243 — — [21/Nov/2016:15:12:06 +0000] “GET /keylogger? HTTP/1.1” 404 152 “https://*******/avakl.svg" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
66.220.145.243 — — [21/Nov/2016:15:12:07 +0000] “GET /keylogger? HTTP/1.1” 404 152 “https://*******/avakl.svg" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
66.220.145.243 — — [21/Nov/2016:15:12:08 +0000] “GET /keylogger? HTTP/1.1” 404 152 “https://*******/avakl.svg" “Mozilla/5.0 (Windows NT 10.0; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0”
~~~

Пояснюю. Спершу якийсь хост Facebook підтягує SVG-файл, а після цього відбувається низка запитів, які генеруються "вбудованим" в SVG скриптом, а це наочно демонструє, що сценарій насправді виконуються в якомусь "браузері". Цілком можливо, що це і є елемент фільтрації вмісту, тому що це відбувається не кожного разу та виглядає як начебто поведінка "живого" користувача. Все одно, це якось дивно :)

Як не дивно, **Google Hangouts** не показав жодних ознак інтересу до мого посилання.

Це залишає багато запитань відкритими, проте, очевидно одне: політики конфіденційності нам не брешуть і ми насправді не є власниками даних, які ми пересилаємо за допомогою месенджерів, якщо наше спілкування не зашифроване з кінця в кінець.

Під час цих тестів я використовував [дивовижний JavaScript-кейлоггер by John Leitch](http://www.xss-payloads.com/payloads/scripts/javascriptkeylogger.js.html).

Залишайтеся в безпеці.
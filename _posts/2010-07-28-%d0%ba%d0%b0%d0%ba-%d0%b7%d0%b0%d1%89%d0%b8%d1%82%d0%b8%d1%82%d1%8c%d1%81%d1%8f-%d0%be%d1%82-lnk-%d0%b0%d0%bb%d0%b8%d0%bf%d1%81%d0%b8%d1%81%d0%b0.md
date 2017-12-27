---
id: 1029
title: Как защититься от LNK-алипсиса
date: 2010-07-28T19:44:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/07/28/%d0%ba%d0%b0%d0%ba-%d0%b7%d0%b0%d1%89%d0%b8%d1%82%d0%b8%d1%82%d1%8c%d1%81%d1%8f-%d0%be%d1%82-lnk-%d0%b0%d0%bb%d0%b8%d0%bf%d1%81%d0%b8%d1%81%d0%b0/
permalink: /2010/07/%d0%ba%d0%b0%d0%ba-%d0%b7%d0%b0%d1%89%d0%b8%d1%82%d0%b8%d1%82%d1%8c%d1%81%d1%8f-%d0%be%d1%82-lnk-%d0%b0%d0%bb%d0%b8%d0%bf%d1%81%d0%b8%d1%81%d0%b0/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/07/lnk.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1179714913205306702
shorturl:
  - http://tinyurl.com/paqcpsj
tags:
  - 0-day
  - microsoft
  - sophos
  - антивирусы
---
Продолжаем тему LNK/Stuxnet. После опубликования двух предыдущих постов я получил аж три существенных замечания.

Я не предупредил, что **[quick-fix](http://support.microsoft.com/kb/2286198)** от Microsoft имеет один очевидный побочный эффект. Исправление _полностью_ отключает механизм отображения графических иконок в меню Пуск, Контрольной панели, Панели задач и т.д. То есть, вообще отключает. Выглядит это не очень красиво. Вот почему для истинных эстетов компания Sophos выпустила [**специальную бесплатную утилиту**](http://www.sophos.com/products/free-tools/sophos-windows-shortcut-exploit-protection-tool.html), которая а) ищет и удаляет Stuxnet-подобный вредоносный код с вашего ПК, и б) предотвращает заражение в будущем. Утилита будет также полезна ненавистникам [**MSSE**](https://www.microsoft.com/security_essentials/) и всем прочим жертвам стойкой аллергии на удачные продукты компании Microsoft.

Также, я получил несколько любопытных вопросов на тему &#171;а как же быть с серверами&#187;, в особенности с файловыми. Разумеется, наряду с флешками и компакт-дисками, файловые сервера также являются потенциальными путями распространения этой заразы. Хорошая новость, начиная с Windows 2003 R2 администратору доступен инструмент File Resource Manager. Воображаю, как админы заулыбались. Да-да, это как раз та тулза, которой вы запрещаете нерадивым пользователям обмениваться через файлохранилища .mp3, .avi и прочими &#171;нерабочими&#187; файлами. Так вот, при помощи FRM можно, аналогично, запретить обмен исполняемыми файлами, такими как .exe, .bat, .com и (та-да!..) .lnk и .pif. К слову, там же можно настроить отсылку почтовых уведомлений о попытках сохранения запрещенных файлов, скажем, на группу администраторов.

Плохая новость, Windows 2000 и Windows 2003 таким образом защитить не получится. Еще один аргумент для скорейшей миграции на более современную операционную систему. А пока можно воспользоваться костылем в виде [Software Restriction Policy](http://technet.microsoft.com/en-us/library/bb457006.aspx), как это [**подробно описано**](http://blog.didierstevens.com/2010/07/20/mitigating-lnk-exploitation-with-srp/) в блоге Дидье Стивенса. Дидье [**предлагает также**](http://blog.didierstevens.com/2010/07/18/mitigating-lnk-exploitation-with-ariad/) воспользоваться утилитой [Ariad](http://blog.didierstevens.com/programs/ariad/) для предотвращения заражения через CD-ROM и флэшки, но это уже, как говорится, на любителя.

Как проверить эффективность мер предосторожности. Если вы счастливец, которого миновала судьба двоих моих знакомых, успевших подхватить червей, паразитирующих на LNK-уязвимости, то образцов вредоносного кода в вашем распоряжении скорее всего пока нет. Я не знаю как у Core и Imunity (подозреваю, что тоже все в порядке), а у Metasploit модуль для имитации LNK-малвари уже имеется. Для поиска выполните _search lnk_ в msfconsole.

Пользуясь случаем, хочу передать привет господам [Дидье Стивенсу](http://didierstevens.com/) и [Карлосу Пересу](http://www.darkoperator.com/), и поблагодарить их за предоставленную возможность предохраниться от этой злой хвори. Вот, вроде, и все. Будьте осторожны!

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_112">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d0%25b7%25d0%25b0%25d1%2589%25d0%25b8%25d1%2582%25d0%25b8%25d1%2582%25d1%258c%25d1%2581%25d1%258f-%25d0%25be%25d1%2582-lnk-%25d0%25b0%25d0%25bb%25d0%25b8%25d0%25bf%25d1%2581%25d0%25b8%25d1%2581%25d0%25b0%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D0%B7%D0%B0%D1%89%D0%B8%D1%82%D0%B8%D1%82%D1%8C%D1%81%D1%8F%20%D0%BE%D1%82%20LNK-%D0%B0%D0%BB%D0%B8%D0%BF%D1%81%D0%B8%D1%81%D0%B0" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d0%25b7%25d0%25b0%25d1%2589%25d0%25b8%25d1%2582%25d0%25b8%25d1%2582%25d1%258c%25d1%2581%25d1%258f-%25d0%25be%25d1%2582-lnk-%25d0%25b0%25d0%25bb%25d0%25b8%25d0%25bf%25d1%2581%25d0%25b8%25d1%2581%25d0%25b0%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D0%B7%D0%B0%D1%89%D0%B8%D1%82%D0%B8%D1%82%D1%8C%D1%81%D1%8F%20%D0%BE%D1%82%20LNK-%D0%B0%D0%BB%D0%B8%D0%BF%D1%81%D0%B8%D1%81%D0%B0" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d0%25b7%25d0%25b0%25d1%2589%25d0%25b8%25d1%2582%25d0%25b8%25d1%2582%25d1%258c%25d1%2581%25d1%258f-%25d0%25be%25d1%2582-lnk-%25d0%25b0%25d0%25bb%25d0%25b8%25d0%25bf%25d1%2581%25d0%25b8%25d1%2581%25d0%25b0%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D0%B7%D0%B0%D1%89%D0%B8%D1%82%D0%B8%D1%82%D1%8C%D1%81%D1%8F%20%D0%BE%D1%82%20LNK-%D0%B0%D0%BB%D0%B8%D0%BF%D1%81%D0%B8%D1%81%D0%B0" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d0%25b7%25d0%25b0%25d1%2589%25d0%25b8%25d1%2582%25d0%25b8%25d1%2582%25d1%258c%25d1%2581%25d1%258f-%25d0%25be%25d1%2582-lnk-%25d0%25b0%25d0%25bb%25d0%25b8%25d0%25bf%25d1%2581%25d0%25b8%25d1%2581%25d0%25b0%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D0%B7%D0%B0%D1%89%D0%B8%D1%82%D0%B8%D1%82%D1%8C%D1%81%D1%8F%20%D0%BE%D1%82%20LNK-%D0%B0%D0%BB%D0%B8%D0%BF%D1%81%D0%B8%D1%81%D0%B0" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
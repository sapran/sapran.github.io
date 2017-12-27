---
id: 1024
title: Microsoft выпустила Fix-It для DLL-уязвимости
date: 2010-09-04T16:45:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/09/04/microsoft-%d0%b2%d1%8b%d0%bf%d1%83%d1%81%d1%82%d0%b8%d0%bb%d0%b0-fix-it-%d0%b4%d0%bb%d1%8f-dll-%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d0%b8/
permalink: /2010/09/microsoft-%d0%b2%d1%8b%d0%bf%d1%83%d1%81%d1%82%d0%b8%d0%bb%d0%b0-fix-it-%d0%b4%d0%bb%d1%8f-dll-%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d0%b8/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/09/microsoft-fix-it-dll.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4899675099226461336
shorturl:
  - http://tinyurl.com/p46ecxk
tags:
  - 0-day
  - dumb asses
  - easy button
  - microsoft
---
Наверняка многие уже слышали, в Интернете буйствует [**очередной 0-day**](https://www.microsoft.com/technet/security/advisory/2269637.mspx), которому, наряду с программным обеспечением компании Microsoft, подвержен ряд программ, разработанных третьими сторонами. На сегодняшний день&nbsp;об этой&nbsp;уязвимости было**&nbsp;**[**написано**](https://blogs.technet.com/b/srd/archive/2010/08/23/an-update-on-the-dll-preloading-remote-attack-vector.aspx)&nbsp;и&nbsp;рассказано очень много, поэтому я не буду вдаваться в детали. Скажу только, что причиной&nbsp;уязвимости&nbsp;послужила **безграмотность&nbsp;разработчиков** программного обеспечения, которые не удосужились прописать полные пути к &nbsp;используемым в их коде динамически загружаемым библиотекам, так называемым **DLL** (Dinamic-Link Libraries). Это позволило злоумышленникам, используя расположенные на съемном носителе или сетевом ресурсе файл данных (например, .mp3 или .pdf) и специально подготовленную DLL-библиотеку, получить возможность выполнения произвольного кода на компьютере жертвы в контексте безопасности уязвимой программы-обработчика (в нашем случае &#8212; проигрывателя звуковых файлов или просмотрщика PDF-документов). Демонстрацию уязвимости можно без труда [**найти на Youtube**](http://www.youtube.com/results?search_query=DLL+Hijack&aq=f).

Наиболее любопытные читатели могут воспользоваться утилитой&nbsp;**DLLHijackAuditKit v2** от HD Moore, которая предназначена для поиска уязвимого ПО, установленного в исследуемой операционной системе. Утилита выполняется не больше часа, а результат выполнения по меньшей мере впечатляет. Все действия, подробно описанные в **[соответствующем посте](http://blog.metasploit.com/2010/08/better-faster-stronger.html),**&nbsp;следует выполнять на виртуальной машине, либо после полного резервного копирования ОС.

Теперь хорошие новости. Microsoft выпустила и разместила в Windows Update экстренное &#171;исправление&#187;, позволяющее значительно снизить вероятность возможного взлома. Слово &#171;исправление&#187; намеренно взято в кавычки, потому что на самом деле предлагаемое решение состоит из двух частей и

  * добавляет в ОС специальную утилиту и ключ реестра&nbsp;**CWDIllegalInDllSearch**,
  * изменяет настройки системного реестра&nbsp;таким образом, чтобы устранить ряд возможных сетевых векторов атаки.

Настройка CWDIllegalInDllSearch позволяет пользователю ОС самостоятельно&nbsp;определить&nbsp;алгоритм поиска DLL-библиотек, как для отдельных приложений, так для системы в целом. То есть, Microsoft любезно предоставляет нам возможность частично исправить ошибку разработчиков.

Подробно о деталях настройки и прочих любопытных тонкостях можно прочитать в [**этой статье**](http://support.microsoft.com/kb/2264107)&nbsp;базы знаний. Для быстрого применения рекомендуемых Microsoft изменений следует скачать и установить [**обновление KB2264107**](http://support.microsoft.com/kb/2264107#)&nbsp;(секция **Update Information**) для вашей ОС, после чего скачать и установить **[Fix-It](http://support.microsoft.com/kb/2264107)&nbsp;**(секция **Fix It For Me**).

Microsoft также составила и опубликовала [руководство](http://msdn.microsoft.com/en-us/library/ff919712(VS.85).aspx) по безопасному программированию с использованием DLL-библиотек.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_117">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2Fmicrosoft-%25d0%25b2%25d1%258b%25d0%25bf%25d1%2583%25d1%2581%25d1%2582%25d0%25b8%25d0%25bb%25d0%25b0-fix-it-%25d0%25b4%25d0%25bb%25d1%258f-dll-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d0%25b8%2F&linkname=Microsoft%20%D0%B2%D1%8B%D0%BF%D1%83%D1%81%D1%82%D0%B8%D0%BB%D0%B0%20Fix-It%20%D0%B4%D0%BB%D1%8F%20DLL-%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2Fmicrosoft-%25d0%25b2%25d1%258b%25d0%25bf%25d1%2583%25d1%2581%25d1%2582%25d0%25b8%25d0%25bb%25d0%25b0-fix-it-%25d0%25b4%25d0%25bb%25d1%258f-dll-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d0%25b8%2F&linkname=Microsoft%20%D0%B2%D1%8B%D0%BF%D1%83%D1%81%D1%82%D0%B8%D0%BB%D0%B0%20Fix-It%20%D0%B4%D0%BB%D1%8F%20DLL-%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2Fmicrosoft-%25d0%25b2%25d1%258b%25d0%25bf%25d1%2583%25d1%2581%25d1%2582%25d0%25b8%25d0%25bb%25d0%25b0-fix-it-%25d0%25b4%25d0%25bb%25d1%258f-dll-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d0%25b8%2F&linkname=Microsoft%20%D0%B2%D1%8B%D0%BF%D1%83%D1%81%D1%82%D0%B8%D0%BB%D0%B0%20Fix-It%20%D0%B4%D0%BB%D1%8F%20DLL-%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2Fmicrosoft-%25d0%25b2%25d1%258b%25d0%25bf%25d1%2583%25d1%2581%25d1%2582%25d0%25b8%25d0%25bb%25d0%25b0-fix-it-%25d0%25b4%25d0%25bb%25d1%258f-dll-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d0%25b8%2F&linkname=Microsoft%20%D0%B2%D1%8B%D0%BF%D1%83%D1%81%D1%82%D0%B8%D0%BB%D0%B0%20Fix-It%20%D0%B4%D0%BB%D1%8F%20DLL-%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
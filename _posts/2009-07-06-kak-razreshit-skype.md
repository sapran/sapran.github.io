---
id: 1113
title: Как разрешить Skype
date: 2009-07-06T10:20:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/07/06/%d0%ba%d0%b0%d0%ba-%d1%80%d0%b0%d0%b7%d1%80%d0%b5%d1%88%d0%b8%d1%82%d1%8c-skype/
permalink: /2009/07/%d0%ba%d0%b0%d0%ba-%d1%80%d0%b0%d0%b7%d1%80%d0%b5%d1%88%d0%b8%d1%82%d1%8c-skype/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/07/skype.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/8140209149084982344
shorturl:
  - http://tinyurl.com/nk5aphd
tags:
  - active directory
  - skype
  - бумажные тигры
---
В [одном из прошлых постов](http://securegalaxy.blogspot.com/2009/04/skype.html) я писал, как парой строк в конфигурационном файле <span style="font-weight: bold;">squid</span> можно закрыть проблему, решить которую не под силу ведущим вендорам в области защиты информации. То есть, заблокировать работу <span style="font-weight: bold;">Skype </span>в локальной сети компании. С тех пор случилось две вещи.

Первое, мне на глаза попалась замечательная публикация под названием [Skype: A Practical Security Analysis](http://www.sans.org/reading_room/whitepapers/voip/32918.php). В ней достаточно подробно и доступно раскрываются особенности реализации сети Skype, а также даются практические рекомендации по обнаружению и блокировке Skype-трафика на сетевом периметре при помощи IPS с открытым исходным кодом Snort. Там все очень круто и вызывает искреннее уважение к автору, рекомендуется к прочтению каждому сисадмину.

Но самым вкусным в этой статье было второе: упоминание о существовании шаблона групповой политики [Active Directory](http://en.wikipedia.org/wiki/Active_Directory), предназначенной для &#171;легализации&#187; использования Skype в вашей компании. В двух словах, в [реестре Windows](http://en.wikipedia.org/wiki/Windows_Registry), в ветке <span style="font-weight: bold;">HKEY_CURRENT_USERSoftwarePoliciesSkypePhone</span> можно размещать ключи, разрешающие или запрещающие отдельные функции приложения. Например, ключи <span style="font-weight: bold;">DisableFileTransfer</span>, <span style="font-weight: bold;">DisableSupernode</span>, <span style="font-weight: bold;">WebStatus </span>и <span style="font-weight: bold;">MemoryOnly </span>позволяют запретить, соответственно, передачу файлов, получение статуса [super node](http://en.wikipedia.org/wiki/Supernode_%28networking%29), отображение в Интернете статуса абонента и сохранение на жестком диске данных программы.

[<img style="margin: 0px auto 10px; display: block; text-align: center; cursor: pointer; width: 320px; height: 142px;" src="http://4.bp.blogspot.com/_qASWdX8owQc/SlHYKgMybFI/AAAAAAAAC_E/olF5czpdOfU/s320/skype02.PNG" alt="" id="BLOGGER_PHOTO_ID_5355299106874092626" border="0" />](http://4.bp.blogspot.com/_qASWdX8owQc/SlHYKgMybFI/AAAAAAAAC_E/olF5czpdOfU/s1600-h/skype02.PNG)  
Полный перечень ключей и прочие вкусности доступны в документе [Network Administrator&#8217;s Guide](http://skype.com/security/network-admin-guide-version2.2.pdf), а шаблон групповой политики можно скачать по этой ссылке <http://www.skype.com/security/Skype-v1.7.adm>.

В программе <span style="font-weight: bold;">Auslogic Tweak Manager</span>, входящей в состав пакета [Auslogic BoostSpeed](http://www.auslogics.com/en/software), присутствуют средства настройки некоторых из этих полезных свойств.

[<img style="margin: 0px auto 10px; display: block; text-align: center; cursor: pointer; width: 320px; height: 230px;" src="http://3.bp.blogspot.com/_qASWdX8owQc/SlHU7bmykFI/AAAAAAAAC-8/HQbjvoaaXu0/s320/skype01.PNG" alt="" id="BLOGGER_PHOTO_ID_5355295549408055378" border="0" />](http://3.bp.blogspot.com/_qASWdX8owQc/SlHU7bmykFI/AAAAAAAAC-8/HQbjvoaaXu0/s1600-h/skype01.PNG)  
Теперь о главном: как нам это может быть полезно. Если вы прогрессивный ИТ/ИБ менеджер, не безразличный к мнению коллег, то одним из ваших подарков общественности может стать регулируемое разрешение использования Skype сотрудниками компании. Для этого нужно, для начала, заручиться поддержкой высшего руководства. Скорее всего придется провести презентацию и привлечь на свою сторону союзников, способных аргументировать такое разрешение. Продавцы, маркетологи и прочие социально активные кадры подойдут наилучшим образом.

Затем стоит составить список счастливцев, которых коснется это разрешение. Исходить нужно из соображений минимальной достаточности и бизнес-необходимости. Естественно, бухгалтеру по з/п такое средство ни к чему &#8212; оно не решает поставленных перед сотрудником служебных задач. К тому же, следует всегда ориентироваться на &#171;классификацию&#187; данных, с которыми работает сотрудник, а также на его &#171;послужной список&#187;, степень доверия, лояльности и т.п.

В итоге, нужно централизованно расставить приложение-клиент, настроить применение и проверить выполнение групповой политики и после этого наслаждаться в сиянии всеобщей любви и восторженного поклонения.

Такой подход к проблеме содержит в себе глубокий философский смысл. Как известно, для обеспечения информационной безопасности следует использовать только знакомые и проверенные средства. На этом пути очень легко впасть в крайность и запрещать все новое и незнакомое, подпадающее под клише вредоносного и бесполезного &#8212; например, Skype. Но если овладеть средствами управления этими технологиями, то их &#171;негативные&#187; свойства можно эффективно использовать во славу и во благо бизнеса.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_28">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d1%2580%25d0%25b0%25d0%25b7%25d1%2580%25d0%25b5%25d1%2588%25d0%25b8%25d1%2582%25d1%258c-skype%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D1%80%D0%B0%D0%B7%D1%80%D0%B5%D1%88%D0%B8%D1%82%D1%8C%20Skype" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d1%2580%25d0%25b0%25d0%25b7%25d1%2580%25d0%25b5%25d1%2588%25d0%25b8%25d1%2582%25d1%258c-skype%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D1%80%D0%B0%D0%B7%D1%80%D0%B5%D1%88%D0%B8%D1%82%D1%8C%20Skype" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d1%2580%25d0%25b0%25d0%25b7%25d1%2580%25d0%25b5%25d1%2588%25d0%25b8%25d1%2582%25d1%258c-skype%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D1%80%D0%B0%D0%B7%D1%80%D0%B5%D1%88%D0%B8%D1%82%D1%8C%20Skype" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d1%2580%25d0%25b0%25d0%25b7%25d1%2580%25d0%25b5%25d1%2588%25d0%25b8%25d1%2582%25d1%258c-skype%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D1%80%D0%B0%D0%B7%D1%80%D0%B5%D1%88%D0%B8%D1%82%D1%8C%20Skype" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
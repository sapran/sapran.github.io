---
id: 1035
title: Уязвимость в Adobe Reader, Flash Player и Acrobat
date: 2010-06-05T06:32:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/06/05/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%b2-adobe-reader-flash-player-%d0%b8-acrobat/
permalink: /2010/06/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%b2-adobe-reader-flash-player-%d0%b8-acrobat/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/06/adobe-reader-flash-player-acrobat.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1127364278693031342
shorturl:
  - http://tinyurl.com/qxeqf3t
tags:
  - 0-day
  - adobe
---
Adobe не прекращает радовать нас новыми&nbsp;дырами&nbsp;в разделяемом коде своих программных продуктов <s>жизнедеятельности</s>. Информация о новой уязвимости [**была размещена**](https://www.adobe.com/support/security/advisories/apsa10-01.html) вчера на сайте компании.

**Уязвимость** классифицирована как **критическая** и, согласно вендору, уже во всю эксплуатируется недобросовестными&nbsp;обитателями дикого Интернета. Успешная эксплуатация уязвимости может позволить (а значит позволит) злоумышленнику **выполнить произвольный код на компьютере жертвы**. То есть, еще хуже бывает очень редко.

**Защита.**&nbsp;Для предотвращения возможной компрометации системы Adobe рекомендует следующее.

  1. Установить&nbsp;**Flash Player 10.1 Release Candidate**, доступный для скачивания по адресу&nbsp;<http://labs.adobe.com/technologies/flashplayer10/>
  2. Удалить, переименовать или ограничить доступ к разделяемой библиотеке&nbsp;**authplay.dll**, поставляемой вместе с Adobe Reader и Adobe Acrobat. Внимание! В результате этих действий вы не сможете просматривать (о ужас!) PDF-документы, содержащие Flash-содержимое: приложение будет завершаться аварийно. Файл&nbsp;authplay.dll обычно обитает по адресу:

  * **C:Program FilesAdobeReader 9.0Readerauthplay.dll**&nbsp;для Reader,
  * **C:Program FilesAdobeAcrobat 9.0Acrobatauthplay.dll** для&nbsp;Acrobat.

<div>
  От себя посоветую использовать расширения <a href="http://noscript.net/">NoScript!</a> для Mozilla Firefox и <a href="https://chrome.google.com/extensions/detail/gofhjkjmkpinhpoiabjplobcaignabnl">FlashBlock</a> для Google Chrome. Эти чудо-примочки блокируют Flash-содержимое на сайте до вашего специального распоряжения.</p> 
  
  <p>
    <b>Update </b>Adobe собирается исправить эту уязвимость уже завтра, 10 июня<br /><a href="http://www.theregister.co.uk/2010/06/08/adobe_flash_fix/">http://www.theregister.co.uk/2010/06/08/adobe_flash_fix/</a></div> 
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_106">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F06%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-adobe-reader-flash-player-%25d0%25b8-acrobat%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20Adobe%20Reader%2C%20Flash%20Player%20%D0%B8%20Acrobat" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F06%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-adobe-reader-flash-player-%25d0%25b8-acrobat%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20Adobe%20Reader%2C%20Flash%20Player%20%D0%B8%20Acrobat" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F06%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-adobe-reader-flash-player-%25d0%25b8-acrobat%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20Adobe%20Reader%2C%20Flash%20Player%20%D0%B8%20Acrobat" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F06%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-adobe-reader-flash-player-%25d0%25b8-acrobat%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20Adobe%20Reader%2C%20Flash%20Player%20%D0%B8%20Acrobat" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
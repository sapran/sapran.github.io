---
id: 977
title: Уязвимость нулевого дня в Skype для MacOS X
date: 2011-05-06T22:24:00+00:00
author: sapran
layout: post
guid: http://styran.com/2011/05/06/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%bd%d1%83%d0%bb%d0%b5%d0%b2%d0%be%d0%b3%d0%be-%d0%b4%d0%bd%d1%8f-%d0%b2-skype-%d0%b4%d0%bb%d1%8f-macos-x/
permalink: /2011/05/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%bd%d1%83%d0%bb%d0%b5%d0%b2%d0%be%d0%b3%d0%be-%d0%b4%d0%bd%d1%8f-%d0%b2-skype-%d0%b4%d0%bb%d1%8f-macos-x/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2011/05/skype-macos-x.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/2558602888800604437
shorturl:
  - http://tinyurl.com/op3x43m
tags:
  - 0-day
  - skype
---
<div dir="ltr" style="text-align: left;">
  <div style="text-align: justify;">
    <b><i>[Updated 2011-05-09]</i></b> Согласно <b><a href="http://blogs.skype.com/security/">официальному блогу Skype</a></b>, уязвимость была исправлена в новой версии для MacOS X: <b><i>&#171;</i></b><i><b>we recommend you update your software with the fix made available on April 14th, just click on Skype -> Check for Updates or you can <a href="http://www.skype.com/intl/en-us/get-skype/on-your-computer/macosx/">download the software here</a>.</b></i><b><i>&#171;</i></b></p> 
    
    <p>
      <b><a href="http://www.purehacking.com/blogs/gordon-maddern/skype-0day-vulnerabilitiy-discovered-by-pure-hacking">Это</a></b>&nbsp;очень нехорошая и заразная уязвимость. <b>Удаленный доступ к компьютеру под управлением MacOS X может быть получен (всего лишь) при помощи отправки специально подготовленного сообщения в Skype</b>.&nbsp;Последствия такого рода уязвимости могут быть очень печальны. Представьте себе сетевого червя, распространяющегося путем рассылки зловредного сообщения по спискам контактов с зараженных&nbsp;компьютеров.</div> 
      
      <div style="text-align: justify;">
      </div>
      
      <div style="text-align: justify;">
        Опечалила реакция Skype на сообщения об обнаружении уязвимости. С момента уведомления прошел уже месяц, а обещание выпустить исправление еще не выполнено. Публичное заявление о существовании &#171;дыры&#187; должно несколько ускорить процесс подготовки обновления, потому что там, в подполье, сотни злых хакеров уже куют&nbsp;соответствующий&nbsp;&#171;<a href="http://en.wikipedia.org/wiki/Advanced_Persistent_Threat">APT</a>&#171;. Я, конечно же, утрирую, но в каждой шутке есть доля шутки. Искать что бы то ни было становится значительно проще, когда тебе прозрачно намекают где именно.
      </div>
      
      <div style="text-align: justify;">
      </div>
      
      <div style="text-align: justify;">
        С другой стороны, выпуск исправления не очень-то и поможет. Автоматических апдейтов у Skype пока нет, а обладая объектным кодом исправленной версии злоумышленникам будет намного проще обнаружить уязвимый участок программы при помощи обратного инжиниринга (<a href="http://en.wikipedia.org/wiki/Reverse_engineering">reverse engineering</a>). Этот метод уже давно используется блэкхэтами на продуктах Microsoft: вслед за ежемесячными &#171;вторниками обновлений&#187; (<a href="http://en.wikipedia.org/wiki/Patch_Tuesday">patch tuesday</a>) приходят &#171;четверги эксплойтов&#187;.
      </div>
      
      <div style="text-align: justify;">
      </div>
      
      <div style="text-align: justify;">
        На этой оптимистической ноте буду закругляться. Всем маководам советую сократить пользование Скайпом до необходимого минимума и затаив дыхание ждать патча. А я, вместе со всеми остальными, буду надеяться, что дыра эта присуща только эпловской сборке Skype и не выпрыгнет в ближайшее время в Windows-версии.
      </div></div> 
      
      <div class="addtoany_share_save_container addtoany_content_bottom">
        <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_164">
          <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F05%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25bd%25d1%2583%25d0%25bb%25d0%25b5%25d0%25b2%25d0%25be%25d0%25b3%25d0%25be-%25d0%25b4%25d0%25bd%25d1%258f-%25d0%25b2-skype-%25d0%25b4%25d0%25bb%25d1%258f-macos-x%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BD%D1%83%D0%BB%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BD%D1%8F%20%D0%B2%20Skype%20%D0%B4%D0%BB%D1%8F%20MacOS%20X" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F05%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25bd%25d1%2583%25d0%25bb%25d0%25b5%25d0%25b2%25d0%25be%25d0%25b3%25d0%25be-%25d0%25b4%25d0%25bd%25d1%258f-%25d0%25b2-skype-%25d0%25b4%25d0%25bb%25d1%258f-macos-x%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BD%D1%83%D0%BB%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BD%D1%8F%20%D0%B2%20Skype%20%D0%B4%D0%BB%D1%8F%20MacOS%20X" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F05%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25bd%25d1%2583%25d0%25bb%25d0%25b5%25d0%25b2%25d0%25be%25d0%25b3%25d0%25be-%25d0%25b4%25d0%25bd%25d1%258f-%25d0%25b2-skype-%25d0%25b4%25d0%25bb%25d1%258f-macos-x%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BD%D1%83%D0%BB%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BD%D1%8F%20%D0%B2%20Skype%20%D0%B4%D0%BB%D1%8F%20MacOS%20X" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F05%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25bd%25d1%2583%25d0%25bb%25d0%25b5%25d0%25b2%25d0%25be%25d0%25b3%25d0%25be-%25d0%25b4%25d0%25bd%25d1%258f-%25d0%25b2-skype-%25d0%25b4%25d0%25bb%25d1%258f-macos-x%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BD%D1%83%D0%BB%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BD%D1%8F%20%D0%B2%20Skype%20%D0%B4%D0%BB%D1%8F%20MacOS%20X" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
        </div>
      </div>
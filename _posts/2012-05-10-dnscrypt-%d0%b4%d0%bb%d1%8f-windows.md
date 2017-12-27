---
id: 910
title: DNSCrypt для Windows
date: 2012-05-10T18:08:00+00:00
author: sapran
layout: post
guid: http://styran.com/2012/05/10/dnscrypt-%d0%b4%d0%bb%d1%8f-windows/
permalink: /2012/05/dnscrypt-%d0%b4%d0%bb%d1%8f-windows/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2012/05/dnscrypt-windows.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4980217617138708459
shorturl:
  - http://tinyurl.com/qjla5ck
tags:
  - mitm
  - opendns
  - криптография
---
<div dir="ltr" style="text-align: left;">
  Спустя некоторое время после &#171;пробного&#187; выпуска утилиты <i><b>DNSCrypt</b></i> для пользователей MacOS, компания <i><b>OpenDNS </b></i>вчера предоставила для скачивания <a href="https://www.opendns.com/technology/dnscrypt/"><i><b>версию для Windows</b></i></a>.</p> 
  
  <p>
    Утилита DNSCrypt, как нетрудно догадаться из названия, шифрует датаграммы DNS на пути между вашим компьютером и DNS-сервером. Это чрезвычайно простое и эффективное средство противодействия прослушиванию и подмене DNS-сообщений.
  </p>
  
  <p>
    Риски конфиденциальности DNS-трафика очевидны далеко не всем, а зря. Прослушивая запросы DNS можно составить достаточно полную картину об истории посещений пользователя. Большинство сисадминов, например, не читают в логах ничего кроме доменных имен, а отсуствие надежного туннелирования DNS-трафика &#8212; одна из уязвимостей сети Tor, способная привести к деанонимизации пользователя (трафик от браузера к серверу шифруется, но DNS-сервер, обслуживающий домен сервера, получает DNS-запросы напрямую, минуя сеть Тор).
  </p>
  
  <p>
    Но важнее конфиденциальности в данном случае целостность и достоверность DNS сообщений, а если точнее, ответов серверов. Потому как атаки типа Man-In-the-Middle на различные прикладные протоколы зачастую включают в себя подмену ответов DNS.
  </p>
  
  <table align="center" cellpadding="0" cellspacing="0" style="margin-left: auto; margin-right: auto; text-align: center;">
    <tr>
      <td style="text-align: center;">
        <a href="http://www.windowsecurity.com/img/upl/image0081270494115187.jpg" style="margin-left: auto; margin-right: auto;"><img border="0" height="206" src="http://www.windowsecurity.com/img/upl/image0081270494115187.jpg" width="320" /></a>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: center;">
        <a href="http://www.windowsecurity.com/">http://www.windowsecurity.com</a>
      </td>
    </tr>
  </table>
  
  <p>
    Спасибо OpenDNS. Ждем версию для Linux.</div> 
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_230">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F05%2Fdnscrypt-%25d0%25b4%25d0%25bb%25d1%258f-windows%2F&linkname=DNSCrypt%20%D0%B4%D0%BB%D1%8F%20Windows" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F05%2Fdnscrypt-%25d0%25b4%25d0%25bb%25d1%258f-windows%2F&linkname=DNSCrypt%20%D0%B4%D0%BB%D1%8F%20Windows" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F05%2Fdnscrypt-%25d0%25b4%25d0%25bb%25d1%258f-windows%2F&linkname=DNSCrypt%20%D0%B4%D0%BB%D1%8F%20Windows" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F05%2Fdnscrypt-%25d0%25b4%25d0%25bb%25d1%258f-windows%2F&linkname=DNSCrypt%20%D0%B4%D0%BB%D1%8F%20Windows" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
---
id: 1046
title: 'pwnat: новое слово в туннелировании трафика'
date: 2010-03-27T19:32:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/03/27/pwnat-%d0%bd%d0%be%d0%b2%d0%be%d0%b5-%d1%81%d0%bb%d0%be%d0%b2%d0%be-%d0%b2-%d1%82%d1%83%d0%bd%d0%bd%d0%b5%d0%bb%d0%b8%d1%80%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d0%b8-%d1%82%d1%80%d0%b0%d1%84%d0%b8%d0%ba/
permalink: /2010/03/pwnat-%d0%bd%d0%be%d0%b2%d0%be%d0%b5-%d1%81%d0%bb%d0%be%d0%b2%d0%be-%d0%b2-%d1%82%d1%83%d0%bd%d0%bd%d0%b5%d0%bb%d0%b8%d1%80%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d0%b8-%d1%82%d1%80%d0%b0%d1%84%d0%b8%d0%ba/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/03/pwnat.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1325813530982780491
shorturl:
  - http://tinyurl.com/ne8rv46
tags:
  - протоколы
  - сети
---
<div dir="ltr" style="text-align: left;">
  <div style="text-align: justify;">
    Уважаемые господа сетевые администраторы. Это для тех из вас, кто до сих пор уверен, что разрешение исходящего ICMP (UDP, TCP etc.) трафика не представляет рисков информационной безопасности.
  </div>
  
  <div style="text-align: justify;">
  </div>
  
  <div style="text-align: justify;">
    Утилита <b>pwnat </b>позволяет (внимание)&nbsp;туннелировать&nbsp;трафик между клиентом и сервером, которые (оба) находятся <b>за NAT-ом</b> и не&nbsp;располагают&nbsp;&#171;реальными&#187; IP-адресами. Подробности реализации этого чудовища можно найти по ссылке:<b>&nbsp;</b><b><a href="http://samy.pl/pwnat/">http://samy.pl/pwnat/</a><span style="font-weight: normal;">.</span></b>&nbsp;Поверьте, многие из вас будут удивлены, насколько очевидна&nbsp;техника, использованная в реализации утилиты.
  </div>
  
  <div style="text-align: justify;">
  </div>
  
  <div style="text-align: justify;">
    Итак, с сегодняшнего дня я прекращаю пугать цискарей <b><a href="http://www.phrack.com/issues.html?issue=49&id=6">Loki</a></b>&nbsp;(устал бедняга, хватит с него) и перехожу на использование <b>pwnat</b>. И да прибудет со мной сила.
  </div>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_95">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F03%2Fpwnat-%25d0%25bd%25d0%25be%25d0%25b2%25d0%25be%25d0%25b5-%25d1%2581%25d0%25bb%25d0%25be%25d0%25b2%25d0%25be-%25d0%25b2-%25d1%2582%25d1%2583%25d0%25bd%25d0%25bd%25d0%25b5%25d0%25bb%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d0%25b8-%25d1%2582%25d1%2580%25d0%25b0%25d1%2584%25d0%25b8%25d0%25ba%2F&linkname=pwnat%3A%20%D0%BD%D0%BE%D0%B2%D0%BE%D0%B5%20%D1%81%D0%BB%D0%BE%D0%B2%D0%BE%20%D0%B2%20%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B8%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F03%2Fpwnat-%25d0%25bd%25d0%25be%25d0%25b2%25d0%25be%25d0%25b5-%25d1%2581%25d0%25bb%25d0%25be%25d0%25b2%25d0%25be-%25d0%25b2-%25d1%2582%25d1%2583%25d0%25bd%25d0%25bd%25d0%25b5%25d0%25bb%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d0%25b8-%25d1%2582%25d1%2580%25d0%25b0%25d1%2584%25d0%25b8%25d0%25ba%2F&linkname=pwnat%3A%20%D0%BD%D0%BE%D0%B2%D0%BE%D0%B5%20%D1%81%D0%BB%D0%BE%D0%B2%D0%BE%20%D0%B2%20%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B8%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F03%2Fpwnat-%25d0%25bd%25d0%25be%25d0%25b2%25d0%25be%25d0%25b5-%25d1%2581%25d0%25bb%25d0%25be%25d0%25b2%25d0%25be-%25d0%25b2-%25d1%2582%25d1%2583%25d0%25bd%25d0%25bd%25d0%25b5%25d0%25bb%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d0%25b8-%25d1%2582%25d1%2580%25d0%25b0%25d1%2584%25d0%25b8%25d0%25ba%2F&linkname=pwnat%3A%20%D0%BD%D0%BE%D0%B2%D0%BE%D0%B5%20%D1%81%D0%BB%D0%BE%D0%B2%D0%BE%20%D0%B2%20%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B8%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F03%2Fpwnat-%25d0%25bd%25d0%25be%25d0%25b2%25d0%25be%25d0%25b5-%25d1%2581%25d0%25bb%25d0%25be%25d0%25b2%25d0%25be-%25d0%25b2-%25d1%2582%25d1%2583%25d0%25bd%25d0%25bd%25d0%25b5%25d0%25bb%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d0%25b8-%25d1%2582%25d1%2580%25d0%25b0%25d1%2584%25d0%25b8%25d0%25ba%2F&linkname=pwnat%3A%20%D0%BD%D0%BE%D0%B2%D0%BE%D0%B5%20%D1%81%D0%BB%D0%BE%D0%B2%D0%BE%20%D0%B2%20%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B8%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
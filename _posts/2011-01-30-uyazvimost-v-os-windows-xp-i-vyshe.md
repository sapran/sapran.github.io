---
id: 997
title: Уязвимость в ОС Windows XP и выше
date: 2011-01-30T19:13:00+00:00
author: sapran
layout: post
guid: http://styran.com/2011/01/30/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%b2-%d0%be%d1%81-windows-xp-%d0%b8-%d0%b2%d1%8b%d1%88%d0%b5/
permalink: /2011/01/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%b2-%d0%be%d1%81-windows-xp-%d0%b8-%d0%b2%d1%8b%d1%88%d0%b5/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2011/01/windows-xp.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4752334876293704527
shorturl:
  - http://tinyurl.com/qxpc2gx
tags:
  - 0-day
  - microsoft
---
<div style="text-align: justify;">
  Уязвимость под названием <b>&#171;<a href="https://www.microsoft.com/technet/security/advisory/2501696.mspx">MHTML Script Injection</a>&#187; </b><i><span style="font-size: x-small;">(неинтересная ссылка на непонятный Advisory, подготовленный пиарщиками Microsoft)</span></i> присутствует именно в ОС <b>Windows всех версий начиная с XP</b>. Хотя из названия может сложиться впечатление, что уязвим браузер Internet Explorer, это не так.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Тем не менее, основным вектором атаки остается Internet Explorer: для успешной компрометации цели атакующему нужно <s>заставить</s>&nbsp;убедить жертву посетить специально подготовленный веб-сайт. То есть, для рядового пользователя Интернет <a href="http://securegalaxy.blogspot.com/2010/12/0-day-internet-explorer.html"><b>ничего не меняется</b></a>: <b>нажми на <s>кнопку</s> ссылку и получи Трояна в подарок</b>. От версии IE тоже ничего не зависит.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  По <a href="http://blogs.technet.com/b/srd/archive/2011/01/28/more-information-about-the-mhtml-script-injection-vulnerability.aspx"><b>этой ссылке</b></a>&nbsp;<i><span style="font-size: x-small;">(интересная ссылка на блог классных парней из Microsoft Security Response Center)</span></i> можно разузнать как уберечься от этой напасти и даже как проверить защищена ли ваша система. Для установки спасительного пакета контрмер просто скачайте и запустите файл, клацнув на дядьку с&nbsp;гаечным&nbsp;ключом.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_144">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F01%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-%25d0%25be%25d1%2581-windows-xp-%25d0%25b8-%25d0%25b2%25d1%258b%25d1%2588%25d0%25b5%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D0%9E%D0%A1%20Windows%20XP%20%D0%B8%20%D0%B2%D1%8B%D1%88%D0%B5" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F01%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-%25d0%25be%25d1%2581-windows-xp-%25d0%25b8-%25d0%25b2%25d1%258b%25d1%2588%25d0%25b5%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D0%9E%D0%A1%20Windows%20XP%20%D0%B8%20%D0%B2%D1%8B%D1%88%D0%B5" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F01%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-%25d0%25be%25d1%2581-windows-xp-%25d0%25b8-%25d0%25b2%25d1%258b%25d1%2588%25d0%25b5%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D0%9E%D0%A1%20Windows%20XP%20%D0%B8%20%D0%B2%D1%8B%D1%88%D0%B5" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F01%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-%25d0%25be%25d1%2581-windows-xp-%25d0%25b8-%25d0%25b2%25d1%258b%25d1%2588%25d0%25b5%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D0%9E%D0%A1%20Windows%20XP%20%D0%B8%20%D0%B2%D1%8B%D1%88%D0%B5" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
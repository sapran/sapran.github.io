---
id: 1129
title: Петр Баня и его Kon-Boot
date: 2009-05-13T10:46:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/05/13/%d0%bf%d0%b5%d1%82%d1%80-%d0%b1%d0%b0%d0%bd%d1%8f-%d0%b8-%d0%b5%d0%b3%d0%be-kon-boot/
permalink: /2009/05/%d0%bf%d0%b5%d1%82%d1%80-%d0%b1%d0%b0%d0%bd%d1%8f-%d0%b8-%d0%b5%d0%b3%d0%be-kon-boot/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/05/kon-boot.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/6518134866152418899
shorturl:
  - http://tinyurl.com/o6wuxqr
tags:
  - kon-boot
  - rootkit
---
<div style="text-align: justify;">
  Первые три из Десяти Незыблемых Законов Безопасности гласят, что компьютер больше не принадлежит владельцу, если:
</div>

<li style="text-align: justify;">
  злоумышленнику удалось выполнить на нем вредоносный код, либо склонить к этому владельца;
</li>
<li style="text-align: justify;">
  злоумышленнику удалось внести изменения в ОС (вероятно, в следствие п. 1);
</li>
<li style="text-align: justify;">
  злоумышленник обладает физическим доступом к компьютеру.
</li>

<div style="text-align: justify;">
  Десятый закон, в свою очередь, лаконично подчеркивает, что технологии &#8212; не панацея.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Выпущенная <strike>на волю</strike> совсем недавно утилита <a href="http://www.piotrbania.com/all/kon-boot/">Kon-Boot</a> представляет собой загрузочный образ, устанавливающий руткит перед началом работы основной ОС. После того, как ОС загрузится, руткит предоставляет пользователю возможность войти в систему с административными правами. На данный момент поддерживаются практически все релизы Windows и ряд Linux-дистрибутивов. Вот демонстрация работы утилиты с BackTrack4 Beta на базе Ubuntu 8.10
</div>

<div style="text-align: center;">
</div>

<div style="text-align: justify;">
  Работу с preboot-шифрованием диска я еще не проверял, но обязательно сделаю это после праздников. Тестируем и наслаждаемся! Но пароль на CMOS и загрузку только с HDD я бы рекомендовал установить.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  <span style="font-weight: bold;">Updated</span>. <span style="font-weight: bold;">Bitlocker </span>обнаруживает изменения в загрузочном секторе и предлагает продолжить с предоставлением ключей шифрования. То есть в принципе защищает &#8212; с ключами нам и Kon-Boot не понадобился бы.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  <span style="font-weight: bold;">Updated</span>. <span style="font-weight: bold;">TrueCrypt </span>System Encryption жалуется на изменения в BIOS и отказывается загружаться. Да здравствует Open Source.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  <span style="font-weight: bold;">Updated. CheckPoint FDE aka Pointsec PC</span> в режиме Windows-аутентификации ничего не замечает и как ни в чем не бывало грузит ОС, после чего Kon-Boot предоставляет доступ к любой локальной УЗ без пароля.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_12">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F05%2F%25d0%25bf%25d0%25b5%25d1%2582%25d1%2580-%25d0%25b1%25d0%25b0%25d0%25bd%25d1%258f-%25d0%25b8-%25d0%25b5%25d0%25b3%25d0%25be-kon-boot%2F&linkname=%D0%9F%D0%B5%D1%82%D1%80%20%D0%91%D0%B0%D0%BD%D1%8F%20%D0%B8%20%D0%B5%D0%B3%D0%BE%20Kon-Boot" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F05%2F%25d0%25bf%25d0%25b5%25d1%2582%25d1%2580-%25d0%25b1%25d0%25b0%25d0%25bd%25d1%258f-%25d0%25b8-%25d0%25b5%25d0%25b3%25d0%25be-kon-boot%2F&linkname=%D0%9F%D0%B5%D1%82%D1%80%20%D0%91%D0%B0%D0%BD%D1%8F%20%D0%B8%20%D0%B5%D0%B3%D0%BE%20Kon-Boot" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F05%2F%25d0%25bf%25d0%25b5%25d1%2582%25d1%2580-%25d0%25b1%25d0%25b0%25d0%25bd%25d1%258f-%25d0%25b8-%25d0%25b5%25d0%25b3%25d0%25be-kon-boot%2F&linkname=%D0%9F%D0%B5%D1%82%D1%80%20%D0%91%D0%B0%D0%BD%D1%8F%20%D0%B8%20%D0%B5%D0%B3%D0%BE%20Kon-Boot" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F05%2F%25d0%25bf%25d0%25b5%25d1%2582%25d1%2580-%25d0%25b1%25d0%25b0%25d0%25bd%25d1%258f-%25d0%25b8-%25d0%25b5%25d0%25b3%25d0%25be-kon-boot%2F&linkname=%D0%9F%D0%B5%D1%82%D1%80%20%D0%91%D0%B0%D0%BD%D1%8F%20%D0%B8%20%D0%B5%D0%B3%D0%BE%20Kon-Boot" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
---
id: 837
title: 'VPN &#171;по-домашнему&#187;. Часть 2 – установка OpenVPN'
date: 2014-04-05T20:07:00+00:00
author: sapran
layout: post
guid: http://styran.com/2014/04/05/vpn-%d0%bf%d0%be-%d0%b4%d0%be%d0%bc%d0%b0%d1%88%d0%bd%d0%b5%d0%bc%d1%83-%d1%87%d0%b0%d1%81%d1%82%d1%8c-2-%d1%83%d1%81%d1%82%d0%b0%d0%bd%d0%be%d0%b2%d0%ba%d0%b0-openvpn/
permalink: /2014/04/vpn-%d0%bf%d0%be-%d0%b4%d0%be%d0%bc%d0%b0%d1%88%d0%bd%d0%b5%d0%bc%d1%83-%d1%87%d0%b0%d1%81%d1%82%d1%8c-2-%d1%83%d1%81%d1%82%d0%b0%d0%bd%d0%be%d0%b2%d0%ba%d0%b0-openvpn/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2014/04/vpn-2-openvpn.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/8371420607813610404
shorturl:
  - http://tinyurl.com/p4f8lfp
tags:
  - openvpn
  - vpn
  - приватность
---
OpenVPN Access Server – это коммерческий программный продукт, основанный на известном одноименном open source проекте. Бывалые админы знают, что подъем OpenVPN занятие нетривиальное и в первый раз приносит немало бурных эмоций. Поэтому обычным пользователям я советую воспользоваться коммерческим вариантом, так как его использование для двух одновременных сессий пользователей – бесплатно. А тру пацаны могут поэкспериментировать.

Заходим на дроплет по SSH. Если вдруг забыли, пароль пользователя root и IP-адрес вам прислали письмом после создания инстанса. На <a href="https://openvpn.net/index.php/access-server/download-openvpn-as-sw/113.html?osfamily=Ubuntu" target="_blank">странице загрузок OpenVPN AS</a> выбраем и копируем ссылку на подходящий дистрибутив. Если вы не отклонялись от советов в первой части, то команда установки в дроплете будет выглядеть так:
  


> root@droplet-ip:~# wget http://swupdate.openvpn.org/as/openvpn-as-2.0.5-Ubuntu13.amd64.deb && sudo dpkg -i openvpn-as-2.0.5-Ubuntu13.amd64.deb</p>
Инсталляция закончится выводом баннера с дальнейшими инструкциями. Вам нужно сменить пароль администратора OpenVPN:
  


> root@droplet-ip:~# passwd openvpn</p>
Для доступа к VPN я советую создать другого пользователя, отличного от openvpn, а лучше двух. Одного – для постоянного туннеля с вашего домашнего роутера, второго – для использования на мобильных устройствах.
  


> root@droplet-ip:~# adduser vpn_home  
> root@droplet-ip:~# adduser vpn_traveler</p>
После этого можно закрывать SSH и приступать к настройке VPN-сервера, перейдя по адресу:
  


> https://droplet-ip:943/admin</p>
После тщательного изучения пользователского соглашения, вы попадете в административный интерфейс OpenVPN AS.

<div style="clear: both; text-align: center;">
  <a href="http://1.bp.blogspot.com/-yC3mt_vSepY/U0Bc9C3VUpI/AAAAAAAAnX8/uJIKROtb6X8/s3200/Screenshot+2014-04-05+22.40.06.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://1.bp.blogspot.com/-yC3mt_vSepY/U0Bc9C3VUpI/AAAAAAAAnX8/uJIKROtb6X8/s3200/Screenshot+2014-04-05+22.40.06.png" height="276" width="400" /></a>
</div>

<div style="clear: both; text-align: center;">
</div>

<div style="clear: both; text-align: left;">
  Я не рекомендую изменять настройки по умолчанию, по крайней мере пока. Сервер принимает соединения от пользователей, которые успешно прошли проверку по протоколу PAM. Если вкратце, это ваши системные пользователи, которых вы только что создали. Зайдите в раздел <u>User Permissions</u>&nbsp;и добавьте пользователей vpn_home и vpn_traveler, после чего обновите настройки сервера кнопкой Update Running Server.
</div>

<div style="clear: both; text-align: left;">
</div>

<div style="clear: both; text-align: center;">
  <a href="http://1.bp.blogspot.com/-cHcowCHQeMg/U0Bf_lM3yhI/AAAAAAAAnYI/XU5t2ro5Wgw/s3200/Screenshot+2014-04-05+22.55.56.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://1.bp.blogspot.com/-cHcowCHQeMg/U0Bf_lM3yhI/AAAAAAAAnYI/XU5t2ro5Wgw/s3200/Screenshot+2014-04-05+22.55.56.png" height="400" width="388" /></a>
</div>

<div style="clear: both; text-align: left;">
</div>

<div style="clear: both; text-align: left;">
  Давайте проверим, что получилось. По адресу&nbsp;https://droplet-ip:943/?src=connect введите логин и пароль пользователя vpn_traveler. Если все предыдущие шаги выполнены успешно, сервер предложит вам скачать клиентское ПО:
</div>

<div style="clear: both; text-align: left;">
</div>

<div style="clear: both; text-align: center;">
  <a href="http://2.bp.blogspot.com/-14x2Niol8Vg/U0BgwGoZ6pI/AAAAAAAAnYQ/L0Qe043gPSM/s3200/Screenshot+2014-04-05+22.59.06.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://2.bp.blogspot.com/-14x2Niol8Vg/U0BgwGoZ6pI/AAAAAAAAnYQ/L0Qe043gPSM/s3200/Screenshot+2014-04-05+22.59.06.png" height="400" width="357" /></a>
</div>

<div style="clear: both; text-align: center;">
</div>

<div style="clear: both; text-align: left;">
  Как видите, свобода выбора зашкаливает. Можете начинать использовать VPN на устройствах под управлением iOS и Android или на вашем ноутбуке пока я буду писать третью часть о настройке перманентного туннеля с OpenWRT-роутера.
</div>

<div style="clear: both; text-align: left;">
</div>

<div style="clear: both; text-align: left;">
  Одно дополнение для пользователей MacOS X. Лично я не использую стандартный клиент OpenVPN AS, а предпочитаю Tunnelblick, настроенный по <a href="https://openvpn.net/index.php/access-server/docs/admin-guides/183-how-to-connect-to-access-server-from-a-mac.html" target="_blank">инструкции в этой статье</a>.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_300">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-2-%25d1%2583%25d1%2581%25d1%2582%25d0%25b0%25d0%25bd%25d0%25be%25d0%25b2%25d0%25ba%25d0%25b0-openvpn%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%202%20%E2%80%93%20%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0%20OpenVPN" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-2-%25d1%2583%25d1%2581%25d1%2582%25d0%25b0%25d0%25bd%25d0%25be%25d0%25b2%25d0%25ba%25d0%25b0-openvpn%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%202%20%E2%80%93%20%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0%20OpenVPN" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-2-%25d1%2583%25d1%2581%25d1%2582%25d0%25b0%25d0%25bd%25d0%25be%25d0%25b2%25d0%25ba%25d0%25b0-openvpn%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%202%20%E2%80%93%20%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0%20OpenVPN" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-2-%25d1%2583%25d1%2581%25d1%2582%25d0%25b0%25d0%25bd%25d0%25be%25d0%25b2%25d0%25ba%25d0%25b0-openvpn%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%202%20%E2%80%93%20%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0%20OpenVPN" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
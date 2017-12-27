---
id: 835
title: 'VPN &#171;по-домашнему&#187;. Часть 3 – настройка OpenWRT'
date: 2014-04-09T21:10:00+00:00
author: sapran
layout: post
guid: http://styran.com/2014/04/09/vpn-%d0%bf%d0%be-%d0%b4%d0%be%d0%bc%d0%b0%d1%88%d0%bd%d0%b5%d0%bc%d1%83-%d1%87%d0%b0%d1%81%d1%82%d1%8c-3-%d0%bd%d0%b0%d1%81%d1%82%d1%80%d0%be%d0%b9%d0%ba%d0%b0-openwrt/
permalink: /2014/04/vpn-%d0%bf%d0%be-%d0%b4%d0%be%d0%bc%d0%b0%d1%88%d0%bd%d0%b5%d0%bc%d1%83-%d1%87%d0%b0%d1%81%d1%82%d1%8c-3-%d0%bd%d0%b0%d1%81%d1%82%d1%80%d0%be%d0%b9%d0%ba%d0%b0-openwrt/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2014/04/vpn-3-openwrt.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/6619868208165965284
shorturl:
  - http://tinyurl.com/omnw4w8
tags:
  - openvpn
  - vpn
  - приватность
  - свобода слова
---
ОС OpenWRT – это прекрасная замена для фирменной прошивки вашего WiFi-роутера, если он есть в <a href="http://wiki.openwrt.org/toh/start" target="_blank">списке поддерживаемого оборудования</a>. Поддерживаются практически все популярные модели роутеров, но если вашего среди них нет – попытайте счастья с <a href="http://www.dd-wrt.com/site/index" target="_blank">DD-WRT</a>. Это еще один альтернативный firmware, поддерживающий OpenVPN. (Справедливости ради замечу, что по удобству использования и наполению софтом DD-WRT намного внушительнее OpenWRT. Но моего девайса пока нет в списке поддерживаемого им оборудования.)

Установить OpenWRT можно, скачав подходящую прошивку в <a href="http://downloads.openwrt.org/" target="_blank">центре загрузок</a> и обновив устройство через функционал обновлений вашей фирменной прошивки. Goole может помочь найти подробную статью об обновлении вашего устройства. Важный момент: для каждой версии OpenWRT и каждого устройства есть два файла обновления: одно – для первого обновления с OEM прошивки, второе – для последующих обновлений OpenWRT. Например, для &#171;крайней&#187; версии, основанной на ночных сборках текущего снепшота репозитария проекта, и для роутера TP-Link WR941ND v6, в директории
  


> <http://downloads.openwrt.org/snapshots/trunk/></p>
расположены соответствующие файлы
  


> openwrt-ar71xx-generic-tl-wr941nd-v6-squashfs-factory.bin  
> openwrt-ar71xx-generic-tl-wr941nd-v6-squashfs-sysupgrade.bin</p>
Обратите внимание на несколько очень важных деталей: 

  * Скорее всего, устанавливая OpenWRT вы лишитесь гарантии на устройство. Поэтому не продолжайте установку, если не готовы остаться с оборудованием один на один.
  * Перед установкой, прочтите все материалы по этой теме на <a href="http://openwrt.org/" target="_blank">официальном сайте проекта</a>&nbsp;и официальном <a href="http://wiki.openwrt.org/" target="_blank">Wiki</a>. Подробно остановитесь на <a href="http://wiki.openwrt.org/doc/howto/generic.flashing#method.1via.oem.firmware" target="_blank">установке</a> и <a href="http://wiki.openwrt.org/doc/howto/generic.overview" target="_blank">базовых операциях</a> (восстановление, возврат на OEM прошивку и т.д.)
  * Сделайте резервную копию вашей прошивки и/или конфигурации.
  * Не обновляйте прошивку по WiFi.

Ну и традиционное в таких случаях заявление: все дальнейшие действия вы совершаете на свой страх и риск.

Итак, допустим, что у вас хватило смелости и терпения установить OpenWRT. <a href="http://wiki.openwrt.org/doc/howto/firstlogin" target="_blank">Первый сеанс</a> доступа к устройству можно осуществить по telnet.
  


> telnet 192.168.1.1</p>
Сразу же смените пароль.
  


> root@openwrt:~$ passwd  
> <span style="color: #666666;">Changing password for root</span>  
> <span style="color: #666666;">New password:</span>  
> <span style="color: #666666;">Retype password:</span>  
> Password for root changed by root  
> <span style="color: #666666;">root@openwrt:~$</span></p>
Выйдите из telnet и подсоединитесь по SSH.
  


> ssh root@192.168.1.1</p>
Работа с OpenWRT с командной строки – занятие не из приятных. Я сразу же устанавливаю веб-интерфейс: LuCI.
  


> root@OpenWrt:~# opkg update  
> <span style="color: #666666;">Downloading http://downloads.openwrt.org/snapshots/trunk/ar71xx/packages/Packages.gz.</span>  
> <span style="color: #666666;">Updated list of available packages in /var/opkg-lists/snapshots.</span>  
> root@OpenWrt:~# opkg install luci luci-ssl  
> <span style="color: #666666;">Installing luci (svn-r9964-1) to root&#8230;</span>  
> <span style="color: #666666;">Downloading http://downloads.openwrt.org/snapshots/trunk/ar71xx/packages/luci_svn-r9964-1_ar71xx.ipk.</span>  
> <span style="color: #666666;">Installing luci-ssl (svn-r9964-1) to root&#8230;</span>  
> <span style="color: #666666;">Downloading http://downloads.openwrt.org/snapshots/trunk/ar71xx/packages/luci-ssl_svn-r9964-1_ar71xx.ipk.</span>  
> <span style="color: #666666;">Configuring luci.</span>  
> <span style="color: #666666;">Configuring luci-ssl.</span>  
> root@OpenWrt:~# /etc/init.d/uhttpd enable  
> root@OpenWrt:~# /etc/init.d/uhttpd start</p>
Если все прошло удачно, теперь по адресу https://192.168.1.1 вы сможете выполнить первичную настройку вашего роутера.

Теперь давайте настроим доступ к VPN. В предыдущем посте вы получили доступ к странице скачивания настроек соединения и клиентов VPN (https://droplet-ip:943/?src=connect). Вернитесь на нее под пользователем vpn_home и скачайте файл, обозначенный как user-locked profile. Разместите его в директории /etc/openvpn вашего роутера командой вроде
  


> scp Downloads/client.ovpn root@192.168.1.1:/etc/openvpn/</p>
В файле настроек нужно будет сделать одно изменение: добавить реквизиты доступа OpenVPN для автоматического соединения. В OpenWRT установлен редактор VI. Найдите в файле строку auth-user-pass и измените ее на такую:
  


> auth-user-pass /etc/openvpn/creds.txt</p><div>
  Сохраните файл и создайте рядом с ним другой, под названием creds.txt, содержащий имя пользователя vpn_home и его пароль – каждое значение в отдельной строке. Теперь откройте файл /etc/config/openvpn, найдите в нем строку, начинающуюся option config и приведите в следующий вид:
</div>

> option config /etc/openvpn/client.ovpn

<div>
  Создайте интерфейс для соединения по VPN – в файле /etc/config/network добавьте такую секцию:
</div>

<div>
  <blockquote>
    config interface &#8216;VPN_client&#8217;<br />&nbsp; &nbsp; &nbsp; &nbsp; option proto &#8216;none&#8217;<br />&nbsp; &nbsp; &nbsp; &nbsp; option ifname &#8216;tun0&#8217;</p>
  </blockquote>
</div>

<div>
  Чтобы трафик вашей локальной сети направлялся в VPN-туннель, добавьте в файл /etc/config/firewall такие строки:
</div>

<div>
  <blockquote>
    # NAT through VPN<br />config zone &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <br />&nbsp; &nbsp; &nbsp; &nbsp; option name &#8216;VPN_client&#8217; &nbsp; &nbsp;<br />&nbsp; &nbsp; &nbsp; &nbsp; option masq &#8216;1&#8217; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<br />&nbsp; &nbsp; &nbsp; &nbsp; option input &#8216;ACCEPT&#8217; &nbsp; &nbsp; &nbsp; &nbsp;<br />&nbsp; &nbsp; &nbsp; &nbsp; option forward &#8216;REJECT&#8217; &nbsp; &nbsp; &nbsp;<br />&nbsp; &nbsp; &nbsp; &nbsp; option output &#8216;ACCEPT&#8217; &nbsp; &nbsp; &nbsp; <br />&nbsp; &nbsp; &nbsp; &nbsp; option network &#8216;VPN_client&#8217;<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <br />config forwarding<br />&nbsp; &nbsp; &nbsp; &nbsp; option dest &#8216;VPN_client&#8217;<br />&nbsp; &nbsp; &nbsp; &nbsp; option src &#8216;lan&#8217;</p>
  </blockquote>
</div>

<div>
  После этого можно запускать openvpn:
</div>

<div>
  <blockquote>
    root@OpenWrt:/etc/openvpn# /etc/init.d/openvpn start<br />root@OpenWrt:/etc/openvpn# /etc/init.d/openvpn enable</p>
  </blockquote>
  
  <p>
    Признаком успешного соединения будет появление в системе сетевого интерфейса tun0. Проверить, что теперь ваш IP-адрес совпадает с адресом дроплета, можно, сделав запрос &#171;my ip&#187; в Google.
  </p>
  
  <p>
    В случае возникновения ошибок, почитайте сообщения в файле /var/log/openvpnas.log на сервере OpenVPN или опробуйте выполнить соединение вручную командой<br /> 
    
    <blockquote>
      root@OpenWrt:~# openvpn /etc/openvpn/client.ovpn</p>
    </blockquote>
    
    <p>
      Если все прошло успешно, то теперь у вас есть отличный VPN-туннель, который может очень пригодиться во время командировки в какую-нибудь не очень приветливую страну. Пользуйтесь с умом и не забудьте сделать резервную копию конфигурации OpenWRT. Оставайтесь в безопасности.
    </p></div> 
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_302">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-3-%25d0%25bd%25d0%25b0%25d1%2581%25d1%2582%25d1%2580%25d0%25be%25d0%25b9%25d0%25ba%25d0%25b0-openwrt%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%203%20%E2%80%93%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20OpenWRT" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-3-%25d0%25bd%25d0%25b0%25d1%2581%25d1%2582%25d1%2580%25d0%25be%25d0%25b9%25d0%25ba%25d0%25b0-openwrt%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%203%20%E2%80%93%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20OpenWRT" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-3-%25d0%25bd%25d0%25b0%25d1%2581%25d1%2582%25d1%2580%25d0%25be%25d0%25b9%25d0%25ba%25d0%25b0-openwrt%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%203%20%E2%80%93%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20OpenWRT" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-3-%25d0%25bd%25d0%25b0%25d1%2581%25d1%2582%25d1%2580%25d0%25be%25d0%25b9%25d0%25ba%25d0%25b0-openwrt%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%203%20%E2%80%93%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20OpenWRT" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
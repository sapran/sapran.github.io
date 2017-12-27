---
id: 838
title: 'VPN &#171;по-домашнему&#187;. Часть 1 – выбор и настройка облачного сервера'
date: 2014-04-04T21:29:00+00:00
author: sapran
layout: post
guid: http://styran.com/2014/04/04/vpn-%d0%bf%d0%be-%d0%b4%d0%be%d0%bc%d0%b0%d1%88%d0%bd%d0%b5%d0%bc%d1%83-%d1%87%d0%b0%d1%81%d1%82%d1%8c-1-%d0%b2%d1%8b%d0%b1%d0%be%d1%80-%d0%b8-%d0%bd%d0%b0%d1%81%d1%82%d1%80%d0%be%d0%b9/
permalink: /2014/04/vpn-%d0%bf%d0%be-%d0%b4%d0%be%d0%bc%d0%b0%d1%88%d0%bd%d0%b5%d0%bc%d1%83-%d1%87%d0%b0%d1%81%d1%82%d1%8c-1-%d0%b2%d1%8b%d0%b1%d0%be%d1%80-%d0%b8-%d0%bd%d0%b0%d1%81%d1%82%d1%80%d0%be%d0%b9/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2014/04/vpn-1.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/572545897996602090
shorturl:
  - http://tinyurl.com/odvgv7n
tags:
  - digitalocean
  - openvpn
  - vpn
  - приватность
---
Выход в Интернет &#171;через черный ход&#187; становится все более актуальной задачей для самых различных пользователей сети. Кто-то живет в стране, в которой зверствует государственная цензура, кто-то желает сохранить в тайне от провайдера характер передаваемых по сети данных, а у кого-то просто есть сомнения в безопасности подключения к оборудованию провайдера по витой паре, подвешенной под потолком подъезда. В таких случаях на помощь приходит старый добрый VPN, который в наше время можно настроить самостоятельно и использовать за вполне вменяемые деньги.

Я начинаю серию постов о том, как настроить персональный VPN-сервис подручными средствами. После некоторых метаний я выбрал для себя такой набор инструментов: 

  * <a href="https://www.digitalocean.com/" target="_blank">DigitalOcean</a> как поставщика облачной виртуальной машины скромной мощности с включенными 1Тб трафика &#8212; 5 долл. США в месяц.
  * <a href="https://openvpn.net/index.php/access-server/overview.html" target="_blank">OpenVPN Access Server</a> в качестве VPN-концентратора, он бесплатный для двух пользователей.
  * Домашний WiFi-роутер, поддерживаемый <a href="https://openwrt.org/" target="_blank">OpenWRT</a>. Может подойти и <a href="http://www.dd-wrt.com/" target="_blank">DD-WRT</a> или любой модем с поддержкой OpenVPN (я не нашел). В крайнем случае, вы просто сможете пользоваться VPN конечно устройства под управлением любой популярной ОС: Linux, MacOS X, Android, iOS и даже Windows.

<div>
  Итак, первый шаг настройки: идем на DigitalOcean, регистрируемся и выбираем самый дешевый инстанс (там они называются droplets) за $5/мес. В машинке будет 512Мб памяти, 1 процессор и 20 Гб винта, – этого с головой хватит для поставленной задачи.
</div>

<div style="clear: both; text-align: center;">
  <a href="http://1.bp.blogspot.com/-rNiZNOFgH_k/Uz8hMUgwQOI/AAAAAAAAnXc/aKH_-kYS0wI/s3200/Screenshot+2014-04-05+00.13.56.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://1.bp.blogspot.com/-rNiZNOFgH_k/Uz8hMUgwQOI/AAAAAAAAnXc/aKH_-kYS0wI/s3200/Screenshot+2014-04-05+00.13.56.png" height="231" width="400" /></a>
</div>

<div>
</div>

<div>
  В качестве региона можно выбрать Штаты, Голландию или Сингапур. Лично я предпочел остаться в Европе. Сингапур не рекомендую, у них государство приватностью особенно не заморачивается.
</div>

<div>
</div>

<div style="clear: both; text-align: center;">
  <a href="http://1.bp.blogspot.com/-XmwKFJhJWGc/Uz8hnNdkk6I/AAAAAAAAnXk/PpV4V15Yzrk/s3200/Screenshot+2014-04-05+00.17.24.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://1.bp.blogspot.com/-XmwKFJhJWGc/Uz8hnNdkk6I/AAAAAAAAnXk/PpV4V15Yzrk/s3200/Screenshot+2014-04-05+00.17.24.png" height="205" width="400" /></a>
</div>

<div>
</div>

<div>
  В качестве несущей ОС я выбрал Ubuntu 13.10, потому что на нее устанавливается OpenVPN AS.
</div>

<div>
</div>

<div style="clear: both; text-align: center;">
  <a href="http://2.bp.blogspot.com/-FGQKId50NBA/Uz8iP_QxawI/AAAAAAAAnXs/JSTJvhNtYsw/s3200/Screenshot+2014-04-05+00.20.15.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://2.bp.blogspot.com/-FGQKId50NBA/Uz8iP_QxawI/AAAAAAAAnXs/JSTJvhNtYsw/s3200/Screenshot+2014-04-05+00.20.15.png" height="296" width="400" /></a>
</div>

<div>
</div>

<div>
  Остальные опции не важны. Выбираем машинке имя и жмем &#171;Create Droplet&#187;.
</div>

<div>
</div>

<div>
  Получить доступ к машинке можно либо по виртуальной консоли (VNC со всеми вытекающими неудобствами), либо по SSH. Советую сразу же его настроить и обновить систему привычными apt-get update && apt-get -y upgrade от рута. В консоли управления дроплетами есть подробная инструкция по настройке доступа по SSH с использованием аутентификации ключами RSA: <a href="https://cloud.digitalocean.com/ssh_keys">https://cloud.digitalocean.com/ssh_keys</a>.
</div>

<div>
</div>

<div>
  Поздравляю, теперь у вас есть вполне рабочий &#171;боевой&#187; инстанс, на котором можно разместить будущий VPN-сервер. В следующем посте мы настроим OpenVPN AS, создадим пользователей и установим клиентское ПО на наши устройства.</p> 
  
  <p>
    <b><i>Update 2014-04-05</i></b><br />Для создания VPN-сервера в облаке можно воспользоваться услугами множества других поставщиков. Например, Amazon предлагает один бесплатный инстанс (<a href="http://aws.amazon.com/free/" target="_blank">free tier</a>) для вашего аккаунта, которым можно пользоваться год. Более того, в коллекции образов Amazon уже имеется виртуальный <a href="http://docs.openvpn.net/how-to-tutorialsguides/virtual-platforms/amazon-ec2-appliance-ami-quick-start-guide/" target="_blank">апплаянс OpenVPN AS</a>. Правда, после года использования услуга превращается в платную и обходится около $30/мес.
  </p>
  
  <p>
    Еще один вариант хостинга VPN-сервера – минимальный <a href="https://www.ubiquityhosting.com/cloud/order/1" target="_blank">инстанс от Ubiquity Hosting</a>. Сравнимые параметры и такой же объем трафика, что и на DigitalOcean, за $4/мес. Правда, все предлагаемые датацентры находятся в Штатах, что некоторым может не подойти.
  </p>
  
  <p>
    Также, есть вариант с использованием <a href="http://exchange.gogrid.com/partnergsi/openvpn%E2%84%A2-access-server" target="_blank">апплаянса OpenVPN AS на GoGrid</a>, о котором у меня нет ни информации, ни отзывов. Заявляется, что одноразовый платеж $5 за пользователя даст вам пожизненное право использовать сервис.</div> 
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_299">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-1-%25d0%25b2%25d1%258b%25d0%25b1%25d0%25be%25d1%2580-%25d0%25b8-%25d0%25bd%25d0%25b0%25d1%2581%25d1%2582%25d1%2580%25d0%25be%25d0%25b9%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%201%20%E2%80%93%20%D0%B2%D1%8B%D0%B1%D0%BE%D1%80%20%D0%B8%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%87%D0%BD%D0%BE%D0%B3%D0%BE%20%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-1-%25d0%25b2%25d1%258b%25d0%25b1%25d0%25be%25d1%2580-%25d0%25b8-%25d0%25bd%25d0%25b0%25d1%2581%25d1%2582%25d1%2580%25d0%25be%25d0%25b9%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%201%20%E2%80%93%20%D0%B2%D1%8B%D0%B1%D0%BE%D1%80%20%D0%B8%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%87%D0%BD%D0%BE%D0%B3%D0%BE%20%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-1-%25d0%25b2%25d1%258b%25d0%25b1%25d0%25be%25d1%2580-%25d0%25b8-%25d0%25bd%25d0%25b0%25d1%2581%25d1%2582%25d1%2580%25d0%25be%25d0%25b9%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%201%20%E2%80%93%20%D0%B2%D1%8B%D0%B1%D0%BE%D1%80%20%D0%B8%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%87%D0%BD%D0%BE%D0%B3%D0%BE%20%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2Fvpn-%25d0%25bf%25d0%25be-%25d0%25b4%25d0%25be%25d0%25bc%25d0%25b0%25d1%2588%25d0%25bd%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-1-%25d0%25b2%25d1%258b%25d0%25b1%25d0%25be%25d1%2580-%25d0%25b8-%25d0%25bd%25d0%25b0%25d1%2581%25d1%2582%25d1%2580%25d0%25be%25d0%25b9%2F&linkname=VPN%20%C2%AB%D0%BF%D0%BE-%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%BC%D1%83%C2%BB.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%201%20%E2%80%93%20%D0%B2%D1%8B%D0%B1%D0%BE%D1%80%20%D0%B8%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%87%D0%BD%D0%BE%D0%B3%D0%BE%20%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
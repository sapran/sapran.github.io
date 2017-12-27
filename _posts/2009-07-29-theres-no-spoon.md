---
id: 1103
title: 'There&#8217;s no spoon'
date: 2009-07-29T19:44:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/07/29/theres-no-spoon/
permalink: /2009/07/theres-no-spoon/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/07/theres-no-spoon.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/8946113014167072362
shorturl:
  - http://tinyurl.com/plkdrmh
tags:
  - периметр
  - сети
---
Еще раз (в который?) о периметре. В двух словах: периметра нет. Как и ложки.

<a style="" href="http://courses.ece.ubc.ca/251/library/images/photo_movieMatrix-quoteSpoon.jpg"><img style="margin: 0pt 10px 10px 0pt; float: left; cursor: pointer; width: 254px; height: 184px;" src="http://courses.ece.ubc.ca/251/library/images/photo_movieMatrix-quoteSpoon.jpg" alt="" border="0" /></a>Нередко можно встретить мнение, что неистово защищать инфраструктуру внутри сетевого периметра не стоит. Мол, мы достаточно потратили на межсетевые экраны ([firewalls](http://en.wikipedia.org/wiki/Firewall)), системы предотвращения вторжений ([NIPS](http://en.wikipedia.org/wiki/Network_Intrusion_Prevention_System)) и прочие секси феньки. Пусть теперь стоят себе, мигают красивыми лампочками и защищают нас от злых хакеров.

Мысль не здоровая и противоречит как минимум следующим фактам. 

  * Надежность логического (читай: сетевого) периметра обычно с лихвой компенсируется прозрачностью периметра физического. Проникновение на территорию компании и подключение к &#171;внутренней&#187; сети редко является недостижимой целью.
  * Установленные на периметре средства защиты редко настроены по принципу безопасного отказа (fail safe). То есть, если NIPS или firewall сдохнет &#8212; трафик продолжит неконтролируемо пересекать периметр. С точки зрения продолжения бизнес процессов это очень правильно, а с точки зрения безопасности &#8212; бред. В этом случае неподготовленные к внешним угрозам внутренние системы становятся более чем уязвимы.
  * Атака извне периметра &#8212; это всего лишь один из возможных векторов. Наряду с ней существуют социальная инженерия, вдохновляющая инсайдера атаковать системы изнутри. Не исключаем также разнообразный клиент-сайд, использующий уязвимое клиентское ПО в качестве отправной точки. В обоих случаях периметр бесполезен.
  * Периметр имеет свойство быть менее прочным на границах с т.н. экстрасетями (extranets) &#8212; точками интеграции с заказчиками, вендорами, аутсорсерами и прочими уважаемыми, но как правило бестолковыми спутниками жизни. Атака подрядчика с целью проникновения в инфраструктуру основной жертвы &#8212; намного более мудрая тактика, чем биться головой об ваш железобетонный периметр.

Список можно продолжать, но крик души не в этом. Забудьте о периметре, вернее, прекратите на него полагаться всецело. Сосредоточьтесь на защите данных и систем, в которых они обрабатываются и хранятся.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_38">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2Ftheres-no-spoon%2F&linkname=There%E2%80%99s%20no%20spoon" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2Ftheres-no-spoon%2F&linkname=There%E2%80%99s%20no%20spoon" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2Ftheres-no-spoon%2F&linkname=There%E2%80%99s%20no%20spoon" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2Ftheres-no-spoon%2F&linkname=There%E2%80%99s%20no%20spoon" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
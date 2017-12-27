---
id: 1136
title: Как заблокировать Skype
date: 2009-04-24T10:26:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/04/24/%d0%ba%d0%b0%d0%ba-%d0%b7%d0%b0%d0%b1%d0%bb%d0%be%d0%ba%d0%b8%d1%80%d0%be%d0%b2%d0%b0%d1%82%d1%8c-skype/
permalink: /2009/04/%d0%ba%d0%b0%d0%ba-%d0%b7%d0%b0%d0%b1%d0%bb%d0%be%d0%ba%d0%b8%d1%80%d0%be%d0%b2%d0%b0%d1%82%d1%8c-skype/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/04/skype.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4214256938077457409
shorturl:
  - http://tinyurl.com/ohzqznj
tags:
  - skype
  - squid
  - бумажные тигры
---
<div style="text-align: justify;">
  Skype рулит, я их фан. Я верю, что основателям проекта удасться выкупить его назад у eBay.&nbsp;Skype&nbsp;здорово шифрует трафик, предоставляя пользователям конфиденциальность общения. Его сетевая распределенная архитектура проста, надежна и не зависит от доступности какого-то определенного списка серверов.
</div>

<div>
</div>

<div>
  <div style="text-align: justify;">
    Эти качества делают Skype бельмом в глазу &#171;злых админов&#187;. Теоретически, Skype не вписывается ни в одну традиционную политику безопасности. О соотвествии всяческим стандартам и &#171;лучшим&#187; практикам не может быть и речи &#8212; DLP-решениям его трафик не прослушать, опционально передавать файлы и/или голос не запретить и т.д.&nbsp;Эта штука может просочиться через любые ограничения использования IM. Классический метод &#8212; работа через HTTP-прокси (который он способен обнаружить автоматически) по порту tcp/443. Серверов для добавления в черный список, как я уже сказал,&nbsp;тоже нет &#8212; все мастер-ноды не перечислить.
  </div>
</div>

<div>
</div>

<div>
  <div style="text-align: justify;">
    Во время посещения разнообразных тематических конференций, я имею обыкновение задавать инженерам на демо-стендах один вопрос: умеет ли ваше решение (UTM, DLP, IDS/IPS etc) блокировать&nbsp;Skype-трафик. Ответ у бизнеса всегда один: конечно же умеет. Но, как правило, после просьбы продемонстрировать этот функционал оказывается, что блокировка осуществляется при помощи, например, распознания в строке HTTP-агента регулярного выражения <span style="font-family: 'courier new';">[s|S]kype</span>, или еще какой-нибудь мега-аналитической фигни.
  </div>
</div>

<div>
</div>

<div>
  <div style="text-align: justify;">
    А на самом деле блокировку&nbsp;Skype можно организовать штатными средствами Squid. Для этого нужно объявить ACL при помощи регулярного выражения, описывающего IP-адрес, &nbsp;и&nbsp;запретить соотвествующий ей трафик.
  </div>
</div>

<div>
  <div>
  </div>
  
  <div>
    <span style="font-weight: bold;"><span style="font-family: 'courier new';">acl Numeric_IPs dstdom_regex ^[0-9]+.[0-9]+.[0-9]+.[0-9]+</span></span>
  </div>
  
  <div>
    <span style="font-weight: bold;"><span style="font-family: 'courier new';">http_access deny CONNECT Numeric_IPs</span></span>
  </div>
</div>

<div>
  <div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Под условия ACL попадают любые соединения, осуществляемые клиентами на IP-адреса, а не доменные имена. Согласитесь, если вашим коллегам понадобится доступ к нумерическому URL, то вы об этом должны знать. Можете разрешить их правилами типа
    </div>
  </div>
  
  <div>
  </div>
  
  <div>
    <div>
      <span style="font-weight: bold;"><span style="font-family: 'courier new';">acl Numeric_IPs_whitelist dst <ip 1="" address=""><ip_address></ip_address></ip></span></span><br /><span style="font-weight: bold;"><span style="font-family: 'courier new';">acl Numeric_IPs_whitelist dst <ip 2="" address=""></ip></span></span><br /><span style="font-family: 'courier new';"><b>&#8230;</b></span><br /><span style="font-weight: bold;"><span style="font-family: 'courier new';">acl Numeric_IPs_whitelist dst <ip address="" n=""></ip></span></span>
    </div>
    
    <div>
      <div>
        <span style="font-weight: bold;"><span style="font-family: 'courier new';">http_access allow CONNECT Numeric_IPs_whitelist</span></span>
      </div>
      
      <div>
      </div>
      
      <div>
        <div style="text-align: justify;">
          Все остальные соединения типа CONNECT на нумерические адреса &#8212; это либо SSL-туннели, либо сессии Skype, либо еще какая ересь. Нерегламентированные соединения такого рода из нашей сети нам не нужны.
        </div>
      </div>
    </div>
  </div>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_5">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F04%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d0%25b7%25d0%25b0%25d0%25b1%25d0%25bb%25d0%25be%25d0%25ba%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d1%2582%25d1%258c-skype%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D0%B7%D0%B0%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D1%82%D1%8C%20Skype" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F04%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d0%25b7%25d0%25b0%25d0%25b1%25d0%25bb%25d0%25be%25d0%25ba%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d1%2582%25d1%258c-skype%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D0%B7%D0%B0%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D1%82%D1%8C%20Skype" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F04%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d0%25b7%25d0%25b0%25d0%25b1%25d0%25bb%25d0%25be%25d0%25ba%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d1%2582%25d1%258c-skype%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D0%B7%D0%B0%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D1%82%D1%8C%20Skype" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F04%2F%25d0%25ba%25d0%25b0%25d0%25ba-%25d0%25b7%25d0%25b0%25d0%25b1%25d0%25bb%25d0%25be%25d0%25ba%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d1%2582%25d1%258c-skype%2F&linkname=%D0%9A%D0%B0%D0%BA%20%D0%B7%D0%B0%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D1%82%D1%8C%20Skype" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
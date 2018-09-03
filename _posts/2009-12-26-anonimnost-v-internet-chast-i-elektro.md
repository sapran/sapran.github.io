---
id: 1065
title: 'Анонимность в Интернет. Часть I: электронная почта'
date: 2009-12-26T21:32:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/12/26/%d0%b0%d0%bd%d0%be%d0%bd%d0%b8%d0%bc%d0%bd%d0%be%d1%81%d1%82%d1%8c-%d0%b2-%d0%b8%d0%bd%d1%82%d0%b5%d1%80%d0%bd%d0%b5%d1%82-%d1%87%d0%b0%d1%81%d1%82%d1%8c-i-%d1%8d%d0%bb%d0%b5%d0%ba%d1%82%d1%80%d0%be/
permalink: /2009/12/%d0%b0%d0%bd%d0%be%d0%bd%d0%b8%d0%bc%d0%bd%d0%be%d1%81%d1%82%d1%8c-%d0%b2-%d0%b8%d0%bd%d1%82%d0%b5%d1%80%d0%bd%d0%b5%d1%82-%d1%87%d0%b0%d1%81%d1%82%d1%8c-i-%d1%8d%d0%bb%d0%b5%d0%ba%d1%82%d1%80%d0%be/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/12/i.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/8580711897882026477
shorturl:
  - http://tinyurl.com/pbaxnyb
tags:
  - email
  - tor
  - анонимность
  - пентесты
  - социальная инженерия
  - фишинг
---
<span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;">Электронная почта, в простонародье email, &#8212; одно из древнейших средств связи </span></span><s><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;">на планете</span></span></s><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"> в Интернет. Самым распространенным протоколом обмена электронной почтой является <a href="http://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol">SMTP</a>. Это протокол был разработан без учета требований безопасности, поэтому практически весь секюрный функционал&nbsp;реализован&nbsp;в нем в виде обертки, или скорее &#171;костыля&#187;. Например, для обеспечения целостности и конфиденциальности сообщений эл. почты традиционно используются протоколы <a href="http://en.wikipedia.org/wiki/S/MIME">S/MIME</a> и <a href="http://en.wikipedia.org/wiki/Pretty_Good_Privacy">OpenPGP</a>, громоздкие &#171;надстройки&#187; над SMTP-сообщениями.</span></span>  
<span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"><br /></span> </span>  
<span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;">Я часто слышу вопросы вроде &#171;<b>насколько анонимна электронная почта?</b>&#187; и &#171;<b>возможно ли определить личность автора вредоносного и/или спамерского email?</b>&#187; В общем случае ответ зависит от технической подготовки злоумышленника, но как&nbsp;правило&nbsp;замаскировать или скрыть идентификационную информацию в email не составляет труда.</span></span>  
<span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"><br /></span> </span>  
<span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;">Сообщение SMTP состоит из <b>тела </b>и <b>заголовков</b>. Тело, это собственно текст и вложения, а заголовки содержат служебную информацию. Разделителем между заголовками и телом письма служат две пустых строки. Увидеть структуру SMTP-сообщения можно в любом почтовом клиентском ПО, в Gmail для этого нужно выбрать действие &#171;Show original&#187;.</span></span>  
<span style="font-family: monospace;"><span style="font-size: small; white-space: pre-wrap;"> </span></span> 

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-size: small;">Delivered-To: xaocuc@gmail.com<br />Received: by 10.86.89.19 with SMTP id m19cs400771fgb;<br />        Fri, 25 Dec 2009 07:09:02 -0800 (PST)<br />Received: by 10.114.214.24 with SMTP id m24mr8615191wag.93.1261753740738;<br />        Fri, 25 Dec 2009 07:09:00 -0800 (PST)<br />Received: from mx006.twitter.com (mx006.twitter.com [128.121.146.142])<br />        by mx.google.com with ESMTP id 18si28987983pwi.37.2009.12.25.07.08.59;<br />        Fri, 25 Dec 2009 07:08:59 -0800 (PST)<br /></span><b><span style="font-size: small;">Received: from twitter.com (localhost [127.0.0.1])<br /> by mx006.twitter.com (Postfix) with ESMTP id 04248DE4D13<br /> for </span></b>&lt;xaocuc@gmail.com><b><span style="font-size: small;">; Fri, 25 Dec 2009 15:08:59 +0000 (UTC)</span></b><span style="font-size: small;"><br />Date: Fri, 25 Dec 2009 15:08:59 +0000<br />From: Twitter </span>&lt;twitter-follow-xaocuc=gmail.com@postmaster.twitter.com><span style="font-size: small;"><br />Reply-To: noreply@postmaster.twitter.com<br />To: xaocuc@gmail.com<br />Subject: Vasiliy Pupkin is now following you on Twitter!<br /><br /><br />Hi, Volodymyr Styran (xaocuc).<br /><br />Vasiliy Pupkin (VasiliyPupkin) is now following your tweets on Twitter.<br /><br />Check out Vasiliy Pupkin's profile here:<br />  http://twitter.com/VasiliyPupkin<br /><br />You may follow Vasiliy Pupkin as well by clicking on the "follow" button.<br />Vasiliy Pupkin may not appear in your follower list. Vasiliy Pupkin may hav=<br />e decided to stop following you, or the account may have been suspended f=<br />or a Terms of Service violation.<br /><br />If you believe Vasiliy Pupkin is engaging in abusive behavior on Twitter, =<br />you may report Vasiliy Pupkin</span>&lt;/twitter-follow-xaocuc=gmail.com@postmaster.twitter.com>&lt;/xaocuc@gmail.com> for spam.</pre>

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-size: small;">Best,<br />Twitter<br /></span></pre>

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-size: small;"><br /></span></pre>

<pre style="white-space: pre-wrap; word-wrap: break-word;"></pre>

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="white-space: normal;"><span style="font-size: small;">Существует великое множество различных заголовков, в этом посте мы рассмотрим только некоторые из них.&nbsp;</span></span><span style="font-size: small;">В примере выше, видно историю доставки сообщения. Она отражена в заголовках <b>Received </b>(читать нужно снизу вверх). В каждом заголовке указан почтовый сервер (имя и IP-адрес), который участвовал в доставке сообщения. Самый первый, или нижний, заголовок демонстрирует, откуда письмо было отправлено первоначально.</span></span></pre>

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"><br /></span></span></pre>

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;">Если первый заголовок Received, содержащий имя и адрес компьютера, дает достаточно информации о расположении компьютера автора, то отыскать его теоретически возможно. Например, первым идет заголовок вида:</span></span></pre>

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"><br /></span></span></pre>

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-family: 'Sans Serif'; white-space: normal;"><br /><br /><br /><br />

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-size: small;">Received: from 133.133.133-pool.ukrtel.net ([95.133.133.133])<br />        by mx.google.com with ESMTP id 5si22328856vws.103.2009.12.26.07.49.01;<br />        Sat, 26 Dec 2009 07:49:34 -0800 (PST)</span></pre>


<p>
  </span></span>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;">Порывшись в Гугле и воспользовавшись службой <b><a href="http://tools.whois.net/whoisbyip/">whois</a></b>, можно предположить, что письмо отправлено из сети ОАО "Укртелеком". Имеем время отправки, есть с чем идти к провайдеру подозреваемого и просить сделать сверку с информацией из биллинга, -- какой абонент в заданное время пользовался этим IP-адресом. И вуаля -- автор сообщения определен. Быстро сказка сказывается, а в действительности это меленный и болезненный бюрократический процесс, справиться с которым в силах разве что следователи правоохранительных органов. Так что без веской причины никто подобные расследования не проводит.</span></pre>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"><br /></span></span></pre>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;">Итак, для того, чтобы отправить сообщение анонимно, злоумышленнику нужно замаскировать информацию в первом заголовке Received. К сожалению, это не очень сложная задача. В большинстве случаев, когда спам или вредоносные сообщения рассылаются на множество пользователей, это делается с использованием ботнетов. Ботнет представляет собой сеть из компьютеров-зомби, на которых выполняется специальная программа-бот (сокращенно от робот). Боты периодически обращаются за инструкциями к командным центрам (C&C) ботнета, через которые хозяева ботнета (bot herders) или злоумышленники, которые этот ботнет арендуют, приказывают ботам делать нам всякие гадости. Например, проводить распределенные DoS-атаки (Distributed Denial of Service attacks) или рассылать вирусы и спам. Естественно, в такой ситуации дальше имени и IP-адреса компьютера-зомби наше расследование не пойдет, а владелец зараженного ботом ПК в большинстве случаев об этом даже не знает. То есть, придется проводить более глубокое расследование, чем бы описали ранее: выяснять методы доставки бота на зомбированный&nbsp;компьютер, отслеживать центры управления, выяснять личность бот-хердера и только после этого, при помощи <a href="http://termorect.narod.ru/">терморектального криптоанализа</a>, выходить на заказчиков.</span></span></pre>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"><br /></span></span></pre>
  
  
  <div style="clear: both; text-align: center;">
    <a href="http://www.redbrick.dcu.ie/~gavin/wp-content/uploads/2007/01/tor_internet.png" style="clear: right; float: right; margin-bottom: 1em; margin-left: 1em;"><img border="0" height="151" src="http://www.redbrick.dcu.ie/~gavin/wp-content/uploads/2007/01/tor_internet.png" width="200" /></a>
  </div>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;">Использование ботнетов не единственный способ разослать почту анонимно. Я уже писал о сети <a href="http://securegalaxy.blogspot.com/search/label/tor">Tor</a>, созданной организацией EFF с самой что ни есть подходящей целью: для обеспечения анонимности в Интернет. Условия использования Tor не разрешают распространение спама и вредоносного кода, но мы ведь говорим сейчас о злостных хакерах и прочих аморальных элементах. Используя Tor, который представляет собой сеть распределенных <a href="http://en.wikipedia.org/wiki/SOCKS">SOCKS</a>-прокси, продвинутый злоумышленник без труда замаскируется до неузнаваемости. В заголовках SMTP будет виден адрес Tor-сервера, "выпустившего" SMTP-сессию в обычный Интернет, и имя компьютера злоумышленника, которым его SMTP-клиент представился первому SMTP-серверу в цепочке доставки. Злоумышленнику не составит труда подставить вместо имени нечто совершенно неразборчивое, вроде sFhBV09fv1jN. С использованием Tor и утилиты <a href="http://www.dest-unreach.org/socat/">socat</a>, я за несколько минут смог сформировать и выслать сообщение, оригинал которого выглядит следующим образом:</span></span></pre>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"><br /></span></span></pre>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-family: 'Sans Serif'; white-space: normal;"><br /><br /><br />

<pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-size: small;">Delivered-To: sapran@gmail.com<br />Received: by 10.220.97.194 with SMTP id m2cs273420vcn;<br />        Sat, 26 Dec 2009 07:49:35 -0800 (PST)<br />Received: by 10.220.122.170 with SMTP id l42mr14851380vcr.33.1261842574567;<br />        Sat, 26 Dec 2009 07:49:34 -0800 (PST)<br />Return-Path: &lt;support@twitter.com><br />&lt;/support@twitter.com></span><b><span style="font-size: small;">Received: from sFhBV09fv1jN ([119.110.103.59])<br /></span></b><span style="font-size: small;">        by mx.google.com with ESMTP id 5si22328856vws.103.2009.12.26.07.49.01;<br />        Sat, 26 Dec 2009 07:49:34 -0800 (PST)<br />Received-SPF: fail (google.com: domain of support@twitter.com does not designate 119.110.103.59 as permitted sender) client-ip=119.110.103.59;<br />Authentication-Results: mx.google.com; spf=hardfail (google.com: domain of support@twitter.com does not designate 119.110.103.59 as permitted sender) smtp.mail=support@twitter.com<br />Message-ID: &lt;486960.911748127-sendEmail@kk64&gt;<br />From: "support@twitter.com" &lt;support@twitter.com><br />To: "sapran@gmail.com" &lt;sapran@gmail.com><br />Subject: <br />Date: Sat, 26 Dec 2009 15:48:25 +0000<br />X-Mailer: sendEmail-1.55<br />MIME-Version: 1.0<br />Content-Type: multipart/related; boundary="----MIME delimiter for sendEmail-576975.834862427"<br /><br />This is a multi-part message in MIME format. To properly display this message you need a MIME-Version 1.0 compliant Email program.<br /><br />------MIME delimiter for sendEmail-576975.834862427<br />Content-Type: text/plain;<br />        charset="iso-8859-1"<br />Content-Transfer-Encoding: 7bit<br /><br />Hi @sapran!<br /><br />We checked your account and now it is unlocked!<br /><br />Happy twitting!<br />------MIME delimiter for sendEmail-576975.834862427--&lt;/sapran@gmail.com>&lt;/support@twitter.com></span></pre>


<p>
  </span></span>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;">Судя по whois, <a href="http://clez.net/net.whois?ip=119.110.103.59&t=ip">119.110.103.59 это где-то в Малайзии</a>.</span></pre>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;"><br /></span></span></pre>
  
  
  <pre style="white-space: pre-wrap; word-wrap: break-word;"><span style="font-family: 'Trebuchet MS', sans-serif;"><span style="font-size: small;">Как же отличить полезное письмо от подделки? В общем случае -- никак. Только подходя критично к каждому получаемому письму, можно существенно снизить свои шансы попасть в число жертв фишинга, социальной инженерии и прочего клиент-сайда. Будьте аккуратны во время работы с электронной почтой, и вам воздастся.</span></span></pre>
  
  
  <div class="addtoany_share_save_container addtoany_content_bottom">
    <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_76">
      <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25b0%25d0%25bd%25d0%25be%25d0%25bd%25d0%25b8%25d0%25bc%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-%25d0%25b8%25d0%25bd%25d1%2582%25d0%25b5%25d1%2580%25d0%25bd%25d0%25b5%25d1%2582-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-i-%25d1%258d%25d0%25bb%25d0%25b5%25d0%25ba%25d1%2582%25d1%2580%25d0%25be%2F&linkname=%D0%90%D0%BD%D0%BE%D0%BD%D0%B8%D0%BC%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%BD%D0%B5%D1%82.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20I%3A%20%D1%8D%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%BF%D0%BE%D1%87%D1%82%D0%B0" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25b0%25d0%25bd%25d0%25be%25d0%25bd%25d0%25b8%25d0%25bc%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-%25d0%25b8%25d0%25bd%25d1%2582%25d0%25b5%25d1%2580%25d0%25bd%25d0%25b5%25d1%2582-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-i-%25d1%258d%25d0%25bb%25d0%25b5%25d0%25ba%25d1%2582%25d1%2580%25d0%25be%2F&linkname=%D0%90%D0%BD%D0%BE%D0%BD%D0%B8%D0%BC%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%BD%D0%B5%D1%82.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20I%3A%20%D1%8D%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%BF%D0%BE%D1%87%D1%82%D0%B0" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25b0%25d0%25bd%25d0%25be%25d0%25bd%25d0%25b8%25d0%25bc%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-%25d0%25b8%25d0%25bd%25d1%2582%25d0%25b5%25d1%2580%25d0%25bd%25d0%25b5%25d1%2582-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-i-%25d1%258d%25d0%25bb%25d0%25b5%25d0%25ba%25d1%2582%25d1%2580%25d0%25be%2F&linkname=%D0%90%D0%BD%D0%BE%D0%BD%D0%B8%D0%BC%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%BD%D0%B5%D1%82.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20I%3A%20%D1%8D%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%BF%D0%BE%D1%87%D1%82%D0%B0" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25b0%25d0%25bd%25d0%25be%25d0%25bd%25d0%25b8%25d0%25bc%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-%25d0%25b8%25d0%25bd%25d1%2582%25d0%25b5%25d1%2580%25d0%25bd%25d0%25b5%25d1%2582-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-i-%25d1%258d%25d0%25bb%25d0%25b5%25d0%25ba%25d1%2582%25d1%2580%25d0%25be%2F&linkname=%D0%90%D0%BD%D0%BE%D0%BD%D0%B8%D0%BC%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%BD%D0%B5%D1%82.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20I%3A%20%D1%8D%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%BF%D0%BE%D1%87%D1%82%D0%B0" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
    </div>
  </div>
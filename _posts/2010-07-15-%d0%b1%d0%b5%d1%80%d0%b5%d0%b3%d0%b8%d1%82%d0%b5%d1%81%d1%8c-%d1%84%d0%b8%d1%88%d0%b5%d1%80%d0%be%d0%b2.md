---
id: 1032
title: Берегитесь фишеров
date: 2010-07-15T18:36:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/07/15/%d0%b1%d0%b5%d1%80%d0%b5%d0%b3%d0%b8%d1%82%d0%b5%d1%81%d1%8c-%d1%84%d0%b8%d1%88%d0%b5%d1%80%d0%be%d0%b2/
permalink: /2010/07/%d0%b1%d0%b5%d1%80%d0%b5%d0%b3%d0%b8%d1%82%d0%b5%d1%81%d1%8c-%d1%84%d0%b8%d1%88%d0%b5%d1%80%d0%be%d0%b2/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/07/blog-post.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/3039371915987061575
shorturl:
  - http://tinyurl.com/oepc7n8
tags:
  - gmail
  - приватность
  - спам
  - фишинг
---
<div style="text-align: justify;">
  Коллега прислал вчера довольно забавный образец фишингового письма. Нужно парням отдать должное, не без чувства юмора, хотя с правописанием не очень. Многоступенчатое шифрование это сильно. Оригинал сообщения следует далее, но давайте по порядку.
</div>

<div style="text-align: justify;">
  Для начала, что такое фишинг. Для большинства читающих этот блог, я уверен, это не новость. <b><a href="http://ru.wikipedia.org/wiki/%D0%A4%D0%B8%D1%88%D0%B8%D0%BD%D0%B3">Фишинг</a> </b>(<b><a href="http://en.wikipedia.org/wiki/Phishing">phishing</a></b>) &#8212; это электронно-почтовая атака с использованием элементов социальной инженерии, а если по-простому &#8212; обмана. Сообщение ниже &#8212; яркий тому пример.
</div>

<div style="text-align: justify;">
  Злоумышленник, под покровом фальшивого электронного адреса (<span style="font-size: x-small;"><span style="font-family: Arial, Helvetica, sans-serif;">conf@googlemail.com</span></span>) пытается выудить у жертвы логин и пароль к Google Mail. В выделенных <b><i>полужирным курсивом</i></b> заголовках (это такие слабо понятные служебные строки в перовой половине письма) видно, откуда (из какого почтового домена, с какого адреса) на самом деле было отправлено письмо. Сложность заключается в том, что в почтовом ящике заголовки полученного письма обычно не отображаются. По замыслу злодеев, жертва нажмет ссылку в конце сообщения, и попадет на специально подготовленный сайт, ничем не отличающийся от оригинала &#8212; GMail. После этого жертва введет свои логин и пароль в форму аутентификации и будет перенаправлена на настоящий GMail, а логин и пароль злой сайт запишет в файл или перешлет фишеру.
</div>

<div style="text-align: justify;">
  Для пущей правдоподобности, злоумышленник замаскировал ссылки в конце письма под доменное имя, которое выглядит вполне &#171;легально&#187;: googlemail.com. Хотя на самом деле в URL фигурирует домен googlernail.com, похожий на первый домен из-за схожести между комбинацией символов <b>rn </b>и буквой <b>m</b>. На данный момент этот домен уже <a href="http://bit.ly/a8bjSs">заблокирован</a> регистратором.
</div>

&#8212; 

<div style="font-family: inherit;">
  <span style="font-size: small;">Delivered-To:&nbsp; ***************@gmail.com<br />Received: by 10.216.210.226 with SMTP id u76cs30368weo;<br />Wed, 14 Jul 2010 05:48:01 -0700 (PDT)<br />Received: by 10.204.115.132 with SMTP id i4mr13248519bkq.129.1279111680867;<br />Wed, 14 Jul 2010 05:48:00 -0700 (PDT)<br />Return-Path: <nobody@rex.hc.ru></nobody@rex.hc.ru><br /><i><b>Received: from rex.hc.ru (rex.hc.ru [194.186.94.73])</b></i><br />by mx.google.com with ESMTP id s1si17899663bkf.85.2010.07.14.05.48.00;<br />Wed, 14 Jul 2010 05:48:00 -0700 (PDT)<br /><i><b>Received-SPF: pass (google.com: best guess record for domain of nobody@rex.hc.ru designates 194.186.94.73 as permitted sender) client-ip=194.186.94.73;</b></i><br /><i><b>Authentication-Results: mx.google.com; spf=pass (google.com: best guess record for domain of nobody@rex.hc.ru designates 194.186.94.73 as permitted sender) smtp.mail=nobody@rex.hc.ru</b></i><br /><i><b>Received: from nobody by rex.hc.ru with local (Exim 4.60 (FreeBSD))</b></i><i><b> </b><b>(envelope-from <nobody@rex.hc.ru>)</nobody@rex.hc.ru></b></i><i><b> </b><b>id 1OZ1NY-000D79-9Z</b></i><br />for ***************@gmail.com; Wed, 14 Jul 2010 16:48:00 +0400<br />To: ***************@gmail.com<br />Subject: =?windows-1251?B?yu7t9Ojk5e326ODr/O3g/yDv7vfy4CBHbWFpbA==?=<br />X-rbc-antispam: 18480<br />Date: Wed, 14 Jul 2010 16:48:00 +0400<br />From: =?windows-1251?B?yu7r6+Xq8ujiIEdtYWls?= <conf@googlemail.com></conf@googlemail.com><i><b><b7a72f4cdb86b070ffea347b9ad06551@muranoglass.ru></b7a72f4cdb86b070ffea347b9ad06551@muranoglass.ru></b></i><br />X-Priority: 3<br />X-Mailer: PHPMailer [version 777]<br />MIME-Version: 1.0<br />Content-Transfer-Encoding: 8bit<br />Content-Type: text/html; charset=&#187;windows-1251&#8243;</span>
</div>

<div style="font-family: inherit;">
  <span style="font-size: small;"><br /></span><br /><span style="font-size: small;">Уважаемый пользователь!</span>
</div>

<div style="font-family: inherit;">
  <span style="font-size: small;"><br />Рады сообщить, что начал работу новый сервис &#8212; <b>Конф<span style="color: red;">е</span>денциальная почта Gmail</b>!<br /></span> 
  
  <div style="text-align: justify;">
    <span style="font-size: small;">С помощью нашего сервиса Вы сможете передавать и принимать важные&nbsp;документы, надежно защищенные от посторонних глаз, благодаря <b>многоступенчатому шифрованию данных</b>.</span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-size: small;">Доступ к таким данным осуществляется с помощью разового пароля. Настроить доступ к сервису Вы сможете перейдя по ссылке ниже.&nbsp;</span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-size: small;">В настоящий момент в вашем ящике 2 новых сообщения. Чтобы прочитать их перейдите по ссылке:</span>
  </div>
  
  <p>
    <span style="font-size: small;"> &nbsp;</span></div> 
    
    <div style="font-family: inherit;">
      <span style="font-size: small;"><a href="http://www.googlernail.com/accounts/ServiceLogin/?%20%20%20***************@gmail.com">Конф<span style="color: red;">е</span>денциальные</a> <b>2</b> (0)</p> 
      
      <p>
        <a href="http://www.googlernail.com/accounts/ServiceLogin/?%20%20%20***************@gmail.com">Корзина</a> <b></b> (0)</span></div> 
        
        <div style="font-family: inherit;">
          <span style="font-size: small;"><br /></span>
        </div>
        
        <div align="&quot;left&quot;" style="font-family: inherit;">
          <span style="font-size: small;"><b>С уважением, Коллектив Gmail</b></span><br /><span style="font-size: x-small;"><b>&#8212; </b></span>
        </div>
        
        <p>
          <div style="text-align: justify;">
            Для того, чтобы избежать участи жертвы фишинга, нужно выполнять такие простые правила.
          </div>
          
          <div style="text-align: justify;">
            1. Не реагировать на спам. Ничего хорошего вам в нем все равно не пришлют.
          </div>
          
          <div style="text-align: justify;">
            2. Внимательно читать URL ссылок перед тем, как нажать на них. Наведите на ссылку указателем мыши и она (настоящая) появится в строке состояния браузера или почтовой программы.
          </div>
          
          <div style="text-align: justify;">
            3. Стараться использовать HTTPS для доступа к критичным сайтам, таким как Интернет-банкинг, веб-почта и корпоративные сайты.
          </div>
          
          <div style="text-align: justify;">
            4. Трижды задумываться перед тем, как вводить куда-то свой пароль.
          </div>
          
          <p>
            Будьте осторожны. Там, за экраном монитора, настоящие джунгли!..
          </p>
          
          <div class="addtoany_share_save_container addtoany_content_bottom">
            <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_109">
              <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d0%25b1%25d0%25b5%25d1%2580%25d0%25b5%25d0%25b3%25d0%25b8%25d1%2582%25d0%25b5%25d1%2581%25d1%258c-%25d1%2584%25d0%25b8%25d1%2588%25d0%25b5%25d1%2580%25d0%25be%25d0%25b2%2F&linkname=%D0%91%D0%B5%D1%80%D0%B5%D0%B3%D0%B8%D1%82%D0%B5%D1%81%D1%8C%20%D1%84%D0%B8%D1%88%D0%B5%D1%80%D0%BE%D0%B2" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d0%25b1%25d0%25b5%25d1%2580%25d0%25b5%25d0%25b3%25d0%25b8%25d1%2582%25d0%25b5%25d1%2581%25d1%258c-%25d1%2584%25d0%25b8%25d1%2588%25d0%25b5%25d1%2580%25d0%25be%25d0%25b2%2F&linkname=%D0%91%D0%B5%D1%80%D0%B5%D0%B3%D0%B8%D1%82%D0%B5%D1%81%D1%8C%20%D1%84%D0%B8%D1%88%D0%B5%D1%80%D0%BE%D0%B2" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d0%25b1%25d0%25b5%25d1%2580%25d0%25b5%25d0%25b3%25d0%25b8%25d1%2582%25d0%25b5%25d1%2581%25d1%258c-%25d1%2584%25d0%25b8%25d1%2588%25d0%25b5%25d1%2580%25d0%25be%25d0%25b2%2F&linkname=%D0%91%D0%B5%D1%80%D0%B5%D0%B3%D0%B8%D1%82%D0%B5%D1%81%D1%8C%20%D1%84%D0%B8%D1%88%D0%B5%D1%80%D0%BE%D0%B2" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d0%25b1%25d0%25b5%25d1%2580%25d0%25b5%25d0%25b3%25d0%25b8%25d1%2582%25d0%25b5%25d1%2581%25d1%258c-%25d1%2584%25d0%25b8%25d1%2588%25d0%25b5%25d1%2580%25d0%25be%25d0%25b2%2F&linkname=%D0%91%D0%B5%D1%80%D0%B5%D0%B3%D0%B8%D1%82%D0%B5%D1%81%D1%8C%20%D1%84%D0%B8%D1%88%D0%B5%D1%80%D0%BE%D0%B2" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
            </div>
          </div>
---
id: 1135
title: 'Repost: Безопасность Firefox'
date: 2009-04-24T10:53:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/04/24/repost-%d0%b1%d0%b5%d0%b7%d0%be%d0%bf%d0%b0%d1%81%d0%bd%d0%be%d1%81%d1%82%d1%8c-firefox/
permalink: /2009/04/repost-%d0%b1%d0%b5%d0%b7%d0%be%d0%bf%d0%b0%d1%81%d0%bd%d0%be%d1%81%d1%82%d1%8c-firefox/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/04/repost-firefox.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/3848837952342564548
shorturl:
  - http://tinyurl.com/pom74vw
tags:
  - firefox
---
<div dir="ltr" style="text-align: left;">
  <div style="text-align: justify;">
    <span style="border-collapse: collapse; font-family: arial; font-size: 13px;"><a href="http://www.mozilla-europe.org/ru/firefox/" style="color: #2244bb;" target="_blank">Firefox</a>&nbsp;по праву считается одним из наиболее безопасных броузеров. Сегодня я расскажу почему.</p> 
    
    <p>
      Беспроигрышный способ сделать систему безопасной &#8212; это сделать ее простой. Чем сложнее система, тем вероятнее возникновения в ней сбоя, способного привести к нарушению реализованной в системе политики безопасности. Браузеры в настоящее время по сложности своей не отстают от операционных систем. Следовательно, для обеспечения защиты браузера стоит воспользоваться той же стратегий, которой придерживаются разработчики безопасных ОС: заключить в ядре (т.н. trusted kernel) минимальный набор жизненно важных функций, а все остальное вынести в отдельные модули и обеспечить простой интерфейс взаимодействия модулей с ядром и друг с другом.
    </p>
    
    <p>
      <a href="http://www.mozilla.org/" style="color: #2244bb;" target="_blank">Mozilla</a>&nbsp;оказались первыми, кто уяснил эту истину. Firefox поставляется в минимальной комплектации:&nbsp;<a href="http://www.mozilla.org/newlayout/" style="color: #2244bb;" target="_blank">HTML-рендер</a>&nbsp;(ниже этого порога не пригнешься, это обязательная составляющая браузера) и компактный&#8230; ну в общем то, что программисты броузеров называют chrome (та часть браузера, которая не имеет отношения непосредственно к рендерингу). Firefox можно дополнить многочисленнейшими дополнениями (<a href="https://addons.mozilla.org/en-US/firefox/addon/220/#install-55052" style="color: #2244bb;" target="_blank">add-ons</a>), расширяя тем самым функционал ПО до необходимых пользователю размеров.
    </p>
    
    <p>
      Теперь о главном: какие настройки и дополнения следует использовать и почему.
    </p>
    
    <p>
      Для начала нужно отключить 3rd party cookies. Вещь эта пользователю совершенно не нужна, зато позволяет многочисленным умникам от рекламы типа DoubleClick эффективно отслеживать активность пользователей. Идем в Options->Privacy и снимаем галку с Accept third-party cookies.Здесь есть один любопытный нюанс. Если кто-то пользуется Google Toolbar, как это делаю я, то перманентная авторизация в учетной записи Google после отключения 3rd party cookies работать перестанет. Чтобы вернуть все на место, добавьте исключение (Exceptions&#8230;) для домена google.com.
    </p>
    
    <p>
      В Options->Security советую использовать опцию Use a master password. Возни много не добавляет, зато защищает от праздно шатающихся любителей посидеть за чужими компьютерами.
    </p>
    
    <p>
      Помимо тех дополнений, которые вы сами себе наставите, в джентельменском наборе обязательно должны присутствовать:<br /></span></div> 
      
      <ul style="text-align: justify;">
        <li>
          <span style="border-collapse: collapse; font-family: arial; font-size: 13px;"><a href="https://addons.mozilla.org/en-US/firefox/addon/722" style="color: #2244bb;" target="_blank">NoScript</a>&nbsp;&#8212; в прямом смысле останавливает выполнение скриптов и прочих выполняемых объектов (Flash, QuickTime etc) на открываемой странице. Защищает от множества распространенных, я бы даже сказал типичных и распиаренных атак типа Crosssite Scripting, Crosssite Request Forgery & Clickjacking. Легко настраивается в процессе использования, позволяя разрешить выполнение скриптов в отдельных доменах.</span>
        </li>
        <p>
          <span style="border-collapse: collapse; font-family: arial; font-size: 13px;"> 
          
          <li>
            <a href="https://addons.mozilla.org/en-US/firefox/addon/1865" style="color: #2244bb;" target="_blank">AdBlock Plus</a>&nbsp;&#8212; превосходный фильтр рекламы. Меня всегда умиляет нытье ЖЖ-фреглов, утомленных перегруженными баннерами френдлентами. С ABP их (баннера) просто не замечаешь.
          </li>
          <p>
            </span></ul> 
            
            <p>
              <span style="border-collapse: collapse; font-family: arial; font-size: 13px;">Для начала достаточно. Если кто-то заинтересовался темой всерьез, добро пожаловать в раздел&nbsp;<a href="https://addons.mozilla.org/en-US/firefox/browse/type:1/cat:12" style="color: #2244bb;" target="_blank">Privacy & Security</a>&nbsp;библиотеки дополнений Firefox.</span> 
              
              <div style="text-align: justify;">
              </div></div> 
              
              <div class="addtoany_share_save_container addtoany_content_bottom">
                <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_6">
                  <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F04%2Frepost-%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-firefox%2F&linkname=Repost%3A%20%D0%91%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20Firefox" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F04%2Frepost-%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-firefox%2F&linkname=Repost%3A%20%D0%91%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20Firefox" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F04%2Frepost-%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-firefox%2F&linkname=Repost%3A%20%D0%91%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20Firefox" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F04%2Frepost-%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-firefox%2F&linkname=Repost%3A%20%D0%91%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20Firefox" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
                </div>
              </div>
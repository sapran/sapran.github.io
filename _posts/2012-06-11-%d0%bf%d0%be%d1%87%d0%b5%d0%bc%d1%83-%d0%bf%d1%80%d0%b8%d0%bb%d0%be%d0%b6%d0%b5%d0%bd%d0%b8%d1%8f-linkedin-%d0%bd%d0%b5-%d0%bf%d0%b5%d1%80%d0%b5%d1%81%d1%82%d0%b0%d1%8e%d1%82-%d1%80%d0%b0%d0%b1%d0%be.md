---
id: 901
title: Почему приложения LinkedIn не перестают работать после смены пароля
date: 2012-06-11T07:52:00+00:00
author: sapran
layout: post
guid: http://styran.com/2012/06/11/%d0%bf%d0%be%d1%87%d0%b5%d0%bc%d1%83-%d0%bf%d1%80%d0%b8%d0%bb%d0%be%d0%b6%d0%b5%d0%bd%d0%b8%d1%8f-linkedin-%d0%bd%d0%b5-%d0%bf%d0%b5%d1%80%d0%b5%d1%81%d1%82%d0%b0%d1%8e%d1%82-%d1%80%d0%b0%d0%b1%d0%be/
permalink: /2012/06/%d0%bf%d0%be%d1%87%d0%b5%d0%bc%d1%83-%d0%bf%d1%80%d0%b8%d0%bb%d0%be%d0%b6%d0%b5%d0%bd%d0%b8%d1%8f-linkedin-%d0%bd%d0%b5-%d0%bf%d0%b5%d1%80%d0%b5%d1%81%d1%82%d0%b0%d1%8e%d1%82-%d1%80%d0%b0%d0%b1%d0%be/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2012/06/linkedin.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/3961342260481975673
shorturl:
  - http://tinyurl.com/p5nhv75
tags:
  - социальные сети
---
<div dir="ltr" style="text-align: left;">
  Многие недоумевают, некоторые даже&nbsp;возмущаются, почему после смены пароля в LinkedIn, выполненной в ответ на недавнюю утечку &#171;пресных&#187; хешей, клиентские приложения (в частности под Андроид) продолжили работать как не в чем не бывало.</p> 
  
  <p>
    Опыт программирования клиентского софта под Twitter дает мне возможность строить догадки. Я понимаю это так: все приложения получают доступ к LinkedIn по API. Аутентификация и авторизация приложений происходит по ключам API, которые приложение получает в момент, когда А) вы жмете кнопку Authorize App или что-то вроде это или Б) вводите логин и пароль в момент первого входа.
  </p>
  
  <p>
    Зачем это делается? Во-первых, чтобы не давать приложению &#171;все права&#187;. В зависимости от веб-сайта,&nbsp;авторизовать&nbsp;можно какой-то специфичный набор&nbsp;привилегий, например, постить сообщения на стену, читать контакты и т.п. Во-вторых, и это правильно, чтобы не хранить пароль.
  </p>
  
  <p>
    Как это исправить? Руководствуясь советами в этом посте: <i><a href="http://securegalaxy.blogspot.com/2010/11/oauth.html" style="font-weight: bold;">OAuth и доступ к вашим учетным записям в социальных сетях</a>.</i></div> 
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_239">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F06%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d0%25bf%25d1%2580%25d0%25b8%25d0%25bb%25d0%25be%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f-linkedin-%25d0%25bd%25d0%25b5-%25d0%25bf%25d0%25b5%25d1%2580%25d0%25b5%25d1%2581%25d1%2582%25d0%25b0%25d1%258e%25d1%2582-%25d1%2580%25d0%25b0%25d0%25b1%25d0%25be%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%20LinkedIn%20%D0%BD%D0%B5%20%D0%BF%D0%B5%D1%80%D0%B5%D1%81%D1%82%D0%B0%D1%8E%D1%82%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D1%82%D1%8C%20%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20%D1%81%D0%BC%D0%B5%D0%BD%D1%8B%20%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D1%8F" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F06%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d0%25bf%25d1%2580%25d0%25b8%25d0%25bb%25d0%25be%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f-linkedin-%25d0%25bd%25d0%25b5-%25d0%25bf%25d0%25b5%25d1%2580%25d0%25b5%25d1%2581%25d1%2582%25d0%25b0%25d1%258e%25d1%2582-%25d1%2580%25d0%25b0%25d0%25b1%25d0%25be%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%20LinkedIn%20%D0%BD%D0%B5%20%D0%BF%D0%B5%D1%80%D0%B5%D1%81%D1%82%D0%B0%D1%8E%D1%82%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D1%82%D1%8C%20%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20%D1%81%D0%BC%D0%B5%D0%BD%D1%8B%20%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D1%8F" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F06%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d0%25bf%25d1%2580%25d0%25b8%25d0%25bb%25d0%25be%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f-linkedin-%25d0%25bd%25d0%25b5-%25d0%25bf%25d0%25b5%25d1%2580%25d0%25b5%25d1%2581%25d1%2582%25d0%25b0%25d1%258e%25d1%2582-%25d1%2580%25d0%25b0%25d0%25b1%25d0%25be%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%20LinkedIn%20%D0%BD%D0%B5%20%D0%BF%D0%B5%D1%80%D0%B5%D1%81%D1%82%D0%B0%D1%8E%D1%82%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D1%82%D1%8C%20%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20%D1%81%D0%BC%D0%B5%D0%BD%D1%8B%20%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D1%8F" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F06%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d0%25bf%25d1%2580%25d0%25b8%25d0%25bb%25d0%25be%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f-linkedin-%25d0%25bd%25d0%25b5-%25d0%25bf%25d0%25b5%25d1%2580%25d0%25b5%25d1%2581%25d1%2582%25d0%25b0%25d1%258e%25d1%2582-%25d1%2580%25d0%25b0%25d0%25b1%25d0%25be%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%20LinkedIn%20%D0%BD%D0%B5%20%D0%BF%D0%B5%D1%80%D0%B5%D1%81%D1%82%D0%B0%D1%8E%D1%82%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D1%82%D1%8C%20%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20%D1%81%D0%BC%D0%B5%D0%BD%D1%8B%20%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D1%8F" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
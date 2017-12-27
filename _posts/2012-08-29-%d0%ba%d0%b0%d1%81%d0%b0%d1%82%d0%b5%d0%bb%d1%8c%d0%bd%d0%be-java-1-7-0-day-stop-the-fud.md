---
id: 893
title: 'Касательно Java 1.7 0-day: STOP THE FUD!'
date: 2012-08-29T10:50:00+00:00
author: sapran
layout: post
guid: http://styran.com/2012/08/29/%d0%ba%d0%b0%d1%81%d0%b0%d1%82%d0%b5%d0%bb%d1%8c%d0%bd%d0%be-java-1-7-0-day-stop-the-fud/
permalink: /2012/08/%d0%ba%d0%b0%d1%81%d0%b0%d1%82%d0%b5%d0%bb%d1%8c%d0%bd%d0%be-java-1-7-0-day-stop-the-fud/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2012/08/java-17-0-day-stop-fud.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/3219254152952045136
shorturl:
  - http://tinyurl.com/p4yddl4
tags:
  - 0-day
  - dumb asses
  - fud
  - java
---
<div dir="ltr" style="text-align: left;">
  Только тем, кто провел последнюю неделю в пещере, не известно, что в Интернете &#171;бушует&#187; очередной client-side 0-day в Java, поэтому буду краток. Бушует он в основном в блогах по безопасности и прочих профильных песочницах. Нередко слышны призывы вендоров, особенно антивирусных, побыстрее скупать &#171;змеиное масло&#187; против этой беды, ведь они уже добавили сигнатуру в свои обновления. Правда, пока только для варианта от Metasploit, но ведь какая, в сущности, разница? А ведь в мире аж целых 3 млрд устройств снабжены Java&#8230;</p> 
  
  <p>
    Я не отрицаю, эксплойт опасный и распространять информацию о нем в массы очень важно. Но задумайтесь на мгновение: сколько компаний и рядовых пользователей уже мигрировали с Java 6 на Java 7? Ведь рабочий эксплойт есть пока только для последней версии.
  </p>
  
  <p>
    И если кто-то мне подскажет, какая часть юзеров уже на Джаве 1.7, я с удовольствием заменю N на действительное число в этом уравнении, а пока:
  </p>
  
  <div style="text-align: center;">
    <b>Реальная_угроза (<a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=2012-4681">CVE-2012-4681</a>) = <a href="http://en.wikipedia.org/wiki/Fear,_uncertainty_and_doubt">FUD</a> / N</b>
  </div>
  
  <div style="text-align: left;">
    <b><br /></b>
  </div>
  
  <div style="text-align: left;">
    <b>P.S. </b>Если вы все-таки уже пользуетесь Java 1.7, удалите ее или пользуйтесь последней версией ветки 1.6 до выхода исправления:)
  </div>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_246">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F08%2F%25d0%25ba%25d0%25b0%25d1%2581%25d0%25b0%25d1%2582%25d0%25b5%25d0%25bb%25d1%258c%25d0%25bd%25d0%25be-java-1-7-0-day-stop-the-fud%2F&linkname=%D0%9A%D0%B0%D1%81%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE%20Java%201.7%200-day%3A%20STOP%20THE%20FUD%21" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F08%2F%25d0%25ba%25d0%25b0%25d1%2581%25d0%25b0%25d1%2582%25d0%25b5%25d0%25bb%25d1%258c%25d0%25bd%25d0%25be-java-1-7-0-day-stop-the-fud%2F&linkname=%D0%9A%D0%B0%D1%81%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE%20Java%201.7%200-day%3A%20STOP%20THE%20FUD%21" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F08%2F%25d0%25ba%25d0%25b0%25d1%2581%25d0%25b0%25d1%2582%25d0%25b5%25d0%25bb%25d1%258c%25d0%25bd%25d0%25be-java-1-7-0-day-stop-the-fud%2F&linkname=%D0%9A%D0%B0%D1%81%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE%20Java%201.7%200-day%3A%20STOP%20THE%20FUD%21" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F08%2F%25d0%25ba%25d0%25b0%25d1%2581%25d0%25b0%25d1%2582%25d0%25b5%25d0%25bb%25d1%258c%25d0%25bd%25d0%25be-java-1-7-0-day-stop-the-fud%2F&linkname=%D0%9A%D0%B0%D1%81%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE%20Java%201.7%200-day%3A%20STOP%20THE%20FUD%21" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
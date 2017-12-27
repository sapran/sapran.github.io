---
id: 960
title: Megafon + Яндекс =
date: 2011-07-19T07:19:00+00:00
author: sapran
layout: post
guid: http://styran.com/2011/07/19/megafon-%d1%8f%d0%bd%d0%b4%d0%b5%d0%ba%d1%81/
permalink: /2011/07/megafon-%d1%8f%d0%bd%d0%b4%d0%b5%d0%ba%d1%81/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2011/07/megafon.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/6731185443034295568
shorturl:
  - http://tinyurl.com/ngr4el8
tags:
  - инциденты
  - приватность
---
<div style="text-align: justify;">
  Все наверняка уже слышали о вакханалии нарушения тайны переписки, которую на днях учинил Мегафон. Если нет, то в двух словах: на их сайте отправки СМС Яндексом были проиндексированы более 8,000 отправленных сообщений. С подробностями можно ознакомиться <a href="https://webcache.googleusercontent.com/search?q=cache%3Ahttp%3A%2F%2Fhabrahabr.ru%2Fblogs%2Finfosecurity%2F124370%2F">на этой проиндексированной странице</a>. По непонятным причинам оригинал с Хабра уже исчез, что совершенно бесполезно в силу надежности кеша Google и широкого распространения этой новости: вчера слова &#171;Megafon&#187; и &#171;Яндекс&#187; на короткое время попали в тренды Twitter.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  После прочтения новости я еще больше разочаровался в Интернет-журналистике. Большинство новостных статей на эту тему явно ассоциировали Яндекс с инцидентом. Хотя на самом деле поисковик просто сделал свою работу: проиндексировал содержимое одного из популярных веб-сайтов рунета. В этой связи ни малейшей вины Яндекса в произошедшем нет.</p> 
  
  <p>
    Виноват сам Мегафон. Вчера я было подумал, что на сайте <i>sendsms.megafon.ru</i> неправильно настроен файл <b><i>robots.txt</i></b>, но как выяснилось сегодня, его там просто не было. В комбинации с &#171;гениальнейшей&#187; идеей хранить отправленные сообщения прямо в одном из подкаталогов сайта мы и получили это происшествие. То есть, резюмируя:</div> 
    
    <ol style="text-align: justify;">
      <li>
        Программисты Мегафона, или кому он там аутсорсит эту функцию, ошиблись в выборе места хранения отправленных сообщений. Для этого было бы безопаснее использовать базу данных, или хотя бы неиндексируемый каталог веб-сервера (см. п. 2).
      </li>
      <li>
        Админы Мегафона серьезно напортачили с robots.txt. Для несведущих, в файле с таким названием каждый вебмастер может запретить индексацию всего своего сайта, или его отдельных подкаталогов. Поисковый &#171;паук&#187;, наткнувшись на robots.txt, следует изложенным в нем инструкциям. Например, файл следующего содержания скомандует поисковику индексировать все кроме каталогов <i>private </i>и <i>sentsms.</i> <pre style="margin-left: 40px;">User-agent: *<br />Disallow: /private<br />Disallow: /sentsms</pre>
      </li>
      
      <li>
        Мегафон показал неэффективность или отсутствие контроля над изменениями и анализа рисков в этом контексте. Можно сколько угодно винить админов и программистов веб-сайта, но пока Мегафон не продемонстрирует наличие действующего контроля над изменениями, и админы, и программисты останутся всего лишь &#171;стрелочниками&#187;.
      </li>
    </ol>
    
    <div style="text-align: justify;">
      Сейчас начнутся всевозможные расследования, анализ законодательства на предмет какие законы были нарушены и прочая возня. Не исключаю, что кого-то из админов, программистов или их руководителей сделают козлом отпущения, но систему это не изменит. Мне хочется надеяться, что произошедшее это исключение из правил, но к сожалению это не так.
    </div>
    
    <div style="text-align: justify;">
    </div>
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_181">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F07%2Fmegafon-%25d1%258f%25d0%25bd%25d0%25b4%25d0%25b5%25d0%25ba%25d1%2581%2F&linkname=Megafon%20%2B%20%D0%AF%D0%BD%D0%B4%D0%B5%D0%BA%D1%81%20%3D" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F07%2Fmegafon-%25d1%258f%25d0%25bd%25d0%25b4%25d0%25b5%25d0%25ba%25d1%2581%2F&linkname=Megafon%20%2B%20%D0%AF%D0%BD%D0%B4%D0%B5%D0%BA%D1%81%20%3D" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F07%2Fmegafon-%25d1%258f%25d0%25bd%25d0%25b4%25d0%25b5%25d0%25ba%25d1%2581%2F&linkname=Megafon%20%2B%20%D0%AF%D0%BD%D0%B4%D0%B5%D0%BA%D1%81%20%3D" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F07%2Fmegafon-%25d1%258f%25d0%25bd%25d0%25b4%25d0%25b5%25d0%25ba%25d1%2581%2F&linkname=Megafon%20%2B%20%D0%AF%D0%BD%D0%B4%D0%B5%D0%BA%D1%81%20%3D" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
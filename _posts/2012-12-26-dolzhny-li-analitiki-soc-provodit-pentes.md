---
id: 883
title: Должны ли аналитики SOC проводить пентесты?
date: 2012-12-26T16:56:00+00:00
author: sapran
layout: post
guid: http://styran.com/2012/12/26/%d0%b4%d0%be%d0%bb%d0%b6%d0%bd%d1%8b-%d0%bb%d0%b8-%d0%b0%d0%bd%d0%b0%d0%bb%d0%b8%d1%82%d0%b8%d0%ba%d0%b8-soc-%d0%bf%d1%80%d0%be%d0%b2%d0%be%d0%b4%d0%b8%d1%82%d1%8c-%d0%bf%d0%b5%d0%bd%d1%82%d0%b5%d1%81/
permalink: /2012/12/%d0%b4%d0%be%d0%bb%d0%b6%d0%bd%d1%8b-%d0%bb%d0%b8-%d0%b0%d0%bd%d0%b0%d0%bb%d0%b8%d1%82%d0%b8%d0%ba%d0%b8-soc-%d0%bf%d1%80%d0%be%d0%b2%d0%be%d0%b4%d0%b8%d1%82%d1%8c-%d0%bf%d0%b5%d0%bd%d1%82%d0%b5%d1%81/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2012/12/soc.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/2996533596763707390
shorturl:
  - http://tinyurl.com/or9tyf8
tags:
  - инциденты
  - пентесты
---
Val Smith написал з[амечательный пост на сайте attackresearch.com](http://carnal0wnage.attackresearch.com/2012/12/your-soldiers-are-untrained.html), в котором поднял тему трагического&nbsp;несоответствия&nbsp;существующих методов и техник тестирования на проникновение (penetration test, pentest) тем действиям кибер-преступников, которые эти пентесты&nbsp;по идее должны симулировать.

По мнению автора, и я склонен с ним согласиться, современный пентест это, как правило, проверка эффективности программы управления уязвимостями. В то время, как актуальные хакерские атаки уже давно не&nbsp;ограничиваются&nbsp;поиском известных уязвимостей в ПО и его настройках с их дальнейшей эксплуатацией.

Вместо проверки исправлений на серверах и маршрутизаторах, автор предлагает&nbsp;тренировать&nbsp;и проверять уровень подготовки подразделений ИБ. Путем симуляции атак, приближенных к реальным, наблюдаемым в диком интернете. Логически возникает вопрос: как и откуда черпать полную и подробную информацию о таких атаках? Автор предлагает замечательный способ &#8212; имитацией атак должны заниматься специалисты, постоянно задействованные в процессе реагирования на инциденты. То есть, имеющее полное представление о тактике атакующего и его инструментах.

Похожей теме был посвящен мой доклад на конференции UISGCON8, но в этом случае автор пошел дальше, копнул глубже, и вообще молодец. Поэтому, мое мнение в этом вопросе может быть необъективным, и я прошу высказаться коллег: как вы считаете, заслуживает ли внимания такой подход к организации процесса тестирования защищенности?

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_255">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F12%2F%25d0%25b4%25d0%25be%25d0%25bb%25d0%25b6%25d0%25bd%25d1%258b-%25d0%25bb%25d0%25b8-%25d0%25b0%25d0%25bd%25d0%25b0%25d0%25bb%25d0%25b8%25d1%2582%25d0%25b8%25d0%25ba%25d0%25b8-soc-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b2%25d0%25be%25d0%25b4%25d0%25b8%25d1%2582%25d1%258c-%25d0%25bf%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b5%25d1%2581%2F&linkname=%D0%94%D0%BE%D0%BB%D0%B6%D0%BD%D1%8B%20%D0%BB%D0%B8%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B8%20SOC%20%D0%BF%D1%80%D0%BE%D0%B2%D0%BE%D0%B4%D0%B8%D1%82%D1%8C%20%D0%BF%D0%B5%D0%BD%D1%82%D0%B5%D1%81%D1%82%D1%8B%3F" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F12%2F%25d0%25b4%25d0%25be%25d0%25bb%25d0%25b6%25d0%25bd%25d1%258b-%25d0%25bb%25d0%25b8-%25d0%25b0%25d0%25bd%25d0%25b0%25d0%25bb%25d0%25b8%25d1%2582%25d0%25b8%25d0%25ba%25d0%25b8-soc-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b2%25d0%25be%25d0%25b4%25d0%25b8%25d1%2582%25d1%258c-%25d0%25bf%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b5%25d1%2581%2F&linkname=%D0%94%D0%BE%D0%BB%D0%B6%D0%BD%D1%8B%20%D0%BB%D0%B8%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B8%20SOC%20%D0%BF%D1%80%D0%BE%D0%B2%D0%BE%D0%B4%D0%B8%D1%82%D1%8C%20%D0%BF%D0%B5%D0%BD%D1%82%D0%B5%D1%81%D1%82%D1%8B%3F" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F12%2F%25d0%25b4%25d0%25be%25d0%25bb%25d0%25b6%25d0%25bd%25d1%258b-%25d0%25bb%25d0%25b8-%25d0%25b0%25d0%25bd%25d0%25b0%25d0%25bb%25d0%25b8%25d1%2582%25d0%25b8%25d0%25ba%25d0%25b8-soc-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b2%25d0%25be%25d0%25b4%25d0%25b8%25d1%2582%25d1%258c-%25d0%25bf%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b5%25d1%2581%2F&linkname=%D0%94%D0%BE%D0%BB%D0%B6%D0%BD%D1%8B%20%D0%BB%D0%B8%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B8%20SOC%20%D0%BF%D1%80%D0%BE%D0%B2%D0%BE%D0%B4%D0%B8%D1%82%D1%8C%20%D0%BF%D0%B5%D0%BD%D1%82%D0%B5%D1%81%D1%82%D1%8B%3F" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F12%2F%25d0%25b4%25d0%25be%25d0%25bb%25d0%25b6%25d0%25bd%25d1%258b-%25d0%25bb%25d0%25b8-%25d0%25b0%25d0%25bd%25d0%25b0%25d0%25bb%25d0%25b8%25d1%2582%25d0%25b8%25d0%25ba%25d0%25b8-soc-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b2%25d0%25be%25d0%25b4%25d0%25b8%25d1%2582%25d1%258c-%25d0%25bf%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b5%25d1%2581%2F&linkname=%D0%94%D0%BE%D0%BB%D0%B6%D0%BD%D1%8B%20%D0%BB%D0%B8%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B8%20SOC%20%D0%BF%D1%80%D0%BE%D0%B2%D0%BE%D0%B4%D0%B8%D1%82%D1%8C%20%D0%BF%D0%B5%D0%BD%D1%82%D0%B5%D1%81%D1%82%D1%8B%3F" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
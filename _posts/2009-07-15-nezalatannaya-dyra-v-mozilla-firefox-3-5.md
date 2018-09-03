---
id: 1109
title: Незалатанная дыра в Mozilla Firefox 3.5
date: 2009-07-15T04:42:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/07/15/%d0%bd%d0%b5%d0%b7%d0%b0%d0%bb%d0%b0%d1%82%d0%b0%d0%bd%d0%bd%d0%b0%d1%8f-%d0%b4%d1%8b%d1%80%d0%b0-%d0%b2-mozilla-firefox-3-5/
permalink: /2009/07/%d0%bd%d0%b5%d0%b7%d0%b0%d0%bb%d0%b0%d1%82%d0%b0%d0%bd%d0%bd%d0%b0%d1%8f-%d0%b4%d1%8b%d1%80%d0%b0-%d0%b2-mozilla-firefox-3-5/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/07/mozilla-firefox-35.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/6087824440356391546
shorturl:
  - http://tinyurl.com/ogdvwhc
tags:
  - firefox
---
[SANS сообщает](http://isc.sans.org/diary.html?storyid=6796), что в Mozilla Security Blog подтверждено существование в дикой природе и активное использование хакерами действующего эксплойта обнаруженной и [опубликованной вчера Secunia](http://secunia.com/advisories/35798/) высоко критичной уязвимости в последней версии Firefox.

Текст експлойта [[SANS сообщает](http://isc.sans.org/diary.html?storyid=6796), что в Mozilla Security Blog подтверждено существование в дикой природе и активное использование хакерами действующего эксплойта обнаруженной и [опубликованной вчера Secunia](http://secunia.com/advisories/35798/) высоко критичной уязвимости в последней версии Firefox.

Текст експлойта](http://www.milw0rm.com/exploits/9137) вопреки недавнему сообщению владельца сайта о прекращении его действия. Успешное выполнение эксплойта стартует Windows Calculator. По имеющимся данным, эксплойт был успешно воспроизведен на Windows Vista и провалился на Windows 7 RC1.

В качестве временного решения проблемы, Mozilla рекомендует отключить опцию `<span style="font-weight: bold;">javascript.options.jit.content</span> <span style="font-size:130%;"><span style="font-family: Sans Serif;">в</span> </span><span style="font-weight: bold;">about:config</span>.` Пользователи дополнения NoScript находятся в стравнительной безопасности, так как потенциально уязвимы только с тех сайтов, для которых уже разрешено выполнение JavaScript.

Патча пока нет, рекомендую следить за обновлениями Firefox в меню <span style="font-weight: bold;">Help->Check for Updates</span>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_32">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2F%25d0%25bd%25d0%25b5%25d0%25b7%25d0%25b0%25d0%25bb%25d0%25b0%25d1%2582%25d0%25b0%25d0%25bd%25d0%25bd%25d0%25b0%25d1%258f-%25d0%25b4%25d1%258b%25d1%2580%25d0%25b0-%25d0%25b2-mozilla-firefox-3-5%2F&linkname=%D0%9D%D0%B5%D0%B7%D0%B0%D0%BB%D0%B0%D1%82%D0%B0%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%B4%D1%8B%D1%80%D0%B0%20%D0%B2%20Mozilla%20Firefox%203.5" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2F%25d0%25bd%25d0%25b5%25d0%25b7%25d0%25b0%25d0%25bb%25d0%25b0%25d1%2582%25d0%25b0%25d0%25bd%25d0%25bd%25d0%25b0%25d1%258f-%25d0%25b4%25d1%258b%25d1%2580%25d0%25b0-%25d0%25b2-mozilla-firefox-3-5%2F&linkname=%D0%9D%D0%B5%D0%B7%D0%B0%D0%BB%D0%B0%D1%82%D0%B0%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%B4%D1%8B%D1%80%D0%B0%20%D0%B2%20Mozilla%20Firefox%203.5" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2F%25d0%25bd%25d0%25b5%25d0%25b7%25d0%25b0%25d0%25bb%25d0%25b0%25d1%2582%25d0%25b0%25d0%25bd%25d0%25bd%25d0%25b0%25d1%258f-%25d0%25b4%25d1%258b%25d1%2580%25d0%25b0-%25d0%25b2-mozilla-firefox-3-5%2F&linkname=%D0%9D%D0%B5%D0%B7%D0%B0%D0%BB%D0%B0%D1%82%D0%B0%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%B4%D1%8B%D1%80%D0%B0%20%D0%B2%20Mozilla%20Firefox%203.5" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2F%25d0%25bd%25d0%25b5%25d0%25b7%25d0%25b0%25d0%25bb%25d0%25b0%25d1%2582%25d0%25b0%25d0%25bd%25d0%25bd%25d0%25b0%25d1%258f-%25d0%25b4%25d1%258b%25d1%2580%25d0%25b0-%25d0%25b2-mozilla-firefox-3-5%2F&linkname=%D0%9D%D0%B5%D0%B7%D0%B0%D0%BB%D0%B0%D1%82%D0%B0%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%B4%D1%8B%D1%80%D0%B0%20%D0%B2%20Mozilla%20Firefox%203.5" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
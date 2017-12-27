---
id: 1126
title: Техника программирования
date: 2009-05-28T13:08:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/05/28/%d1%82%d0%b5%d1%85%d0%bd%d0%b8%d0%ba%d0%b0-%d0%bf%d1%80%d0%be%d0%b3%d1%80%d0%b0%d0%bc%d0%bc%d0%b8%d1%80%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d1%8f/
permalink: /2009/05/%d1%82%d0%b5%d1%85%d0%bd%d0%b8%d0%ba%d0%b0-%d0%bf%d1%80%d0%be%d0%b3%d1%80%d0%b0%d0%bc%d0%bc%d0%b8%d1%80%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d1%8f/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/05/blog-post_28.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/2430391680680609793
shorturl:
  - http://tinyurl.com/q264utg
tags:
  - java
  - кодирование
---
Сегодня наблюдал следующую картину.

На одном сервере после обновления JDK перестал запускаться один сервис. В результате расследования стало ясно, что ошибка была вызвана отсутствием библиотеки JVM.LIB там, где загрузчик сервиса ожидал ее встретить. Путь к библиотеке был прописан программистами в загрузчике жестко, и ссылался на директорию установки J2SE 5.0 Update 1. Естественно, новая Java жила в своей собственной папке для Update 19.

Ошибка была устранена копированием Java в директорию с именем, требуемым загрузчиком сервиса &#8212; пришлось изменить в имени каталога 19 на 01.

Это ПО является частью здоровенного АПК, стоящего немереное количество бабла.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_15">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F05%2F%25d1%2582%25d0%25b5%25d1%2585%25d0%25bd%25d0%25b8%25d0%25ba%25d0%25b0-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d1%258f%2F&linkname=%D0%A2%D0%B5%D1%85%D0%BD%D0%B8%D0%BA%D0%B0%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F05%2F%25d1%2582%25d0%25b5%25d1%2585%25d0%25bd%25d0%25b8%25d0%25ba%25d0%25b0-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d1%258f%2F&linkname=%D0%A2%D0%B5%D1%85%D0%BD%D0%B8%D0%BA%D0%B0%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F05%2F%25d1%2582%25d0%25b5%25d1%2585%25d0%25bd%25d0%25b8%25d0%25ba%25d0%25b0-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d1%258f%2F&linkname=%D0%A2%D0%B5%D1%85%D0%BD%D0%B8%D0%BA%D0%B0%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F05%2F%25d1%2582%25d0%25b5%25d1%2585%25d0%25bd%25d0%25b8%25d0%25ba%25d0%25b0-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d0%25b8%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d1%258f%2F&linkname=%D0%A2%D0%B5%D1%85%D0%BD%D0%B8%D0%BA%D0%B0%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
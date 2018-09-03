---
id: 1017
title: Почему программы уязвимы
date: 2010-10-08T18:12:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/10/08/%d0%bf%d0%be%d1%87%d0%b5%d0%bc%d1%83-%d0%bf%d1%80%d0%be%d0%b3%d1%80%d0%b0%d0%bc%d0%bc%d1%8b-%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d1%8b/
permalink: /2010/10/%d0%bf%d0%be%d1%87%d0%b5%d0%bc%d1%83-%d0%bf%d1%80%d0%be%d0%b3%d1%80%d0%b0%d0%bc%d0%bc%d1%8b-%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d1%8b/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/10/blog-post.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1455435638425802997
shorturl:
  - http://tinyurl.com/o4odxoo
tags:
  - 0-day
  - adobe
  - microsoft
---
<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
    Уверен, этот вопрос не требует длительного обсуждения. Программное обеспечение&nbsp;уязвимо,&nbsp;потому что люди делают ошибки. Это могут быть как мелкие неточности в коде программ, так и серьезные недоработки на стадии дизайна&nbsp;архитектуры&nbsp;программного обеспечения. И прочие, не такие банальные, но в равной степени пагубные причины.
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
    Более интересен вопрос о том,&nbsp;почему&nbsp;одни программы &#171;уязвимее&#187;&nbsp;других.
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
    Наверняка вы знакомы с некоторыми мнениями по этому поводу. Например, сторонники open source зачастую настаивают, что ПО с открытым исходным кодом содержит меньше ошибок. Потому, мол, что каждый желающий может своими глазами проверить качество кода и сообщить разработчику об уязвимостях. Да, такая теоретическая возможность существует, но на практике она используется реже, чем хотелось бы. Некоторые результаты, показывают, что количество ошибок &#171;на квадратный метр&#187; в открытом и в проприетарном программном коде статистически особенно не отличается&nbsp;(<a href="http://www.swdsi.org/swdsi07/2007_proceedings/papers/236.pdf">PDF</a>).&nbsp;Еще одно&nbsp;распространенное&nbsp;заблуждение &#8212; MacOS безопаснее Windows, потому что в ней меньше ошибок. Как показывает практика, это не совсем так.
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
    Я склонен согласиться с версией, что уязвимость ПО зависит в первую очередь от его распространенности. Посмотрим в глаза реальности, лидеры по количеству обнаруженных уязвимостей у нас кто? <b>Adobe Acrobat Reader, Flash PLayer, Java</b> и всяческие поделки <b>Microsoft &#8212; Office, Internet Explorer </b>и т.д. Это программное обеспечение установлено на боле чем 90% компьютеров в мире. А как&nbsp;выросло&nbsp;число обнаруживаемых дыр в <b>Firefox </b>с ростом его доли на рынке браузеров? Именно распространенность привлекает внимание багхантеров &#8212; как благородных, так и злонамеренных. Найдя дыру в&nbsp;популярной программе, хакер может (в зависимости от своей системы ценностей) сообщить о ней открыто, предупредить о ней вендора, продать ее <b>ZDI</b>, продать ее на черном рынке,&nbsp;написать Интернет-червя и захватить мир&#8230;&nbsp;В общем, перспективы открываются широченные. А кому интересен баг в экзотической программе, которую даже ее создатель использует от случая к случаю? Когда вокруг так много вкусного?
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
    Широкое распространение программы привлекает к ней внимание исследователей, исследователи находят уязвимости, вендоры эти уязвимости исправляют. Процесс повторяется, пока вендоры не начинают утопать в потоке уязвимостей. Тогда в ход идут <b>SDLC</b>, <b>peer review, static analysis</b> и прочие магические трюки по&nbsp;предотвращению&nbsp;возникновения уязвимостей до выхода программы в свет &#8212; компания-производитель вырабатывает иммунитет. Отличным примером может служить Microsoft Inc. Те, кто наблюдает за&nbsp;индустрией&nbsp;хотя бы года с 2000-го, могут сравнить состояние дел у софтверного гиганта &#8212; тогда и сейчас. Со временем, адаптировавшись в условиях непрекращающегося потока 0-day уязвимостей, компания реформировала процесс разработки, уделили больше времени безопасности, и вуаля &#8212; уступила место лидера Adobe. (Правда, если слухи о слиянии подтвердятся, все может вернуться на круги своя).
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
  </div>
</div>

<div style="font-family: arial; font-size: small;">
  <div style="text-align: justify;">
    Резюмируя: все программы уязвимы одинаково. Ну или почти одинаково. Просто кого-то фаззят, а кого-то игнорируют. Помните, как в анекдоте о Неуловимом Джо. Всем солнечных выходных.
  </div>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_124">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F10%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d1%258b-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d1%258b%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D1%8B" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F10%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d1%258b-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d1%258b%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D1%8B" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F10%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d1%258b-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d1%258b%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D1%8B" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F10%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d1%258b-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d1%258b%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D1%8B" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
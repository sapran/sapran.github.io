---
id: 1026
title: Мухи против котлет, или почему стоит объяснять очевидные вещи
date: 2010-08-29T10:25:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/08/29/%d0%bc%d1%83%d1%85%d0%b8-%d0%bf%d1%80%d0%be%d1%82%d0%b8%d0%b2-%d0%ba%d0%be%d1%82%d0%bb%d0%b5%d1%82-%d0%b8%d0%bb%d0%b8-%d0%bf%d0%be%d1%87%d0%b5%d0%bc%d1%83-%d1%81%d1%82%d0%be%d0%b8%d1%82-%d0%be%d0%b1/
permalink: /2010/08/%d0%bc%d1%83%d1%85%d0%b8-%d0%bf%d1%80%d0%be%d1%82%d0%b8%d0%b2-%d0%ba%d0%be%d1%82%d0%bb%d0%b5%d1%82-%d0%b8%d0%bb%d0%b8-%d0%bf%d0%be%d1%87%d0%b5%d0%bc%d1%83-%d1%81%d1%82%d0%be%d0%b8%d1%82-%d0%be%d0%b1/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/08/blog-post.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/5219244696996205363
shorturl:
  - http://tinyurl.com/o3vsvl7
tags:
  - dumb asses
  - iso27000
  - pci:dss
  - менеджеры
  - осведомленность
---
<div style="text-align: justify;">
  Необходимость компромисса между безопасностью и производительностью уже давно не новость, и даже не свежая идея. Безопасность, превращающая систему в фортифицированного бегемота, не способного обработать запрос пользователя за приемлемый промежуток времени, вряд ли нужна коммерческой компании, сражающейся за каждого клиента. С другой стороны, системного администратора, не обновляющего программное обеспечение исправлениями уязвимостей (<i>а вдруг сломается!..</i>) и отключающего журналирование событий во имя прироста производительности, от неизбежного взлома или вирусной эпидемии отделяет только время.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Но давайте по-порядку. С одной стороны, поддержка ПО в актуальном состоянии, безопасная настройка, логирование событий безопасности и прочие меры предосторожности &#8212; это, несомненно, дань безопасности. А поддержка сервиса на уровне, достаточном для непрерывного выполнения бизнес функции, разве нет? Почему же, ведь по определению, доступность (availability), наряду с целостностью и конфиденциальностью (integrity & confidentiality) как раз и составляют понятие информационной безопасности.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Тем не менее, <strike>в дикой природе</strike> нередко приходится наблюдать за спором между айтишниками и безопасниками на тему: включать или не включать в системе очередной контроль безопасности. Аргументы сторон обычно выглядят следующим образом. Айтишники во всю уверяют, что новый контроль всячески вредит <strike>и никого не украшает</strike>. Что, мол, и производительность упадет, и стабильность понизится, и вообще, контроль не сертифицирован вендором. Безопасники же, в свою очередь, обычно настаивают на том, что контроль этот общепринят, рекомендован авторитетными институтами (NIST / ISO / ISACA / ISS) в международных стандартах (27k / CobiT / SP800-*). А также, стыд и позор айтишникам, что они до сих пор контроль не включили, и вообще, удивительно, как бизнес без этого контроля прожил так долго.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Причин для подобных пререканий я определяю две. Первая заключается в массовой безграмотности айтишников в вопросах безопасности. Очень редко выпадает удача встретить человека, который имеет внушительные познания в сфере ИБ и при этом работает в ИТ. Как правило, айтишники этим не заморачиваются. В моем личном соц опросе явления типа &#171;<i>прочитал GAISP, CobiT, ISO27002, NIST Han<span style="color: red;">d</span>book</i>&#187; или что-то в этом роде встречается среди айтишников крайне редко. Почему так происходит, мне не совсем понятно. Вероятно от того, что ИТ-безопасность до сих пор считается айтишниками темой узкой специализации, поэтому им пока не до нее &#8212; есть для этого безопасники. Хотя все вокруг твердит об обратном &#8212; начиная с массовых слияний ИТ и ИБ вендоров и заканчивая позиционированием супердержавами ИБ как приоритетного направления государственной политики. Но это все где-то там, за океаном, не у нас. У нас же ИТ-персонал черпает информацию о безопасности из новостей, Хабра, Хакер.ру и прочей желтой прессы &#8212; и это в лучшем случае. В худшем же, знания поступают из материалов маркетинговых конференций, так что лучше бы они не приходили вовсе. О каком уровне восприятия высоких идей <strike>мирового господства</strike> ИБ можно говорить в таки<span style="color: red;">х</span> условиях?
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Вторая причина &#8212; нежелание безопасников объяснять суть предлагаемых изменений на языке, доступном айтишникам. Правильная коммуникация идей очень важна, особенно тогда, когда собеседнику сложно понять о чем речь (как в нашем случае, помните о безграмотности). Объяснять нужно доступно и подробно, монотонно и по нескольку раз, настойчиво и подкрепляя сказанное примерами. Нельзя забывать о ловушке банальности &#8212; то, что для безопасника очевидно, для айтишника &#8212; дремучий лес. Не переоценивайте людей, всем нам есть чему учиться. И главное &#8212; старайтесь выдавать аргументы в пользу обеспечения именно той составляющей ИБ, которая так дорога сердцу каждого айтишника &#8212; производительности, то есть доступности (availability).
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Как следствие второй причины, обычно рождается такое явление, как давление на &#171;лучшие практики&#187; (best practice) и &#171;соответствие&#187; (compliance). Это когда ИБ бегает по ИТ-департаменту, размахивая над головой томами международных стандартов типа PCI:DSS. Но это уже другая история.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_115">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F08%2F%25d0%25bc%25d1%2583%25d1%2585%25d0%25b8-%25d0%25bf%25d1%2580%25d0%25be%25d1%2582%25d0%25b8%25d0%25b2-%25d0%25ba%25d0%25be%25d1%2582%25d0%25bb%25d0%25b5%25d1%2582-%25d0%25b8%25d0%25bb%25d0%25b8-%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2581%25d1%2582%25d0%25be%25d0%25b8%25d1%2582-%25d0%25be%25d0%25b1%2F&linkname=%D0%9C%D1%83%D1%85%D0%B8%20%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%20%D0%BA%D0%BE%D1%82%D0%BB%D0%B5%D1%82%2C%20%D0%B8%D0%BB%D0%B8%20%D0%BF%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D1%81%D1%82%D0%BE%D0%B8%D1%82%20%D0%BE%D0%B1%D1%8A%D1%8F%D1%81%D0%BD%D1%8F%D1%82%D1%8C%20%D0%BE%D1%87%D0%B5%D0%B2%D0%B8%D0%B4%D0%BD%D1%8B%D0%B5%20%D0%B2%D0%B5%D1%89%D0%B8" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F08%2F%25d0%25bc%25d1%2583%25d1%2585%25d0%25b8-%25d0%25bf%25d1%2580%25d0%25be%25d1%2582%25d0%25b8%25d0%25b2-%25d0%25ba%25d0%25be%25d1%2582%25d0%25bb%25d0%25b5%25d1%2582-%25d0%25b8%25d0%25bb%25d0%25b8-%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2581%25d1%2582%25d0%25be%25d0%25b8%25d1%2582-%25d0%25be%25d0%25b1%2F&linkname=%D0%9C%D1%83%D1%85%D0%B8%20%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%20%D0%BA%D0%BE%D1%82%D0%BB%D0%B5%D1%82%2C%20%D0%B8%D0%BB%D0%B8%20%D0%BF%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D1%81%D1%82%D0%BE%D0%B8%D1%82%20%D0%BE%D0%B1%D1%8A%D1%8F%D1%81%D0%BD%D1%8F%D1%82%D1%8C%20%D0%BE%D1%87%D0%B5%D0%B2%D0%B8%D0%B4%D0%BD%D1%8B%D0%B5%20%D0%B2%D0%B5%D1%89%D0%B8" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F08%2F%25d0%25bc%25d1%2583%25d1%2585%25d0%25b8-%25d0%25bf%25d1%2580%25d0%25be%25d1%2582%25d0%25b8%25d0%25b2-%25d0%25ba%25d0%25be%25d1%2582%25d0%25bb%25d0%25b5%25d1%2582-%25d0%25b8%25d0%25bb%25d0%25b8-%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2581%25d1%2582%25d0%25be%25d0%25b8%25d1%2582-%25d0%25be%25d0%25b1%2F&linkname=%D0%9C%D1%83%D1%85%D0%B8%20%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%20%D0%BA%D0%BE%D1%82%D0%BB%D0%B5%D1%82%2C%20%D0%B8%D0%BB%D0%B8%20%D0%BF%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D1%81%D1%82%D0%BE%D0%B8%D1%82%20%D0%BE%D0%B1%D1%8A%D1%8F%D1%81%D0%BD%D1%8F%D1%82%D1%8C%20%D0%BE%D1%87%D0%B5%D0%B2%D0%B8%D0%B4%D0%BD%D1%8B%D0%B5%20%D0%B2%D0%B5%D1%89%D0%B8" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F08%2F%25d0%25bc%25d1%2583%25d1%2585%25d0%25b8-%25d0%25bf%25d1%2580%25d0%25be%25d1%2582%25d0%25b8%25d0%25b2-%25d0%25ba%25d0%25be%25d1%2582%25d0%25bb%25d0%25b5%25d1%2582-%25d0%25b8%25d0%25bb%25d0%25b8-%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-%25d1%2581%25d1%2582%25d0%25be%25d0%25b8%25d1%2582-%25d0%25be%25d0%25b1%2F&linkname=%D0%9C%D1%83%D1%85%D0%B8%20%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%20%D0%BA%D0%BE%D1%82%D0%BB%D0%B5%D1%82%2C%20%D0%B8%D0%BB%D0%B8%20%D0%BF%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20%D1%81%D1%82%D0%BE%D0%B8%D1%82%20%D0%BE%D0%B1%D1%8A%D1%8F%D1%81%D0%BD%D1%8F%D1%82%D1%8C%20%D0%BE%D1%87%D0%B5%D0%B2%D0%B8%D0%B4%D0%BD%D1%8B%D0%B5%20%D0%B2%D0%B5%D1%89%D0%B8" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
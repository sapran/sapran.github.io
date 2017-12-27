---
id: 1033
title: Опочтарение Терри Пратчета и информационная безопасность (Осторожно, спойлер!)
date: 2010-06-28T12:47:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/06/28/%d0%be%d0%bf%d0%be%d1%87%d1%82%d0%b0%d1%80%d0%b5%d0%bd%d0%b8%d0%b5-%d1%82%d0%b5%d1%80%d1%80%d0%b8-%d0%bf%d1%80%d0%b0%d1%82%d1%87%d0%b5%d1%82%d0%b0-%d0%b8-%d0%b8%d0%bd%d1%84%d0%be%d1%80%d0%bc%d0%b0/
permalink: /2010/06/%d0%be%d0%bf%d0%be%d1%87%d1%82%d0%b0%d1%80%d0%b5%d0%bd%d0%b8%d0%b5-%d1%82%d0%b5%d1%80%d1%80%d0%b8-%d0%bf%d1%80%d0%b0%d1%82%d1%87%d0%b5%d1%82%d0%b0-%d0%b8-%d0%b8%d0%bd%d1%84%d0%be%d1%80%d0%bc%d0%b0/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/06/blog-post_28.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/394191432133906462
shorturl:
  - http://tinyurl.com/psr6yyp
tags:
  - fuzzing
  - mitm
  - социальная инженерия
---
<div style="text-align: justify;">
  Нет-нет, это не оффтопик. <a href="http://www.imdb.com/title/tt1219817/">Опочтарение</a> имеет непосредственное отношение к теме блога, то есть к информационной безопасности.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Во-первых, на протяжении всего фильма главный герой (М. фон Липвиг в исполнении Ричарда Койла) демонстрирует публике начала социальной инженерии.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Во-вторых, метод, при помощи которого хакеры из &#171;Дымящегося Гну&#187; во главе с А. Добросерд обнаружили уязвимость семафоров, является примером <a href="http://en.wikipedia.org/wiki/Fuzz_testing">фаззинга (fuzzing)</a>, &#8212; беспорядочной подачи случайных данных на вход программы с целью создания и дальнейшей эксплуатации исключительной ситуации, или попросту ошибки. Именно этим они и занимались: пытались подобрать последовательность сообщений, последовательно передавая которые, семафоры совершали &#171;недопустимую ошибку&#187; и прекращали работу.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Ну и в-третьих, операция по блокировке семафорных передач натянутым парусом, с последующей &#171;инъекцией&#187; части сообщения с заброшенной семафорной станции, &#8212; это классический пример &#171;man in the middle&#187;-атаки.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Само по себе кино неплохое, хотя как по мне актеры немного переигрывают.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_108">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F06%2F%25d0%25be%25d0%25bf%25d0%25be%25d1%2587%25d1%2582%25d0%25b0%25d1%2580%25d0%25b5%25d0%25bd%25d0%25b8%25d0%25b5-%25d1%2582%25d0%25b5%25d1%2580%25d1%2580%25d0%25b8-%25d0%25bf%25d1%2580%25d0%25b0%25d1%2582%25d1%2587%25d0%25b5%25d1%2582%25d0%25b0-%25d0%25b8-%25d0%25b8%25d0%25bd%25d1%2584%25d0%25be%25d1%2580%25d0%25bc%25d0%25b0%2F&linkname=%D0%9E%D0%BF%D0%BE%D1%87%D1%82%D0%B0%D1%80%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%A2%D0%B5%D1%80%D1%80%D0%B8%20%D0%9F%D1%80%D0%B0%D1%82%D1%87%D0%B5%D1%82%D0%B0%20%D0%B8%20%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%28%D0%9E%D1%81%D1%82%D0%BE%D1%80%D0%BE%D0%B6%D0%BD%D0%BE%2C%20%D1%81%D0%BF%D0%BE%D0%B9%D0%BB%D0%B5%D1%80%21%29" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F06%2F%25d0%25be%25d0%25bf%25d0%25be%25d1%2587%25d1%2582%25d0%25b0%25d1%2580%25d0%25b5%25d0%25bd%25d0%25b8%25d0%25b5-%25d1%2582%25d0%25b5%25d1%2580%25d1%2580%25d0%25b8-%25d0%25bf%25d1%2580%25d0%25b0%25d1%2582%25d1%2587%25d0%25b5%25d1%2582%25d0%25b0-%25d0%25b8-%25d0%25b8%25d0%25bd%25d1%2584%25d0%25be%25d1%2580%25d0%25bc%25d0%25b0%2F&linkname=%D0%9E%D0%BF%D0%BE%D1%87%D1%82%D0%B0%D1%80%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%A2%D0%B5%D1%80%D1%80%D0%B8%20%D0%9F%D1%80%D0%B0%D1%82%D1%87%D0%B5%D1%82%D0%B0%20%D0%B8%20%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%28%D0%9E%D1%81%D1%82%D0%BE%D1%80%D0%BE%D0%B6%D0%BD%D0%BE%2C%20%D1%81%D0%BF%D0%BE%D0%B9%D0%BB%D0%B5%D1%80%21%29" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F06%2F%25d0%25be%25d0%25bf%25d0%25be%25d1%2587%25d1%2582%25d0%25b0%25d1%2580%25d0%25b5%25d0%25bd%25d0%25b8%25d0%25b5-%25d1%2582%25d0%25b5%25d1%2580%25d1%2580%25d0%25b8-%25d0%25bf%25d1%2580%25d0%25b0%25d1%2582%25d1%2587%25d0%25b5%25d1%2582%25d0%25b0-%25d0%25b8-%25d0%25b8%25d0%25bd%25d1%2584%25d0%25be%25d1%2580%25d0%25bc%25d0%25b0%2F&linkname=%D0%9E%D0%BF%D0%BE%D1%87%D1%82%D0%B0%D1%80%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%A2%D0%B5%D1%80%D1%80%D0%B8%20%D0%9F%D1%80%D0%B0%D1%82%D1%87%D0%B5%D1%82%D0%B0%20%D0%B8%20%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%28%D0%9E%D1%81%D1%82%D0%BE%D1%80%D0%BE%D0%B6%D0%BD%D0%BE%2C%20%D1%81%D0%BF%D0%BE%D0%B9%D0%BB%D0%B5%D1%80%21%29" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F06%2F%25d0%25be%25d0%25bf%25d0%25be%25d1%2587%25d1%2582%25d0%25b0%25d1%2580%25d0%25b5%25d0%25bd%25d0%25b8%25d0%25b5-%25d1%2582%25d0%25b5%25d1%2580%25d1%2580%25d0%25b8-%25d0%25bf%25d1%2580%25d0%25b0%25d1%2582%25d1%2587%25d0%25b5%25d1%2582%25d0%25b0-%25d0%25b8-%25d0%25b8%25d0%25bd%25d1%2584%25d0%25be%25d1%2580%25d0%25bc%25d0%25b0%2F&linkname=%D0%9E%D0%BF%D0%BE%D1%87%D1%82%D0%B0%D1%80%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%A2%D0%B5%D1%80%D1%80%D0%B8%20%D0%9F%D1%80%D0%B0%D1%82%D1%87%D0%B5%D1%82%D0%B0%20%D0%B8%20%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%28%D0%9E%D1%81%D1%82%D0%BE%D1%80%D0%BE%D0%B6%D0%BD%D0%BE%2C%20%D1%81%D0%BF%D0%BE%D0%B9%D0%BB%D0%B5%D1%80%21%29" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
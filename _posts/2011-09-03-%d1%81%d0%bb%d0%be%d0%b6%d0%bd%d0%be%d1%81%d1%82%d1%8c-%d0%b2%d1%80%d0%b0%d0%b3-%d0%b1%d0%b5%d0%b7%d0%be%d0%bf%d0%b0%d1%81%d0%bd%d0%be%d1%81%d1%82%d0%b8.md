---
id: 952
title: Сложность враг безопасности
date: 2011-09-03T20:49:00+00:00
author: sapran
layout: post
guid: http://styran.com/2011/09/03/%d1%81%d0%bb%d0%be%d0%b6%d0%bd%d0%be%d1%81%d1%82%d1%8c-%d0%b2%d1%80%d0%b0%d0%b3-%d0%b1%d0%b5%d0%b7%d0%be%d0%bf%d0%b0%d1%81%d0%bd%d0%be%d1%81%d1%82%d0%b8/
permalink: /2011/09/%d1%81%d0%bb%d0%be%d0%b6%d0%bd%d0%be%d1%81%d1%82%d1%8c-%d0%b2%d1%80%d0%b0%d0%b3-%d0%b1%d0%b5%d0%b7%d0%be%d0%bf%d0%b0%d1%81%d0%bd%d0%be%d1%81%d1%82%d0%b8/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2011/09/blog-post.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/9088413814219499885
shorturl:
  - http://tinyurl.com/pr3lgba
categories:
  - Uncategorized
tags:
  - Uncategorized
---
<div dir="ltr" style="text-align: left;">
  <div style="text-align: justify;">
    Почему усложнение системы приводит к уменьшению ее безопасности? Эта прописная истина, известная каждому ибэшнику, нередко требует очень подробного разъяснения людям неискушенным.&nbsp;Прекрасный пример такого разъяснения я прочитал недавно в&nbsp;<a href="http://www.laresblog.com/2011/07/brittish-are-comming.html">блоге Криса Никерсона</a>. Развивая его тему, я пришел вот к чему.
  </div>
  
  <div style="text-align: justify;">
  </div>
  
  <div style="text-align: justify;">
    Представьте себе модель: одна система, на ней открыт один порт. Сервис, крутящийся на этом порту, имеет, скажем,&nbsp;<b><i>N&nbsp;</i></b>уязвимостей. Для того, чтобы защитить этот сервис, мы&nbsp;устанавливаем&nbsp;перед нашей системой межсетевой экран. У которого открыт один порт &#8212; консоль управления. Эта самая консоль содержит, скажем,&nbsp;<b><i>M&nbsp;</i></b>уязвимостей. Что мы получаем? Общее количество уязвимостей, равное&nbsp;<b><i>M + N</i></b>, то есть, возросшее в результате внедрения средства защиты.&nbsp;Идем дальше. Перед всем этим хозяйством мы устанавливаем систему&nbsp;предотвращения&nbsp;вторжений, на которой открыт один порт, а количество потенциальных уязвимостей равно&nbsp;<b><i>K</i></b>. Итого имеем&nbsp;<b><i>S = K + M + N</i></b>&nbsp;уязвимостей.
  </div>
  
  <div style="text-align: justify;">
  </div>
  
  <div style="text-align: justify;">
    Продолжая процесс внедрения средств защиты, мы неумолимо&nbsp;увеличиваем&nbsp;количество уязвимостей и в конце концов приходим к необходимости построения и автоматизации процесса управления этими самыми уязвимостями. Для этих целей мы покупаем и внедряем специальное программное обеспечение, которого в последнее время на рынке развелось предостаточно. А если наш ИТ-директор поддался новым веяниям и &#171;витает в облаках&#187; &#8212;&nbsp;приобретаем&nbsp;управление уязвимостями как сервис, используя для сканирования наших устройств и обнаружения в них уязвимостей не локально установленное оборудование, а оборудование &#171;в облаке&#187;.
  </div>
  
  <div style="text-align: justify;">
  </div>
  
  <div style="text-align: justify;">
    Что в в таком случае&nbsp;происходит&nbsp;с количеством уязвимостей? О том, сколько &#171;дыр&#187; в облаке поставщика услуг мы не знаем. Единственное, в чем мы можем быть уверены, это то, что уязвимости в нем есть (допустим, их&nbsp;<b><i>C</i></b>). Итак, мы получаем дополнение к нашему уравнению, но не в виде&nbsp;слагаемого, а в виде множителя, ведь компрометация каждой существенной уязвимости в облаке приведет к раскрытию информации обо всех наших уязвимостях. Итого,&nbsp;<b><i>S = ( K + M + N ) * C</i></b>.
  </div>
  
  <div style="text-align: justify;">
  </div>
  
  <div style="text-align: justify;">
    Надеюсь, этот пример наглядно демонстрирует как усложнение системы отражается на ее безопасности. Помните с чего все начиналось? С одного порта на сервере, который можно было просто выключить.
  </div>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_189">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F09%2F%25d1%2581%25d0%25bb%25d0%25be%25d0%25b6%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2%25d1%2580%25d0%25b0%25d0%25b3-%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d0%25b8%2F&linkname=%D0%A1%D0%BB%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%D1%80%D0%B0%D0%B3%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D0%B8" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F09%2F%25d1%2581%25d0%25bb%25d0%25be%25d0%25b6%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2%25d1%2580%25d0%25b0%25d0%25b3-%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d0%25b8%2F&linkname=%D0%A1%D0%BB%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%D1%80%D0%B0%D0%B3%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D0%B8" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F09%2F%25d1%2581%25d0%25bb%25d0%25be%25d0%25b6%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2%25d1%2580%25d0%25b0%25d0%25b3-%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d0%25b8%2F&linkname=%D0%A1%D0%BB%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%D1%80%D0%B0%D0%B3%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D0%B8" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F09%2F%25d1%2581%25d0%25bb%25d0%25be%25d0%25b6%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2%25d1%2580%25d0%25b0%25d0%25b3-%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d0%25b8%2F&linkname=%D0%A1%D0%BB%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%D1%80%D0%B0%D0%B3%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D0%B8" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
---
id: 933
title: Уязвимость точек доступа WiFi со включенным WPS
date: 2012-01-02T22:07:00+00:00
author: sapran
layout: post
guid: http://styran.com/2012/01/02/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d1%82%d0%be%d1%87%d0%b5%d0%ba-%d0%b4%d0%be%d1%81%d1%82%d1%83%d0%bf%d0%b0-wifi-%d1%81%d0%be-%d0%b2%d0%ba%d0%bb%d1%8e%d1%87%d0%b5%d0%bd/
permalink: /2012/01/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d1%82%d0%be%d1%87%d0%b5%d0%ba-%d0%b4%d0%be%d1%81%d1%82%d1%83%d0%bf%d0%b0-wifi-%d1%81%d0%be-%d0%b2%d0%ba%d0%bb%d1%8e%d1%87%d0%b5%d0%bd/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2012/01/wifi-wps-4-10.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/8100027157505924216
shorturl:
  - http://tinyurl.com/o9aefmj
tags:
  - wifi
---
<div dir="ltr" style="text-align: left;">
  <div style="text-align: justify;">
    <b><i>[UPDATE 03.01.2012 11:54]</i>:&nbsp;</b>Точные цифры по статистике использования WPS следующие: из&nbsp;15424 точек доступа, со включенным шифрованием, WPS поддерживают&nbsp;5306, что составляет 34%. Данные получены по результатам исследования информации о 16439 точках доступа в г. Киеве. Прошу прощения за устаревшие данные в первой версии поста. </p> 
    
    <p>
      Практически все беспроводные точки доступа, выпускаемые в настоящее время для частного использования, позволяют своим владельцам избежать тягот настройки шифрования при помощи функции <i><b><a href="http://en.wikipedia.org/wiki/Wi-Fi_Protected_Setup">WiFi Protected Setup (WPS)</a></b></i>. Вы можете прямо сейчас проверить, поддерживает ли ваше устройство этот протокол. Найдите на корпусе щиток со штрих-кодом, серийным номером, MAC-адресом и т.д. Если помимо всего прочего на нем значится <i><b>WPS PIN</b></i>, то обсуждаемая нынче уязвимость протокола WPS распространяется и на вас. (В этом&nbsp;месте нужно понемногу начинать бояться. А что ж вы думали, блог ведь о безопасности).</div> 
      
      <div>
        <div style="text-align: justify;">
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
          Немного истории. Как и большинство других плохих инструментов безопасности, WPS придумали для удобства. Обычно, для того, чтобы настроить шифрование на точке доступа, пользователям приходится довольно долго ковыряться в слабо понятных нормальному человеку настройках меню, а также выдумывать длиннющий ключ шифрования, чтобы потом с третьего-четвертого раза вводить его на ноутбуке, планшете и мобильном телефоне. Чтобы избавить мир от этих мучений, в 2007 году организация <i><b><a href="http://www.wi-fi.org/">WiFi Alliance</a></b></i> выпустила протокол WPS, который оставляет всю черную работу на усмотрение точки доступа и ее программного обеспечения. Пользователю остается всего лишь ввести в каждое подключаемое к беспроводной сети устройство короткий восьмициферный PIN-код, что, несомненно, намного проще. (В этом месте самое время для саркастического &#171;Казалось бы, что могло пойти не так?&#187;)
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
          Протокол WPS получил самое широкое распространение. По моим подсчетам, в Киеве более 40% точек доступа, настроенных на шифрование трафика, поддерживают WPS (если точнее, это почти 4300&nbsp;из приблизительно 10000&nbsp;устройств).
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
          Теперь о главном: <i><b>WPS был взломан</b></i>. (Здесь не помешает еще немного сарказму: &#171;Что и требовалось доказать.&#187;) А именно, 26 декабря&nbsp;<i><b>Stefan Viehböck</b></i> опубликовал статью на тему взлома PIN-кодов WPS путем неполного перебора. В коде всего 8 символов, причем восьмой играет роль контрольной суммы, то есть, является функцией первых семи. Оставшиеся семь можно подобрать менее чем за 10 часов, а для некоторых моделей точек доступа &#8212; за 4 часа, используя при переборе небольшую хитрость, позволяющую атакующему удостовериться в том, что первые 4 символа подобраны верно, еще до того, как он приступил к подбору последних трех.
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
          Тема эта широко освещается в прессе, хотя я не видел пока, чтобы в русскоязычном ИБ-сообществе кто-то ее затрагивал. В частности, о провале WPS написали <a href="https://krebsonsecurity.com/2011/12/new-tools-bypass-wireless-router-security/">Brian Krebs</a> и &#171;страшный и ужасный&#187; <a href="http://dankaminsky.com/2012/01/02/wps/">Dan Kaminsky</a>. Вот <a href="https://docs.google.com/viewer?url=http://sviehb.files.wordpress.com/2011/12/viehboeck_wps.pdf&pli=1">ссылка на первоисточник</a> и на <a href="http://www.tacnetsol.com/news/2011/12/28/cracking-wifi-protected-setup-with-reaver.html">утилиту Reaver</a>, предназначенную&nbsp;для демонстрации простоты атаки на WPS.
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
          Несколько слов о том, почему все не так печально, как кажется. Во-первых, для того, чтобы избежать участи жертвы хакерствующих соседей и других неблагонадежных граждан, <i><b>достаточно отключить на &nbsp;вашей точке доступа функцию WPS</b></i>. Обратите внимание, WPS обычно включен по умолчанию и не выключается сам по себе, если вы им не пользуетесь. То есть, выключить его нужно явно, даже если вы используете вручную настроенный WPA2. Во-вторых, <i><b>не стоит путать WPS и WPA/WPA2</b></i>. Уязвимость WPS никак не влияет на стойкость WPA2, просто это вот такая вот дыра, позволяющая кому угодно за короткое время получить ваш ключ WPA2 и использовать его для подключения к вашей сети и прослушивания вашего трафика.
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
          Есть и неприятный момент: в некоторых моделях WPS просто невозможно отключить, но это уже вопрос к выбору поставщика оборудования.&nbsp;Оставайтесь в безопасности.
        </div>
      </div></div> 
      
      <div class="addtoany_share_save_container addtoany_content_bottom">
        <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_208">
          <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F01%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d1%2582%25d0%25be%25d1%2587%25d0%25b5%25d0%25ba-%25d0%25b4%25d0%25be%25d1%2581%25d1%2582%25d1%2583%25d0%25bf%25d0%25b0-wifi-%25d1%2581%25d0%25be-%25d0%25b2%25d0%25ba%25d0%25bb%25d1%258e%25d1%2587%25d0%25b5%25d0%25bd%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D1%82%D0%BE%D1%87%D0%B5%D0%BA%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20WiFi%20%D1%81%D0%BE%20%D0%B2%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%BD%D1%8B%D0%BC%20WPS" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F01%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d1%2582%25d0%25be%25d1%2587%25d0%25b5%25d0%25ba-%25d0%25b4%25d0%25be%25d1%2581%25d1%2582%25d1%2583%25d0%25bf%25d0%25b0-wifi-%25d1%2581%25d0%25be-%25d0%25b2%25d0%25ba%25d0%25bb%25d1%258e%25d1%2587%25d0%25b5%25d0%25bd%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D1%82%D0%BE%D1%87%D0%B5%D0%BA%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20WiFi%20%D1%81%D0%BE%20%D0%B2%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%BD%D1%8B%D0%BC%20WPS" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F01%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d1%2582%25d0%25be%25d1%2587%25d0%25b5%25d0%25ba-%25d0%25b4%25d0%25be%25d1%2581%25d1%2582%25d1%2583%25d0%25bf%25d0%25b0-wifi-%25d1%2581%25d0%25be-%25d0%25b2%25d0%25ba%25d0%25bb%25d1%258e%25d1%2587%25d0%25b5%25d0%25bd%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D1%82%D0%BE%D1%87%D0%B5%D0%BA%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20WiFi%20%D1%81%D0%BE%20%D0%B2%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%BD%D1%8B%D0%BC%20WPS" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F01%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d1%2582%25d0%25be%25d1%2587%25d0%25b5%25d0%25ba-%25d0%25b4%25d0%25be%25d1%2581%25d1%2582%25d1%2583%25d0%25bf%25d0%25b0-wifi-%25d1%2581%25d0%25be-%25d0%25b2%25d0%25ba%25d0%25bb%25d1%258e%25d1%2587%25d0%25b5%25d0%25bd%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D1%82%D0%BE%D1%87%D0%B5%D0%BA%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20WiFi%20%D1%81%D0%BE%20%D0%B2%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%BD%D1%8B%D0%BC%20WPS" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
        </div>
      </div>
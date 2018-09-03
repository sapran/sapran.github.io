---
id: 1018
title: Stuxnet и иранская ядерная программа
date: 2010-09-30T07:17:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/09/30/stuxnet-%d0%b8-%d0%b8%d1%80%d0%b0%d0%bd%d1%81%d0%ba%d0%b0%d1%8f-%d1%8f%d0%b4%d0%b5%d1%80%d0%bd%d0%b0%d1%8f-%d0%bf%d1%80%d0%be%d0%b3%d1%80%d0%b0%d0%bc%d0%bc%d0%b0/
permalink: /2010/09/stuxnet-%d0%b8-%d0%b8%d1%80%d0%b0%d0%bd%d1%81%d0%ba%d0%b0%d1%8f-%d1%8f%d0%b4%d0%b5%d1%80%d0%bd%d0%b0%d1%8f-%d0%bf%d1%80%d0%be%d0%b3%d1%80%d0%b0%d0%bc%d0%bc%d0%b0/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/09/stuxnet.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/6514229036172449851
shorturl:
  - http://tinyurl.com/nv4zna4
tags:
  - bullshit
  - stuxnet
  - зловредный код
  - политика
---
<div style="text-align: justify;">
  В последнее время в сети наблюдается много спекуляций на тему интернет-червя Stuxnet. Началось все с неизвестной уязвимости в Windows, которая использовалась для доставки вредоносного кода (т.н. пейлоуда). После выяснилось, что уязвимости две, а пейлоуд предназначен для заражения SCADA-систем производства фирмы Siemens (<i>WinCC</i>), контролирующих крупные производственные и энергетические автоматизированные системы. На этом этапе в прессе впервые прозвучало предположение о том, что настолько сложный механизм не может являться продуктом аматоров, и скорее всего здесь замешаны государственные спецслужбы. Все, естественно, покосились на Китай. Но вскоре отмели эту версию, так как выяснилось, что одной из наиболее пострадавших от Stuxnet инфраструктур оказалась иранская атомная энергетика. Теперь в кругу подозреваемых США и Израиль, но я уверен, что на этом тема не исчерпана, и мнение общественности еще не раз изменится.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  В общем, слухов было много. Мне даже неудобно снова заводить об этом речь. Но нужно себя заставлять.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Лично я, чисто интуитивно и без претензий на достоверность выводов, сделал одно весьма любопытное предположение. Исходил я из следующих фактов:
</div>

<div style="text-align: justify;">
</div>

<li style="text-align: justify;">
  Иранские атомные станции пострадали. Тут без комментариев.
</li>
<li style="text-align: justify;">
  Stuxnet, несомненно, наиболее сложная зловредная программа из ныне известных. Червь использует четыре 0-day уязвимости, исполняемый код подписан &#171;честным&#187; сертификатом реально существующей компании (<i>Realtek</i>), в пейлоуде доставляется руткит, способный предоставить полный доступ к зараженной системе.
</li>
<li style="text-align: justify;">
  При всей своей продвинутости, <b>Stuxnet по сути не делает ничего</b>. Он будто бы ждет команды хозяина, но при этом совершенно ни от кого не скрывается. Он мог бы отдать контроль над системой своему автору, без следа удалить себя или скрыть следы своего проникновения и признаки присутствия, даже зарикроллить, к чертям, всю планету&#8230; Но он ничего этого не делает. Это выглядит так, будто автор (а скорее всего группа авторов) либо очень серьезно постарался в одной части проекта и совершенно не уделил внимания прочим задачам, либо не ставил перед собой целей, присущих большинству программ подобного рода. Все это выглядит как разведка боем, proof of concept. Если желаете, <b>глобальный тест на проникновение</b> &#8212; проверка устойчивости отдельного класса ИТ-инфраструктур к атакам с <i>таким </i>вектором и<i> таким</i> финансированием.
</li>

<div>
  <div style="text-align: justify;">
    А теперь давайте немного пофантазируем. С точки зрения общественного мнения, то есть средне статистического гражданина, на кого из фигурантов происшедшего падет наименьшее подозрение? Естественно, на жертву.
  </div>
</div>

<div>
  <div style="text-align: justify;">
  </div>
</div>

<div>
  <div style="text-align: justify;">
    <i>P.S. Все выше изложенное является полной и абсолютной спекуляцией и не имеет отношения к проверенным фактам. Все возможные совпадения и кажущиеся намеки &#8212; чистая случайность =)</i>
  </div>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_123">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2Fstuxnet-%25d0%25b8-%25d0%25b8%25d1%2580%25d0%25b0%25d0%25bd%25d1%2581%25d0%25ba%25d0%25b0%25d1%258f-%25d1%258f%25d0%25b4%25d0%25b5%25d1%2580%25d0%25bd%25d0%25b0%25d1%258f-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d0%25b0%2F&linkname=Stuxnet%20%D0%B8%20%D0%B8%D1%80%D0%B0%D0%BD%D1%81%D0%BA%D0%B0%D1%8F%20%D1%8F%D0%B4%D0%B5%D1%80%D0%BD%D0%B0%D1%8F%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2Fstuxnet-%25d0%25b8-%25d0%25b8%25d1%2580%25d0%25b0%25d0%25bd%25d1%2581%25d0%25ba%25d0%25b0%25d1%258f-%25d1%258f%25d0%25b4%25d0%25b5%25d1%2580%25d0%25bd%25d0%25b0%25d1%258f-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d0%25b0%2F&linkname=Stuxnet%20%D0%B8%20%D0%B8%D1%80%D0%B0%D0%BD%D1%81%D0%BA%D0%B0%D1%8F%20%D1%8F%D0%B4%D0%B5%D1%80%D0%BD%D0%B0%D1%8F%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2Fstuxnet-%25d0%25b8-%25d0%25b8%25d1%2580%25d0%25b0%25d0%25bd%25d1%2581%25d0%25ba%25d0%25b0%25d1%258f-%25d1%258f%25d0%25b4%25d0%25b5%25d1%2580%25d0%25bd%25d0%25b0%25d1%258f-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d0%25b0%2F&linkname=Stuxnet%20%D0%B8%20%D0%B8%D1%80%D0%B0%D0%BD%D1%81%D0%BA%D0%B0%D1%8F%20%D1%8F%D0%B4%D0%B5%D1%80%D0%BD%D0%B0%D1%8F%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2Fstuxnet-%25d0%25b8-%25d0%25b8%25d1%2580%25d0%25b0%25d0%25bd%25d1%2581%25d0%25ba%25d0%25b0%25d1%258f-%25d1%258f%25d0%25b4%25d0%25b5%25d1%2580%25d0%25bd%25d0%25b0%25d1%258f-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b3%25d1%2580%25d0%25b0%25d0%25bc%25d0%25bc%25d0%25b0%2F&linkname=Stuxnet%20%D0%B8%20%D0%B8%D1%80%D0%B0%D0%BD%D1%81%D0%BA%D0%B0%D1%8F%20%D1%8F%D0%B4%D0%B5%D1%80%D0%BD%D0%B0%D1%8F%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
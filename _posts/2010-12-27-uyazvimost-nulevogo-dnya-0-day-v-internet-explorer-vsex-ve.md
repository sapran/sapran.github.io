---
id: 1002
title: Уязвимость нулевого дня (0-day) в Internet Explorer всех версий
date: 2010-12-27T12:53:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/12/27/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%bd%d1%83%d0%bb%d0%b5%d0%b2%d0%be%d0%b3%d0%be-%d0%b4%d0%bd%d1%8f-0-day-%d0%b2-internet-explorer-%d0%b2%d1%81%d0%b5%d1%85-%d0%b2%d0%b5/
permalink: /2010/12/%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%bd%d1%83%d0%bb%d0%b5%d0%b2%d0%be%d0%b3%d0%be-%d0%b4%d0%bd%d1%8f-0-day-%d0%b2-internet-explorer-%d0%b2%d1%81%d0%b5%d1%85-%d0%b2%d0%b5/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/12/0-day-internet-explorer.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4953242131165128992
shorturl:
  - http://tinyurl.com/pkaz52y
tags:
  - 0-day
  - aslr
  - dep
  - emet
  - ie
  - microsoft
---
<div style="text-align: justify;">
  В преддверии Нового года хакеры порадовали фишеров: опубликована <a href="https://www.microsoft.com/technet/security/advisory/2488013.mspx"><b>актуальная 0-day уязвимость</b></a> <b>во всех стабильных версиях Internet Eplorer</b> (<a href="https://www.offensive-security.com/offsec/internet-explorer-css-0day-on-windows-7/">ссылка</a> на демо-ролик). Более того, соответствующий эксплойт <b>добавлен в</b> <b>Metasploit Framework</b>, следовательно, теперь каждый script kiddie сможет им воспользоваться. Очень опасно и несвоевременно, с учетом того, что активность фишеров в период рождественских и новогодних праздников традиционно возрастает в несколько раз. Имея на вооружении client side уязвимость такого калибра, кибер-мошенники смогут существенно повысить свои шансы на успех.
</div>

<div style="text-align: justify;">
  Среди особенностей этой уязвимости ярко выделяется тот факт, что воспользоваться ею можно в обход обоих инструментов обеспечения безопасности приложений, выгодно отличающих Windows Vista & Windows 7 от их предшественниц. Да-да, <b><a href="http://ru.wikipedia.org/wiki/Data_Execution_Prevention">DEP</a> и <a href="http://ru.wikipedia.org/wiki/Address_Space_Layout_Randomization">ASLR</a> против этого эксплойта не работают</b>. Так случилось потому, что DLL библиотеки в Windows вправе самостоятельно &#171;решать&#187;, используют они DEP/ASLR, или нет.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Риск &#171;попасть под раздачу&#187; может быть несколько снижен c использованием утилиты Microsoft <b>Enhanced Mitigation Experience Toolkit (EMET) </b>для настройки принудительного использования инструментов безопасности приложениями и разделяемыми библиотеками. Для этого следует <a href="https://www.microsoft.com/downloads/en/details.aspx?FamilyID=c6f0a6ee-05ac-4eb6-acd0-362559fd2f04"><b>скачать</b></a>, установить и запустить EMET 2.0. Если желаете рискнуть &#8212; в настройках <b><i>&#171;Configure System&#187;</i></b> выберите в пункте <b><i>&#171;Profile Name&#187;</i></b> значение <b><i>&#171;Maximum Security Settings&#187;</i></b>. <b>Предупреждение:</b> есть сигналы о том, что после применения настроек глобально &#8212; ко всей системе &#8212; наблюдаются проблемы с запуском отельных приложений и даже с загрузкой операционной системы. Подтвердить или опровергнуть это не могу, так как у меня на Windows 7 x64 &#171;все работает&#187;.
</div>

<div style="clear: both; text-align: center;">
  <a href="http://2.bp.blogspot.com/_qASWdX8owQc/TRhy3l71aYI/AAAAAAAAFgU/ngkPBvx9Ul8/s1600/emet.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="400" src="http://2.bp.blogspot.com/_qASWdX8owQc/TRhy3l71aYI/AAAAAAAAFgU/ngkPBvx9Ul8/s400/emet.png" width="345" /></a>
</div>

<div style="text-align: justify;">
  Более осторожные пользователи могут настроить Internet Explorer, так сказать, персонально. Для этого идем в меню <i><b>&#171;Configure Apps&#187;</b></i>, добавляем в открывшееся окошко полный путь к<b> <i>iexplore.exe</i></b><i> </i>и отмечаем все доступные галочки. Ну и как же без перезагрузки. Расположение файла iexpore.exe может отличаться для разных версий Windows, обычно это<b><i> &#171;C:Program FilesInternet Exporeriexplore.exe&#187;.</i></b>
</div>

<div style="clear: both; text-align: center;">
</div>

<div style="clear: both; text-align: center;">
  <a href="http://2.bp.blogspot.com/_qASWdX8owQc/TRh1Ea3B7XI/AAAAAAAAFgc/W7Z3iTLMN4A/s1600/emet2.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="111" src="http://2.bp.blogspot.com/_qASWdX8owQc/TRh1Ea3B7XI/AAAAAAAAFgc/W7Z3iTLMN4A/s400/emet2.png" width="400" /></a>
</div>

<div style="text-align: justify;">
  Из незыблемого: пусти дальнейшего сокращения рисков традиционно состоят в не нажимании по посторонним ссылкам, присланных не известно кем. Даже если известно &#8212; кликать совершенно не обязательно. Подробнее об угрозах фишинга и средствах борьбы с ними я писал <a href="http://securegalaxy.blogspot.com/2010/07/blog-post.html">в этом посте</a>. Будьте осторожны.
</div>

Всех с наступающим Новым годом!

_Источник оригинальной новости: [Krebs on Security](https://krebsonsecurity.com/2010/12/exploit-published-for-new-internet-explorer-flaw/)_

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_139">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F12%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25bd%25d1%2583%25d0%25bb%25d0%25b5%25d0%25b2%25d0%25be%25d0%25b3%25d0%25be-%25d0%25b4%25d0%25bd%25d1%258f-0-day-%25d0%25b2-internet-explorer-%25d0%25b2%25d1%2581%25d0%25b5%25d1%2585-%25d0%25b2%25d0%25b5%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BD%D1%83%D0%BB%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BD%D1%8F%20%280-day%29%20%D0%B2%20Internet%20Explorer%20%D0%B2%D1%81%D0%B5%D1%85%20%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F12%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25bd%25d1%2583%25d0%25bb%25d0%25b5%25d0%25b2%25d0%25be%25d0%25b3%25d0%25be-%25d0%25b4%25d0%25bd%25d1%258f-0-day-%25d0%25b2-internet-explorer-%25d0%25b2%25d1%2581%25d0%25b5%25d1%2585-%25d0%25b2%25d0%25b5%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BD%D1%83%D0%BB%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BD%D1%8F%20%280-day%29%20%D0%B2%20Internet%20Explorer%20%D0%B2%D1%81%D0%B5%D1%85%20%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F12%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25bd%25d1%2583%25d0%25bb%25d0%25b5%25d0%25b2%25d0%25be%25d0%25b3%25d0%25be-%25d0%25b4%25d0%25bd%25d1%258f-0-day-%25d0%25b2-internet-explorer-%25d0%25b2%25d1%2581%25d0%25b5%25d1%2585-%25d0%25b2%25d0%25b5%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BD%D1%83%D0%BB%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BD%D1%8F%20%280-day%29%20%D0%B2%20Internet%20Explorer%20%D0%B2%D1%81%D0%B5%D1%85%20%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F12%2F%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25bd%25d1%2583%25d0%25bb%25d0%25b5%25d0%25b2%25d0%25be%25d0%25b3%25d0%25be-%25d0%25b4%25d0%25bd%25d1%258f-0-day-%25d0%25b2-internet-explorer-%25d0%25b2%25d1%2581%25d0%25b5%25d1%2585-%25d0%25b2%25d0%25b5%2F&linkname=%D0%A3%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BD%D1%83%D0%BB%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BD%D1%8F%20%280-day%29%20%D0%B2%20Internet%20Explorer%20%D0%B2%D1%81%D0%B5%D1%85%20%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
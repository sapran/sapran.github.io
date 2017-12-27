---
id: 858
title: Грабли начинающего пентестера
date: 2013-06-19T21:30:00+00:00
author: sapran
layout: post
guid: http://styran.com/2013/06/19/%d0%b3%d1%80%d0%b0%d0%b1%d0%bb%d0%b8-%d0%bd%d0%b0%d1%87%d0%b8%d0%bd%d0%b0%d1%8e%d1%89%d0%b5%d0%b3%d0%be-%d0%bf%d0%b5%d0%bd%d1%82%d0%b5%d1%81%d1%82%d0%b5%d1%80%d0%b0/
permalink: /2013/06/%d0%b3%d1%80%d0%b0%d0%b1%d0%bb%d0%b8-%d0%bd%d0%b0%d1%87%d0%b8%d0%bd%d0%b0%d1%8e%d1%89%d0%b5%d0%b3%d0%be-%d0%bf%d0%b5%d0%bd%d1%82%d0%b5%d1%81%d1%82%d0%b5%d1%80%d0%b0/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2013/06/blog-post_20.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/8316981770189020571
shorturl:
  - http://tinyurl.com/oeve5st
categories:
  - Uncategorized
tags:
  - Uncategorized
---
Есть такие знания, которые получаешь не из книжек, а путем набивания шишек разного калибра. Размещу некоторые из них здесь, потому что не редко доводится делиться ими с коллегами.

1. В запросах протокола HTTP/1.1 обязателен заголовок Host. Если его не указать, вы получите ответ Bad request. В этом случае люди, не знакомые с протоколом HTTP, могут ошибочно решить, что &#171;что-то не так с сервером&#187; и пойти копать где-то в другом месте. А счастье было так возможно&#8230;

2. Существует отличная замена NetCat &#8212; Ncat. Входит в один пакет с Nmap и обязателен к использованию на &#171;своем&#187; хосте (на чужом &#8212; как повезет). Он более гибок в плане доступных опций и поэтому использовать его легче, чем классический NC. Там же ищите классные утилиты ndiff, nping и ncrack.

3. У Microsoft ESMTP есть одна неприятная особенность: она ждет &#171;чистый&#187; telnet от клиента. Телнет мы все не любим; по разным причинам, например, я потому, что в нем нет поддержки readline, и невозможно редактировать введенный текст. Поэтому, если вы усвоили п. 2 и пришли &#171;разговаривать&#187; с Exchange на протоколе SMTP при помощи Ncat, вам придется использовать его с ключом -t (Answer Telnet negotiations).

4. Если ваша программа или утилита не поддерживает соединения SSL/TLS, вы можете &#171;завернуть&#187; ее в openssl или тот же Ncat с ключом &#8212;ssl. Подробности, традиционно, в мане (man ncat; man s_client), но если в кратце, то
  


> cat | openssl s_client -connect <host><host><host>:443  
> _<Пропущено много текста про SSL-сертификат>_  
> GET / HTTP/1.1  
> Host: <host>&nbsp;<host><host></host></host></host></host></p>
> ^d

5. Nmap, запущенный от root, меняет свое поведение по умолчанию. Это не всегда интуитивно понятно и местами жутко раздражает. Например, обычный nmap <ip> сделает скан методом установки соединения TCP (или connect-скан), принудительно запускаемый с ключом -sT. Если же Nmap запущен от root, то скан без опций по умолчанию выберет метод SYN (или half-open), то есть -sS. Методы различны по создаваемому шуму и, что тоже важно, по скорости.</ip>  
<ip>  
</ip><ip>Надеюсь, кому-нибудь пригодится.</ip>  
<ip>  
</ip>**Update**&nbsp;Благодаря&nbsp;<a href="https://twitter.com/snowytoxa" target="_blank">@snowytoxa</a>, у меня&nbsp;+1 шишка: в п. 3 ESMTP ждет не Telnet negotiation, а виндовый перевод строки (rn). Поэтому нужно использовать ncat -C.

P.S. Блин, а кто же хочет -t?.. FTP?..:)

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_279">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F06%2F%25d0%25b3%25d1%2580%25d0%25b0%25d0%25b1%25d0%25bb%25d0%25b8-%25d0%25bd%25d0%25b0%25d1%2587%25d0%25b8%25d0%25bd%25d0%25b0%25d1%258e%25d1%2589%25d0%25b5%25d0%25b3%25d0%25be-%25d0%25bf%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b5%25d1%2581%25d1%2582%25d0%25b5%25d1%2580%25d0%25b0%2F&linkname=%D0%93%D1%80%D0%B0%D0%B1%D0%BB%D0%B8%20%D0%BD%D0%B0%D1%87%D0%B8%D0%BD%D0%B0%D1%8E%D1%89%D0%B5%D0%B3%D0%BE%20%D0%BF%D0%B5%D0%BD%D1%82%D0%B5%D1%81%D1%82%D0%B5%D1%80%D0%B0" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F06%2F%25d0%25b3%25d1%2580%25d0%25b0%25d0%25b1%25d0%25bb%25d0%25b8-%25d0%25bd%25d0%25b0%25d1%2587%25d0%25b8%25d0%25bd%25d0%25b0%25d1%258e%25d1%2589%25d0%25b5%25d0%25b3%25d0%25be-%25d0%25bf%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b5%25d1%2581%25d1%2582%25d0%25b5%25d1%2580%25d0%25b0%2F&linkname=%D0%93%D1%80%D0%B0%D0%B1%D0%BB%D0%B8%20%D0%BD%D0%B0%D1%87%D0%B8%D0%BD%D0%B0%D1%8E%D1%89%D0%B5%D0%B3%D0%BE%20%D0%BF%D0%B5%D0%BD%D1%82%D0%B5%D1%81%D1%82%D0%B5%D1%80%D0%B0" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F06%2F%25d0%25b3%25d1%2580%25d0%25b0%25d0%25b1%25d0%25bb%25d0%25b8-%25d0%25bd%25d0%25b0%25d1%2587%25d0%25b8%25d0%25bd%25d0%25b0%25d1%258e%25d1%2589%25d0%25b5%25d0%25b3%25d0%25be-%25d0%25bf%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b5%25d1%2581%25d1%2582%25d0%25b5%25d1%2580%25d0%25b0%2F&linkname=%D0%93%D1%80%D0%B0%D0%B1%D0%BB%D0%B8%20%D0%BD%D0%B0%D1%87%D0%B8%D0%BD%D0%B0%D1%8E%D1%89%D0%B5%D0%B3%D0%BE%20%D0%BF%D0%B5%D0%BD%D1%82%D0%B5%D1%81%D1%82%D0%B5%D1%80%D0%B0" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F06%2F%25d0%25b3%25d1%2580%25d0%25b0%25d0%25b1%25d0%25bb%25d0%25b8-%25d0%25bd%25d0%25b0%25d1%2587%25d0%25b8%25d0%25bd%25d0%25b0%25d1%258e%25d1%2589%25d0%25b5%25d0%25b3%25d0%25be-%25d0%25bf%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b5%25d1%2581%25d1%2582%25d0%25b5%25d1%2580%25d0%25b0%2F&linkname=%D0%93%D1%80%D0%B0%D0%B1%D0%BB%D0%B8%20%D0%BD%D0%B0%D1%87%D0%B8%D0%BD%D0%B0%D1%8E%D1%89%D0%B5%D0%B3%D0%BE%20%D0%BF%D0%B5%D0%BD%D1%82%D0%B5%D1%81%D1%82%D0%B5%D1%80%D0%B0" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
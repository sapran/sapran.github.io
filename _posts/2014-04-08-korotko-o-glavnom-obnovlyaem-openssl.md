---
id: 836
title: 'Коротко о главном: обновляем OpenSSL'
date: 2014-04-08T04:02:00+00:00
author: sapran
layout: post
guid: http://styran.com/2014/04/08/%d0%ba%d0%be%d1%80%d0%be%d1%82%d0%ba%d0%be-%d0%be-%d0%b3%d0%bb%d0%b0%d0%b2%d0%bd%d0%be%d0%bc-%d0%be%d0%b1%d0%bd%d0%be%d0%b2%d0%bb%d1%8f%d0%b5%d0%bc-openssl/
permalink: /2014/04/%d0%ba%d0%be%d1%80%d0%be%d1%82%d0%ba%d0%be-%d0%be-%d0%b3%d0%bb%d0%b0%d0%b2%d0%bd%d0%be%d0%bc-%d0%be%d0%b1%d0%bd%d0%be%d0%b2%d0%bb%d1%8f%d0%b5%d0%bc-openssl/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2014/04/openssl.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/8881537283492366112
shorturl:
  - http://tinyurl.com/q3ltdj2
tags:
  - 0-day
  - openssl
  - управление обновлениями
---
<div>
  В OpenSSL версий 1.0.1f и 1.0.2-beta найдена серьезная уязвимость, позволяющая раскрыть до 64Кб памяти подсоединенному хосту. Уязвимость затрагивает библиотеку libcrypto со всеми вытекающими. Например, ее использует сервер OpenSSH. Уязвимось и связанная с ней атака получила романтическое название Heartbleed. Звучит зловеще, поэтому срочно обновляем все свои боксы до 1.0.1g.
</div>

<div>
</div>

<div>
  <a href="http://www.openssl.org/news/secadv_20140407.txt" target="_blank">Оригинал advisory</a> на сайте проекта.
</div>

> OpenSSL Security Advisory [07 Apr 2014]  
> ========================================  
> TLS heartbeat read overrun (CVE-2014-0160)  
> ==========================================  
> A missing bounds check in the handling of the TLS heartbeat extension can be  
> used to reveal up to 64k of memory to a connected client or server.  
> Only 1.0.1 and 1.0.2-beta releases of OpenSSL are affected including  
> 1.0.1f and 1.0.2-beta1.  
> Thanks for Neel Mehta of Google Security for discovering this bug and to  
> Adam Langley <agl chromium.org=""> and Bodo Moeller <bmoeller acm.org=""> for  
> preparing the fix.  
> Affected users should upgrade to OpenSSL 1.0.1g. Users unable to immediately  
> upgrade can alternatively recompile OpenSSL with -DOPENSSL\_NO\_HEARTBEATS.  
> 1.0.2 will be fixed in 1.0.2-beta2.</bmoeller></agl>

Проверить устойчивость вашего сервера к этой уязвимости и почитать о ней много интересного можно по адресу:&nbsp;<http://filippo.io/Heartbleed/>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_301">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2F%25d0%25ba%25d0%25be%25d1%2580%25d0%25be%25d1%2582%25d0%25ba%25d0%25be-%25d0%25be-%25d0%25b3%25d0%25bb%25d0%25b0%25d0%25b2%25d0%25bd%25d0%25be%25d0%25bc-%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b2%25d0%25bb%25d1%258f%25d0%25b5%25d0%25bc-openssl%2F&linkname=%D0%9A%D0%BE%D1%80%D0%BE%D1%82%D0%BA%D0%BE%20%D0%BE%20%D0%B3%D0%BB%D0%B0%D0%B2%D0%BD%D0%BE%D0%BC%3A%20%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D1%8F%D0%B5%D0%BC%20OpenSSL" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2F%25d0%25ba%25d0%25be%25d1%2580%25d0%25be%25d1%2582%25d0%25ba%25d0%25be-%25d0%25be-%25d0%25b3%25d0%25bb%25d0%25b0%25d0%25b2%25d0%25bd%25d0%25be%25d0%25bc-%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b2%25d0%25bb%25d1%258f%25d0%25b5%25d0%25bc-openssl%2F&linkname=%D0%9A%D0%BE%D1%80%D0%BE%D1%82%D0%BA%D0%BE%20%D0%BE%20%D0%B3%D0%BB%D0%B0%D0%B2%D0%BD%D0%BE%D0%BC%3A%20%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D1%8F%D0%B5%D0%BC%20OpenSSL" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2F%25d0%25ba%25d0%25be%25d1%2580%25d0%25be%25d1%2582%25d0%25ba%25d0%25be-%25d0%25be-%25d0%25b3%25d0%25bb%25d0%25b0%25d0%25b2%25d0%25bd%25d0%25be%25d0%25bc-%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b2%25d0%25bb%25d1%258f%25d0%25b5%25d0%25bc-openssl%2F&linkname=%D0%9A%D0%BE%D1%80%D0%BE%D1%82%D0%BA%D0%BE%20%D0%BE%20%D0%B3%D0%BB%D0%B0%D0%B2%D0%BD%D0%BE%D0%BC%3A%20%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D1%8F%D0%B5%D0%BC%20OpenSSL" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F04%2F%25d0%25ba%25d0%25be%25d1%2580%25d0%25be%25d1%2582%25d0%25ba%25d0%25be-%25d0%25be-%25d0%25b3%25d0%25bb%25d0%25b0%25d0%25b2%25d0%25bd%25d0%25be%25d0%25bc-%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b2%25d0%25bb%25d1%258f%25d0%25b5%25d0%25bc-openssl%2F&linkname=%D0%9A%D0%BE%D1%80%D0%BE%D1%82%D0%BA%D0%BE%20%D0%BE%20%D0%B3%D0%BB%D0%B0%D0%B2%D0%BD%D0%BE%D0%BC%3A%20%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D1%8F%D0%B5%D0%BC%20OpenSSL" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
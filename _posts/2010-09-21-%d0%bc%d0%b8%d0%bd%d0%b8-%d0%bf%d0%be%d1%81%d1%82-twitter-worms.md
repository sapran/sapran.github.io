---
id: 1019
title: 'Мини пост: Twitter worms'
date: 2010-09-21T14:28:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/09/21/%d0%bc%d0%b8%d0%bd%d0%b8-%d0%bf%d0%be%d1%81%d1%82-twitter-worms/
permalink: /2010/09/%d0%bc%d0%b8%d0%bd%d0%b8-%d0%bf%d0%be%d1%81%d1%82-twitter-worms/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/09/twitter-worms.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1871512813917954932
shorturl:
  - http://tinyurl.com/om3xhno
tags:
  - 0-day
  - twitter
  - xss
  - зловредный код
---
Как многие уже знают, в настоящее время в Twitter активно эксплуатируется неисправленная Cross Site Scripting (XSS) уязвимость. Жертвы постят от своего имени всякую гадость и заражаются вирусами. В связи с этим, рекомендую

  * выйти (logoff) из Twitter;
  * отключить&nbsp;JavaScript в браузере;
  * настроить блокировку JavaScript в используемом вами расширении типа NoScript;
  * не нажимать и не наводить указателем мыши на ссылки (есть черви, которые распространяются по коду в обработчике события onMouseOver);
  * <s>и никакого секса!</s>

Если без Твиттера уж совсем невтерпежь, используйте клиентское ПО типа **Seesmic** или мобильный сайт [http://m.twitter.com](http://m.twitter.com/), на нем нет JS.

Twitter вроде бы работает над исправлением XSS, посмотрим в какие сроки уложатся.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_122">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2F%25d0%25bc%25d0%25b8%25d0%25bd%25d0%25b8-%25d0%25bf%25d0%25be%25d1%2581%25d1%2582-twitter-worms%2F&linkname=%D0%9C%D0%B8%D0%BD%D0%B8%20%D0%BF%D0%BE%D1%81%D1%82%3A%20Twitter%20worms" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2F%25d0%25bc%25d0%25b8%25d0%25bd%25d0%25b8-%25d0%25bf%25d0%25be%25d1%2581%25d1%2582-twitter-worms%2F&linkname=%D0%9C%D0%B8%D0%BD%D0%B8%20%D0%BF%D0%BE%D1%81%D1%82%3A%20Twitter%20worms" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2F%25d0%25bc%25d0%25b8%25d0%25bd%25d0%25b8-%25d0%25bf%25d0%25be%25d1%2581%25d1%2582-twitter-worms%2F&linkname=%D0%9C%D0%B8%D0%BD%D0%B8%20%D0%BF%D0%BE%D1%81%D1%82%3A%20Twitter%20worms" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F09%2F%25d0%25bc%25d0%25b8%25d0%25bd%25d0%25b8-%25d0%25bf%25d0%25be%25d1%2581%25d1%2582-twitter-worms%2F&linkname=%D0%9C%D0%B8%D0%BD%D0%B8%20%D0%BF%D0%BE%D1%81%D1%82%3A%20Twitter%20worms" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
---
id: 859
title: Двух-чего-то-там аутентификация
date: 2013-06-06T16:12:00+00:00
author: sapran
layout: post
guid: http://styran.com/2013/06/06/%d0%b4%d0%b2%d1%83%d1%85-%d1%87%d0%b5%d0%b3%d0%be-%d1%82%d0%be-%d1%82%d0%b0%d0%bc-%d0%b0%d1%83%d1%82%d0%b5%d0%bd%d1%82%d0%b8%d1%84%d0%b8%d0%ba%d0%b0%d1%86%d0%b8%d1%8f/
permalink: /2013/06/%d0%b4%d0%b2%d1%83%d1%85-%d1%87%d0%b5%d0%b3%d0%be-%d1%82%d0%be-%d1%82%d0%b0%d0%bc-%d0%b0%d1%83%d1%82%d0%b5%d0%bd%d1%82%d0%b8%d1%84%d0%b8%d0%ba%d0%b0%d1%86%d0%b8%d1%8f/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2013/06/blog-post.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/3914622501813578158
shorturl:
  - http://tinyurl.com/pyhv322
tags:
  - dumb asses
  - мультифакторная аутентификация
  - образование
---
Как многие уже слышали, LinkedIn, вслед за Google и Facebook, ввел так называемую двухфакторную аутентификацию пользователей. Вношу поправку.

Все мы знаем, что фактор аутентификации это: 

  * _**или**_ известный пользователю кусок данных (например, пароль),
  * _**или**_ принадлежащий пользователю редкий (или уникальный) предмет (например, криптографический токен),
  * _**или**_, снова таки, уникальный элемент строения тела пользователя (отпечаток пальца, рисунок сетчатки глаза, форма кисти руки и пр.)

Если пользователь предъявляет системе два _**разных**_ фактора, такая аутентификация называется _**двухфакторной**_. Если пользователь представляет системе два экземпляра одного фактора (в случае с LinkedIn так и есть), такая аутентификация не называется двухфакторной. Предъявление двух паролей, один из которых пользователь знает, а второй получает через SMS, называется <b style="font-style: italic;">двухканальной</b>.

Можно, конечно, возразить, что в этом случае вторым фактором является телефонный аппарат или SIM-карта пользователя, но это уже полемика: SIM-карта клонируется или &#171;восстанавливается&#187; через уязвимости организационных процессов центра поддержки абонентов мобильной сети, так что у нас редко есть уверенность в том, что в настоящий момент номер мобильного телефона принадлежит конкретному пользователю.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_278">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F06%2F%25d0%25b4%25d0%25b2%25d1%2583%25d1%2585-%25d1%2587%25d0%25b5%25d0%25b3%25d0%25be-%25d1%2582%25d0%25be-%25d1%2582%25d0%25b0%25d0%25bc-%25d0%25b0%25d1%2583%25d1%2582%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b8%25d1%2584%25d0%25b8%25d0%25ba%25d0%25b0%25d1%2586%25d0%25b8%25d1%258f%2F&linkname=%D0%94%D0%B2%D1%83%D1%85-%D1%87%D0%B5%D0%B3%D0%BE-%D1%82%D0%BE-%D1%82%D0%B0%D0%BC%20%D0%B0%D1%83%D1%82%D0%B5%D0%BD%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D1%8F" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F06%2F%25d0%25b4%25d0%25b2%25d1%2583%25d1%2585-%25d1%2587%25d0%25b5%25d0%25b3%25d0%25be-%25d1%2582%25d0%25be-%25d1%2582%25d0%25b0%25d0%25bc-%25d0%25b0%25d1%2583%25d1%2582%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b8%25d1%2584%25d0%25b8%25d0%25ba%25d0%25b0%25d1%2586%25d0%25b8%25d1%258f%2F&linkname=%D0%94%D0%B2%D1%83%D1%85-%D1%87%D0%B5%D0%B3%D0%BE-%D1%82%D0%BE-%D1%82%D0%B0%D0%BC%20%D0%B0%D1%83%D1%82%D0%B5%D0%BD%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D1%8F" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F06%2F%25d0%25b4%25d0%25b2%25d1%2583%25d1%2585-%25d1%2587%25d0%25b5%25d0%25b3%25d0%25be-%25d1%2582%25d0%25be-%25d1%2582%25d0%25b0%25d0%25bc-%25d0%25b0%25d1%2583%25d1%2582%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b8%25d1%2584%25d0%25b8%25d0%25ba%25d0%25b0%25d1%2586%25d0%25b8%25d1%258f%2F&linkname=%D0%94%D0%B2%D1%83%D1%85-%D1%87%D0%B5%D0%B3%D0%BE-%D1%82%D0%BE-%D1%82%D0%B0%D0%BC%20%D0%B0%D1%83%D1%82%D0%B5%D0%BD%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D1%8F" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F06%2F%25d0%25b4%25d0%25b2%25d1%2583%25d1%2585-%25d1%2587%25d0%25b5%25d0%25b3%25d0%25be-%25d1%2582%25d0%25be-%25d1%2582%25d0%25b0%25d0%25bc-%25d0%25b0%25d1%2583%25d1%2582%25d0%25b5%25d0%25bd%25d1%2582%25d0%25b8%25d1%2584%25d0%25b8%25d0%25ba%25d0%25b0%25d1%2586%25d0%25b8%25d1%258f%2F&linkname=%D0%94%D0%B2%D1%83%D1%85-%D1%87%D0%B5%D0%B3%D0%BE-%D1%82%D0%BE-%D1%82%D0%B0%D0%BC%20%D0%B0%D1%83%D1%82%D0%B5%D0%BD%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D1%8F" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
---
id: 991
title: Будет день, будет Adobe 0-day
date: 2011-03-15T09:12:00+00:00
author: sapran
layout: post
guid: http://styran.com/2011/03/15/%d0%b1%d1%83%d0%b4%d0%b5%d1%82-%d0%b4%d0%b5%d0%bd%d1%8c-%d0%b1%d1%83%d0%b4%d0%b5%d1%82-adobe-0-day/
permalink: /2011/03/%d0%b1%d1%83%d0%b4%d0%b5%d1%82-%d0%b4%d0%b5%d0%bd%d1%8c-%d0%b1%d1%83%d0%b4%d0%b5%d1%82-adobe-0-day/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2011/03/adobe-0-day.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4425264624367894038
shorturl:
  - http://tinyurl.com/oqr2vy2
tags:
  - 0-day
  - adobe
  - emet
  - microsoft
---
<div style="text-align: justify;">
  Не углубляясь в детали, Adobe снова <a href="http://blogs.adobe.com/psirt/2011/03/security-advisory-for-adobe-flash-player-adobe-reader-and-acrobat-apsa11-01.html">радует нас</a> уявзимостями нулевого дня, на этот раз в Flash Player. Так как Adobe <strike>тычет флэш куда попало</strike> большой сторонник тесной интеграции своих продуктов, эта уязвимость наносит удар по Adobe Reader & Acrobat всех версий.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Пользователи Adobe Reader X находятся в сравнительной безопасности, потому что sandbox. Так что советую обновиться до десятой версии, если еще не.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  В настоящее время по Интернету гуляет письмо, в которое вложен XLS файл, в который вложен SWF файл, который эксплуатирует данную&nbsp;уязвимость с целью получения контроля над ПК жертвы. <i><b><span style="font-size: x-small;">[Update 18.02.2011] </span></b></i>Microsoft <a href="https://blogs.technet.com/b/srd/archive/2011/03/17/blocking-exploit-attempts-of-the-recent-flash-0-day.aspx">опубликовала рекомендации по защите</a> от этого конкретного метода атаки при помощи <a href="http://www.microsoft.com/downloads/en/details.aspx?FamilyID=c6f0a6ee-05ac-4eb6-acd0-362559fd2f04">EMET</a>. Google <a href="https://threatpost.com/en_us/blogs/google-fixes-flash-bug-chrome-researchers-track-targeted-attacks-031711">отреагировал обновлением Chrome</a>.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_150">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F03%2F%25d0%25b1%25d1%2583%25d0%25b4%25d0%25b5%25d1%2582-%25d0%25b4%25d0%25b5%25d0%25bd%25d1%258c-%25d0%25b1%25d1%2583%25d0%25b4%25d0%25b5%25d1%2582-adobe-0-day%2F&linkname=%D0%91%D1%83%D0%B4%D0%B5%D1%82%20%D0%B4%D0%B5%D0%BD%D1%8C%2C%20%D0%B1%D1%83%D0%B4%D0%B5%D1%82%20Adobe%200-day" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F03%2F%25d0%25b1%25d1%2583%25d0%25b4%25d0%25b5%25d1%2582-%25d0%25b4%25d0%25b5%25d0%25bd%25d1%258c-%25d0%25b1%25d1%2583%25d0%25b4%25d0%25b5%25d1%2582-adobe-0-day%2F&linkname=%D0%91%D1%83%D0%B4%D0%B5%D1%82%20%D0%B4%D0%B5%D0%BD%D1%8C%2C%20%D0%B1%D1%83%D0%B4%D0%B5%D1%82%20Adobe%200-day" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F03%2F%25d0%25b1%25d1%2583%25d0%25b4%25d0%25b5%25d1%2582-%25d0%25b4%25d0%25b5%25d0%25bd%25d1%258c-%25d0%25b1%25d1%2583%25d0%25b4%25d0%25b5%25d1%2582-adobe-0-day%2F&linkname=%D0%91%D1%83%D0%B4%D0%B5%D1%82%20%D0%B4%D0%B5%D0%BD%D1%8C%2C%20%D0%B1%D1%83%D0%B4%D0%B5%D1%82%20Adobe%200-day" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F03%2F%25d0%25b1%25d1%2583%25d0%25b4%25d0%25b5%25d1%2582-%25d0%25b4%25d0%25b5%25d0%25bd%25d1%258c-%25d0%25b1%25d1%2583%25d0%25b4%25d0%25b5%25d1%2582-adobe-0-day%2F&linkname=%D0%91%D1%83%D0%B4%D0%B5%D1%82%20%D0%B4%D0%B5%D0%BD%D1%8C%2C%20%D0%B1%D1%83%D0%B4%D0%B5%D1%82%20Adobe%200-day" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
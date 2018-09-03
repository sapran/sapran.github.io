---
id: 1030
title: Ударим MSSE по Stuxnet-подобной вирусятине!
date: 2010-07-24T10:51:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/07/24/%d1%83%d0%b4%d0%b0%d1%80%d0%b8%d0%bc-msse-%d0%bf%d0%be-stuxnet-%d0%bf%d0%be%d0%b4%d0%be%d0%b1%d0%bd%d0%be%d0%b9-%d0%b2%d0%b8%d1%80%d1%83%d1%81%d1%8f%d1%82%d0%b8%d0%bd%d0%b5/
permalink: /2010/07/%d1%83%d0%b4%d0%b0%d1%80%d0%b8%d0%bc-msse-%d0%bf%d0%be-stuxnet-%d0%bf%d0%be%d0%b4%d0%be%d0%b1%d0%bd%d0%be%d0%b9-%d0%b2%d0%b8%d1%80%d1%83%d1%81%d1%8f%d1%82%d0%b8%d0%bd%d0%b5/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/07/msse-stuxnet.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/7799213821258789128
shorturl:
  - http://tinyurl.com/ntaejg2
tags:
  - 0-day
  - microsoft
  - антивирусы
---
В продолжение [предыдущего поста](http://securegalaxy.blogspot.com/2010/07/stuxnet.html) хочу добавить, что Microsoft не спешит выпускать патч для Windows, исправляющий уязвимость в Windows Explorer, также известную как Stuxnet. Скорее всего, соответствующее обновление выйдет &#171;по расписанию&#187;, во второй вторник следующего месяца.

Зато MSFT очень шустро [добавляет сигнатуры червей](http://blogs.technet.com/b/mmpc/archive/2010/07/23/protection-for-new-malware-families-using-lnk-vulnerability.aspx), использующих Stuxnet, в базы данных своих антивирусов, в частности [**Microsoft Security Essentials**](https://www.microsoft.com/security_essentials/), распространяемый бесплатно. Так что, если у вас честная винда, настоятельно рекомендую установить этот антивирус с последними обновлениями. Даже в дополнение к тому антивирусу, который у вас уже имеется. На счет возможных &#171;тормозов&#187; можете не переживать, пока никто не жаловался. Если вы окажетесь первым, прошу отписаться в комментариях.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_111">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d1%2583%25d0%25b4%25d0%25b0%25d1%2580%25d0%25b8%25d0%25bc-msse-%25d0%25bf%25d0%25be-stuxnet-%25d0%25bf%25d0%25be%25d0%25b4%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b9-%25d0%25b2%25d0%25b8%25d1%2580%25d1%2583%25d1%2581%25d1%258f%25d1%2582%25d0%25b8%25d0%25bd%25d0%25b5%2F&linkname=%D0%A3%D0%B4%D0%B0%D1%80%D0%B8%D0%BC%20MSSE%20%D0%BF%D0%BE%20Stuxnet-%D0%BF%D0%BE%D0%B4%D0%BE%D0%B1%D0%BD%D0%BE%D0%B9%20%D0%B2%D0%B8%D1%80%D1%83%D1%81%D1%8F%D1%82%D0%B8%D0%BD%D0%B5%21" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d1%2583%25d0%25b4%25d0%25b0%25d1%2580%25d0%25b8%25d0%25bc-msse-%25d0%25bf%25d0%25be-stuxnet-%25d0%25bf%25d0%25be%25d0%25b4%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b9-%25d0%25b2%25d0%25b8%25d1%2580%25d1%2583%25d1%2581%25d1%258f%25d1%2582%25d0%25b8%25d0%25bd%25d0%25b5%2F&linkname=%D0%A3%D0%B4%D0%B0%D1%80%D0%B8%D0%BC%20MSSE%20%D0%BF%D0%BE%20Stuxnet-%D0%BF%D0%BE%D0%B4%D0%BE%D0%B1%D0%BD%D0%BE%D0%B9%20%D0%B2%D0%B8%D1%80%D1%83%D1%81%D1%8F%D1%82%D0%B8%D0%BD%D0%B5%21" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d1%2583%25d0%25b4%25d0%25b0%25d1%2580%25d0%25b8%25d0%25bc-msse-%25d0%25bf%25d0%25be-stuxnet-%25d0%25bf%25d0%25be%25d0%25b4%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b9-%25d0%25b2%25d0%25b8%25d1%2580%25d1%2583%25d1%2581%25d1%258f%25d1%2582%25d0%25b8%25d0%25bd%25d0%25b5%2F&linkname=%D0%A3%D0%B4%D0%B0%D1%80%D0%B8%D0%BC%20MSSE%20%D0%BF%D0%BE%20Stuxnet-%D0%BF%D0%BE%D0%B4%D0%BE%D0%B1%D0%BD%D0%BE%D0%B9%20%D0%B2%D0%B8%D1%80%D1%83%D1%81%D1%8F%D1%82%D0%B8%D0%BD%D0%B5%21" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F07%2F%25d1%2583%25d0%25b4%25d0%25b0%25d1%2580%25d0%25b8%25d0%25bc-msse-%25d0%25bf%25d0%25be-stuxnet-%25d0%25bf%25d0%25be%25d0%25b4%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b9-%25d0%25b2%25d0%25b8%25d1%2580%25d1%2583%25d1%2581%25d1%258f%25d1%2582%25d0%25b8%25d0%25bd%25d0%25b5%2F&linkname=%D0%A3%D0%B4%D0%B0%D1%80%D0%B8%D0%BC%20MSSE%20%D0%BF%D0%BE%20Stuxnet-%D0%BF%D0%BE%D0%B4%D0%BE%D0%B1%D0%BD%D0%BE%D0%B9%20%D0%B2%D0%B8%D1%80%D1%83%D1%81%D1%8F%D1%82%D0%B8%D0%BD%D0%B5%21" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
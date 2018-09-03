---
id: 1045
title: Принцип наименьших привилегий против 0-day expoits
date: 2010-04-01T04:04:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/04/01/%d0%bf%d1%80%d0%b8%d0%bd%d1%86%d0%b8%d0%bf-%d0%bd%d0%b0%d0%b8%d0%bc%d0%b5%d0%bd%d1%8c%d1%88%d0%b8%d1%85-%d0%bf%d1%80%d0%b8%d0%b2%d0%b8%d0%bb%d0%b5%d0%b3%d0%b8%d0%b9-%d0%bf%d1%80%d0%be%d1%82%d0%b8/
permalink: /2010/04/%d0%bf%d1%80%d0%b8%d0%bd%d1%86%d0%b8%d0%bf-%d0%bd%d0%b0%d0%b8%d0%bc%d0%b5%d0%bd%d1%8c%d1%88%d0%b8%d1%85-%d0%bf%d1%80%d0%b8%d0%b2%d0%b8%d0%bb%d0%b5%d0%b3%d0%b8%d0%b9-%d0%bf%d1%80%d0%be%d1%82%d0%b8/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/04/0-day-expoits.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1581386256737984856
shorturl:
  - http://tinyurl.com/q5c742p
tags:
  - microsoft
  - осведомленность
---
<div style="text-align: justify;">
  Занимательный отчет о том, что 64% уязвимостей в ПО Microsoft, обнаруженных в 2009 году, были эффективно компенсированы использованием&nbsp;непривилегированных&nbsp;учетных записей. То есть, даже в случае успешной компрометации системы, атакующему не было от этого особой радости. Закрепиться в системе и/или осуществить эскалацию до доменного администратора&nbsp;с правами текущего непривилегированного пользователя не представлялось возможным. В этом блоге уже <a href="http://securegalaxy.blogspot.com/2009/07/windows.html">неоднократно</a>(1) <a href="http://securegalaxy.blogspot.com/2009/12/blog-post_07.html">подчеркивалась</a>(2) важность принципа наименьших привилегий в организации ИБ.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Цитирую оригинальную новость (<a href="http://blogs.zdnet.com/security/?p=5964">http://blogs.zdnet.com/security/?p=5964</a>)
</div>

<div style="text-align: justify;">
</div>

<ul style="font-family: Verdana, sans-serif; font-size: 12px; line-height: 18px; list-style-type: none; margin-bottom: 8px; margin-left: 0px; margin-right: 0px; margin-top: 8px; padding-bottom: 0px; padding-left: 0px; padding-right: 0px; padding-top: 0px;">
  <li style="background-attachment: initial; background-clip: initial; background-color: initial; background-image: url(http://i.zdnet.com/images/200803/icn_bullet.gif); background-origin: initial; background-position: 0px 4px; background-repeat: no-repeat no-repeat; margin-bottom: 6px; margin-left: 0px; margin-right: 0px; margin-top: 6px; padding-bottom: 0px; padding-left: 17px; padding-right: 0px; padding-top: 0px; text-align: justify;">
    90% of Critical Windows 7 operating system vulnerabilities are mitigated by having users log in as standard users
  </li>
  <li style="background-attachment: initial; background-clip: initial; background-color: initial; background-image: url(http://i.zdnet.com/images/200803/icn_bullet.gif); background-origin: initial; background-position: 0px 4px; background-repeat: no-repeat no-repeat; margin-bottom: 6px; margin-left: 0px; margin-right: 0px; margin-top: 6px; padding-bottom: 0px; padding-left: 17px; padding-right: 0px; padding-top: 0px; text-align: justify;">
    100% of Microsoft Office vulnerabilities reported in 2009
  </li>
  <li style="background-attachment: initial; background-clip: initial; background-color: initial; background-image: url(http://i.zdnet.com/images/200803/icn_bullet.gif); background-origin: initial; background-position: 0px 4px; background-repeat: no-repeat no-repeat; margin-bottom: 6px; margin-left: 0px; margin-right: 0px; margin-top: 6px; padding-bottom: 0px; padding-left: 17px; padding-right: 0px; padding-top: 0px; text-align: justify;">
    94% of Internet Explorer and 100% of IE 8 vulnerabilities reported in 2009
  </li>
  <li style="background-attachment: initial; background-clip: initial; background-color: initial; background-image: url(http://i.zdnet.com/images/200803/icn_bullet.gif); background-origin: initial; background-position: 0px 4px; background-repeat: no-repeat no-repeat; margin-bottom: 6px; margin-left: 0px; margin-right: 0px; margin-top: 6px; padding-bottom: 0px; padding-left: 17px; padding-right: 0px; padding-top: 0px; text-align: justify;">
    64% of all Microsoft vulnerabilities reported in 2009
  </li>
  <li style="background-attachment: initial; background-clip: initial; background-color: initial; background-image: url(http://i.zdnet.com/images/200803/icn_bullet.gif); background-origin: initial; background-position: 0px 4px; background-repeat: no-repeat no-repeat; margin-bottom: 6px; margin-left: 0px; margin-right: 0px; margin-top: 6px; padding-bottom: 0px; padding-left: 17px; padding-right: 0px; padding-top: 0px; text-align: justify;">
    87% of vulnerabilities categorized as Remote Code Execution vulnerabilities are mitigated by removing administrator rights
  </li>
</ul>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Хороший отчет, рекомендую к прочтению.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  <a href="https://docs.google.com/viewer?url=http://www.beyondtrust.com/downloads/whitepapers/documents/wp039_BeyondTrust_2009_Microsoft_Vulnerability_Analysis.pdf">https://docs.google.com/viewer?url=http://www.beyondtrust.com/downloads/whitepapers/documents/wp039_BeyondTrust_2009_Microsoft_Vulnerability_Analysis.pdf</a>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_96">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2F%25d0%25bf%25d1%2580%25d0%25b8%25d0%25bd%25d1%2586%25d0%25b8%25d0%25bf-%25d0%25bd%25d0%25b0%25d0%25b8%25d0%25bc%25d0%25b5%25d0%25bd%25d1%258c%25d1%2588%25d0%25b8%25d1%2585-%25d0%25bf%25d1%2580%25d0%25b8%25d0%25b2%25d0%25b8%25d0%25bb%25d0%25b5%25d0%25b3%25d0%25b8%25d0%25b9-%25d0%25bf%25d1%2580%25d0%25be%25d1%2582%25d0%25b8%2F&linkname=%D0%9F%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%20%D0%BD%D0%B0%D0%B8%D0%BC%D0%B5%D0%BD%D1%8C%D1%88%D0%B8%D1%85%20%D0%BF%D1%80%D0%B8%D0%B2%D0%B8%D0%BB%D0%B5%D0%B3%D0%B8%D0%B9%20%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%200-day%20expoits" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2F%25d0%25bf%25d1%2580%25d0%25b8%25d0%25bd%25d1%2586%25d0%25b8%25d0%25bf-%25d0%25bd%25d0%25b0%25d0%25b8%25d0%25bc%25d0%25b5%25d0%25bd%25d1%258c%25d1%2588%25d0%25b8%25d1%2585-%25d0%25bf%25d1%2580%25d0%25b8%25d0%25b2%25d0%25b8%25d0%25bb%25d0%25b5%25d0%25b3%25d0%25b8%25d0%25b9-%25d0%25bf%25d1%2580%25d0%25be%25d1%2582%25d0%25b8%2F&linkname=%D0%9F%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%20%D0%BD%D0%B0%D0%B8%D0%BC%D0%B5%D0%BD%D1%8C%D1%88%D0%B8%D1%85%20%D0%BF%D1%80%D0%B8%D0%B2%D0%B8%D0%BB%D0%B5%D0%B3%D0%B8%D0%B9%20%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%200-day%20expoits" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2F%25d0%25bf%25d1%2580%25d0%25b8%25d0%25bd%25d1%2586%25d0%25b8%25d0%25bf-%25d0%25bd%25d0%25b0%25d0%25b8%25d0%25bc%25d0%25b5%25d0%25bd%25d1%258c%25d1%2588%25d0%25b8%25d1%2585-%25d0%25bf%25d1%2580%25d0%25b8%25d0%25b2%25d0%25b8%25d0%25bb%25d0%25b5%25d0%25b3%25d0%25b8%25d0%25b9-%25d0%25bf%25d1%2580%25d0%25be%25d1%2582%25d0%25b8%2F&linkname=%D0%9F%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%20%D0%BD%D0%B0%D0%B8%D0%BC%D0%B5%D0%BD%D1%8C%D1%88%D0%B8%D1%85%20%D0%BF%D1%80%D0%B8%D0%B2%D0%B8%D0%BB%D0%B5%D0%B3%D0%B8%D0%B9%20%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%200-day%20expoits" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2F%25d0%25bf%25d1%2580%25d0%25b8%25d0%25bd%25d1%2586%25d0%25b8%25d0%25bf-%25d0%25bd%25d0%25b0%25d0%25b8%25d0%25bc%25d0%25b5%25d0%25bd%25d1%258c%25d1%2588%25d0%25b8%25d1%2585-%25d0%25bf%25d1%2580%25d0%25b8%25d0%25b2%25d0%25b8%25d0%25bb%25d0%25b5%25d0%25b3%25d0%25b8%25d0%25b9-%25d0%25bf%25d1%2580%25d0%25be%25d1%2582%25d0%25b8%2F&linkname=%D0%9F%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%20%D0%BD%D0%B0%D0%B8%D0%BC%D0%B5%D0%BD%D1%8C%D1%88%D0%B8%D1%85%20%D0%BF%D1%80%D0%B8%D0%B2%D0%B8%D0%BB%D0%B5%D0%B3%D0%B8%D0%B9%20%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%200-day%20expoits" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
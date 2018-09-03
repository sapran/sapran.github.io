---
id: 1027
title: Как MSSE и Sophos блокируют попытки использования LNK-уязвимости
date: 2010-08-01T13:50:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/08/01/%d0%ba%d0%b0%d0%ba-msse-%d0%b8-sophos-%d0%b1%d0%bb%d0%be%d0%ba%d0%b8%d1%80%d1%83%d1%8e%d1%82-%d0%bf%d0%be%d0%bf%d1%8b%d1%82%d0%ba%d0%b8-%d0%b8%d1%81%d0%bf%d0%be%d0%bb%d1%8c%d0%b7%d0%be%d0%b2%d0%b0/
permalink: /2010/08/%d0%ba%d0%b0%d0%ba-msse-%d0%b8-sophos-%d0%b1%d0%bb%d0%be%d0%ba%d0%b8%d1%80%d1%83%d1%8e%d1%82-%d0%bf%d0%be%d0%bf%d1%8b%d1%82%d0%ba%d0%b8-%d0%b8%d1%81%d0%bf%d0%be%d0%bb%d1%8c%d0%b7%d0%be%d0%b2%d0%b0/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/08/msse-sophos-lnk.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/7642547781740114098
shorturl:
  - http://tinyurl.com/o9s4y96
tags:
  - 0-day
  - microsoft
  - sophos
---
А вот как: 

<div style="clear: both; text-align: center;">
  <a href="http://4.bp.blogspot.com/_qASWdX8owQc/TFV7itY3ZoI/AAAAAAAAFF4/IIVfXFSCGlE/s1600/MSSE+anti-LNK.PNG" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="172" src="http://4.bp.blogspot.com/_qASWdX8owQc/TFV7itY3ZoI/AAAAAAAAFF4/IIVfXFSCGlE/s320/MSSE+anti-LNK.PNG" width="320" /></a>
</div>

<div style="clear: both; text-align: center;">
  <a href="http://2.bp.blogspot.com/_qASWdX8owQc/TFV7miC-ZJI/AAAAAAAAFF8/sVNAz_GyN7U/s1600/Sophos+anti-LNK.PNG" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="85" src="http://2.bp.blogspot.com/_qASWdX8owQc/TFV7miC-ZJI/AAAAAAAAFF8/sVNAz_GyN7U/s320/Sophos+anti-LNK.PNG" width="320" /></a>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_114">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F08%2F%25d0%25ba%25d0%25b0%25d0%25ba-msse-%25d0%25b8-sophos-%25d0%25b1%25d0%25bb%25d0%25be%25d0%25ba%25d0%25b8%25d1%2580%25d1%2583%25d1%258e%25d1%2582-%25d0%25bf%25d0%25be%25d0%25bf%25d1%258b%25d1%2582%25d0%25ba%25d0%25b8-%25d0%25b8%25d1%2581%25d0%25bf%25d0%25be%25d0%25bb%25d1%258c%25d0%25b7%25d0%25be%25d0%25b2%25d0%25b0%2F&linkname=%D0%9A%D0%B0%D0%BA%20MSSE%20%D0%B8%20Sophos%20%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D1%83%D1%8E%D1%82%20%D0%BF%D0%BE%D0%BF%D1%8B%D1%82%D0%BA%D0%B8%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%20LNK-%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F08%2F%25d0%25ba%25d0%25b0%25d0%25ba-msse-%25d0%25b8-sophos-%25d0%25b1%25d0%25bb%25d0%25be%25d0%25ba%25d0%25b8%25d1%2580%25d1%2583%25d1%258e%25d1%2582-%25d0%25bf%25d0%25be%25d0%25bf%25d1%258b%25d1%2582%25d0%25ba%25d0%25b8-%25d0%25b8%25d1%2581%25d0%25bf%25d0%25be%25d0%25bb%25d1%258c%25d0%25b7%25d0%25be%25d0%25b2%25d0%25b0%2F&linkname=%D0%9A%D0%B0%D0%BA%20MSSE%20%D0%B8%20Sophos%20%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D1%83%D1%8E%D1%82%20%D0%BF%D0%BE%D0%BF%D1%8B%D1%82%D0%BA%D0%B8%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%20LNK-%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F08%2F%25d0%25ba%25d0%25b0%25d0%25ba-msse-%25d0%25b8-sophos-%25d0%25b1%25d0%25bb%25d0%25be%25d0%25ba%25d0%25b8%25d1%2580%25d1%2583%25d1%258e%25d1%2582-%25d0%25bf%25d0%25be%25d0%25bf%25d1%258b%25d1%2582%25d0%25ba%25d0%25b8-%25d0%25b8%25d1%2581%25d0%25bf%25d0%25be%25d0%25bb%25d1%258c%25d0%25b7%25d0%25be%25d0%25b2%25d0%25b0%2F&linkname=%D0%9A%D0%B0%D0%BA%20MSSE%20%D0%B8%20Sophos%20%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D1%83%D1%8E%D1%82%20%D0%BF%D0%BE%D0%BF%D1%8B%D1%82%D0%BA%D0%B8%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%20LNK-%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F08%2F%25d0%25ba%25d0%25b0%25d0%25ba-msse-%25d0%25b8-sophos-%25d0%25b1%25d0%25bb%25d0%25be%25d0%25ba%25d0%25b8%25d1%2580%25d1%2583%25d1%258e%25d1%2582-%25d0%25bf%25d0%25be%25d0%25bf%25d1%258b%25d1%2582%25d0%25ba%25d0%25b8-%25d0%25b8%25d1%2581%25d0%25bf%25d0%25be%25d0%25bb%25d1%258c%25d0%25b7%25d0%25be%25d0%25b2%25d0%25b0%2F&linkname=%D0%9A%D0%B0%D0%BA%20MSSE%20%D0%B8%20Sophos%20%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D1%83%D1%8E%D1%82%20%D0%BF%D0%BE%D0%BF%D1%8B%D1%82%D0%BA%D0%B8%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%20LNK-%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
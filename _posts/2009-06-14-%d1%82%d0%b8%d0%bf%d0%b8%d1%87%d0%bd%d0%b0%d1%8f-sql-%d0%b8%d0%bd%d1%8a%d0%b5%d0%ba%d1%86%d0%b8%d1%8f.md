---
id: 1122
title: Типичная SQL-инъекция
date: 2009-06-14T12:51:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/06/14/%d1%82%d0%b8%d0%bf%d0%b8%d1%87%d0%bd%d0%b0%d1%8f-sql-%d0%b8%d0%bd%d1%8a%d0%b5%d0%ba%d1%86%d0%b8%d1%8f/
permalink: /2009/06/%d1%82%d0%b8%d0%bf%d0%b8%d1%87%d0%bd%d0%b0%d1%8f-sql-%d0%b8%d0%bd%d1%8a%d0%b5%d0%ba%d1%86%d0%b8%d1%8f/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/06/sql.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/333730525447212493
shorturl:
  - http://tinyurl.com/o3x5foa
tags:
  - sql injection
---
<div style="text-align: left;">
  Ковырялся сегодня в Maltego и наткнулся на безобидный пример результата SQL-инъекции. Судя по беспорядочному контенту &#8212; какой-то бот.
</div>

<div>
  <img src="http://2.bp.blogspot.com/_qASWdX8owQc/SjT-4YSOcmI/AAAAAAAACy0/AZbrgOdDxEM/s320/sqlin2.PNG" style="text-align: left;display: block; margin-top: 0px; margin-right: auto; margin-bottom: 10px; margin-left: auto; cursor: pointer; width: 320px; height: 209px; " border="0" alt="" id="BLOGGER_PHOTO_ID_5347178902140645986" /><img src="http://3.bp.blogspot.com/_qASWdX8owQc/SjT-cT9HcwI/AAAAAAAACys/9oVKSPkHfuA/s320/sqlin1.PNG" style="text-align: left;display: block; margin-top: 0px; margin-right: auto; margin-bottom: 10px; margin-left: auto; cursor: pointer; width: 320px; height: 301px; " border="0" alt="" id="BLOGGER_PHOTO_ID_5347178419942028034" /><img src="http://4.bp.blogspot.com/_qASWdX8owQc/SjT9ipN755I/AAAAAAAACyk/eNQqMdX5WQU/s320/sqlin0.PNG" style="text-align: left;display: block; margin-top: 0px; margin-right: auto; margin-bottom: 10px; margin-left: auto; cursor: pointer; width: 320px; height: 179px; " border="0" alt="" id="BLOGGER_PHOTO_ID_5347177429217306514" />
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_19">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F06%2F%25d1%2582%25d0%25b8%25d0%25bf%25d0%25b8%25d1%2587%25d0%25bd%25d0%25b0%25d1%258f-sql-%25d0%25b8%25d0%25bd%25d1%258a%25d0%25b5%25d0%25ba%25d1%2586%25d0%25b8%25d1%258f%2F&linkname=%D0%A2%D0%B8%D0%BF%D0%B8%D1%87%D0%BD%D0%B0%D1%8F%20SQL-%D0%B8%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F06%2F%25d1%2582%25d0%25b8%25d0%25bf%25d0%25b8%25d1%2587%25d0%25bd%25d0%25b0%25d1%258f-sql-%25d0%25b8%25d0%25bd%25d1%258a%25d0%25b5%25d0%25ba%25d1%2586%25d0%25b8%25d1%258f%2F&linkname=%D0%A2%D0%B8%D0%BF%D0%B8%D1%87%D0%BD%D0%B0%D1%8F%20SQL-%D0%B8%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F06%2F%25d1%2582%25d0%25b8%25d0%25bf%25d0%25b8%25d1%2587%25d0%25bd%25d0%25b0%25d1%258f-sql-%25d0%25b8%25d0%25bd%25d1%258a%25d0%25b5%25d0%25ba%25d1%2586%25d0%25b8%25d1%258f%2F&linkname=%D0%A2%D0%B8%D0%BF%D0%B8%D1%87%D0%BD%D0%B0%D1%8F%20SQL-%D0%B8%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F06%2F%25d1%2582%25d0%25b8%25d0%25bf%25d0%25b8%25d1%2587%25d0%25bd%25d0%25b0%25d1%258f-sql-%25d0%25b8%25d0%25bd%25d1%258a%25d0%25b5%25d0%25ba%25d1%2586%25d0%25b8%25d1%258f%2F&linkname=%D0%A2%D0%B8%D0%BF%D0%B8%D1%87%D0%BD%D0%B0%D1%8F%20SQL-%D0%B8%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
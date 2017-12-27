---
id: 1043
title: Критическая уязвимость в Java
date: 2010-04-09T19:20:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/04/09/%d0%ba%d1%80%d0%b8%d1%82%d0%b8%d1%87%d0%b5%d1%81%d0%ba%d0%b0%d1%8f-%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%b2-java/
permalink: /2010/04/%d0%ba%d1%80%d0%b8%d1%82%d0%b8%d1%87%d0%b5%d1%81%d0%ba%d0%b0%d1%8f-%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82%d1%8c-%d0%b2-java/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/04/java.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1306273267647863054
shorturl:
  - http://tinyurl.com/nqv4gev
tags:
  - java
---
<span style="font-family: Arial; font-size: small;"><span style="font-size: 13px;"><a href="http://www.exploit-db.com/exploits/12122">Это серьезно</a>:</span></span> 

<div>
  <span style="font-family: Arial; font-size: 13px;"><br /></span>
</div>

<div>
  <span style="font-family: Arial; font-size: 13px;"><i>&#8230;basically the Java-Plugin Browser is running &#171;javaws.exe&#187; without validating command-line parameters. These parameters can be controlled by attackers via specially crafted embed html tags within a webpage.</i></span>
</div>

<div>
  <span style="font-family: Arial; font-size: 13px;"><i></i></span><br /><span style="font-family: Arial; font-size: 13px;"><i></i></span><br /><span style="font-family: Arial; font-size: 13px;"><i> 
  
  <div>
  </div>
  
  <div>
    &#8230;What type of arguments can we abuse to compromise a system?
  </div>
  
  <div>
    java.exe and javaw.exe support an undocumented-hidden command-line parameter &#171;-XXaltjvm&#187; and curiosly also &#171;-J-XXaltjvm&#187; (see -J switch in javaws.exe). This instructs Java to load an alternative JavaVM library (jvm.dll or libjvm.so) from the desired path. Game over. We can set -XXaltjvm=\IPevil , in this way javaw.exe will load our evil jvm.dll. Bye bye ASLR, DEP&#8230;
  </div>
  
  <div>
  </div>
  
  <div>
    <span style="font-style: normal;"><i></i></span><br /><span style="font-style: normal;"><i></i></span><br /><span style="font-style: normal;"><i> 
    
    <div style="display: inline !important;">
      <b>&#8230;Workaround</b>
    </div>
    
    <p>
      </i></span></div> 
      
      <div>
      </div>
      
      <div>
        Disable javaws/javaws.exe in linux and Windows by any mean. Disable Deployment Toolkit to avoid unwanted installation as stated in <a href="http://www.exploit-db.com/exploits/12117">Tavis&#8217; advisory</a>.</p> 
        
        <p>
          <span style="font-style: normal;"><b>Update&nbsp;</b>Вопреки&nbsp;мнениям скептиков, к которым я отношу и себя,&nbsp;Sun&nbsp;(то есть<b>&nbsp;</b>Oracle) <a href="http://www.theregister.co.uk/2010/04/15/emergency_java_patch/">выпустил экстренное исправление</a> для этой уязвимости. Для установки обновления, выполните следующие действия:&nbsp;<b>Start > Control Panel > Java > Update > Update Now</b>.</span></div> 
          
          <p>
            </i></span></div> 
            
            <div class="addtoany_share_save_container addtoany_content_bottom">
              <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_98">
                <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2F%25d0%25ba%25d1%2580%25d0%25b8%25d1%2582%25d0%25b8%25d1%2587%25d0%25b5%25d1%2581%25d0%25ba%25d0%25b0%25d1%258f-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-java%2F&linkname=%D0%9A%D1%80%D0%B8%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20Java" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2F%25d0%25ba%25d1%2580%25d0%25b8%25d1%2582%25d0%25b8%25d1%2587%25d0%25b5%25d1%2581%25d0%25ba%25d0%25b0%25d1%258f-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-java%2F&linkname=%D0%9A%D1%80%D0%B8%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20Java" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2F%25d0%25ba%25d1%2580%25d0%25b8%25d1%2582%25d0%25b8%25d1%2587%25d0%25b5%25d1%2581%25d0%25ba%25d0%25b0%25d1%258f-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-java%2F&linkname=%D0%9A%D1%80%D0%B8%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20Java" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2F%25d0%25ba%25d1%2580%25d0%25b8%25d1%2582%25d0%25b8%25d1%2587%25d0%25b5%25d1%2581%25d0%25ba%25d0%25b0%25d1%258f-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d0%25b2-java%2F&linkname=%D0%9A%D1%80%D0%B8%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20Java" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
              </div>
            </div>
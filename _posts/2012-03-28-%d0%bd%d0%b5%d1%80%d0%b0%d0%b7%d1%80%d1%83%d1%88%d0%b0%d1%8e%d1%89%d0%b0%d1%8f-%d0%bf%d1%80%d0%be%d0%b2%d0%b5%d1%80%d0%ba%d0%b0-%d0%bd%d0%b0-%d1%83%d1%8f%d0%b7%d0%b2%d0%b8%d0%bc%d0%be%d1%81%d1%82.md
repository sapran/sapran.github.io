---
id: 920
title: Неразрушающая проверка на уязвимость к MS12-020
date: 2012-03-28T12:51:00+00:00
author: sapran
layout: post
guid: http://styran.com/2012/03/28/%d0%bd%d0%b5%d1%80%d0%b0%d0%b7%d1%80%d1%83%d1%88%d0%b0%d1%8e%d1%89%d0%b0%d1%8f-%d0%bf%d1%80%d0%be%d0%b2%d0%b5%d1%80%d0%ba%d0%b0-%d0%bd%d0%b0-%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82/
permalink: /2012/03/%d0%bd%d0%b5%d1%80%d0%b0%d0%b7%d1%80%d1%83%d1%88%d0%b0%d1%8e%d1%89%d0%b0%d1%8f-%d0%bf%d1%80%d0%be%d0%b2%d0%b5%d1%80%d0%ba%d0%b0-%d0%bd%d0%b0-%d1%83%d1%8f%d0%b7%d0%b2%d0%b8%d0%bc%d0%be%d1%81%d1%82/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2012/03/ms12-020.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/6768955339268668266
shorturl:
  - http://tinyurl.com/p664mxz
tags:
  - microsoft
  - nmap
---
<div dir="ltr" style="text-align: left;">
  Многие наверняка уже слышали страшную сказку о том, что в последний <a href="http://en.wikipedia.org/wiki/Patch_Tuesday" target="_blank"><i>Черный Вторник</i></a> корпорация Майкрософт выпустила критическое обновление для всех версий Windows, которое исправляет Страшную и Ужасную Уязвимость в RDP, а именно <a href="http://technet.microsoft.com/ru-ru/security/bulletin/MS12-020" target="_blank"><i><b>MS12-020</b></i></a>. По разным данным эксплуатировать эту уязвимость для чего-то более неприятного, чем вызов отказа в обслуживании (система уходит в <a href="http://ru.wikipedia.org/wiki/%D0%A1%D0%B8%D0%BD%D0%B8%D0%B9_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD_%D1%81%D0%BC%D0%B5%D1%80%D1%82%D0%B8" target="_blank"><i>Синий Экран Смерти</i></a>), очень сложно, и пока об удачных попытках удаленного выполнения кода лично мне ничего не известно. (Что, в принципе, ничего не доказывает, но надежда все-таки есть.) Потому что иначе, если будет найден способ выполнить на машине произвольный код, последствия могут быть сравнимы с эксплуатацией <i><b><a href="http://www.securitylab.ru/analytics/361827.php" target="_blank">MS08-067</a></b></i>, а это, как мы помним, чрезвычайно проворные сетевые черви типа&nbsp;<i><b><a href="http://www.f-secure.com/weblog/archives/00001576.html" target="_blank">Downadup/Conflicker</a></b></i>.</p> 
  
  <p>
    Как же проверить, что ваши драгоценные винды все до одной пропатчились и уже неуязвимы к этой потенциально катастрофической заразе? Существующий <i>Proof-of-Concept код на Питоне</i> вызывает отказ в обслуживании системы, то есть, им проверять обширные парки серверов и рабочих станций не очень-то удобно. Выдернуть каждый комп в Интернет и посетить с него <i>RDPcheck.com</i> тоже как-то не с руки. К счастью, на днях для этих целей был написан скрипт для <b><i><a href="http://nmap.org/" target="_blank">NMap</a></i></b>, выполнить который можно вот таким простейшим образом, а результаты выполнения в комментариях не нуждаются.
  </p>
  
  <p>
    Состояние &#171;до&#187;:<br /> 
    
    <blockquote>
      <span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;"></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">sudo wget http://seclists.org/nmap-dev/2012/q1/att-662/rdp-ms12-020.nse -O /usr/local/share/nmap/scripts/rdp-ms12-020.nse</span></p>
    </blockquote>
    
    <blockquote>
      <p>
        <span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">sudo nmap -p3389 &#8212;script rdp-ms12-020 IP<ip></ip></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;"><br /></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">Starting Nmap 5.61TEST5 ( http://nmap.org ) at 2012-03-28 15:22 EEST</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">Nmap scan report for HOST&nbsp;<host>(IP<ip>)</ip></host></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">Host is up (0.14s latency).</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">PORT &nbsp; &nbsp; STATE SERVICE</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">3389/tcp open &nbsp;ms-wbt-server</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| rdp-ms12-020:&nbsp;</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; VULNERABLE:</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; MS12-020 Remote Desktop Protocol Vulnerability</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; State: VULNERABLE</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; IDs: &nbsp;CVE:CVE-2012-0152,CVE-2012-0002</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; Risk factor: High &nbsp;CVSSv2: 9.3 (HIGH) (AV:N/AC:M/Au:N/C:C/I:C/A:C)</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; Description:</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; &nbsp; <span style="white-space: pre;"> </span>Remote Desktop Protocol vulnerability that could allow remote attackers to execute arbitrary code on the targeted system.&nbsp;</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; &nbsp; <span style="white-space: pre;"> </span></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; Disclosure date: 2012-03-13</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; References:</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">| &nbsp; &nbsp; &nbsp; http://technet.microsoft.com/en-us/security/bulletin/ms12-020</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">|_ &nbsp; &nbsp; &nbsp;http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0152,CVE-2012-0002</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">MAC Address: 00:0C:29:39:77:E7 (VMware)</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;"><br /></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">Nmap done: 1 IP address (1 host up) scanned in 1.02 seconds</span>
      </p>
    </blockquote>
    
    <div>
      Состояние &#171;после&#187;:
    </div>
    
    <blockquote>
      <p>
        <span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;"></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">sudo nmap -p3389 &#8212;script rdp-ms12-020 IP</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;"><br /></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">Starting Nmap 5.61TEST5 ( http://nmap.org ) at 2012-03-28 15:40 EEST</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">Nmap scan report for HOST (IP)</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">Host is up (0.00040s latency).</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">PORT &nbsp; &nbsp; STATE SERVICE</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">3389/tcp open &nbsp;ms-wbt-server</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">MAC Address: 00:0C:29:39:77:E7 (VMware)</span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;"><br /></span><br /><span style="font-family: 'Helvetica Neue', Arial, Helvetica, sans-serif;">Nmap done: 1 IP address (1 host up) scanned in 0.09 seconds</span>
      </p>
    </blockquote>
    
    <div>
      <span style="font-family: inherit;">Переход из одного состояния в другое осуществляется путем установки обновления <i><b><a href="http://support.microsoft.com/kb/2621440" target="_blank">KB2621440</a></b></i>.</span>
    </div></div> 
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_221">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F03%2F%25d0%25bd%25d0%25b5%25d1%2580%25d0%25b0%25d0%25b7%25d1%2580%25d1%2583%25d1%2588%25d0%25b0%25d1%258e%25d1%2589%25d0%25b0%25d1%258f-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b2%25d0%25b5%25d1%2580%25d0%25ba%25d0%25b0-%25d0%25bd%25d0%25b0-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%2F&linkname=%D0%9D%D0%B5%D1%80%D0%B0%D0%B7%D1%80%D1%83%D1%88%D0%B0%D1%8E%D1%89%D0%B0%D1%8F%20%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%BD%D0%B0%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BA%20MS12-020" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F03%2F%25d0%25bd%25d0%25b5%25d1%2580%25d0%25b0%25d0%25b7%25d1%2580%25d1%2583%25d1%2588%25d0%25b0%25d1%258e%25d1%2589%25d0%25b0%25d1%258f-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b2%25d0%25b5%25d1%2580%25d0%25ba%25d0%25b0-%25d0%25bd%25d0%25b0-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%2F&linkname=%D0%9D%D0%B5%D1%80%D0%B0%D0%B7%D1%80%D1%83%D1%88%D0%B0%D1%8E%D1%89%D0%B0%D1%8F%20%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%BD%D0%B0%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BA%20MS12-020" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F03%2F%25d0%25bd%25d0%25b5%25d1%2580%25d0%25b0%25d0%25b7%25d1%2580%25d1%2583%25d1%2588%25d0%25b0%25d1%258e%25d1%2589%25d0%25b0%25d1%258f-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b2%25d0%25b5%25d1%2580%25d0%25ba%25d0%25b0-%25d0%25bd%25d0%25b0-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%2F&linkname=%D0%9D%D0%B5%D1%80%D0%B0%D0%B7%D1%80%D1%83%D1%88%D0%B0%D1%8E%D1%89%D0%B0%D1%8F%20%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%BD%D0%B0%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BA%20MS12-020" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F03%2F%25d0%25bd%25d0%25b5%25d1%2580%25d0%25b0%25d0%25b7%25d1%2580%25d1%2583%25d1%2588%25d0%25b0%25d1%258e%25d1%2589%25d0%25b0%25d1%258f-%25d0%25bf%25d1%2580%25d0%25be%25d0%25b2%25d0%25b5%25d1%2580%25d0%25ba%25d0%25b0-%25d0%25bd%25d0%25b0-%25d1%2583%25d1%258f%25d0%25b7%25d0%25b2%25d0%25b8%25d0%25bc%25d0%25be%25d1%2581%25d1%2582%2F&linkname=%D0%9D%D0%B5%D1%80%D0%B0%D0%B7%D1%80%D1%83%D1%88%D0%B0%D1%8E%D1%89%D0%B0%D1%8F%20%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%BD%D0%B0%20%D1%83%D1%8F%D0%B7%D0%B2%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%BA%20MS12-020" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
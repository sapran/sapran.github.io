---
id: 891
title: Обнаружена утечка ключей цифровой подписи кода Adobe
date: 2012-09-28T09:24:00+00:00
author: sapran
layout: post
guid: http://styran.com/2012/09/28/%d0%be%d0%b1%d0%bd%d0%b0%d1%80%d1%83%d0%b6%d0%b5%d0%bd%d0%b0-%d1%83%d1%82%d0%b5%d1%87%d0%ba%d0%b0-%d0%ba%d0%bb%d1%8e%d1%87%d0%b5%d0%b9-%d1%86%d0%b8%d1%84%d1%80%d0%be%d0%b2%d0%be%d0%b9-%d0%bf%d0%be/
permalink: /2012/09/%d0%be%d0%b1%d0%bd%d0%b0%d1%80%d1%83%d0%b6%d0%b5%d0%bd%d0%b0-%d1%83%d1%82%d0%b5%d1%87%d0%ba%d0%b0-%d0%ba%d0%bb%d1%8e%d1%87%d0%b5%d0%b9-%d1%86%d0%b8%d1%84%d1%80%d0%be%d0%b2%d0%be%d0%b9-%d0%bf%d0%be/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2012/09/adobe.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/5993568365958082573
shorturl:
  - http://tinyurl.com/q47u5jm
tags:
  - adobe
  - инциденты
---
<div dir="ltr" style="text-align: left;">
  Такие инциденты случаются редко, поэтому имею дерзость обратить ваше внимание.</p> 
  
  <p>
    Точно неизвестно когда, в Adobe Inc. произошел взлом, в результате которого хакерам удалось получить доступ к серверам, накладывающим цифровую подпись на исполняемые файлы (некоторых) программ этого вендора. Ключ был использован 26 июня 2012 г. для подписи кода <i><b>pwdump7</b></i> (утилиты для извлечения хешей паролей пользователей Windows) и &nbsp;<i><b>myGeeksmail.dll</b></i> (доселе неизвестной в широких кругах, предположительно это фильтр ISAPI &#8212; один из способов расширения функциональности ПО вебсервера IIS).
  </p>
  
  <p>
    Небольшой ликбез по цифровой подписи кода.&nbsp;Отсутствие&nbsp;цифровой подписи при попытке запустить исполняемый файл выглядит вот так:
  </p>
  
  <div style="clear: both; text-align: center;">
    <a href="http://3.bp.blogspot.com/-UhFTA7WY8yY/UGVe_HlEboI/AAAAAAAAUx0/q0w1EQnrhSo/s1600/unsigned.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="244" src="http://3.bp.blogspot.com/-UhFTA7WY8yY/UGVe_HlEboI/AAAAAAAAUx0/q0w1EQnrhSo/s320/unsigned.png" width="320" /></a>
  </div>
  
  <p>
    То есть, вылетает окно предупреждения, сообщающее о том, что код поступил от неизвестного издателя. Если же на код наложена цифровая подпись, сообщение выглядит иначе: 
    
    <div style="clear: both; text-align: center;">
    </div>
    
    <div style="clear: both; text-align: center;">
      <a href="http://1.bp.blogspot.com/-wi-JKvwNnP4/UGViYPVNQMI/AAAAAAAAUyE/gXNB_yg0OuM/s1600/signed.png" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="244" src="http://1.bp.blogspot.com/-wi-JKvwNnP4/UGViYPVNQMI/AAAAAAAAUyE/gXNB_yg0OuM/s320/signed.png" width="320" /></a>
    </div>
    
    <p>
      То есть, уведомления об&nbsp;отсутствии&nbsp;подписи издателя уже нет, осталась только форма повышения&nbsp;привилегий&nbsp;<a href="http://en.wikipedia.org/wiki/User_Account_Control"><i><b>UAC</b></i></a>. Если же UAC в вашей системе отключен, <strike>то это полный провал</strike> то уведомление не появляется вовсе.
    </p>
    
    <p>
      Использование цифровой подписи кода &#8212; не идеальный, но действенный контроль безопасности приложений. Как и в любой инкарнации PKI, в нем существует ряд&nbsp;уязвимостей. Одна из них, слабая защита центра сертификации ключей, по-видимому была<br />эксплуатирована взломщиками. Я не разделяю энтузиазма некоторых коллег, которые предполагают, что взлом произошел во время нашумевшей <i><b><a href="http://en.wikipedia.org/wiki/Operation_Aurora">комплексной атаки Аврора</a></b></i> в 2009 г., хотя и не исключаю такую возможность.
    </p>
    
    <p>
      Приятно наблюдать, что мир узнает об инциденте из <a href="https://blogs.adobe.com/asset/2012/09/inappropriate-use-of-adobe-code-signing-certificate.html"><b><i>блога компании Adobe</i></b></a>.</div> 
      
      <div class="addtoany_share_save_container addtoany_content_bottom">
        <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_248">
          <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F09%2F%25d0%25be%25d0%25b1%25d0%25bd%25d0%25b0%25d1%2580%25d1%2583%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b0-%25d1%2583%25d1%2582%25d0%25b5%25d1%2587%25d0%25ba%25d0%25b0-%25d0%25ba%25d0%25bb%25d1%258e%25d1%2587%25d0%25b5%25d0%25b9-%25d1%2586%25d0%25b8%25d1%2584%25d1%2580%25d0%25be%25d0%25b2%25d0%25be%25d0%25b9-%25d0%25bf%25d0%25be%2F&linkname=%D0%9E%D0%B1%D0%BD%D0%B0%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B0%20%D1%83%D1%82%D0%B5%D1%87%D0%BA%D0%B0%20%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%B9%20%D1%86%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%BE%D0%B9%20%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D0%B8%20%D0%BA%D0%BE%D0%B4%D0%B0%20Adobe" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F09%2F%25d0%25be%25d0%25b1%25d0%25bd%25d0%25b0%25d1%2580%25d1%2583%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b0-%25d1%2583%25d1%2582%25d0%25b5%25d1%2587%25d0%25ba%25d0%25b0-%25d0%25ba%25d0%25bb%25d1%258e%25d1%2587%25d0%25b5%25d0%25b9-%25d1%2586%25d0%25b8%25d1%2584%25d1%2580%25d0%25be%25d0%25b2%25d0%25be%25d0%25b9-%25d0%25bf%25d0%25be%2F&linkname=%D0%9E%D0%B1%D0%BD%D0%B0%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B0%20%D1%83%D1%82%D0%B5%D1%87%D0%BA%D0%B0%20%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%B9%20%D1%86%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%BE%D0%B9%20%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D0%B8%20%D0%BA%D0%BE%D0%B4%D0%B0%20Adobe" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F09%2F%25d0%25be%25d0%25b1%25d0%25bd%25d0%25b0%25d1%2580%25d1%2583%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b0-%25d1%2583%25d1%2582%25d0%25b5%25d1%2587%25d0%25ba%25d0%25b0-%25d0%25ba%25d0%25bb%25d1%258e%25d1%2587%25d0%25b5%25d0%25b9-%25d1%2586%25d0%25b8%25d1%2584%25d1%2580%25d0%25be%25d0%25b2%25d0%25be%25d0%25b9-%25d0%25bf%25d0%25be%2F&linkname=%D0%9E%D0%B1%D0%BD%D0%B0%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B0%20%D1%83%D1%82%D0%B5%D1%87%D0%BA%D0%B0%20%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%B9%20%D1%86%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%BE%D0%B9%20%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D0%B8%20%D0%BA%D0%BE%D0%B4%D0%B0%20Adobe" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F09%2F%25d0%25be%25d0%25b1%25d0%25bd%25d0%25b0%25d1%2580%25d1%2583%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b0-%25d1%2583%25d1%2582%25d0%25b5%25d1%2587%25d0%25ba%25d0%25b0-%25d0%25ba%25d0%25bb%25d1%258e%25d1%2587%25d0%25b5%25d0%25b9-%25d1%2586%25d0%25b8%25d1%2584%25d1%2580%25d0%25be%25d0%25b2%25d0%25be%25d0%25b9-%25d0%25bf%25d0%25be%2F&linkname=%D0%9E%D0%B1%D0%BD%D0%B0%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B0%20%D1%83%D1%82%D0%B5%D1%87%D0%BA%D0%B0%20%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%B9%20%D1%86%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%BE%D0%B9%20%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D0%B8%20%D0%BA%D0%BE%D0%B4%D0%B0%20Adobe" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
        </div>
      </div>
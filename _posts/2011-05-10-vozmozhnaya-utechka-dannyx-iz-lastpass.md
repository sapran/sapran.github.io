---
id: 975
title: Возможная утечка данных из LastPass
date: 2011-05-10T07:43:00+00:00
author: sapran
layout: post
guid: http://styran.com/2011/05/10/%d0%b2%d0%be%d0%b7%d0%bc%d0%be%d0%b6%d0%bd%d0%b0%d1%8f-%d1%83%d1%82%d0%b5%d1%87%d0%ba%d0%b0-%d0%b4%d0%b0%d0%bd%d0%bd%d1%8b%d1%85-%d0%b8%d0%b7-lastpass/
permalink: /2011/05/%d0%b2%d0%be%d0%b7%d0%bc%d0%be%d0%b6%d0%bd%d0%b0%d1%8f-%d1%83%d1%82%d0%b5%d1%87%d0%ba%d0%b0-%d0%b4%d0%b0%d0%bd%d0%bd%d1%8b%d1%85-%d0%b8%d0%b7-lastpass/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2011/05/lastpass.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/6573274202983417741
shorturl:
  - http://tinyurl.com/q8vw3sh
tags:
  - lastpass
  - инциденты
  - пароли
---
<div dir="ltr" style="text-align: left;">
  <div style="text-align: justify;">
    Всем пользователям <b><a href="https://lastpass.com/">LastPass</a>&nbsp;</b>следует изменить свои мастер-пароли и переосмыслить использование этого сервиса для хранения данных доступа к важным ресурсам. Лично я советую не использовать LastPass для электронной почты, социальных сетей и сайтов, оперирующих платежной информацией и персональными данными. Для хранения многочисленных <i>важных</i> паролей следует использовать что-то, работающее в режиме offline: например, <a href="http://keepass.info/"><b>KeePass</b></a>.
  </div>
  
  <p>
    <div style="text-align: justify;">
      Подробное описание причины такой спешки <a href="https://lastpass.com/status.php"><b>размещено по ссылке</b></a>. Существует уверенность в том, что сеть LastPass была взломана. Также, есть подозрение, что злоумышленники осуществили доступ к клиентской информации (логично, зачем еще это делать).
    </div></div> 
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_166">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F05%2F%25d0%25b2%25d0%25be%25d0%25b7%25d0%25bc%25d0%25be%25d0%25b6%25d0%25bd%25d0%25b0%25d1%258f-%25d1%2583%25d1%2582%25d0%25b5%25d1%2587%25d0%25ba%25d0%25b0-%25d0%25b4%25d0%25b0%25d0%25bd%25d0%25bd%25d1%258b%25d1%2585-%25d0%25b8%25d0%25b7-lastpass%2F&linkname=%D0%92%D0%BE%D0%B7%D0%BC%D0%BE%D0%B6%D0%BD%D0%B0%D1%8F%20%D1%83%D1%82%D0%B5%D1%87%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B8%D0%B7%20LastPass" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F05%2F%25d0%25b2%25d0%25be%25d0%25b7%25d0%25bc%25d0%25be%25d0%25b6%25d0%25bd%25d0%25b0%25d1%258f-%25d1%2583%25d1%2582%25d0%25b5%25d1%2587%25d0%25ba%25d0%25b0-%25d0%25b4%25d0%25b0%25d0%25bd%25d0%25bd%25d1%258b%25d1%2585-%25d0%25b8%25d0%25b7-lastpass%2F&linkname=%D0%92%D0%BE%D0%B7%D0%BC%D0%BE%D0%B6%D0%BD%D0%B0%D1%8F%20%D1%83%D1%82%D0%B5%D1%87%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B8%D0%B7%20LastPass" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F05%2F%25d0%25b2%25d0%25be%25d0%25b7%25d0%25bc%25d0%25be%25d0%25b6%25d0%25bd%25d0%25b0%25d1%258f-%25d1%2583%25d1%2582%25d0%25b5%25d1%2587%25d0%25ba%25d0%25b0-%25d0%25b4%25d0%25b0%25d0%25bd%25d0%25bd%25d1%258b%25d1%2585-%25d0%25b8%25d0%25b7-lastpass%2F&linkname=%D0%92%D0%BE%D0%B7%D0%BC%D0%BE%D0%B6%D0%BD%D0%B0%D1%8F%20%D1%83%D1%82%D0%B5%D1%87%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B8%D0%B7%20LastPass" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F05%2F%25d0%25b2%25d0%25be%25d0%25b7%25d0%25bc%25d0%25be%25d0%25b6%25d0%25bd%25d0%25b0%25d1%258f-%25d1%2583%25d1%2582%25d0%25b5%25d1%2587%25d0%25ba%25d0%25b0-%25d0%25b4%25d0%25b0%25d0%25bd%25d0%25bd%25d1%258b%25d1%2585-%25d0%25b8%25d0%25b7-lastpass%2F&linkname=%D0%92%D0%BE%D0%B7%D0%BC%D0%BE%D0%B6%D0%BD%D0%B0%D1%8F%20%D1%83%D1%82%D0%B5%D1%87%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B8%D0%B7%20LastPass" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
---
id: 833
title: Детские страхи украинских айтишников
date: 2014-05-21T18:51:00+00:00
author: sapran
layout: post
guid: http://styran.com/2014/05/21/%d0%b4%d0%b5%d1%82%d1%81%d0%ba%d0%b8%d0%b5-%d1%81%d1%82%d1%80%d0%b0%d1%85%d0%b8-%d1%83%d0%ba%d1%80%d0%b0%d0%b8%d0%bd%d1%81%d0%ba%d0%b8%d1%85-%d0%b0%d0%b9%d1%82%d0%b8%d1%88%d0%bd%d0%b8%d0%ba%d0%be/
permalink: /2014/05/%d0%b4%d0%b5%d1%82%d1%81%d0%ba%d0%b8%d0%b5-%d1%81%d1%82%d1%80%d0%b0%d1%85%d0%b8-%d1%83%d0%ba%d1%80%d0%b0%d0%b8%d0%bd%d1%81%d0%ba%d0%b8%d1%85-%d0%b0%d0%b9%d1%82%d0%b8%d1%88%d0%bd%d0%b8%d0%ba%d0%be/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2014/05/blog-post_21.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/3481122992750639087
shorturl:
  - http://tinyurl.com/nkr4mhx
tags:
  - dumb asses
  - безопасность облаков
  - облачная безопасность
---
<div style="clear: both; text-align: left;">
  Пока в моей голове зреет серия постов о безопасности &#171;облачных инфраструктур&#187;, позволю себе коротко высказаться не в пользу украинских айтишников.
</div>

Очень часто, особенно в последнее время, случается слышать диалоги между поставщиками услуг и потенциальными клиентами приблизительно такого содержания.
  


> – Скажите, а у вас нет ничего такого же, только чтобы не в облаке?  
> – Э-э&#8230; А зачем?  
> – &#8230;</p>
То есть, после уточняющего вопроса клиенту ответить нечего, потому что его страх перед неизведанным подсознательный и фактических аргументов под собой не имеет. Идея перенесения части трафика или даже, не дай бог, драгоценных данных в &#171;облако&#187; вызывает у многих первобытный ужас.

Возьмем, к примеру, &#171;мойку трафика&#187;, также известную под названием защита от DDoS. &#171;– В облако не хочу, хочу железку у себя на площадке.&#187; Ну ОК, поставит вам вендор мигающую коробочку в серверной. Постоит она там годик. Принимая во внимание динамику роста объемов трафика DDoS, к концу этого годика вы сможете ее смело выбросить или озадачиться &#171;расширением лицензии&#187;. Передумывать будет уже поздно, потому что деньги за железку заплачены, боссы не поймут, бухгалтерия линчует. И будете сидеть на этом решении как на игле аж до end-of-support, а потом еще и на следующую версию переедете. И все это вместо того, чтобы заплатить провайдеру облачной услуги значительно меньшую сумму, причем &#171;по счетчику&#187; – за защиту от реальных атак.

Еще пример, обработка данных. Всем с пеленок известно, что бизнес-данные должны защищаться end-to-end, то есть, на протяжении всего жизненного цикла. В этом случае, если вы зашифровали или еще как-то ограничили доступ к ним уже в момент создания документа, то какая вам разница, будет он храниться, обрабатываться и передаваться на вашем корпоративном &#171;шарике&#187;, &#171;сиквеле&#187; или &#171;ексчейндже&#187;, или на их аналогах в &#171;Ажуре&#187;, которые места не занимают и воздух не греют? Ах, вы их не шифруете и не защищаете? Тогда простите, но судя по моему богатому жизненному опыту, у вас в подвале они в большей опасности, чем в облаке Микрософта.

В общем, все беды от невежества. Каждый, хотя бы попытавшийся разобраться в профиле рисков облачных сред, прекрасно знает, какие из таких страхов действительно заслуживают внимания, а какие надуманы. Более того, многие до сих пор не в курсе, что &#171;переезд&#187; в облако автоматически решает кучу наследственных проблем безопасности, таких как неучтенные активы и сегментация сети. Так что, надеюсь, последующие посты найдут своего читателя, так как я, похоже, в этой теме надолго.

Вот вам для затравки пара вайтпейперов на тему, развлекайтесь. 

  * <a href="https://github.com/Securosis/The-CISOs-Guide-to-Cloud-Security/blob/master/CISO_Cloud.md" target="_blank">What CISOs Need to Know about Cloud Computing</a>
  * <a href="https://securosis.com/blog/new-whitepaper-a-practical-example-of-software-defined-security" target="_blank">A Practical Example of Software Defined Security</a>

<table align="center" cellpadding="0" cellspacing="0" style="margin-left: auto; margin-right: auto; text-align: center;">
  <tr>
    <td style="text-align: center;">
      <a href="http://blogs.msdn.com/resized-image.ashx/__size/550x0/__key/communityserver-blogs-components-weblogfiles/00-00-01-40-24/0743.chris_5F00_slane_5F00_cloud_5F00_cartoon.png" style="margin-left: auto; margin-right: auto;"><img border="0" src="http://blogs.msdn.com/resized-image.ashx/__size/550x0/__key/communityserver-blogs-components-weblogfiles/00-00-01-40-24/0743.chris_5F00_slane_5F00_cloud_5F00_cartoon.png" height="419" width="640" /></a>
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      <ul style="background-color: white; color: #333333; font-family: 'Segoe UI', Verdana, Geneva, sans-serif; font-size: small; list-style: none outside none; margin: 0px; padding: 3px 0px; text-align: center;">
        <li style="display: inline; font-size: 11px; margin: 0px; padding: 0px;">
          © 2014 Microsoft Corporation
        </li>
      </ul>
    </td>
  </tr>
</table>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_304">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F05%2F%25d0%25b4%25d0%25b5%25d1%2582%25d1%2581%25d0%25ba%25d0%25b8%25d0%25b5-%25d1%2581%25d1%2582%25d1%2580%25d0%25b0%25d1%2585%25d0%25b8-%25d1%2583%25d0%25ba%25d1%2580%25d0%25b0%25d0%25b8%25d0%25bd%25d1%2581%25d0%25ba%25d0%25b8%25d1%2585-%25d0%25b0%25d0%25b9%25d1%2582%25d0%25b8%25d1%2588%25d0%25bd%25d0%25b8%25d0%25ba%25d0%25be%2F&linkname=%D0%94%D0%B5%D1%82%D1%81%D0%BA%D0%B8%D0%B5%20%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%B8%20%D1%83%D0%BA%D1%80%D0%B0%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D1%85%20%D0%B0%D0%B9%D1%82%D0%B8%D1%88%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F05%2F%25d0%25b4%25d0%25b5%25d1%2582%25d1%2581%25d0%25ba%25d0%25b8%25d0%25b5-%25d1%2581%25d1%2582%25d1%2580%25d0%25b0%25d1%2585%25d0%25b8-%25d1%2583%25d0%25ba%25d1%2580%25d0%25b0%25d0%25b8%25d0%25bd%25d1%2581%25d0%25ba%25d0%25b8%25d1%2585-%25d0%25b0%25d0%25b9%25d1%2582%25d0%25b8%25d1%2588%25d0%25bd%25d0%25b8%25d0%25ba%25d0%25be%2F&linkname=%D0%94%D0%B5%D1%82%D1%81%D0%BA%D0%B8%D0%B5%20%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%B8%20%D1%83%D0%BA%D1%80%D0%B0%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D1%85%20%D0%B0%D0%B9%D1%82%D0%B8%D1%88%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F05%2F%25d0%25b4%25d0%25b5%25d1%2582%25d1%2581%25d0%25ba%25d0%25b8%25d0%25b5-%25d1%2581%25d1%2582%25d1%2580%25d0%25b0%25d1%2585%25d0%25b8-%25d1%2583%25d0%25ba%25d1%2580%25d0%25b0%25d0%25b8%25d0%25bd%25d1%2581%25d0%25ba%25d0%25b8%25d1%2585-%25d0%25b0%25d0%25b9%25d1%2582%25d0%25b8%25d1%2588%25d0%25bd%25d0%25b8%25d0%25ba%25d0%25be%2F&linkname=%D0%94%D0%B5%D1%82%D1%81%D0%BA%D0%B8%D0%B5%20%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%B8%20%D1%83%D0%BA%D1%80%D0%B0%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D1%85%20%D0%B0%D0%B9%D1%82%D0%B8%D1%88%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2014%2F05%2F%25d0%25b4%25d0%25b5%25d1%2582%25d1%2581%25d0%25ba%25d0%25b8%25d0%25b5-%25d1%2581%25d1%2582%25d1%2580%25d0%25b0%25d1%2585%25d0%25b8-%25d1%2583%25d0%25ba%25d1%2580%25d0%25b0%25d0%25b8%25d0%25bd%25d1%2581%25d0%25ba%25d0%25b8%25d1%2585-%25d0%25b0%25d0%25b9%25d1%2582%25d0%25b8%25d1%2588%25d0%25bd%25d0%25b8%25d0%25ba%25d0%25be%2F&linkname=%D0%94%D0%B5%D1%82%D1%81%D0%BA%D0%B8%D0%B5%20%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%B8%20%D1%83%D0%BA%D1%80%D0%B0%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D1%85%20%D0%B0%D0%B9%D1%82%D0%B8%D1%88%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
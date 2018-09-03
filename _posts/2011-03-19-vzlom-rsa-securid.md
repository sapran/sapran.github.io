---
id: 989
title: Взлом RSA SecurID
date: 2011-03-19T16:05:00+00:00
author: sapran
layout: post
guid: http://styran.com/2011/03/19/%d0%b2%d0%b7%d0%bb%d0%be%d0%bc-rsa-securid/
permalink: /2011/03/%d0%b2%d0%b7%d0%bb%d0%be%d0%bc-rsa-securid/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2011/03/rsa-securid.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/36802886142013401
shorturl:
  - http://tinyurl.com/nwo3wfg
tags:
  - apt
  - rsa
  - инциденты
---
<div style="text-align: justify;">
  Все уже наверняка слышали, что 17 марта легендарная компания <b>RSA</b>, основанная патриархами индустрии ИТ-безопасности и производящая передовые криптографические технологии, <s>подверглась вероломному нападению</s> испытала на себе неукротимую мощь <b>APT</b>. Для непосвященных, APT расшифровывается как <b>Advanced Persistent Threat</b>, и обычно означает, что <s>взлом осуществлялся из Китая, но прямых доказательств этому пока нет</s> атака была целенаправленной, хорошо финансировалась и выполнялась мастерами своего дела.
</div>

<div>
</div>

<div style="text-align: justify;">
  Принимая во внимание отсутствие подробностей инцидента (известно лишь, что целью атакующих был продукт <b>SecurID</b>, один из признанных лидеров в области двухфакторной аутентификации пользователей), любые комментарии на эту тему являются спекуляцией. Активность конкурентов и прочих игроков на рынке безопасности выглядят не иначе, как попытки пнуть лежачего (как это сделала NSS Labs в своей <a href="http://www.nsslabs.com/research/analytical-brief-rsa-breach.html">аналитической записке</a>, порекомендовав клиентам, в том числе, рассмотреть альтернативные решения по двухфакторной аутентификации).
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Тем временем RSA <a href="http://www.rsa.com/node.aspx?id=3872">сделала публичное заявление</a>, <a href="http://www.sec.gov/Archives/edgar/data/790070/000119312511070159/dex992.htm">проинструктировала заказчиков</a> и затаилась в ожидании проявления последствий инцидента. (Не могу не отметить один из пунктов заявления: рекомендацию клиентам усилить парольную политику. Ирония состоит в том, что клиенты зачастую внедряют SecurID как раз для того, чтобы не париться со строгой парольной политикой.) По мере прочтения <a href="http://www.sec.gov/Archives/edgar/data/790070/000119312511070159/dex992.htm">рекомендаций</a>, между строк очень отчетливо просматривается и как ломали (<i>We recommend customers increase their focus on security for social media applications&#8230;</i>), и какого рода уязвимости использовали (<i>We recommend customers re-educate employees on the importance of avoiding suspicious emails&#8230;</i> <i>We recommend customers follow the rule of least privilege&#8230; etc.</i>) Но утверждать что-то наверняка все-таки нельзя: все рекомендации носят очень общий характер. RSA ограничилась намеками. В такой ситуации сложно ожидать от вендора большего.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Что нас ждет в будущем, можно только догадываться. Возможно, у SecurID очень скоро появится конкурент, производимый в Юго-восточной Азии. Вероятно, данные, полученные в результате атаки, будут использованы в масштабном нападении на одного или группу клиентов RSA, а их миллионы, причем компании со скромным бюджетом такие вещи не покупают. В настоящий момент все, что мы имеем, это подтверждения тезиса, что защититься от целенаправленной хорошо финансируемой атаки практически невозможно.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_152">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F03%2F%25d0%25b2%25d0%25b7%25d0%25bb%25d0%25be%25d0%25bc-rsa-securid%2F&linkname=%D0%92%D0%B7%D0%BB%D0%BE%D0%BC%20RSA%20SecurID" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F03%2F%25d0%25b2%25d0%25b7%25d0%25bb%25d0%25be%25d0%25bc-rsa-securid%2F&linkname=%D0%92%D0%B7%D0%BB%D0%BE%D0%BC%20RSA%20SecurID" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F03%2F%25d0%25b2%25d0%25b7%25d0%25bb%25d0%25be%25d0%25bc-rsa-securid%2F&linkname=%D0%92%D0%B7%D0%BB%D0%BE%D0%BC%20RSA%20SecurID" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F03%2F%25d0%25b2%25d0%25b7%25d0%25bb%25d0%25be%25d0%25bc-rsa-securid%2F&linkname=%D0%92%D0%B7%D0%BB%D0%BE%D0%BC%20RSA%20SecurID" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
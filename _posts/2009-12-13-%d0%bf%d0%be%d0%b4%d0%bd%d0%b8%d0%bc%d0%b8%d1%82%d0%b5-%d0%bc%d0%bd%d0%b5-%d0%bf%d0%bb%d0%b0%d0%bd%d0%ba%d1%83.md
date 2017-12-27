---
id: 1069
title: 'Поднимите мне&#8230; планку'
date: 2009-12-13T20:53:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/12/13/%d0%bf%d0%be%d0%b4%d0%bd%d0%b8%d0%bc%d0%b8%d1%82%d0%b5-%d0%bc%d0%bd%d0%b5-%d0%bf%d0%bb%d0%b0%d0%bd%d0%ba%d1%83/
permalink: /2009/12/%d0%bf%d0%be%d0%b4%d0%bd%d0%b8%d0%bc%d0%b8%d1%82%d0%b5-%d0%bc%d0%bd%d0%b5-%d0%bf%d0%bb%d0%b0%d0%bd%d0%ba%d1%83/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/12/blog-post_13.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4019900900767263509
shorturl:
  - http://tinyurl.com/o578dss
tags:
  - управление рисками
---
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Еще об одном распространенном недоразумении между безопасниками и айтишниками.</span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"><br /></span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Абсолютной безопасности не существует. Возьмите сервер, поместите его в экранирующий кожух, установите на него </span></span>[<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Trusted Solaris</span></span>](http://www.sun.com/software/solaris/trustedsolaris/index.xml)<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">, отключите его от сети, залейте все интерфейсные порты эпоксидкой. После этого погрузите его на корабль, отвезите на Филиппины и сбросьте в Марианскую впадину. По достижении дна ваш сервер будет в безопасности на 99,98%.</span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"><br /></span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Вместо того, чтобы стремиться к платоническому идеалу абсолютно безопасной системы, опытные специалисты руководствуются следующим принципом управления рисками. Прежде всего, для системы (здесь, прежде и далее &#171;система&#187; &#8212; это некий абстрактный объект защиты) определяется текущий уровень риска. Допустим, что после учета всех возможных угроз и вероятностей их актуализации,&nbsp;среднегодовой риск&nbsp;составляет 80%. Это означает, что если &#171;ничего не трогать, все и так работает&#187; (с), то система будет скомпрометирована с вот такой вот вероятностью &#8212; ежегодно. Затем вычисляется допустимый уровень риска. Допустим, что в нашем примере допустимый среднегодовой риск равен 20%. То есть, теоретически, для владельца системы допустимо, что ее будут взламывать раз в пять лет. На практике это может означать то, что систему не планируют использовать так долго.</span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"><br /></span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Для достижения допустимого уровня риска, специалисту по безопасности нужно понизить риск с отметки 80% до отметки 20%. Сделать это можно внедряя т.н. контроли или средства обеспечения безопасности. Допустим, что в силах специалиста понизить риск следующими контролями:</span></span>

  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">сегментировать сеть и&nbsp;установить межсетевой экран (-15%),</span></span>
  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">развернуть систему предотвращения вторжений (-20%),</span></span>
  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">установить антивирус (-5%),</span></span>
  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">обучить пользователей системы основам ИБ (-10%),</span></span>
  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">автоматизировать анализ логов системы с целью раннего обнаружения попыток взлома (-15%),</span></span>
  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">и т.д., и т.п.</span></span>

<div>
  <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Исходя из стоимости внедрения средств защиты, из их числа выбирают несколько контролей, которые в сумме понижают риск до допустимого уровня. Этот процесс имеет зеркальное отображение: чем ниже опускается уровень риска, тем выше поднимается &#171;планка&#187; стоимости удачной атаки. Чем больше прикладывается усилий для защиты системы, тем больше требуется ресурсов для их преодоления. В итоге, взламывать систему становится экономически не выгодно для большинства потенциальных желающих. А меньшинство&#8230; на меньшинство мы как раз и оставили те 20% допустимого риска.</span></span>
</div>

<div>
  <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"><br /></span></span>
</div>

<div>
  <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Итак, работа специалиста по ИБ состоит в поднятии планки на&nbsp;приемлемую&nbsp;высоту.&nbsp;Тем не менее, не редки споры, в ходе которых в ответ на предложение внедрить тот или иной контроль, раздается нечто вроде: &#171;-Зачем, достаточно мотивированный атакующий все равно преодолеет этот барьер&#187; или &#171;-Администратора системы это все равно не остановит&#187;. На лицо полное непонимание цели внедрения контролей и принципов защиты в целом. Контраргументы в таком случае могут быть следующими: Сколько нам будет стоить внедрение контроля? Ничего не будет стоить, только немного повозиться придется&#8230; А риск при этом хоть немного понизится? Ах, не немного, а даже существенно&#8230; Ну тогда &#171;давайте сделаем это&#187; (с).</span></span>
</div>

<div>
  <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"><br /></span></span>
</div>

<div>
  <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Тот факт, что после всех усилий, вероятность&nbsp;компрометации&nbsp;системы не исчезнет, не означает, что мы не должны стараться свести ее к минимуму.</span></span>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_72">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25bf%25d0%25be%25d0%25b4%25d0%25bd%25d0%25b8%25d0%25bc%25d0%25b8%25d1%2582%25d0%25b5-%25d0%25bc%25d0%25bd%25d0%25b5-%25d0%25bf%25d0%25bb%25d0%25b0%25d0%25bd%25d0%25ba%25d1%2583%2F&linkname=%D0%9F%D0%BE%D0%B4%D0%BD%D0%B8%D0%BC%D0%B8%D1%82%D0%B5%20%D0%BC%D0%BD%D0%B5%E2%80%A6%20%D0%BF%D0%BB%D0%B0%D0%BD%D0%BA%D1%83" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25bf%25d0%25be%25d0%25b4%25d0%25bd%25d0%25b8%25d0%25bc%25d0%25b8%25d1%2582%25d0%25b5-%25d0%25bc%25d0%25bd%25d0%25b5-%25d0%25bf%25d0%25bb%25d0%25b0%25d0%25bd%25d0%25ba%25d1%2583%2F&linkname=%D0%9F%D0%BE%D0%B4%D0%BD%D0%B8%D0%BC%D0%B8%D1%82%D0%B5%20%D0%BC%D0%BD%D0%B5%E2%80%A6%20%D0%BF%D0%BB%D0%B0%D0%BD%D0%BA%D1%83" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25bf%25d0%25be%25d0%25b4%25d0%25bd%25d0%25b8%25d0%25bc%25d0%25b8%25d1%2582%25d0%25b5-%25d0%25bc%25d0%25bd%25d0%25b5-%25d0%25bf%25d0%25bb%25d0%25b0%25d0%25bd%25d0%25ba%25d1%2583%2F&linkname=%D0%9F%D0%BE%D0%B4%D0%BD%D0%B8%D0%BC%D0%B8%D1%82%D0%B5%20%D0%BC%D0%BD%D0%B5%E2%80%A6%20%D0%BF%D0%BB%D0%B0%D0%BD%D0%BA%D1%83" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25bf%25d0%25be%25d0%25b4%25d0%25bd%25d0%25b8%25d0%25bc%25d0%25b8%25d1%2582%25d0%25b5-%25d0%25bc%25d0%25bd%25d0%25b5-%25d0%25bf%25d0%25bb%25d0%25b0%25d0%25bd%25d0%25ba%25d1%2583%2F&linkname=%D0%9F%D0%BE%D0%B4%D0%BD%D0%B8%D0%BC%D0%B8%D1%82%D0%B5%20%D0%BC%D0%BD%D0%B5%E2%80%A6%20%D0%BF%D0%BB%D0%B0%D0%BD%D0%BA%D1%83" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
---
id: 1052
title: Управление обновлениями (Patch Management)
date: 2010-02-15T19:48:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/02/15/%d1%83%d0%bf%d1%80%d0%b0%d0%b2%d0%bb%d0%b5%d0%bd%d0%b8%d0%b5-%d0%be%d0%b1%d0%bd%d0%be%d0%b2%d0%bb%d0%b5%d0%bd%d0%b8%d1%8f%d0%bc%d0%b8-patch-management/
permalink: /2010/02/%d1%83%d0%bf%d1%80%d0%b0%d0%b2%d0%bb%d0%b5%d0%bd%d0%b8%d0%b5-%d0%be%d0%b1%d0%bd%d0%be%d0%b2%d0%bb%d0%b5%d0%bd%d0%b8%d1%8f%d0%bc%d0%b8-patch-management/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/02/patch-management.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4279480758162149900
shorturl:
  - http://tinyurl.com/o84hkw8
tags:
  - bsod
  - easy button
  - mbsa
  - microsoft
  - управление обновлениями
---
В начале века, после нескольких ошибок, совершенных компанией Майкрософт в ходе первых попыток наладить систему&nbsp;обновлений&nbsp;ОС Windows, в умах миллионов ИТ-специалистов закрепился один очень опасный&nbsp;стереотип. Дело было примерно так: молодой и неотесанный Майкрософт выдал на гора несколько патчей, которые предварительно, чего уж греха таить, не очень усердно протестировал. В результате, сотни тысяч серверов и ПК по всему миру получили обновления, которые, при взаимодействии с существующими до их установки программами и настройками, привели операционные системы к полному краху. Из этого неприятного эпизода ИТ-специалисты сделали совершенно неправильный вывод. Вместо того, чтобы в дальнейшем тщательно тестировать обновления перед их установкой в продуктивной среде, они решили (где там наш **easy button**?..) отказаться от установки обновлений вообще. Этот глубокомысленное умозаключение ярко проиллюстрировано в&nbsp;старом анекдоте про Билла Гейтса, его сына и ежедневное путешествие солнца с востока на запад: **&#171;Пока все работает, ничего не трогай.&#187;** Оно настолько широко присуще ИТ-специалистам старой закалки, что я даже не постесняюсь добавить его в категорию **&#171;****[ctrl+shift](http://securegalaxy.blogspot.com/2009/05/ctrlshift.html)&#171;.**

Проблема заключается в том, что злоумышленнику, интернет-червю, вирусу и прочей нечисти именно это и нужно: по-больше уязвимостей в операционных системах и программном обеспечении. Я не удивился бы, если бы стало известно, что&nbsp;киберпреступники&nbsp;в какой-то мере поучаствовали в распространении и закреплении этого ущербного стереотипа. Уж слишком глубоко он засел в умах непосвященных айтишников.

К сожалению, самый распространенный путь ИТ-специалиста на светлую сторону лежит через возникновение инцидента. Ярким примером тому служит недавнее триумфальное шествие [Conficker](http://en.wikipedia.org/wiki/Conficker)&#8216;а. Казалось бы, установите вы везде обновления безопасности (хотите &#8212; протестируйте их предварительно, хоть в лаборатории, а хоть и на фокусной группе компьютеров) и спите себе спокойно. Ан-нет, **все же работало**, чего его трогать, &#8212; вот и дождались эпидемии. В общем, пока гром не грянет, мужик не перекрестится.

Вот и после последнего &#171;вторника обновлений&#187; (&#171;Patch Tuesday&#187;) по рядам сисадминов пронесся недобрый шепот. Видите, мол, что ваш [**MS10-015**](http://www.microsoft.com/technet/security/bulletin/MS10-015.mspx) натворил, мы же вас предупреждали&#8230; Все же работало! Что случилось на самом деле, и почему многие компьютеры отвечали на установку обновления отчаянным [Blue Screen of Death](http://securegalaxy.blogspot.com/search/label/bsod), пока точно не известно. Но по последним данным, Майкрософт [не исключает](http://www.theregister.co.uk/2010/02/15/rootkit_blue_screen_culprit_probably/), что такой результат стал следствием несовместимости обновления с якобы установленным в операционной системе руткитом (rootkit). Если это правда, представляете каким ударом для противников обновлений безопасности это может стать?

Итого, каковы **позитивные выводы**.&nbsp;Не обновляемая система намного более уязвима к атакам. То есть, обновляться нужно. Запятая. Если опасаетесь негативных последствий применения обновлений &#8212; тестируйте их на тестовых ОС перед установкой в продуктивную среду.&nbsp;Точка.

Теперь о том, как организовать процесс ****тестирования и установки обновлений. Для&nbsp;тестирования очень удобно использовать операционные системы, установленные на виртуальных машинах: благо, [VMWare Server](http://www.vmware.com/products/server/landing.html) бесплатен и потрясающе прост в использовании. Также, стоит отметить, что не все обновления ОС являются обновлениями безопасности. В принципе, какие обновления к чему относятся можно посмотреть в коротком описании к каждому патчу,&nbsp;предлагаемом к установке при помощи [Microsoft Update](http://www.update.microsoft.com/). С другой стороны, эти описания малоинформативны и не содержат никакой классификации (&#171;Low&#187;, &#171;Medium&#187;, &#171;High&#187;). Для установки обновлений в &#171;ручном&#187; режиме, Майкрософт предлагает утилиту [Microsoft Baseline Security Analyzer](http://www.microsoft.com/downloads/details.aspx?FamilyID=b1e76bbe-71df-41e8-8b52-c871d012ba78&displaylang=en), о которой я уже неоднократно [писал в этом блоге](http://securegalaxy.blogspot.com/search/label/mbsa). В отличие от Microsoft Update, MBSA ранжирует обновления безопасности в зависимости от критичности той уязвимости, которую это обновление исправляет.

Собственно, **процесс можно организовать следующим образом**. Майкрософт выпускает обновления периодически, во второй вторник каждого месяца. Исключения составляют экстренные обновления для очень серьезных&nbsp;критичных&nbsp;уязвимостей. Отталкиваясь от этого графика, компания может сформировать свое собственное расписание применения обновлений безопасности. Скажем,

  * уязвимости &#171;высокой&#187; критичности должны быть&nbsp;исправлены&nbsp;в течение 5 дней,
  * &#171;средне&#187;-критичные &#8212; не позднее двух недель,&nbsp;с момента выхода обновления,
  * а уязвимости &#171;низкой&#187; критичности могут подождать месяц.

<div>
  Естественно, цифры могут меняться от компании к компании, но я думаю, что общий смысл понятен. В&nbsp;указанный&nbsp;период времени обновление должно быть проверено в тестовом окружении, по возможности в&nbsp;условиях, максимально приближенных к продуктиву, &#8212; то есть в комбинации с ПО третьих поставщиков, установленном в ОС.
</div>

<div>
</div>

<div>
  Разумеется, все изложенное выше применимо к любому вендору, а не только к компании Майкрософт. И помните: правильно налаженный процесс применения обновлений безопасности значительно сокращает количество уязвимостей и переводит&nbsp;систему информационной безопасности&nbsp;компании на следующий уровень зрелости.</p> 
  
  <p>
    <b>[19.02.2010] Update </b>Спустя неделю после обнаружения проблемы, в Майкрософт подтвердили, что BSoD после установки MS10-015 вызван присутствием в системе вредоносного ПО&nbsp;Win32/Alureon. Детали:&nbsp;<a href="http://news.cnet.com/8301-27080_3-10456162-245.html?part=rss&tag=feed&subj=News-Security">http://news.cnet.com/8301&#8230;</a>&nbsp;<a href="http://blogs.technet.com/msrc/archive/2010/02/17/update-restart-issues-after-installing-ms10-015-and-the-alureon-rootkit.aspx">http://blogs.technet.com/msrc&#8230;</a></div> 
    
    <div class="addtoany_share_save_container addtoany_content_bottom">
      <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_89">
        <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F02%2F%25d1%2583%25d0%25bf%25d1%2580%25d0%25b0%25d0%25b2%25d0%25bb%25d0%25b5%25d0%25bd%25d0%25b8%25d0%25b5-%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b2%25d0%25bb%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f%25d0%25bc%25d0%25b8-patch-management%2F&linkname=%D0%A3%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F%D0%BC%D0%B8%20%28Patch%20Management%29" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F02%2F%25d1%2583%25d0%25bf%25d1%2580%25d0%25b0%25d0%25b2%25d0%25bb%25d0%25b5%25d0%25bd%25d0%25b8%25d0%25b5-%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b2%25d0%25bb%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f%25d0%25bc%25d0%25b8-patch-management%2F&linkname=%D0%A3%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F%D0%BC%D0%B8%20%28Patch%20Management%29" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F02%2F%25d1%2583%25d0%25bf%25d1%2580%25d0%25b0%25d0%25b2%25d0%25bb%25d0%25b5%25d0%25bd%25d0%25b8%25d0%25b5-%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b2%25d0%25bb%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f%25d0%25bc%25d0%25b8-patch-management%2F&linkname=%D0%A3%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F%D0%BC%D0%B8%20%28Patch%20Management%29" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F02%2F%25d1%2583%25d0%25bf%25d1%2580%25d0%25b0%25d0%25b2%25d0%25bb%25d0%25b5%25d0%25bd%25d0%25b8%25d0%25b5-%25d0%25be%25d0%25b1%25d0%25bd%25d0%25be%25d0%25b2%25d0%25bb%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f%25d0%25bc%25d0%25b8-patch-management%2F&linkname=%D0%A3%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F%D0%BC%D0%B8%20%28Patch%20Management%29" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
      </div>
    </div>
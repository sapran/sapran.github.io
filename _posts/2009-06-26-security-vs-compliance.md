---
id: 1116
title: Security vs Compliance
date: 2009-06-26T08:39:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/06/26/security-vs-compliance/
permalink: /2009/06/security-vs-compliance/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/06/security-vs-compliance.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1032289287707984801
shorturl:
  - http://tinyurl.com/p9ahmp5
tags:
  - iso27000
  - pci:dss
  - sox
  - бумажные тигры
---
<div style="text-align: justify;">
  В последнее время все большую популярность приобретают всевозможные стандарты в сфере информационной безопасности. Наиболее популярными в нашей стране являются:
</div>

<li style="text-align: justify;">
  <a href="http://pcidss.ru/faq/">PSI:DSS</a>, диктуемый &#171;большой четверкой&#187; пластиковых карт (AmEx, Maestro, Mastercard, Visa) &#8212; это индустриальный стандарт;
</li>
<li style="text-align: justify;">
  серия стандартов <a href="http://www.27000.org/">ISO/IEC 27000</a>, разработанная институтом ISO на основе и BS7799 &#8212; это т.н. &#171;лучшие практики&#187; в сфере ИБ;
</li>
<li style="text-align: justify;">
  Всяческие законы и постановления, большинство которых морально устарели: Законы об информации, ее конфиденциальности, ЭЦП, всяческие постановления НБУ и т.п. &#8212; это правовые регулирующие механизмы;
</li>
<li style="text-align: justify;">
  Вопросам ИБ также уделяют некоторое внимание общеайтишные <a href="http://ru.wikipedia.org/wiki/Cobit">CobiT</a>&nbsp;и <a href="http://ru.wikipedia.org/wiki/ITIL">ITIL</a>.
</li>

<div style="text-align: justify;">
  Отчего возникает подобная активность? Причин несколько.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Во-первых, иностранные инвесторы все чаще требуют от своих украинских &#171;дочек&#187; выполнения тех обязательств, которые взяла на себя родительская компания. Особенно когда в дочернее предприятие мигрируют процессы по обслуживанию VIP-клиентов.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Во-вторых, соответствие индустриальным стандартам &#8212; это неплохое подспорье в бизнесе. Безопасность должна приносить прибыль, иначе ее очень трудно будет поддерживать. А формально подтвержденный статус компании, соответствующей, скажем, ISO27001, &#8212; это хорошее средство капитализации. Для клиентов сертификат от ISO &#8212; прекрасное доказательство зрелости системы управления ИБ компании. А это для поставщика услуг или аутсорсера, участвующего в тендере, неоценимый плюс. PCI:DSS в свою очередь необходим для самоего участия в обработке карточных транзакций, иначе вашему бизнесу грозят штрафы, тяжбы, отказ в процессинге и т.п.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  В-третьих, для подтверждения корректности финансовых отчетов в компаниях, активно использующих ИТ-системы<span style="font-weight: bold;"> </span>для их составления, существуют целые своды контролей целостности данных при передаче из одной системы в другую, адекватности отчетов исходным данным и т.д. В основном у нас это коснулось мобильных операторов, так как в связке &#171;Биллинг->ERP->Финансовый отчет&#187; обрабатывается просто колоссальные объемы данных. На вооружение в этой связи взят <a href="http://en.wikipedia.org/wiki/Sarbanes-Oxley_Act">SOX</a>, который у себя на родине в Штатах является важнейшим компонентом успешного выхода на <a href="http://en.wikipedia.org/wiki/IPO">IPO</a>. То есть, у нас это боле индустриальный стандарт, хотя он задумывался создателями как самый настоящий закон.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  К сожалению, роль соответствия стандартам в сфере ИБ нередко переоценивают и путают с собственно информационной безопасностью. К сожалению, эта точка зрения активно поддерживается ведущими аудиторами и консультантами. Такой подход среди специалистов называется использованием &#171;бумажных тигров&#187; для защиты информации. Бизнес настаивает на том, что сертификат с печатью PCI защищает его от утечки информации и остановки операций. Масштабы заблуждения общественности в этой связи достигли невообразимых масштабов. Посему считаю своим долгом высказаться на эту тему.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Соответствие и безопасность не одно и то же. Между ними, по сути, нет никакой логической связи. Первое вполне возможно в отсутствие второго и наоборот. То есть, корректно заполненный чек-лист аудита PCI:DSS не может спасти компанию от утечки информации (<a href="http://www.networkworld.com/news/2007/011807-tjx-computer-hack.html">TJX</a> и <a href="http://www.computerworld.com/action/article.do?command=viewArticleBasic&articleId=9126379">HeartLand</a> успешно это про<span style="font-weight: bold;">демон</span>стрировали). А здоровая, зрелая и безопасная ИТ-инфраструктура может обойтись и без всяческих стандартов &#8212; особенно, если ее клиенты способны самостоятельно оценить состояние дел, а не равняются на заключение внешнего аудитора.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  То есть, если компания сертифицирована по ISO27001, это значит только то, что в ней реализована СУИБ, удовлетворяющая требованиям этого стандарта, и компонентами которой являются 109 (вроде) контролей из коллекции ISO27002. Точка. Если после ухода аудиторов вы пригласите продвинутую команду <a href="http://en.wikipedia.org/wiki/Penetration_testing">пентестеров</a> и они проведут полный спектр мероприятий (сканирование и эксплуатация уязвимостей, атаки с использованием инсайдеров, взлом замков, социальную инженерию с использованием НЛП и т.д., и т.п.) то скорее всего &#171;бумажные тигры&#187; их не остановят. Но это не значит, что аудит бесполезен, &#8212; это значит, что его не достаточно.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  И соответствие, и безопасность компании необходимы. Но не следует их путать, нужно поддерживать и то, и другое. Постройте успешную СУИБ, ориентируясь на потребности бизнеса (т.е. результаты анализа рисков) и хорошие практики безопасной архитектуры и настройки ИТ-систем. Благо, источников такой информации немало &#8212; <a href="http://www.sans.org/">SANS</a>, <a href="http://www.cisecurity.org/">CIS</a>, <a href="http://eff.org/">EFF</a>&#8230; Тысячи светлых умов только того и ждут, чтобы кто-то воспользовался результатами их работы.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Когда закончите, то есть построите СУИБ и начнете ее сопровождать, возьмитесь за приведение процессов и документации в соответствие выбранному стандарту. Это поможет усилить административную и физическую грани безопасности. После этого приглашайте аудиторов и наслаждайтесь зрелищем.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Поселите &#171;бумажных тигров&#187; за &#171;огненными стенами&#187;, пусть трудятся сообща.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_25">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F06%2Fsecurity-vs-compliance%2F&linkname=Security%20vs%20Compliance" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F06%2Fsecurity-vs-compliance%2F&linkname=Security%20vs%20Compliance" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F06%2Fsecurity-vs-compliance%2F&linkname=Security%20vs%20Compliance" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F06%2Fsecurity-vs-compliance%2F&linkname=Security%20vs%20Compliance" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
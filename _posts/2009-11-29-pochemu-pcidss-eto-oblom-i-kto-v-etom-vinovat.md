---
id: 1073
title: 'Почему PCI:DSS &#8212; это облом, и кто в этом виноват'
date: 2009-11-29T14:57:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/11/29/%d0%bf%d0%be%d1%87%d0%b5%d0%bc%d1%83-pcidss-%d1%8d%d1%82%d0%be-%d0%be%d0%b1%d0%bb%d0%be%d0%bc-%d0%b8-%d0%ba%d1%82%d0%be-%d0%b2-%d1%8d%d1%82%d0%be%d0%bc-%d0%b2%d0%b8%d0%bd%d0%be%d0%b2%d0%b0%d1%82/
permalink: /2009/11/%d0%bf%d0%be%d1%87%d0%b5%d0%bc%d1%83-pcidss-%d1%8d%d1%82%d0%be-%d0%be%d0%b1%d0%bb%d0%be%d0%bc-%d0%b8-%d0%ba%d1%82%d0%be-%d0%b2-%d1%8d%d1%82%d0%be%d0%bc-%d0%b2%d0%b8%d0%bd%d0%be%d0%b2%d0%b0%d1%82/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/11/payment-card-industry-data-security.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/714029650832893312
shorturl:
  - http://tinyurl.com/oy56nqs
tags:
  - dumb asses
  - pci:dss
  - sox
  - аудит
  - банки
  - бумажные тигры
  - менеджеры
---
<div dir="ltr" style="text-align: left;">
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><b><a href="https://www.pcisecuritystandards.org/security_standards/pci_dss.shtml">Payment Card Industry Data Security Standard</a></b> был разработан <b><a href="https://www.pcisecuritystandards.org/">PCI Security Standards Council</a></b> и является набором рекомендаций и &#171;лучших практик&#187; по обеспечению безопасности информации о платежных картах (номер, дата истечения, данные о владельце, параметры магнитной полоски и т.д.). Любой бизнес, так или иначе занимающийся обработкой платежных карт,<b> &#171;обязан&#187;</b> следовать этому стандарту в той части своей ИТ-инфраструктуры, которая непосредственно задействована в обработке подобной информации. Это значит, что под требования стандарта подпадают только те сетевые сегменты и ИТ-системы, которые хранят, обрабатывают или передают информацию о пластиковых картах. Слово &#171;обязан&#187; заключено в кавычки потому, что PCI:DSS является т.н. индустриальным стандартом и его несоблюдение не преследуется по закону (пока).</span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><br /></span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;">Противоречивость PCI:DSS состоит в том, что не смотря на целесообразность его требований, некоторые громкие кражи информации о платежных картах в последние годы были совершены как раз в компаниях, имеющих статус соответствия этому стандарту. Причины этого, на первый взгляд, недоразумения могут показаться неявными или даже мистическими. Первое что приходит обычно в голову: наши сертифицированные аудиторы (aka Qualified Security Assessors) нас обманули. У некоторых жертв кардеров были даже порывы судиться с QSA, но на моей памяти дальше эмоциональных заявлений дело не шло, видать обломалось что-то&#8230; Но не суть. В этом посте я хочу поделиться своими соображениями на тему почему PCI:DSS это полный облом и кто в этом виноват.</span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><br /></span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><b>Первая причина</b> &#8212; это традиционное отношение бизнеса к ИБ. С точки зрение менеджмента, безопасность бизнесу не только не помогает, а зачастую даже вредит. Бизнес на подъеме не хочет безопасности, потому что она затормозит его бурное развитие. Бизнес на спаде не хочет безопасности, потому что&#8230; да потому что денег нет <b>вообще</b>, а не то, что на вашу безопасность. Единственное, что нужно бизнесу &#8212; это тот business enabler, который дает соответствие тем или иным стандартам в области ИБ. Например, соответствие SOX позволяет размещать акции на бирже, а соответствие PCI:DSS &#8212; принимать платежи через электронные платежные системы. То есть, все что по сути нужно бизнесу &#8212; это заключение внешнего аудитора о его (бизнеса) соответствии стандарту. Красивые галочки в симпатичном чек-листе. К сожалению, для безопасности этого мало.</span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><br /></span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><b>Вторая причина</b> &#8212; это отношение к безопасности как <b>проекту</b>, а не как к <b>процессу</b>. <b>Проект это нечто разовое</b>, после завершения которого бизнес становится сертифицированным и может забыть о безопасности до следующего периодического аудита. А за пару недель до этого аудита админы немного понервничают, все прилижут и будут готовы в &#171;внезапному&#187; визиту, после которого &#8212; еще пол года спокойной и радостной жизни. <b>Процесс </b>же &#8212; это непрерывное поддержание инфраструктуры в &#171;боевом&#187; состоянии. В этой форме безопасность максимально эффективна, а визит внешнего аудитора превращается в сущую формальность. К сожалению, зачастую бизнес все еще мыслит категориями проектов, а не процессов. Согласитесь, нам это очень свойственно: срубить бабла по-бырику, а потом хоть трава не расти.</span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><br /></span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><b>Третья причина</b> &#8212; неправильное трактование самого стандарта. PCI:DSS &#8212; это описание тех процессов, выполняя которые компания будет хранить и обрабатывать клиентские данные в сравнительной безопасности. Описание на достаточно высоком уровне, без глубокой детализации. К сожалению, такой подход порождает полную неразбериху в головах менеджеров. Руководство ориентируется не на проблемы, а на решения; ищет панацею и решительно шагает дальше. <b>Давайте купим файерволл </b>(с), установим антивирус, зашифруем диски на лаптопах и окажемся в безопасности. Как, этого мало? Да вам, ребята, не угодить&#8230;</span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><br /></span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;">Менеджеры &#8212; это еще только пол беды. Вторая половина &#8212; это некомпетентные кадры в сфере ИТ и ИБ, либо же их отсутствие. Маленькой компании, принимающей к оплате пластиковые карты, отдельное подразделение, занимающееся ИБ, просто не по карману. В большой же корпорации, в силу необразованности высшего руководства в вопросах информационной безопасности, а так же по причине дефицита квалифицированного персонала, возникает риск &#171;воцарения&#187; в компании ложного ощущения безопасности. Казлось бы и служба ИБ есть, и люди там работают вроде бы неглупые, а в итоге бюджет на ИБ уходит на &#171;решения&#187; несуществующих проблем. При этом актуальные проблемы остаются нерешенными, а для возникающих факапов всегда находятся объяснения типа &#171;у нас мало людей&#187;, &#171;у нас мало денег&#187; и т.п. Как вы думаете, такие люди способны реализовать прогрессивные веяния PCI:DSS в конкретных контролях и контр-мерах? Очень вряд ли, одна надежда на то, что продавец-интегратор порекомендует адекватное &#171;решение&#187;.</span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;"><br /></span></span>
  </div>
  
  <div style="text-align: justify;">
    <span style="font-family: Arial; font-size: small;"><span style="background-color: white; font-size: 13px;">Есть еще <b>четвертая причина</b>, она созвучна с третьей, но только шишки полетят в сторону PCI SSC. Во-первых, стандарт не безупречен. Вот вам <a href="http://superconductor.voltage.com/2009/11/its-possible-to-comply-with-the-pci-dss-yet-provide-essentially-no-protection-to-credit-card-numbers-heres-why--secti.html"><b>пример</b></a><b>, когда соблюдение требований стандарта привносит уязвимость</b>. Во-вторых, его действительно следовало сделать более приземленным и детализированным, спуститься как можно ниже по лестнице абстракции. До конкретных настроек ОС и ПО, если хотите. В таком случае следовать ему смогли бы даже самые мелкие компании. К сожалению, &#8212; это утопия, так как никому это не нужно. Существует мнение, что основной целью PCI:DSS является не защита клиентских данных, а трансфер рисков ИБ с могучих плеч VISA, Mastercard & AmEx на тощие плечики мерчантов и сервис-провайдеров. В каждой шутке, как говориться, есть доля шутки. И я не склонен полагать, что в ближайшем будущем ситуация с ИБ в бизнесе электронных платежей существенно улучшится.</span></span>
  </div>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_68">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-pcidss-%25d1%258d%25d1%2582%25d0%25be-%25d0%25be%25d0%25b1%25d0%25bb%25d0%25be%25d0%25bc-%25d0%25b8-%25d0%25ba%25d1%2582%25d0%25be-%25d0%25b2-%25d1%258d%25d1%2582%25d0%25be%25d0%25bc-%25d0%25b2%25d0%25b8%25d0%25bd%25d0%25be%25d0%25b2%25d0%25b0%25d1%2582%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20PCI%3ADSS%20%E2%80%94%20%D1%8D%D1%82%D0%BE%20%D0%BE%D0%B1%D0%BB%D0%BE%D0%BC%2C%20%D0%B8%20%D0%BA%D1%82%D0%BE%20%D0%B2%20%D1%8D%D1%82%D0%BE%D0%BC%20%D0%B2%D0%B8%D0%BD%D0%BE%D0%B2%D0%B0%D1%82" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-pcidss-%25d1%258d%25d1%2582%25d0%25be-%25d0%25be%25d0%25b1%25d0%25bb%25d0%25be%25d0%25bc-%25d0%25b8-%25d0%25ba%25d1%2582%25d0%25be-%25d0%25b2-%25d1%258d%25d1%2582%25d0%25be%25d0%25bc-%25d0%25b2%25d0%25b8%25d0%25bd%25d0%25be%25d0%25b2%25d0%25b0%25d1%2582%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20PCI%3ADSS%20%E2%80%94%20%D1%8D%D1%82%D0%BE%20%D0%BE%D0%B1%D0%BB%D0%BE%D0%BC%2C%20%D0%B8%20%D0%BA%D1%82%D0%BE%20%D0%B2%20%D1%8D%D1%82%D0%BE%D0%BC%20%D0%B2%D0%B8%D0%BD%D0%BE%D0%B2%D0%B0%D1%82" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-pcidss-%25d1%258d%25d1%2582%25d0%25be-%25d0%25be%25d0%25b1%25d0%25bb%25d0%25be%25d0%25bc-%25d0%25b8-%25d0%25ba%25d1%2582%25d0%25be-%25d0%25b2-%25d1%258d%25d1%2582%25d0%25be%25d0%25bc-%25d0%25b2%25d0%25b8%25d0%25bd%25d0%25be%25d0%25b2%25d0%25b0%25d1%2582%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20PCI%3ADSS%20%E2%80%94%20%D1%8D%D1%82%D0%BE%20%D0%BE%D0%B1%D0%BB%D0%BE%D0%BC%2C%20%D0%B8%20%D0%BA%D1%82%D0%BE%20%D0%B2%20%D1%8D%D1%82%D0%BE%D0%BC%20%D0%B2%D0%B8%D0%BD%D0%BE%D0%B2%D0%B0%D1%82" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d0%25bf%25d0%25be%25d1%2587%25d0%25b5%25d0%25bc%25d1%2583-pcidss-%25d1%258d%25d1%2582%25d0%25be-%25d0%25be%25d0%25b1%25d0%25bb%25d0%25be%25d0%25bc-%25d0%25b8-%25d0%25ba%25d1%2582%25d0%25be-%25d0%25b2-%25d1%258d%25d1%2582%25d0%25be%25d0%25bc-%25d0%25b2%25d0%25b8%25d0%25bd%25d0%25be%25d0%25b2%25d0%25b0%25d1%2582%2F&linkname=%D0%9F%D0%BE%D1%87%D0%B5%D0%BC%D1%83%20PCI%3ADSS%20%E2%80%94%20%D1%8D%D1%82%D0%BE%20%D0%BE%D0%B1%D0%BB%D0%BE%D0%BC%2C%20%D0%B8%20%D0%BA%D1%82%D0%BE%20%D0%B2%20%D1%8D%D1%82%D0%BE%D0%BC%20%D0%B2%D0%B8%D0%BD%D0%BE%D0%B2%D0%B0%D1%82" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
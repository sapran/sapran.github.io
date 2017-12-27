---
id: 1079
title: Шифрование P2P трафика
date: 2009-10-31T11:21:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/10/31/%d1%88%d0%b8%d1%84%d1%80%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d0%b5-p2p-%d1%82%d1%80%d0%b0%d1%84%d0%b8%d0%ba%d0%b0/
permalink: /2009/10/%d1%88%d0%b8%d1%84%d1%80%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d0%b5-p2p-%d1%82%d1%80%d0%b0%d1%84%d0%b8%d0%ba%d0%b0/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/10/p2p.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/5749206195068751360
shorturl:
  - http://tinyurl.com/qjejdsq
tags:
  - p2p
  - криптография
---
Предыдущий пост натолкнул на идею&nbsp;более детально&nbsp;поковыряться в информации о распределении протоколов Интернет-трафика. Хочу поделиться некоторыми фактами и&nbsp;сделанными&nbsp;обобщениями.

  * P2P-протоколы генерируют **50-70% трафика** во всех регионах, кроме Ближнего Востока и Северной Африки. Там P2P-трафика меньше, но его все равно больше, чем Web.
  * Web-трафик составляет **от 16% до 33%** в зависимости от региона.
  * В Восточной Европе эти показатели максимальны и&nbsp;минимальны&nbsp;соответственно и составляют **70% &#8212; P2P и 16% &#8212; Web**.
  * Потоковое видео/аудио покрывает всего 5-10%
  * Доля шифрованного P2P-трафика резко (по некоторым данным &#8212; в 10 раз) увеличилась в 2006-2007 годах.
  * До 2006 года шифровалось не более 15% P2P-трафика. В 2007 году шифровалось 18-20% Bittorrent.&nbsp;В 2008-2009 &nbsp;году доля шифруемого трафика выросла до 16% в eDonkey и до **22-26%** для Bittorrent.

Данные могут быть неполны, а статистика всегда врет, но выводы об общих тенденциях можно сделать и из этого. Peer-to-peer трафик увеличивается как в объеме, так и по отношению к другим средствам передачи данных. Процент шифруемого файлообменного трафика ежегодно возрастает.

**Ipoque Internet Study**  
[2006](http://www.ipoque.com/resources/internet-studies/p2p-survey-2006)&nbsp;[2007](http://www.ipoque.com/resources/internet-studies/internet-study-2007)&nbsp;[2008/2009](http://www.ipoque.com/resources/internet-studies/internet-study-2008_2009)

**The Register**&nbsp;[Surge in encrypted torrents blindsides record biz](http://www.theregister.co.uk/2007/11/08/bittorrent_encryption_explosion/) (11/2007)

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_62">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F10%2F%25d1%2588%25d0%25b8%25d1%2584%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d0%25b5-p2p-%25d1%2582%25d1%2580%25d0%25b0%25d1%2584%25d0%25b8%25d0%25ba%25d0%25b0%2F&linkname=%D0%A8%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20P2P%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F10%2F%25d1%2588%25d0%25b8%25d1%2584%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d0%25b5-p2p-%25d1%2582%25d1%2580%25d0%25b0%25d1%2584%25d0%25b8%25d0%25ba%25d0%25b0%2F&linkname=%D0%A8%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20P2P%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F10%2F%25d1%2588%25d0%25b8%25d1%2584%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d0%25b5-p2p-%25d1%2582%25d1%2580%25d0%25b0%25d1%2584%25d0%25b8%25d0%25ba%25d0%25b0%2F&linkname=%D0%A8%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20P2P%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F10%2F%25d1%2588%25d0%25b8%25d1%2584%25d1%2580%25d0%25be%25d0%25b2%25d0%25b0%25d0%25bd%25d0%25b8%25d0%25b5-p2p-%25d1%2582%25d1%2580%25d0%25b0%25d1%2584%25d0%25b8%25d0%25ba%25d0%25b0%2F&linkname=%D0%A8%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20P2P%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
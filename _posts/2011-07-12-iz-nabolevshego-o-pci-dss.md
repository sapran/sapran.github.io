---
id: 961
title: Из наболевшего о PCI DSS
date: 2011-07-12T05:33:00+00:00
author: sapran
layout: post
guid: http://styran.com/2011/07/12/%d0%b8%d0%b7-%d0%bd%d0%b0%d0%b1%d0%be%d0%bb%d0%b5%d0%b2%d1%88%d0%b5%d0%b3%d0%be-%d0%be-pci-dss/
permalink: /2011/07/%d0%b8%d0%b7-%d0%bd%d0%b0%d0%b1%d0%be%d0%bb%d0%b5%d0%b2%d1%88%d0%b5%d0%b3%d0%be-%d0%be-pci-dss/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2011/07/pci-dss.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1293446972512114299
shorturl:
  - http://tinyurl.com/nhfkrlm
tags:
  - pci:dss
  - бумажные тигры
  - соответствие требованиям
---
<div style="text-align: justify;">
  Соответствие требованиям стандарта безопасности PCI DSS сейчас довольно горячая тема. И очень часто во время ее обсуждения участники дискуссии забывают об основном назначении стандарта. А PCI DSS был изобретен для того, чтобы перенести риски карточного мошенничества с платежных систем <b>VISA, MasterCard, AmEx и Discover </b>на банки-эмитенты пластиковых карт и прочие субъекты их обработки: торговцев, поставщиков услуг, процессинг, эквайринг и пр.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Вы заметили, PCI DSS не содержит раздела, касающегося оценки рисков, как это принято во многих других методиках и стандартах ИБ? Это потому, что оценка рисков, на основании результатов которой составлялись требования стандарта, уже давно выполнена Визой со товарищи. Стандарт регулирует <i><b>их </b></i>риски, а не ваши или ваших клиентов, и вступая в сотрудничество с платежными вендорами вы обязаны взять какую-то часть этих рисков на себя. Другими словами, если хотите работать с платежными системами, соблюдайте стандарт, или&#8230; или есть другой путь.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Как всегда, есть альтернатива и она в этом случае логично следует из выше сказанного. Но тем не менее, она очень редко фигурирует в &#171;писиайных&#187; дискуссиях специалистов по ИБ и сочувствующих. Альтернатива заключается в том, что если сотрудничество с несоблюдающим стандарт партнером выгодно учредителям PCI, то соблюдать требования партнеру совсем не обязательно. Никто не будет гнобить за несоответствие гусыню, несущую золотые яйца, потому что это невыгодно с точки зрения бизнеса, а PCI DSS &#8212; это бизнес-стандарт.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  Вот почему я глубоко убежден, что гигантские банки, обладающие своим процессингом и не спешащие им делиться (то есть, представлять его услуги) еще очень нескоро всерьез задумаются о соответствии. Потому что в этом нет коммерческой необходимости, а делать это &#171;просто так&#187; совершенно невыгодно. Представьте себе ИТ-инфраструктуру большого распределенного банка, прошедшего через несколько слияний и поглощений: там и без писиая есть чем заняться. С другой стороны, небольшие и очень маленькие банки, а также разного рода поставщики услуг и торговые предприятия придут к этому очень и очень скоро, потому что для них путь соответствия более выгоден и менее накладен.
</div>

<div style="text-align: justify;">
</div>

<div style="text-align: justify;">
  И не нужно причислять PCI DSS к стандартам государственного или отраслевого уровня. В этой области никогда не будет справедливости: кому-то соблюдать требования будет обязательно, а кто-то будет состоять в белом списке в силу своей важности и полезности. И надеяться на то, что грубое несоблюдение требований ИБ крупными игроками чем-то им аукнется &#8212; тоже не стоит.
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_180">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F07%2F%25d0%25b8%25d0%25b7-%25d0%25bd%25d0%25b0%25d0%25b1%25d0%25be%25d0%25bb%25d0%25b5%25d0%25b2%25d1%2588%25d0%25b5%25d0%25b3%25d0%25be-%25d0%25be-pci-dss%2F&linkname=%D0%98%D0%B7%20%D0%BD%D0%B0%D0%B1%D0%BE%D0%BB%D0%B5%D0%B2%D1%88%D0%B5%D0%B3%D0%BE%20%D0%BE%20PCI%20DSS" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F07%2F%25d0%25b8%25d0%25b7-%25d0%25bd%25d0%25b0%25d0%25b1%25d0%25be%25d0%25bb%25d0%25b5%25d0%25b2%25d1%2588%25d0%25b5%25d0%25b3%25d0%25be-%25d0%25be-pci-dss%2F&linkname=%D0%98%D0%B7%20%D0%BD%D0%B0%D0%B1%D0%BE%D0%BB%D0%B5%D0%B2%D1%88%D0%B5%D0%B3%D0%BE%20%D0%BE%20PCI%20DSS" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F07%2F%25d0%25b8%25d0%25b7-%25d0%25bd%25d0%25b0%25d0%25b1%25d0%25be%25d0%25bb%25d0%25b5%25d0%25b2%25d1%2588%25d0%25b5%25d0%25b3%25d0%25be-%25d0%25be-pci-dss%2F&linkname=%D0%98%D0%B7%20%D0%BD%D0%B0%D0%B1%D0%BE%D0%BB%D0%B5%D0%B2%D1%88%D0%B5%D0%B3%D0%BE%20%D0%BE%20PCI%20DSS" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2011%2F07%2F%25d0%25b8%25d0%25b7-%25d0%25bd%25d0%25b0%25d0%25b1%25d0%25be%25d0%25bb%25d0%25b5%25d0%25b2%25d1%2588%25d0%25b5%25d0%25b3%25d0%25be-%25d0%25be-pci-dss%2F&linkname=%D0%98%D0%B7%20%D0%BD%D0%B0%D0%B1%D0%BE%D0%BB%D0%B5%D0%B2%D1%88%D0%B5%D0%B3%D0%BE%20%D0%BE%20PCI%20DSS" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
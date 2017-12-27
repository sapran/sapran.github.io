---
id: 1044
title: Adobe vs FoxIt
date: 2010-04-04T15:47:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/04/04/adobe-vs-foxit/
permalink: /2010/04/adobe-vs-foxit/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/04/adobe-vs-foxit.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/2135511220860470843
shorturl:
  - http://tinyurl.com/nekfbvv
tags:
  - adobe
  - foxit
  - pdf
  - подкасты
---
За последние два-три года Adobe сильно досталось: уязвимости в Adobe Reader обнаруживались с завидной регулярностью, а компания-разработчик откровенно не была готова оперативно на это реагировать. В результате исправленные версии выходили поздно, а устанавливались пользователями еще позже, в следствие чего Adobe Actobat Reader надолго занял почетное место лидера по&nbsp;уязвимостям&nbsp;среди прикладного ПО.

Многих&nbsp;пользователей,&nbsp;преимущественно&nbsp;работающих в сферах ИТ и ИБ, такая стабильная ненадежность Adobe Reader натолкнула на идею заменить его на что-то другое, менее популярное, а от того не особенно аппетитное для хакеров. Выбор зачастую падал на FoxIt Reader &#8212; простую и удобную программу, занимающую в десятки раз меньшие объемы жесткого диска и ОЗУ. И все бы ничего, да вот только появился на прошлой неделе Proof of Concept вектора атаки, заставивший усомниться в надежности FoxIt даже самых ярых его поклонников.

<div style="text-align: right;">
</div>

<div style="clear: both; text-align: center;">
</div>

Началось все с того, что [Didier Stevens](http://didierstevens.com/), исследователь из Бельгии, опубликовал видео, на котором [продемонстрировал](http://blog.didierstevens.com/2010/03/29/escape-from-pdf/) оригинальное использование&nbsp;метода **/launch** из спецификации PDF. Этот метод позволяет запустить существующий в системе исполняемый код, например cmd.exe, и передать ему аргументы командной строки. При этом пользователю выдается предупреждение о намерении PDF-документа запустить внешнюю программу, и требование показа такого предупреждения зафиксировано все в той же спецификации. Дидье&nbsp;поэкспериментировал&nbsp;некоторое время с этим методом &nbsp;и достиг результата, при котором PDF-документ осуществлял попытку запуска вложенного в файл документа мобильного кода(!), но у пользователя все еще оставалась возможность предотвратить атаку нажав кнопку &#171;Отмена&#187; в окне предупреждения. Похимичив над документом еще какое-то время, исследователь нашел способ частично&nbsp;контролировать&nbsp;текст выдаваемого предупреждения, что раскрыло перед ним широкую перспективу дополнения вектора атаки элементами социальной инженерии.

Вдоволь наигравшись с Acrobat Reader, Дидье оформил письмо с деталями своих изысканий в Adobe и решил проверить, как же на подобные PDF-файлы реагирует хваленый безопасный FoxIt Reader.&nbsp;FoxIt открыл PDF и [запустил](http://blog.didierstevens.com/2010/03/31/escape-from-foxit-reader/)&nbsp;вложенный&nbsp;исполняемый&nbsp;код, при этом не&nbsp;продемонстрировав&nbsp;ни намека на всплывающее окно с предупреждением. Естественно, сознательный Дидье сразу же информировал об этом вендора, который [оперативно отреагировал](http://forums.foxitsoftware.com/showthread.php?p=41323) выпуском исправленной версии, в которой теперь все почти так же, как и в Adobe Reader. Предупреждение появляется, но его текст нельзя&nbsp;контролировать, что оставляет хакеру меньше возможностей выполнения кода на машине жертвы, используя методы социальной инженерии.

Подробнее обо этих событиях&nbsp;Дидье&nbsp;рассказывает в&nbsp;[интервью подкасту Eurotrash Security](http://www.eurotrashsecurity.eu/index.php/Episodes#Episode_8.5_.28Exclusocast.29).&nbsp;Меня же они натолкнули на вот такое предположение. По-моему, **люди осознающие ущербность Adobe Reader, уже достаточно образованы для того, чтобы не открывать все попадающие под руку PDF-файлы**. Зачем же тогда мигрировать на альтернативное ПО, которое, как оказалось, в&nbsp;определенном&nbsp;смысле отнюдь не безопаснее, а даже наоборот? Между тем, я остаюсь при мнении, что для массового использования пользователями, не имеющими представления об опасностях, таящихся в полученных из ненадежных источников PDF-файлах, все-таки лучше подошел бы FoxIt Reader.&nbsp;Если у вас есть соображения по этому поводу, прошу делиться.

**Update** [Статья](http://news.cnet.com/8301-27080_3-20001792-245.html) на эту же тему на CNet.

**Update** [Официальный ответ](http://blogs.adobe.com/adobereader/2010/04/didier_stevens_launch_function.html)&nbsp;Adobe с руководством по&nbsp;безусловной&nbsp;блокировке опасного функционала.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_97">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2Fadobe-vs-foxit%2F&linkname=Adobe%20vs%20FoxIt" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2Fadobe-vs-foxit%2F&linkname=Adobe%20vs%20FoxIt" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2Fadobe-vs-foxit%2F&linkname=Adobe%20vs%20FoxIt" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F04%2Fadobe-vs-foxit%2F&linkname=Adobe%20vs%20FoxIt" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
---
id: 1078
title: Blue Screen Of Death
date: 2009-11-06T20:14:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/11/06/blue-screen-of-death/
permalink: /2009/11/blue-screen-of-death/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/11/blue-screen-of-death.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/4871784942029094463
shorturl:
  - http://tinyurl.com/nf583sv
tags:
  - bsod
  - microsoft
  - sysinternals
  - windows vista
  - windows xp
---
<div style="clear: both; text-align: auto;">
  С этим неприятным явлением наверняка сталкивался каждый более или менее опытный пользователь MS Windows. А системные администраторы и подавно, для них это явный признак того, что либо (а) последние изменения в системе (установленные драйверы или программы, измененные настройки) явно не пошли ОС на пользу, либо (б) в скором будущем ОС придется&nbsp;переустановить. В последнее время, из-за повсеместного&nbsp;общественного&nbsp;неприятия Windows Vista, от этого страдают большинство пользователей современных ноутбуков, предназначенных для работы под Vista, но волею судеб корчащиеся под XP. Большинство &#171;членов клуба&#187; относится к <b>BSoD </b>как к неизбежному злу, и мало кто пробовал разобраться, каковы его истинные причины, что за теоретические аспекты за ним скрываются и какую&#8230; пользу можно из него извлечь.
</div>

<div style="clear: both; text-align: center;">
  <a href="http://jmobley123.files.wordpress.com/2008/10/blue-screen-of-death1.jpg" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="240" src="http://jmobley123.files.wordpress.com/2008/10/blue-screen-of-death1.jpg" width="320" /></a>
</div>

Немного теории. Есть такое понятие, как **безопасное состояние системы**. Это когда отношения между субъектом (пользователь, клиентское ПО, драйвер) и объектом (сервис, системный вызов, прерывание) регламентируются определенной **политикой безопасности**. Допустим, существует некое количество безопасных состояний и некое количество&nbsp;**транзитных функций**, переводящих систему из одного состояния в следующее (примеры транзитных функций: ввод текста пользователем, начало итерации цикла, получение и обработка сетевой датаграммы). Это так называемая&nbsp;**машина состояний**, которая основывается на математическом выводе: если стартовое состояние системы &#8212; безопасное, а все выполняемые над системой транзитные функции &#8212; тоже безопасны, то и каждое последующее состояние системы будет безопасным (вспоминаете метод математической индукции?)

Естественно, немногие системы настолько &#171;замкнуты&#187; и защищены, что категорически не позволяют добавлять в себя новые функции. Эти новые функции (ПО, драйверы и т.п.) крайне редко&nbsp;безопасны&nbsp;настолько, насколько хотелось бы создателям системы. Поэтому создатели предусматривают проверку соблюдения политики безопасности системы перед каждой сменой состояния. В случае, когда транзитная функция пытается перевести систему в&nbsp;**небезопасное**&nbsp;**состояние&nbsp;**угрожающее целостности системы, последней не остается&nbsp;ничего лучше, чем вернуться к изначальному состоянию &#8212; то есть перезагрузиться. Blue Screen Of Death как раз для этого и предназначен: сохранив на диск (для возможного последующего расследования) &nbsp;доказательства целесообразности своих действий, он блокирует подозрительную транзитную функцию и перезагружает операционку. 

<div style="clear: both; text-align: auto;">
</div>

Для тех счастливцев, которые не в теме: синий экран смерти отображается на мониторе компьютера доли секунды, поэтому разглядеть, что на нем написано неподготовленному пользователю очень трудно. Удается только определить, что на нем явно что-то написано &#8212; белым по синему, отсюда и название. Во время отображения синего экрана и предупреждающего сообщения, система совершает т.н. дамп памяти, т.е. выгружает содержимое (или его часть) ОЗУ в файл на диске &#8212; на тот случай, если позже кто-то захочет разобраться в причинах ошибки. Много времени выполнение дампа не занимает, и после этого система автоматически перезагружается. Настроить параметры обработки&nbsp;критических&nbsp;ошибок можно в меню **Мой компьютер-Свойства-Дополнительно-Загрузка и восстановление-Параметры-Отказ системы**.

<div style="clear: both; text-align: center;">
  <a href="http://dl.dropbox.com/u/198252/bsod_settings.JPG" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="320" src="http://dl.dropbox.com/u/198252/bsod_settings.JPG" width="269" /></a>
</div>

Здесь можно выбрать тип дампа. Лучше выбрать полный, но не забудьте периодически удалять его из&nbsp;соответствующей&nbsp;директории или поставьте галочку &#171;Заменять&nbsp;существующий&nbsp;файл дампа&#187;.&nbsp;Для того, чтобы произвольно вызвать BSoD, присвойте ключу&nbsp;**HKLMSYSTEMCurrentControlSetServicesi8042prtParametersCrashOnCtrlScroll** (REG_DWORD) значение **1&nbsp;**(изменения вступят в силу после перезагрузки). После этого удерживая **правый**&nbsp;**Ctrl** дважды нажмите **Scroll Lock** и вуаля! До встречи после ребута!

<div style="clear: both; text-align: center;">
  <a href="http://dl.dropbox.com/u/198252/crashonctrlscroll.JPG" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="54" src="http://dl.dropbox.com/u/198252/crashonctrlscroll.JPG" width="400" /></a>
</div>

Давайте теперь проанализируем файл дампа ОЗУ. Поверьте, там можно найти очень много интересного. Подробный анализ лучше проводить специальными средствами: бинарным редактором и/или дизассемблером. Начать можно с поиска &#171;читабельных&#187; строк при помощи утилиты [**strings**](http://live.sysinternals.com/strings.exe)&nbsp;в составе [Sysinternals Suite](http://technet.microsoft.com/en-us/sysinternals/bb842062.aspx).

<div style="clear: both; text-align: center;">
  <a href="http://dl.dropbox.com/u/198252/cmd.JPG" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="195" src="http://dl.dropbox.com/u/198252/cmd.JPG" width="400" /></a>
</div>

<div style="clear: both; text-align: center;">
</div>

<div style="clear: both; text-align: left;">
  В результате получится очень большой ТХТ-файл, не советую пробовать открывать его обычным Блокнотом. Вместо этого используйте <a href="http://notepad-plus.sourceforge.net/ru/site.htm">Notepad++</a>. Поковыряйтесь в нем пол часика, будете удивлены как много любопытных вещей хранятся в ОЗУ в текстовом виде.
</div>

Кстати, цвета отображения сообщения о критической ошибке можно изменять. Практического смысла нет, но в качестве шутки над начинающим админом &#8212; то что надо. За цвета отвечают два параметра в файле **C:WINDOWSsystem.ini** в секции&nbsp;**[386enh]**  
******MessageBackColor=9**  
******MessageTextColor=F**  
Если таких строк нет, их придется создать.&nbsp;Коды цветов следующие: &nbsp;**0&nbsp;= черный, 1 =&nbsp;<span style="font-weight: normal;"><b>синий<span style="font-weight: normal;"><b>, 2 = зеленый, 3 = голубой, 4 = красный, 5 =&nbsp;<span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b>пурпурный,&nbsp;<span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b>6 = желто-коричневый, 7 = белый, 8 =&nbsp;<span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b>серый,<span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b>&nbsp;9 = ярко-синий, A =&nbsp;<span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b>ярко-зеленый<span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b><span style="font-weight: normal;"><b>, B = яркий бирюзовый, C = ярко-красный, D = ярко пурпурного, E = ярко-желтый, F = ярко-белый.</b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span></b></span>**

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_63">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2Fblue-screen-of-death%2F&linkname=Blue%20Screen%20Of%20Death" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2Fblue-screen-of-death%2F&linkname=Blue%20Screen%20Of%20Death" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2Fblue-screen-of-death%2F&linkname=Blue%20Screen%20Of%20Death" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2Fblue-screen-of-death%2F&linkname=Blue%20Screen%20Of%20Death" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
---
id: 1067
title: Очередной Adobe 0-day/UISG CTF
date: 2009-12-17T15:23:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/12/17/%d0%be%d1%87%d0%b5%d1%80%d0%b5%d0%b4%d0%bd%d0%be%d0%b9-adobe-0-dayuisg-ctf/
permalink: /2009/12/%d0%be%d1%87%d0%b5%d1%80%d0%b5%d0%b4%d0%bd%d0%be%d0%b9-adobe-0-dayuisg-ctf/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/12/adobe-0-dayuisg-ctf.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/5280723487152429226
shorturl:
  - http://tinyurl.com/ncyheb3
tags:
  - adobe
  - ctf
  - google
  - metasploit
  - приватность
---
[](http://www.blogger.com/)<span></span><span></span><span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Не хотел я, да видно придется написать об очередном zero-day эксплойте для Adobe Acrobat & Reader. Не хотел потому, что уязвимости для этих, с позволения сказать, программных продуктов возникают теперь чуть ли не ежемесячно. А придется по нескольким причинам.</span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"><br /></span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Во-первых, для этого конкретного эксплойта </span></span>**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">уже два дня как есть </span></span>**[**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">модуль</span></span>**](http://www.metasploit.com/redmine/projects/framework/repository/revisions/7882/entry/modules/exploits/windows/fileformat/adobe_media_newplayer.rb)**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"> в Metasploit Framework</span></span>**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">. Это означает, что любой подросток на планете может им воспользоваться. Во-вторых, </span></span>**[<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Adobe выпустит&nbsp;исправление&nbsp;этой уязвимости только 12 января</span></span>](http://news.cnet.com/8301-27080_3-10416816-245.html?part=rss&tag=feed&subj=News-Security)**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">. В-третьих, давно пора написать о средствах защиты от уязвимостей подобного рода. И в-четвертых, </span></span>[**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">client-side</span></span>**](http://www.honeynet.org/node/157)<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"> с недавних пор является моим излюбленным вектором атаки во время тестов на проникновение.</span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"><br /></span></span>  
<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Для начала, что делать.</span></span> 

  1. <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">&nbsp;Если это возможно, отказаться от использования продукции компании Adobe. Просматривать PDF-файлы можно в </span></span>[**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">FoxIt Reader</span></span>**](http://www.foxitsoftware.com/pdf/reader/)<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"> или </span></span>**[<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Google Docs</span></span>](http://docs.google.com/)**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">. Первый вариант &#8212; это небольшая и удобная программа-просмотрщик. Второй вариант снимает вопрос полностью, так как в этом случае PDF-файл открывается не на вашем ПК, а на сервере Google.</span></span>
  2. <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Если по каким-то причинам это (п. 1) не возможно, отключить JavaScript. Сделать это можно в меню </span></span>**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Edit/Preferences/JavaScript/Enable Acrobat JavaScript</span></span>**<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">. Я не знаю, зачем в PDF-ах javaScript, наверное Adobe знает, поэтому и устанавливает эту опцию включенной по умолчанию. Отключение JavaScript от всех бед не убережет, но большинство эксплойтов просто не запустится.</span></span>
  3. <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">В любом случае и в любых обстоятельствах следовать правилам персональной безопасности в Интернете.</span></span>

  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Не открывать письма из незнакомых источников. Вообще. Удалять до прочтения. Не помещать в спам! Индексация Google Desktop или Windows Search может запустить фоновый просмотрщик документа и тогда все труды насмарку!</span></span>
  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Не открывать вложения в подозрительных письмах, а еще лучше &#8212; во всех письмах, прочтение которых для вас не является необходимым. Примеры: PowerPoint-презентации с зевающими котами и восхитительными пейзажами, PDF-ки с прикольными карикатурами и так далее.</span></span>
  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Использовать антивирус. Да, </span></span>[<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">он неспособен предотвратить целенаправленную атаку</span></span>](http://securegalaxy.blogspot.com/2009/10/blog-post_18.html)<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">, но все-таки иметь антивирус лучше, чем не иметь. Впрочем, решать вам.</span></span>
  * <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Обновлять ПО по мере выпуска исправлений. Подробнее </span></span>[<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">в этом посте</span></span>](http://securegalaxy.blogspot.com/2009/11/2.html)<span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">.</span></span>

<div>
  <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Теперь об уязвимости. Это ошибка в обработчике формата файла. Позволяет выполнить произвольный код с правами текущего пользователя &#8212; еще один аргумент не входить в Windows с правами администратора. &#171;Зараженные&#187; документы свободно циркулируют в диком Интернете: рассылаются со спамом &nbsp;и распространяются через вредоносные сайты.</span></span>
</div>

<div>
  <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"><br /></span></span>
</div>

<div>
  <span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">Пару слов о хорошем.&nbsp;Сдается&nbsp;мне, что </span></span><a href="http://securegalaxy.blogspot.com/2009/12/ukrainian-information-security-group.html"><span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;">CTF ивент в эту субботу</span></span></a><span style="font-size: small;"><span style="font-family: 'Trebuchet MS', sans-serif;"> таки состоится. Сегодня освободилось одно место в &#171;Красной&#187; команде, желающие могут присоединиться.</span></span>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_74">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25be%25d1%2587%25d0%25b5%25d1%2580%25d0%25b5%25d0%25b4%25d0%25bd%25d0%25be%25d0%25b9-adobe-0-dayuisg-ctf%2F&linkname=%D0%9E%D1%87%D0%B5%D1%80%D0%B5%D0%B4%D0%BD%D0%BE%D0%B9%20Adobe%200-day%2FUISG%20CTF" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25be%25d1%2587%25d0%25b5%25d1%2580%25d0%25b5%25d0%25b4%25d0%25bd%25d0%25be%25d0%25b9-adobe-0-dayuisg-ctf%2F&linkname=%D0%9E%D1%87%D0%B5%D1%80%D0%B5%D0%B4%D0%BD%D0%BE%D0%B9%20Adobe%200-day%2FUISG%20CTF" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25be%25d1%2587%25d0%25b5%25d1%2580%25d0%25b5%25d0%25b4%25d0%25bd%25d0%25be%25d0%25b9-adobe-0-dayuisg-ctf%2F&linkname=%D0%9E%D1%87%D0%B5%D1%80%D0%B5%D0%B4%D0%BD%D0%BE%D0%B9%20Adobe%200-day%2FUISG%20CTF" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F12%2F%25d0%25be%25d1%2587%25d0%25b5%25d1%2580%25d0%25b5%25d0%25b4%25d0%25bd%25d0%25be%25d0%25b9-adobe-0-dayuisg-ctf%2F&linkname=%D0%9E%D1%87%D0%B5%D1%80%D0%B5%D0%B4%D0%BD%D0%BE%D0%B9%20Adobe%200-day%2FUISG%20CTF" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
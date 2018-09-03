---
id: 1082
title: Небезопасные вложения
date: 2009-10-24T18:17:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/10/24/%d0%bd%d0%b5%d0%b1%d0%b5%d0%b7%d0%be%d0%bf%d0%b0%d1%81%d0%bd%d1%8b%d0%b5-%d0%b2%d0%bb%d0%be%d0%b6%d0%b5%d0%bd%d0%b8%d1%8f/
permalink: /2009/10/%d0%bd%d0%b5%d0%b1%d0%b5%d0%b7%d0%be%d0%bf%d0%b0%d1%81%d0%bd%d1%8b%d0%b5-%d0%b2%d0%bb%d0%be%d0%b6%d0%b5%d0%bd%d0%b8%d1%8f/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/10/blog-post_24.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/1796361675660436983
shorturl:
  - http://tinyurl.com/ofzewll
tags:
  - metasploit
  - антивирусы
---
Нередко приходится наблюдать за радостным повизгиванием коллег, торопящихся разослать всей своей адресной книге PowerPoint-презентацию с новой порцией зевающих котов, очередной подборкой пейзажей или текущим Топ-20 фотожаб рунета. Рассуждать на тему художественной ценности таких рассылок считаю жестким оффтопом, посему предлагаю пообщаться на тему информационных угроз, таящихся в подобных &#171;письмах счастья&#187;.

Существует целый класс (или, по версии [OSSTMM](http://www.isecom.org/osstmm/), &#171;канал&#187;) атак, гордо именуемый **client side**. Грубо говоря, это все, что (намеренно, по ошибке, или в следствие неосторожности)&nbsp;инициируется&nbsp;пользователем&nbsp;атакуемой системы. Например, юзер просматривает зараженный PDF файл в уязвимой версии Adobe Reader, или открывает полученный из неизвестного источника документ, содержащий зловредный макрос, в то время, как в настройках его&nbsp;MS Word выполнение макросов разрешено.&nbsp;Каковы могут быть последствия?

Для начала, вас уже &#171;сделали&#187;: компьютер находится под контролем автора зловредного кода. Эффект может&nbsp;варьироваться в зависимости от его (кода) предназначения (например, на ПК будет размещен бот или командно контрольный пункт бот-сети) и от контекста, в котором этот код был выполнен (проще говоря, админ его запустил, или обычный юзер). Рассуждения на тему можно продолжать очень долго, лично я могу болтать на такие темы часами. Но, как говориться, лучше один раз увидеть.

В этом ролике я сформировал вредоносный код (mean payload) и упаковал его в VBScript. Этот код я разместил в вордовском документе и скопировал на машину под управлением Windows XP SP3 с полностью обновленным MS Office 2007. После открытия документа, payload устанавливает соединение с &#171;родительским&#187; компьютером (LHOST) и предоставляет хозяину&nbsp;командный&nbsp;интерфейс к компьютеру жертвы. Заметьте, так как соединение инициируется жертвой, межсетевой экран Windows XP его не блокирует.

<div style="text-align: center;">
</div>

Кто-то может спросить &#171;А как же антивирусы?&#187;. На атакуемой машине установлен и полностью обновлен продукт одного из лидеров этой индустрии.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_59">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F10%2F%25d0%25bd%25d0%25b5%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d1%258b%25d0%25b5-%25d0%25b2%25d0%25bb%25d0%25be%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f%2F&linkname=%D0%9D%D0%B5%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D1%8B%D0%B5%20%D0%B2%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F10%2F%25d0%25bd%25d0%25b5%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d1%258b%25d0%25b5-%25d0%25b2%25d0%25bb%25d0%25be%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f%2F&linkname=%D0%9D%D0%B5%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D1%8B%D0%B5%20%D0%B2%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F10%2F%25d0%25bd%25d0%25b5%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d1%258b%25d0%25b5-%25d0%25b2%25d0%25bb%25d0%25be%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f%2F&linkname=%D0%9D%D0%B5%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D1%8B%D0%B5%20%D0%B2%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F10%2F%25d0%25bd%25d0%25b5%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d1%258b%25d0%25b5-%25d0%25b2%25d0%25bb%25d0%25be%25d0%25b6%25d0%25b5%25d0%25bd%25d0%25b8%25d1%258f%2F&linkname=%D0%9D%D0%B5%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D1%8B%D0%B5%20%D0%B2%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
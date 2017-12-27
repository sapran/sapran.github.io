---
id: 1104
title: Identity-Based Encryption
date: 2009-07-25T16:05:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/07/25/identity-based-encryption/
permalink: /2009/07/identity-based-encryption/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/07/identity-based-encryption.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/3004908695192197052
shorturl:
  - http://tinyurl.com/oapozgs
tags:
  - ibe
  - pki
  - криптография
---
Сегодня открыл для себя [IBE](http://crypto.stanford.edu/ibe/). Спешу поделиться первым впечатлением. В двух словах: <span style="font-weight: bold;">это круто</span>.

Теперь подробнее. IBE это реализация [криптографии открытых ключей](http://en.wikipedia.org/wiki/Public-key_cryptography). Напомню, <span style="font-weight: bold;">публичный </span>ключ соответствует некоему <span style="font-weight: bold;">приватному </span>ключу, и все, что зашифровано с использованием публичного ключа, может быть расшифровано владельцем ключа приватного. На первый взгляд непросто, а если разбираться в теории &#8212; еще сложнее. Так что ограничимся примером.

Коля любит Олю и хочет написать ей письмо. Да так, чтобы злой хакер Вася это письмо не прочитал. Он просит Олю прислать ему ее <span style="font-weight: bold;">открытый </span>(он же публичный) ключ, шифрует им свое сообщение и жмет кнопку &#171;Send&#187;. Теперь только Оля может его расшифровать и прочитать. Естественно, быть в этом уверенным можно только исходя из предположения, что единственным человеком, обладающим доступом к Олиному <span style="font-weight: bold;">закрытому </span>ключу, является Оля, только Оля и никто кроме Оли.

Вот здесь начинаются трудности. <span style="font-weight: bold;">Трудность Один: где </span>Оле <span style="font-weight: bold;">взять </span>приватный и публичный ключи? Естественно, генерировать самостоятельно при помощи специального ПО. <span style="font-weight: bold;">Трудность Два: как Коля может быть уверен</span> в том, что полученный им публичный ключ действительно принадлежит Оле? Если она ему из рук в руки его не передала &#8212; то никак. Если возможность обменяться ключами с глазу на глаз у Коли и Оли нет, то нужно звать некую Марию Ивановну, которой и Коля, и Оля безмерно доверяют, чтобы она послужила <span style="font-weight: bold;">посредником</span> в этой передаче. <span style="font-weight: bold;">Трудность Три: как</span> Оле <span style="font-weight: bold;">сохранить</span> приватный ключ <span style="font-weight: bold;">в секрете</span>? Защитить его текст симметричным шифром? Запереть в железную коробочку и носить в виде брелока? Будет ли такая схема достаточно безопасной? <span style="font-weight: bold;">Трудность Четыре: где хранить</span> опубликованные открытые ключи, так чтобы их по необходимости могли получить все, желающие переписываться с Олей безопасно? У Марии Ивановны в письменном столе?

То, что описано в предыдущем абзаце, называется <span style="font-weight: bold;">Инфраструктурой открытого ключа</span> или [ <span style="font-weight: bold;">Public Key Infrastructure (PKI)</span>](http://en.wikipedia.org/wiki/Public_key_infrastructure). Это одно из самых неудачных применений публичной криптографии, что к сожалению компенсируется его повсеместным использованием и высокой стоимостью. [IBE](http://crypto.stanford.edu/ibe/), напротив, избавляет нас от всех присущих такой модели трудностей, так как в этом случае Коле для шифрования сообщения не нужно иметь публичный ключ Оли. Даже более того, Оле совсем не обязательно его к этому моменту генерировать, так как Коля может использовать в качестве открытого ключа что угодно, например название Олиного электронного почтового ящика. Я же говорил, что <span style="font-weight: bold;">это круто</span>.

[<img style="margin: 0pt 10px 10px 0pt; float: left; cursor: pointer; width: 215px; height: 155px;" src="http://www.keytrust.com.au/images/voltage.jpg" alt="" border="0" />](http://www.keytrust.com.au/images/voltage.jpg)Итак, Коля шифрует текст сообщение ключом типа <span style="font-weight: bold;">`olya@somemail.com&#8217;</span> и отсылает на этот адрес. Напоминаю, что используемый ключ &#8212; <span style="font-weight: bold;">публичный</span>, то есть Васе для расшифровки сообщения его знать не то что не достаточно, а и вовсе бесполезно. Письмо приходит на сервер <span style="font-weight: bold;">IBE-провайдера</span>, где использованному Колей публичному ключу ставится в соответствие ключ приватный. Осталось только доставить его (приватный ключ) вместе с зашифрованным сообщением Оле. Как это сделать? Очень просто &#8212; выслать Оле на почту приглашение зарегистрироваться на IBE-провайдере и прочитать адресованное ей послание. Оля обладает доступом к почтовому ящику, на который Коля шлет письмо шифруя текст его названием. Это и есть тот фокус, согласно которому Encryption является <span style="font-weight: bold;">Identity</span>-Based. Итого: <span style="font-weight: bold;">IBE = PKI &#8212; ATS</span>, где ATS (all the sh*t) &#8212; все те сложности, которые делают PKI громоздким и неудобным для частного применения. Хотя доверять провайдеру IBE обоим адресатам все-таки придется.

Надеюсь, это замечательное достижение криптографии послужит толчком к повсеместному шифрованию электронной почты. Протестировать работу систем, использующих IBE, можно двумя способами (по крайней мере, мне известно только два =). Способ Один: купить устройство <span style="font-weight: bold;">IronPort</span> с поддержкой <span style="font-weight: bold;">Email Encryption</span>. Решение вполне готовое и для бизнеса очень удобное. Способ Два: воспользоваться 14-дневным триалом [<span style="font-weight: bold;">Voltage Security Network</span>](http://www.voltage.com/vsn/freetrial.htm). Регистрация в системе проходит быстро, уже через пару минут можно будет начать тестирование. И что особенно приятно: никакого софта устанавливать не нужно.

<span style="font-weight: bold;">Оффтопик</span>: [ссылка](http://www.irongeek.com/i.php?page=videos/pn12/handgrip-buttstock-open-source-ak-47s) на демонстрацию процесса сборки т.н. Open Source AK-47

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_37">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2Fidentity-based-encryption%2F&linkname=Identity-Based%20Encryption" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2Fidentity-based-encryption%2F&linkname=Identity-Based%20Encryption" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2Fidentity-based-encryption%2F&linkname=Identity-Based%20Encryption" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F07%2Fidentity-based-encryption%2F&linkname=Identity-Based%20Encryption" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
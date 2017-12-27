---
id: 868
title: Me vs Apple FileVault
date: 2013-03-06T20:29:00+00:00
author: sapran
layout: post
guid: http://styran.com/2013/03/06/me-vs-apple-filevault/
permalink: /2013/03/me-vs-apple-filevault/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2013/03/me-vs-apple-filevault.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/6971974976831048872
shorturl:
  - http://tinyurl.com/patozqd
tags:
  - apple
  - fde
  - filevault
  - криптография
---
Вот какая история случилась между мной и ноутбуком. Драматизма, конечно, меньше, чем [у Гроссмана](http://blog.whitehatsec.com/cracking-aes-256-dmgs-and-epic-self-pwnage/), но тоже про Apple и криптографию, хотя и под другим углом.

Решил я в MacOS добавить французский язык ввода. И так получилось, что стал он языком ввода по умолчанию. Если честно, меня о моем желании никто не спрашивал. Макось, со свойственной ей уверенностью, что &#171;мама знает лучше&#187;, сделала все за меня.

Минут через пять я ненадолго отлучился, и система, как водится, заблокировалась. Возвращаюсь, просит ввести пароль. Ввожу, не подходит. Еще раз ввожу, снова не то. После третьего раза начинаю подозревать наихудшее и панически пытаюсь отыскать на экране логона меню переключения источника ввода &#8212; его нет.

В надежде, что мое подозрение верно и ОС все-таки ждет от меня ввода пароля во французской раскладке, начинаю беспорядочно вспоминать, какие клавиши в ней расставлены не так, как в английской. То, что W меняется на Z, а Q на A, вспоминаю сразу, но на этом мысль останавливается. И самое главное: а где же тогда &#171;живут&#187; спец-символы!?

Понимаю, что без гугла не обойтись. [Google Images](http://images.google.com/) наше все, как часто я в отъезде в какую-нибудь экзотическую страну искал в сети фотографии клавиатур для ввода паролей, набираемых по-русски в латинской раскладке? Много раз, давай теперь французскую поищем. Оказывается, не так уж это и просто: ее вариантов как минимум два, причем один в возвратах гугла доминирует и при этом ничем не отличается от привычной латинской клавы.

Наконец-то нахожу нужную, вроде бы, мне картинку в достойном разрешении. Все это делается на смартфоне, поэтому детали еще нужно разглядеть. Нахожу нужные символы, в очередной раз ввожу пароль и&#8230; снова штанга. В голову предательски закрадывается мысль о том, что жесткий диск-то зашифрован, и, похоже, всем моим несинхронизированным данным хана.

Мысль о шифровании диска неожиданно возвращает проблеск надежды. Что-то не припоминаю я, чтобы в эпловой pre-boot аутентификации была возможность выбрать раскладку, отличную от английской. Так как терять больше нечего, движимый одной интуицией, перезагружаю комп.

[FileVault](https://en.wikipedia.org/wiki/FileVault) с радостью хавает мой пароль и ноутбук начинает загрузку. И через несколько секунд, о чудо! На экране появляется рабочий стол. Похоже, за отсутствием в системе других пользователей, ОС выполняет авто-логон в аккаунт юзера, разблокировавшего загрузочный диск. Опять же, очень мило со стороны Apple, я ничего такого не настраивал.

Вот так средство защиты сослужило мне неожиданно полезную службу. Целились в конфиденциальность, а попали в доступность, короче.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_269">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F03%2Fme-vs-apple-filevault%2F&linkname=Me%20vs%20Apple%20FileVault" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F03%2Fme-vs-apple-filevault%2F&linkname=Me%20vs%20Apple%20FileVault" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F03%2Fme-vs-apple-filevault%2F&linkname=Me%20vs%20Apple%20FileVault" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2013%2F03%2Fme-vs-apple-filevault%2F&linkname=Me%20vs%20Apple%20FileVault" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
---
id: 1095
title: Все свое ношу с собой
date: 2009-08-28T19:30:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/08/28/%d0%b2%d1%81%d0%b5-%d1%81%d0%b2%d0%be%d0%b5-%d0%bd%d0%be%d1%88%d1%83-%d1%81-%d1%81%d0%be%d0%b1%d0%be%d0%b9/
permalink: /2009/08/%d0%b2%d1%81%d0%b5-%d1%81%d0%b2%d0%be%d0%b5-%d0%bd%d0%be%d1%88%d1%83-%d1%81-%d1%81%d0%be%d0%b1%d0%be%d0%b9/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/08/blog-post_28.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/2073899514644830881
shorturl:
  - http://tinyurl.com/q8gwzqj
tags:
  - dropbox
  - keepass
  - truecrypt
  - криптография
  - пароли
  - приватность
---
Когда-то очень давно я понял, что пароли должны быть сложными и разными. Мысль эта грела меня достаточно долго, но количество паролей росло, и вскоре головы для их хранения стало маловато. Тогда я начал пользоваться парольными менеджерами и через месяц-полтора остановился на [KeePass](http://keepass.info/), который и по сей день служит мне верой и правдой. Держал я его на зашифрованной при помощи [TrueCrypt](http://www.truecrypt.org/) флешке, вместе с коллекцией портативных приложений, личными документами и прочими вкусностями, которые всегда хочется иметь под рукой.

Около полугода меня такой расклад устраивал, а потом я подумал, что флешку можно использовать более удачно, например установить на ней полезную операционную систему типа [BackTrack](http://www.remote-exploit.org/backtrack.html). А предыдущее содержимое флешки я разместил в [DropBox](http://www.getdropbox.com/) &#8212; сервисе, изначально предназначенном для синхронизации информации на нескольких компьютерах. Работает он так: вы регистрируетесь в сервисе и получаете 2Гб дискового пространства (бесплатно, расширяется за деньги). Потом качаете программку-клиент, доступную для Windows, Linux & Mac, устанавливаете ее и указываете, где на диске разместить структуру папок, синхронизируемую с сервисом. Все сохраненное в этих папках будет автоматически размещено на сервере, а после установки программы-клиента с вашими учетными данными на другом компьютере &#8212; будет автоматически загружено с сервиса на локальный диск. Если вы за компьютером ненадолго, то устанавливать клиента не обязательно &#8212; сервис предоставляет удобный веб-интерфейс, через который нужные файлы можно скачать вручную.

Естественно, БД паролей и конфиденциальная информация не содержаться там в чистом виде. Для этих целей я создал файл-контейнер TrueCrypt размером 32Мб и поместил в него все ценное. То есть, теперь все мои утилиты, приложения и прочие инструменты лежат в DropBox, а все ценное храниться в TrueCrypt-сейфе там же, по-близости. Такую схему считаю удобной: помнить нужно всего три пароля &#8212; на аккаунт в DropBox, на TrueCrypt-файл и на БД паролей, остальные можно генерировать и сохранять в KeePass; и сравнительно безопасной &#8212; дважды AES как-никак, плюс у самого DropBox какая-никакая защита есть.

На этом все. Берегите себя.

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_46">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F08%2F%25d0%25b2%25d1%2581%25d0%25b5-%25d1%2581%25d0%25b2%25d0%25be%25d0%25b5-%25d0%25bd%25d0%25be%25d1%2588%25d1%2583-%25d1%2581-%25d1%2581%25d0%25be%25d0%25b1%25d0%25be%25d0%25b9%2F&linkname=%D0%92%D1%81%D0%B5%20%D1%81%D0%B2%D0%BE%D0%B5%20%D0%BD%D0%BE%D1%88%D1%83%20%D1%81%20%D1%81%D0%BE%D0%B1%D0%BE%D0%B9" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F08%2F%25d0%25b2%25d1%2581%25d0%25b5-%25d1%2581%25d0%25b2%25d0%25be%25d0%25b5-%25d0%25bd%25d0%25be%25d1%2588%25d1%2583-%25d1%2581-%25d1%2581%25d0%25be%25d0%25b1%25d0%25be%25d0%25b9%2F&linkname=%D0%92%D1%81%D0%B5%20%D1%81%D0%B2%D0%BE%D0%B5%20%D0%BD%D0%BE%D1%88%D1%83%20%D1%81%20%D1%81%D0%BE%D0%B1%D0%BE%D0%B9" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F08%2F%25d0%25b2%25d1%2581%25d0%25b5-%25d1%2581%25d0%25b2%25d0%25be%25d0%25b5-%25d0%25bd%25d0%25be%25d1%2588%25d1%2583-%25d1%2581-%25d1%2581%25d0%25be%25d0%25b1%25d0%25be%25d0%25b9%2F&linkname=%D0%92%D1%81%D0%B5%20%D1%81%D0%B2%D0%BE%D0%B5%20%D0%BD%D0%BE%D1%88%D1%83%20%D1%81%20%D1%81%D0%BE%D0%B1%D0%BE%D0%B9" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F08%2F%25d0%25b2%25d1%2581%25d0%25b5-%25d1%2581%25d0%25b2%25d0%25be%25d0%25b5-%25d0%25bd%25d0%25be%25d1%2588%25d1%2583-%25d1%2581-%25d1%2581%25d0%25be%25d0%25b1%25d0%25be%25d0%25b9%2F&linkname=%D0%92%D1%81%D0%B5%20%D1%81%D0%B2%D0%BE%D0%B5%20%D0%BD%D0%BE%D1%88%D1%83%20%D1%81%20%D1%81%D0%BE%D0%B1%D0%BE%D0%B9" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
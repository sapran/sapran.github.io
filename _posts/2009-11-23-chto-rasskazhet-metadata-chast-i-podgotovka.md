---
id: 1075
title: 'Что расскажет metadata. Часть I: Подготовка.'
date: 2009-11-23T07:59:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/11/23/%d1%87%d1%82%d0%be-%d1%80%d0%b0%d1%81%d1%81%d0%ba%d0%b0%d0%b6%d0%b5%d1%82-metadata-%d1%87%d0%b0%d1%81%d1%82%d1%8c-i-%d0%bf%d0%be%d0%b4%d0%b3%d0%be%d1%82%d0%be%d0%b2%d0%ba%d0%b0/
permalink: /2009/11/%d1%87%d1%82%d0%be-%d1%80%d0%b0%d1%81%d1%81%d0%ba%d0%b0%d0%b6%d0%b5%d1%82-metadata-%d1%87%d0%b0%d1%81%d1%82%d1%8c-i-%d0%bf%d0%be%d0%b4%d0%b3%d0%be%d1%82%d0%be%d0%b2%d0%ba%d0%b0/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/11/metadata-i.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/9011637183398047708
shorturl:
  - http://tinyurl.com/pcypmm6
tags:
  - adobe
  - email
  - gmail
  - metadata
  - metasploit
  - менеджеры
  - пентесты
  - периметр
  - социальная инженерия
  - социальные сети
  - фишинг
---
<div dir="ltr" style="text-align: left;">
  <div style="text-align: justify;">
    Весьма распространено мнение о том, что социальная инженерия является наиболее эффективным методом взлома корпоративной защиты. Спорить не стану, потому что мнение это &#8212; верно. Не скажу, что оно математически доказуемо, но практика его подтверждает. Да и интуитивно понятно, что все технические &#171;дыры&#187; возможно залатать, а на каждый 0-day найдется свой IPS, главное чтобы бюджет был по-больше. А вот гарантированный способ защититься от человеческой глупости пока не изобретен и в ближайшее время на рынке вряд ли появится.
  </div>
  
  <div style="text-align: justify;">
  </div>
  
  <div style="text-align: justify;">
    На этапе подготовки социальной атаки, основной задачей является&nbsp;т.н. &#171;домашняя работа&#187; &#8212;&nbsp;сбор и анализ публично доступных данных о компании-цели.&nbsp;Среднестатистический&nbsp;корпоративный сайт содержит основную информацию о компании, ее продуктах, способах связаться с представителями и т.д. Этих данных может быть вполне достаточно для нормального пользователя Интернет, но&#8230; не наш случай. Помимо &#171;открытой&#187; информации, на сайте как правило существует уйма &#171;скрытых&#187; данных, которые могут оказаться полезны для осуществления социальной атаки.
  </div>
  
  <div style="text-align: justify;">
  </div>
  
  <div style="text-align: justify;">
    Все возможные сценарии перебирать не будем, а очертим для примера один классический план. Вопреки многочисленным недостаткам и уязвимостям, во многих компаниях используется ПО<b> Adobe Actobat Reader</b> (это <b>предположение #1</b>). Также, традиционно, многие сотрудники ИТ все еще используют&nbsp;<b>привилегированные учетные записи для интерактивного входа</b> в ОС на рабочих станциях (это <b>предположение #2</b>). Комбинация этих двух фактов дает нам надежду <b>получить доступ к админской учетке путем эксплуатации</b> какой-нибудь<b> известной уязвимости в Adobe Reader</b>, благо последний не прекращает ими радовать чуть ли не ежемесячно. Для этого всего нужно-то, &#8212; сесть за <b>Metasploit </b>да скрафтить зловредный PDF-ник, содержащий нужный <b>exploit. </b>В&nbsp;качестве <b>payload </b>поместить в него, скажем, <b>meterpreter/reverse_http </b>(все еще жутко глючит, но если часок поколдовать, то можно добиться нужного результата). А потом разослать этот PDF-ник во вложении к письму, &#171;декорированному&#187; в&nbsp;корпоративном&nbsp;стиле какого-нибудь известного вендора из числа поставщиков компании-цели. То есть, дело за малым, осталось всего лишь уточнить некоторые детали:
  </div>
  
  <ul>
    <li style="text-align: justify;">
      от кого слать письмо, для того, чтобы его гарантированно прочитали;
    </li>
    <li style="text-align: justify;">
      кому слать письмо, чтобы его гарантированно если не прочитали, то хотя бы открыли.
    </li>
  </ul>
  
  <div>
    <div style="text-align: justify;">
      На вопрос <b>&#171;От кого?&#187; </b>ответы можно найти следующими способами.
    </div>
  </div>
  
  <div>
    <ul>
      <li style="text-align: justify;">
        Просканировать &#171;внешний периметр&#187; компании-цели на предмет версий оборудования и ПО. В результате получим список предпочтений.
      </li>
      <li style="text-align: justify;">
        Проштудировать сайты местных интеграторов на предмет хвастовства об очередном супер-внедрении какого-нибудь мега-аппаратно-программного комплекса в компании-цели. Кстати, интегратор вероятно осуществляет первый уровень поддержки этого мега-решения, так что можно рассмотреть вариант действия от его лица.
      </li>
      <li style="text-align: justify;">
        Дополнительно, стоит&nbsp;профильтровать&nbsp;на тему мега-внедрений айтишную прессу, так как она с голодухи только об этом сейчас и пишет.
      </li>
      <li style="text-align: justify;">
        Подробно изучить веб-сайт компании-цели, возможно она сама не постеснялась похвастаться тем, какая она современная и технологичная, и какие мега-решения она использует. И какие версии. С точностью до пятого разряда.
      </li>
      <li style="text-align: justify;">
        Если охота экстриму &#8212; можно заняться dumpster diving-ом или попросту порыться в мусоре. Поверьте, инвойсы уничтожают в шредере очень редко, а коммерческие предложения &#8212; почти никогда.
      </li>
    </ul>
    
    <div>
      <div style="text-align: justify;">
        Альтернативно, можно &#171;забить&#187; на возню с вендорами и интеграторами и проработать вариант отправки письма от имени генерального или еще какого-нибудь директора. Лучше, с GMail-а и когда &#171;автор&#187; будет в командировке или в отпуске. Общий смысл послания: &#171;вашу мать, опять VPN не работает&#187;, только в предельно вежливом &#171;корпоративном&#187; стиле. А во вложении &#8212; PDF-ник со скрином ошибки. Скажете, подозрительно, могут догадаться? Поверьте, никто не заподозрит неладное, от менеджеров и не такого ожидать можно.
      </div>
    </div>
    
    <div>
      <div style="text-align: justify;">
      </div>
    </div>
    
    <div>
      <div style="text-align: justify;">
        В общем, &#171;что&#187; и &#171;от кого&#187; &#8212; выяснили. Осталось определиться <b>&#171;Кому?&#187;</b> Тут нам и поможет <b>metadata</b> из документов хранящихся (обычно в изобилии) на сайте компании-цели. Почти все типы документов &#171;круче&#187; текстовых содержат в себе <b>метаданные</b> &#8212; вспомогательную информацию, помещаемую в документ программой-редактором для каких-то одной ей понятных целей. Среди этих данных обычно содержатся всяческие параметры формата документа: типы, идентификаторы, кол-во слов/символов, даты создания и последнего сохранения и пр. Но самое главное &#8212; версия ПО редактора, в котором документ был создан, и имена пользователей, создавших и/или редактировавших документ. Эта информация &#8212; золото для социального&nbsp;инженера, так как она почти всегда правдива и служит отличной отправной точкой для дальнейших исследований. Ну например, получив из метаданных документа имя пользователя vpupkin мы&nbsp;автоматически&nbsp;имеем:
      </div>
    </div>
    
    <div>
      <ol>
        <li style="text-align: justify;">
          имя пользователя в домене компании-цели &#8212; vpupkin;
        </li>
        <li style="text-align: justify;">
          действительный адрес электронной почты &#8212; vpupkin@victim.tld;
        </li>
      </ol>
      
      <div>
        <div style="text-align: justify;">
          Далее, отправляем запрос <b>&#171;Пупкин Victim LLC&#187;</b> в <b>LinkedIn, Мой Круг</b> и т.п. &#8212; личность жертвы установлена. Роемся в его контактах в поисках разнообразных айтишников (если он сам таковым не является). Эту процедуру повторяем до тех пор, пока не составим внушительный список ИТ-персонала компании-цели. Что до полезности версии ПО, тут разговор короткий. Даже если она и не позволит подобрать конкретные эксплойты, то хотя бы поможет составить общее впечатление о культуре ИБ в компании: используются ли устаревшие программы, обновляются ли они после выхода критических патчей безопасности и т.п.
        </div>
      </div>
      
      <div>
        <div style="text-align: justify;">
        </div>
        
        <div style="text-align: justify;">
          В следующем посте я напишу о том, как собирать необходимые метаданные из открытых источников, как этот процесс автоматизировать,&nbsp;а также о том, как защитить &#171;критичные данные от утечки в виде метаданных.</p> 
          
          <p>
            <a href="http://securegalaxy.blogspot.com/search/label/metadata"><i>Больше о метаданных в этом блоге</i></a></div> </div> </div> </div> </div> 
            
            <div class="addtoany_share_save_container addtoany_content_bottom">
              <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_66">
                <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d1%2587%25d1%2582%25d0%25be-%25d1%2580%25d0%25b0%25d1%2581%25d1%2581%25d0%25ba%25d0%25b0%25d0%25b6%25d0%25b5%25d1%2582-metadata-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-i-%25d0%25bf%25d0%25be%25d0%25b4%25d0%25b3%25d0%25be%25d1%2582%25d0%25be%25d0%25b2%25d0%25ba%25d0%25b0%2F&linkname=%D0%A7%D1%82%D0%BE%20%D1%80%D0%B0%D1%81%D1%81%D0%BA%D0%B0%D0%B6%D0%B5%D1%82%20metadata.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20I%3A%20%D0%9F%D0%BE%D0%B4%D0%B3%D0%BE%D1%82%D0%BE%D0%B2%D0%BA%D0%B0." title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d1%2587%25d1%2582%25d0%25be-%25d1%2580%25d0%25b0%25d1%2581%25d1%2581%25d0%25ba%25d0%25b0%25d0%25b6%25d0%25b5%25d1%2582-metadata-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-i-%25d0%25bf%25d0%25be%25d0%25b4%25d0%25b3%25d0%25be%25d1%2582%25d0%25be%25d0%25b2%25d0%25ba%25d0%25b0%2F&linkname=%D0%A7%D1%82%D0%BE%20%D1%80%D0%B0%D1%81%D1%81%D0%BA%D0%B0%D0%B6%D0%B5%D1%82%20metadata.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20I%3A%20%D0%9F%D0%BE%D0%B4%D0%B3%D0%BE%D1%82%D0%BE%D0%B2%D0%BA%D0%B0." title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d1%2587%25d1%2582%25d0%25be-%25d1%2580%25d0%25b0%25d1%2581%25d1%2581%25d0%25ba%25d0%25b0%25d0%25b6%25d0%25b5%25d1%2582-metadata-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-i-%25d0%25bf%25d0%25be%25d0%25b4%25d0%25b3%25d0%25be%25d1%2582%25d0%25be%25d0%25b2%25d0%25ba%25d0%25b0%2F&linkname=%D0%A7%D1%82%D0%BE%20%D1%80%D0%B0%D1%81%D1%81%D0%BA%D0%B0%D0%B6%D0%B5%D1%82%20metadata.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20I%3A%20%D0%9F%D0%BE%D0%B4%D0%B3%D0%BE%D1%82%D0%BE%D0%B2%D0%BA%D0%B0." title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d1%2587%25d1%2582%25d0%25be-%25d1%2580%25d0%25b0%25d1%2581%25d1%2581%25d0%25ba%25d0%25b0%25d0%25b6%25d0%25b5%25d1%2582-metadata-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-i-%25d0%25bf%25d0%25be%25d0%25b4%25d0%25b3%25d0%25be%25d1%2582%25d0%25be%25d0%25b2%25d0%25ba%25d0%25b0%2F&linkname=%D0%A7%D1%82%D0%BE%20%D1%80%D0%B0%D1%81%D1%81%D0%BA%D0%B0%D0%B6%D0%B5%D1%82%20metadata.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20I%3A%20%D0%9F%D0%BE%D0%B4%D0%B3%D0%BE%D1%82%D0%BE%D0%B2%D0%BA%D0%B0." title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
              </div>
            </div>
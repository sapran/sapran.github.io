---
id: 1074
title: 'Что расскажет metadata. Часть II: Сбор данных.'
date: 2009-11-26T21:42:00+00:00
author: sapran
layout: post
guid: http://styran.com/2009/11/26/%d1%87%d1%82%d0%be-%d1%80%d0%b0%d1%81%d1%81%d0%ba%d0%b0%d0%b6%d0%b5%d1%82-metadata-%d1%87%d0%b0%d1%81%d1%82%d1%8c-ii-%d1%81%d0%b1%d0%be%d1%80-%d0%b4%d0%b0%d0%bd%d0%bd%d1%8b%d1%85/
permalink: /2009/11/%d1%87%d1%82%d0%be-%d1%80%d0%b0%d1%81%d1%81%d0%ba%d0%b0%d0%b6%d0%b5%d1%82-metadata-%d1%87%d0%b0%d1%81%d1%82%d1%8c-ii-%d1%81%d0%b1%d0%be%d1%80-%d0%b4%d0%b0%d0%bd%d0%bd%d1%8b%d1%85/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2009/11/metadata-ii_26.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/2325452491707106741
shorturl:
  - http://tinyurl.com/pz7a4hw
tags:
  - adobe
  - firefox
  - metadata
  - ms office
  - pdftk
  - пентесты
---
<div dir="ltr" style="text-align: left;">
  <div>
    <div style="text-align: justify;">
      В предыдущем посте мы выяснили, зачем нам нужны метаданные и что мы с ними собираемся делать. Приступим непосредственно к их сбору. Для сохранения чистоты эксперимента, в качестве примера будем использовать все те же документы PDF. Результаты их исследования получаются по-скромнее, но для тренировки сойдет.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Существует масса способов получения PDF-документов компании-цели. Можно, например, запросить счет на товар или услугу, &#8212; многие предоставляют их в виде &#171;подписанных&#187; PDF-файлов. Также, можно ввязаться в переписку с маркетологами или продавцами, просить презентации и прайс-листы, врать на счет несовместимости форматов (у меня, мол, древний StarOfiice, он эти PPTX и XMLX не понимает). В какой-то момент ваши измученные подопытные ретируются к проверенному средству &#8212; формат PDF для того и разрабатывался, чтобы открываться всегда и везде. Но накопленные таблицы и презентации ни в коем случае не выбрасывайте!
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Но самый простой и ненавязчивый способ &#8212; это <b>поиск Google</b>. Запустив поиск с ключевыми словами &#171;<b>site:victim.tld filetype:pdf</b>&#187; вы получите в распоряжение все PDF-документы на сайте &#171;объекта&#187;, доступные для индексации. Если честно, то мне никогда ничего сверх этого делать не приходилось &#8212; &#171;вываливающейся&#187; в поиске сотни-другой документов вполне достаточно для сбора необходимого объема данных. Естественно, нужно будет все это добро как-то сохранить. В ранней молодости я делал это при помощи дополнения Firefox под названием <b><a href="http://flashgot.net/">FlashGot</a></b>. Оно позволяет &#171;сохранить все&#187; ссылки на текущей странице, отфильтровав их по расширению файла. Огнелисом я уже какое-то время не пользуюсь, поэтому приходится комбинировать.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Сохранив локально достаточное количество файлов, приступаем, собственно, к извлечению метаданных. Банальный подход &#8212; открыть каждый файл в <b>Arobe Reader</b> и записать на бумажке данные в его свойствах. Но если файлов много, хотелось бы этот процесс автоматизировать. Для этого у меня есть &#171;виртуалка&#187; с <b>Ubuntu Linux</b>, которая с каждым днем все больше похожа на <b><a href="http://www.remote-exploit.org/backtrack.html">BackTrack</a></b>. В линуксе есть утилита extract. Она неплохо отыгрывает против &#171;офисных&#187; документов, но для PDF ее маловато.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      <b>$ extract volodymyr_styran_cv_en_2009.doc</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      mimetype &#8212; application/msword
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      language &#8212; Russian
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      paragraph count &#8212; 13
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      line count &#8212; 46
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      word count &#8212; 977
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      page count &#8212; 3
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      creator &#8212; <b>vstyran</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      date &#8212; 2009-06-04T15:54:00Z
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      generator &#8212; Microsoft Office Word
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      character count &#8212; 5575
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      last saved by &#8212; Vladimir S. Styran
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      creation date &#8212; 2008-10-16T19:01:00Z
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      template &#8212; Normal.dotm
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      <b>$ extract volodymyr_styran_cv_en_2009.pdf</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      format &#8212; PDF 1.5
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      mimetype &#8212; application/pdf
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Взамен я рекомендую использовать pdftk, от него толку значительно больше, хотя с результатами придется немного повозиться.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      <b>$ pdftk volodymyr_styran_cv_en_2009.pdf dump_data</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoKey: Creator
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoValue: Microsoft® Office Word 2007&#0;
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoKey: Producer
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoValue: Microsoft® Office Word 2007&#0;
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoKey: Author
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoValue: vstyran
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoKey: ModDate
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoValue: D:20090604160025
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoKey: CreationDate
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      InfoValue: D:20090604160025
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      PdfID0: ec683aaa7b39e945a28671b9f538e9
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      PdfID1: ec683aaa7b39e945a28671b9f538e9
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      NumberOfPages: 3
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      <b>$ pdftk volodymyr_styran_cv_en_2009.pdf dump_data | perl -ne &#8216;s/n$// if /^InfoKey:/; s/^InfoKey: //; s/^InfoValue//; print&#8217;</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Creator: Microsoft® Office Word 2007&#0;
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Producer: Microsoft® Office Word 2007&#0;
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Author: vstyran
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      ModDate: D:20090604160025
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      CreationDate: D:20090604160025
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      PdfID0: ec683aaa7b39e945a28671b9f538e9
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      PdfID1: ec683aaa7b39e945a28671b9f538e9
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      NumberOfPages: 3
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Итак, искать мы вроде как научились. Теперь давайте поищем что-нибудь по-интереснее.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      <b>$ pdftk CSG-V3.pdf dump_data | perl -ne &#8216;s/n$// if /^InfoKey:/; s/^InfoKey: //; s/^InfoValue//; print&#8217;</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Creator: <b>Acrobat PDFMaker 8.1</b> for Word
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Title: Small Businesses Practices
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Company: Carnegie Mellon University
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Producer: <b>Acrobat Distiller 8.1.0&nbsp;</b>(Windows)
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Author: <b>carolinev</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      ModDate: D:20090121131437-05&#8217;00&#8217;
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      SourceModified: D:20090121172942
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      CreationDate: D:20090121131408-05&#8217;00&#8217;
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      PdfID0: 3e74d4e723d11dc2a2711ef22c22f81
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      PdfID1: c661cfd5592c75479ec7d97d6f03be8
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Прекрасно, то что нужно. Тут вам и имя пользователя, и версии ПО. Еще один пример.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      <b>$ pdftk cisco_PCI.pdf dump_data | perl -ne &#8216;s/n$// if /^InfoKey:/; s/^InfoKey: //; s/^InfoValue//; print&#8217; | head -10</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Creator: <b>FrameMaker 7.2</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Title: roc.fm
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Producer: <b>Acrobat Distiller 7.0</b> (Windows)
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Author: <b>ctsadmin-p.gen</b>
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      ModDate: D:20090627001912Z
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      CreationDate: D:20090225103321Z
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      PdfID0: 1c6e1873d0e93de8a815d8d32ac2e4f5
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      PdfID1: ab27924169ec4db2dbe8d9a81ae2
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      NumberOfPages: 110
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      BookmarkTitle: Verizon Business Assessment for: Cisco PCI Solution for Retail: Cisco Systems, Inc.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Из имени пользователя очевидно, что Cisco захватили роботы.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Конечно, искать, сохранять PDF-файлы, а потом еще и скрипты писать для их анализа &#8212; занятие утомительное. К счастью, (1) мир не без добрых людей и (2) существует <b><a href="http://www.edge-security.com/metagoofil.php">metagoofil</a></b>. Эта прекрасная утилита на Питоне великолепно справляется с поиском файлов на сайте, их сохранением (!) и извлечением метаданных из документов различного формата. Для последнего в ней используется extract, так что поиграться с pdftk для PDF-файлов все равно придется. <b>Внимание!</b> Использование автоматических средств поиска идет в разрез с<b> Google Terms of Service</b>, так что будьте осторожны. Для сохранения status quo я должен уточнить, что упоминаю о metagoofil не для того, чтобы побудить вас к его использованию, а для того, чтобы подчеркнуть, как легко &#171;плохие парни&#187; могут получить доступ к вашим драгоценным метаданным (смайл вырезан цензурой).
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      В заключение, советую потренироваться в извлечении метаданных из файлов различных форматов. Напомню, что PDF был выбран мной в качестве примера и полной картинки не дает. &nbsp;Файлы MS Office содержат в себе больше &#171;полезной&#187; информации. Конвертация в PDF даже рекомендуется в качестве одного из методов сокрытия метаданных, коими изобилуют документы MS Office. Для удаления метаданных существует несколько решений как для персонального, так и для корпоративного использования (например, для очистки документов в исходящих электронных письмах). Рекламировать никого не буду, поиск по ключевым словам &#171;<b>metadata removal application</b>&#187; и так все покажет.
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
    </div>
  </div>
  
  <div>
    <div style="text-align: justify;">
      Всем удачных выходных.</p> 
      
      <p>
        <a href="http://securegalaxy.blogspot.com/search/label/metadata"><i>Больше о метаданных в этом блоге</i></a></div> </div> </div> 
        
        <div class="addtoany_share_save_container addtoany_content_bottom">
          <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_67">
            <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d1%2587%25d1%2582%25d0%25be-%25d1%2580%25d0%25b0%25d1%2581%25d1%2581%25d0%25ba%25d0%25b0%25d0%25b6%25d0%25b5%25d1%2582-metadata-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-ii-%25d1%2581%25d0%25b1%25d0%25be%25d1%2580-%25d0%25b4%25d0%25b0%25d0%25bd%25d0%25bd%25d1%258b%25d1%2585%2F&linkname=%D0%A7%D1%82%D0%BE%20%D1%80%D0%B0%D1%81%D1%81%D0%BA%D0%B0%D0%B6%D0%B5%D1%82%20metadata.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20II%3A%20%D0%A1%D0%B1%D0%BE%D1%80%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85." title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d1%2587%25d1%2582%25d0%25be-%25d1%2580%25d0%25b0%25d1%2581%25d1%2581%25d0%25ba%25d0%25b0%25d0%25b6%25d0%25b5%25d1%2582-metadata-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-ii-%25d1%2581%25d0%25b1%25d0%25be%25d1%2580-%25d0%25b4%25d0%25b0%25d0%25bd%25d0%25bd%25d1%258b%25d1%2585%2F&linkname=%D0%A7%D1%82%D0%BE%20%D1%80%D0%B0%D1%81%D1%81%D0%BA%D0%B0%D0%B6%D0%B5%D1%82%20metadata.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20II%3A%20%D0%A1%D0%B1%D0%BE%D1%80%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85." title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d1%2587%25d1%2582%25d0%25be-%25d1%2580%25d0%25b0%25d1%2581%25d1%2581%25d0%25ba%25d0%25b0%25d0%25b6%25d0%25b5%25d1%2582-metadata-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-ii-%25d1%2581%25d0%25b1%25d0%25be%25d1%2580-%25d0%25b4%25d0%25b0%25d0%25bd%25d0%25bd%25d1%258b%25d1%2585%2F&linkname=%D0%A7%D1%82%D0%BE%20%D1%80%D0%B0%D1%81%D1%81%D0%BA%D0%B0%D0%B6%D0%B5%D1%82%20metadata.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20II%3A%20%D0%A1%D0%B1%D0%BE%D1%80%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85." title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2009%2F11%2F%25d1%2587%25d1%2582%25d0%25be-%25d1%2580%25d0%25b0%25d1%2581%25d1%2581%25d0%25ba%25d0%25b0%25d0%25b6%25d0%25b5%25d1%2582-metadata-%25d1%2587%25d0%25b0%25d1%2581%25d1%2582%25d1%258c-ii-%25d1%2581%25d0%25b1%25d0%25be%25d1%2580-%25d0%25b4%25d0%25b0%25d0%25bd%25d0%25bd%25d1%258b%25d1%2585%2F&linkname=%D0%A7%D1%82%D0%BE%20%D1%80%D0%B0%D1%81%D1%81%D0%BA%D0%B0%D0%B6%D0%B5%D1%82%20metadata.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20II%3A%20%D0%A1%D0%B1%D0%BE%D1%80%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85." title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
          </div>
        </div>
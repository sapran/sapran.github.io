---
id: 1010
title: Безопасность точек доступа WiFi в Киеве
date: 2010-11-30T17:32:00+00:00
author: sapran
layout: post
guid: http://styran.com/2010/11/30/%d0%b1%d0%b5%d0%b7%d0%be%d0%bf%d0%b0%d1%81%d0%bd%d0%be%d1%81%d1%82%d1%8c-%d1%82%d0%be%d1%87%d0%b5%d0%ba-%d0%b4%d0%be%d1%81%d1%82%d1%83%d0%bf%d0%b0-wifi-%d0%b2-%d0%ba%d0%b8%d0%b5%d0%b2%d0%b5/
permalink: /2010/11/%d0%b1%d0%b5%d0%b7%d0%be%d0%bf%d0%b0%d1%81%d0%bd%d0%be%d1%81%d1%82%d1%8c-%d1%82%d0%be%d1%87%d0%b5%d0%ba-%d0%b4%d0%be%d1%81%d1%82%d1%83%d0%bf%d0%b0-wifi-%d0%b2-%d0%ba%d0%b8%d0%b5%d0%b2%d0%b5/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2010/11/wifi.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/2031021242681844543
shorturl:
  - http://tinyurl.com/psbhg2e
tags:
  - wifi
  - киев
---
Разрешите представить вашему вниманию результаты небольшого исследования. Несколько дней я, не жалея батареи в мобильном телефоне, собирал информацию о точках доступа беспроводной сети в городе Киеве. В итоге мной была собрана информация о 483 точках доступа WiFi, которая включала в том числе данные о типе шифрования настроенном на оборудовании. Не удивительно, что именно информация о защите беспроводных сетей интересовала вашего покорного слугу.

Далее следует &#171;сырая&#187; информация о типах защиты исследуемых точек доступа. Информация представлена в процентах от количества обнаруженных типов шифрования. (Поэтому, так как одна точка доступа может поддерживать два или даже три типа защиты, это количество получилось больше числа беспроводных сетей.)

<table align="center">
  <tr>
    <td>
      <b>Тип шифрования</b>
    </td>
    
    <td align="right">
      <b>Количество точек доступа, %</b>
    </td>
  </tr>
  
  <tr>
    <td>
      Шифрование отсутствует
    </td>
    
    <td align="right">
      3
    </td>
  </tr>
  
  <tr>
    <td>
      WEP
    </td>
    
    <td align="right">
      13
    </td>
  </tr>
  
  <tr>
    <td>
      WPA-PSK-CCMP
    </td>
    
    <td align="right">
      3
    </td>
  </tr>
  
  <tr>
    <td>
      WPA-PSK-TKIP
    </td>
    
    <td align="right">
      28
    </td>
  </tr>
  
  <tr>
    <td>
      WPA-PSK-TKIP+CCMP
    </td>
    
    <td align="right">
      12
    </td>
  </tr>
  
  <tr>
    <td>
      WPA2-PSK-CCMP
    </td>
    
    <td align="right">
      9
    </td>
  </tr>
  
  <tr>
    <td>
      WPA2-PSK-TKIP
    </td>
    
    <td align="right">
      18
    </td>
  </tr>
  
  <tr>
    <td>
      WPA2-PSK-TKIP+CCMP
    </td>
    
    <td align="right">
      14
    </td>
  </tr>
</table>

<div>
  Для того, чтобы связать полученные результаты с количеством точек доступа, я обобщил информацию о шифровании и сделал следующие выводы.
</div>

<div>
  <ul>
    <li>
      26% точек доступа настроены на использование слабого протокола защиты, или же предоставляют открытый доступ и не используют шифрование.
    </li>
    <li>
      68% точек доступа настроены с использованием потенциально небезопасного протокола шифрования. Например, существует метод практической атаки на точку доступа, в которой используется шифрование типа WPA-PSK-TKIP и при этом настроены параметры <a href="http://ru.wikipedia.org/wiki/QoS">Quality of Service</a> (QoS).
    </li>
    <li>
      68% (да, вот такое совпадение) точек доступа настроены с использованием надежных методов шифрования, и в случае выбора администратором сильного пароля могут предоставлять безопасное подключение.
    </li>
  </ul>
  
  <div>
    (По той же причине &#8212; методов шифрования больше, чем точек доступа &#8212; процентные показатели в сумме дают число большее 100%.)
  </div>
</div>

<div>
</div>

<div>
  Общий результат, даже с учетом погрешности (число рассмотренных беспроводных сетей все-таки очень скромное), я считаю удовлетворительным. Я надеюсь продолжить сбор информации и со&nbsp;временем&nbsp;уточнить и улучшить качество этих результатов.
</div>

<div>
</div>

<div>
  Под занавес, несколько забавных фактов.
</div>

<div>
  <ul>
    <li>
      Почти треть имен точек доступа настроены по умолчанию. И да &#8212; dlink лидирует.
    </li>
    <li>
      Несколько имен точек доступа выглядели как номера мобильных телефонов. Судя по всему, они там давно, так как начинаются с восьмерки.
    </li>
    <li>
      Всего 8% обнаруженных точек доступа используют методы аутентификации корпоративного уровня.
    </li>
  </ul>
  
  <div>
    Очень полезную глобальную статистику можно посмотреть на&nbsp;<a href="http://wigle.net/gps/gps/main/stats/">этом сайте</a>.&nbsp;
  </div>
</div>

<div class="addtoany_share_save_container addtoany_content_bottom">
  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_131">
    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F11%2F%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d1%2582%25d0%25be%25d1%2587%25d0%25b5%25d0%25ba-%25d0%25b4%25d0%25be%25d1%2581%25d1%2582%25d1%2583%25d0%25bf%25d0%25b0-wifi-%25d0%25b2-%25d0%25ba%25d0%25b8%25d0%25b5%25d0%25b2%25d0%25b5%2F&linkname=%D0%91%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D1%82%D0%BE%D1%87%D0%B5%D0%BA%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20WiFi%20%D0%B2%20%D0%9A%D0%B8%D0%B5%D0%B2%D0%B5" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F11%2F%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d1%2582%25d0%25be%25d1%2587%25d0%25b5%25d0%25ba-%25d0%25b4%25d0%25be%25d1%2581%25d1%2582%25d1%2583%25d0%25bf%25d0%25b0-wifi-%25d0%25b2-%25d0%25ba%25d0%25b8%25d0%25b5%25d0%25b2%25d0%25b5%2F&linkname=%D0%91%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D1%82%D0%BE%D1%87%D0%B5%D0%BA%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20WiFi%20%D0%B2%20%D0%9A%D0%B8%D0%B5%D0%B2%D0%B5" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F11%2F%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d1%2582%25d0%25be%25d1%2587%25d0%25b5%25d0%25ba-%25d0%25b4%25d0%25be%25d1%2581%25d1%2582%25d1%2583%25d0%25bf%25d0%25b0-wifi-%25d0%25b2-%25d0%25ba%25d0%25b8%25d0%25b5%25d0%25b2%25d0%25b5%2F&linkname=%D0%91%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D1%82%D0%BE%D1%87%D0%B5%D0%BA%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20WiFi%20%D0%B2%20%D0%9A%D0%B8%D0%B5%D0%B2%D0%B5" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2010%2F11%2F%25d0%25b1%25d0%25b5%25d0%25b7%25d0%25be%25d0%25bf%25d0%25b0%25d1%2581%25d0%25bd%25d0%25be%25d1%2581%25d1%2582%25d1%258c-%25d1%2582%25d0%25be%25d1%2587%25d0%25b5%25d0%25ba-%25d0%25b4%25d0%25be%25d1%2581%25d1%2582%25d1%2583%25d0%25bf%25d0%25b0-wifi-%25d0%25b2-%25d0%25ba%25d0%25b8%25d0%25b5%25d0%25b2%25d0%25b5%2F&linkname=%D0%91%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D1%82%D0%BE%D1%87%D0%B5%D0%BA%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20WiFi%20%D0%B2%20%D0%9A%D0%B8%D0%B5%D0%B2%D0%B5" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
  </div>
</div>
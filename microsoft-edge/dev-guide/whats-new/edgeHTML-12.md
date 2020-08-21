---
description: На этой странице представлен обзор новых возможностей Microsoft EdgeHTML 12.
title: Новые функции и API в Microsoft EdgeHTML 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 51c5c89b8ae4ea0e02de68f6b413c162336661f6
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941953"
---
# Новые возможности в EdgeHTML 12  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge представляет microsoft EdgeHTML — новый модуль с инженером на совместимости с базовыми возможностями, чтобы гарантировать наличие актуальной и наиболее наиболее популярной веб-платформы Windows.  Microsoft Edge дает чистый перерыв из старых версий, необходим для поддержки элементов управления ActiveX, объектов помощника браузера \(BHOS\) и других методик разработки веб-страниц.  Кроме того, Microsoft Edge поддерживает внутреннюю поддержку PDF-файлов.  По состоянию IE11 устаревшие режимы документов не рекомендуется использовать, а в Microsoft Edge инфраструктура браузера не поддерживают их.  Дополнительные сведения см. в [IEBlog.](/archive/blogs/ie/living-on-the-edge-our-next-step-in-interoperability)  

Ниже перечислены изменения, публикуемые вместе с EdgeHTML 12 в первом выпуске [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) \(07.07.2015, сборка 10240\).  Общие сведения об изменениях браузеров Microsoft Edge см. в прошлом браузере Microsoft Edge: старший модуль Microsoft создан ный инженер нового [веб-приложения Майкрософт](https://blogs.windows.com/msedgedev/2015/02/26) [и а) от прошлого, часть 2: "Продажа хорошо до ActiveX, VBScript, attachEvent...](https://blogs.windows.com/msedgedev/2015/05/06)  

Вот как и вот такая перечень изменений. [https://aka.ms/devguide_edgehtml_12](./edgehtml-12.md)  

## Новые возможности  

### Политика безопасности содержимого 1.0  

Microsoft Edge теперь реализует политику безопасности содержимого \(CSP\) 1.0.  Стандарт безопасности облачных служб позволяет разработчикам контролируйте ресурсы \(сценарий, CSS, подключаемые модули, изображения, т. е. и т. д.), которая может выполнять ся с аналогичным и запуском перекрестных веб-сайтов или механизмов перекрестного кода.  Дополнительные сведения [об CSP](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Content_Security_Policy) в Microsoft Edge см. в политике безопасности содержимого.  

### Эффекты фильтра  

Microsoft Edge предоставляет простой способ добавления визуальных эффектов к элементам.  С `filter` помощью свойств можно добавлять размытия, настроить яркость, добавить тень, изменить продолжительность и многое другое для элемента.  Используя формат CSS, к одному элементу можно применить несколько эффектов фильтра к одному элементу и анимировать фильтры.  Дополнительные сведения см. в статье ["Применение фильтра".](https://developer.mozilla.org/docs/Web/CSS/filter)  

### JavaScript  

Поддержка JavaScript немного отличается от окончательной версии Браузера Internet Explorer \(IE11\) и Microsoft Edge.  В нем относятся следующие новые возможности в Edge.  

:::row:::
   :::column span="1":::
      **Выписки**  
   :::column-end:::
   :::column span="2":::
      [class](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) \(экспертальный\) [для... из](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Объекты**  
   :::column-end:::
   :::column span="2":::
      [Promise,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise) [Proxy,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) [Symbol,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol) [WeakSet](/scripting/javascript/reference/weakset-object-javascript)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Функции**  
   :::column-end:::
   :::column span="2":::
      [acosh,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh) [codePointAt,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat) [fromCodePoint,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint) [hypot,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot) [imul,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul) [isInteger,](/scripting/javascript/reference/number-isinteger-function-number-javascript) [isNaN,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan) [raw](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Методы**  
   :::column-end:::
   :::column span="2":::
      [включает:](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes) [ключи](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) \(массив\), повтор\(String\), [значения](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) \(массив\) [repeat](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Другие возможности**  
   :::column-end:::
   :::column span="2":::
      [Функции](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) \(экспериментальные\), [генерации,](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators)  [итерации,](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators) [пометка обычных `y` ](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) выражений \(экспериментальные\), [строки шаблона,](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals) [точка esicode point scape character scape character](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals)  
   :::column-end:::
:::row-end:::  

Сравнение поддержки JavaScript в приложениях Internet Explorer, Microsoft Edge и Microsoft Store см. в сведениях о [версии JavaScript.](./javascript-version-information.md)  

### Media Capture и Streams  

Реализует поддержку камер мультимедиа и API-каналов на основе [спецификации W3C Media Capture и Streams.](https://w3c.github.io/mediacapture-main/getusermedia.html)  Эти API JavaScript позволяют веб-страницам получать доступ к устройствам захвата, таким как веб-камеры и микрофоны, с разрешением пользователя.  С помощью API media Capture и Streams можно создавать сценарии, например запись с помощью веб-камеры или захвата голосового сообщения с микрофона.  Дополнительные сведения о медиаданных capture в Microsoft Edge в [блоге разработчика Microsoft Edge.](https://blogs.windows.com/msedgedev/2015/05/13)  

### Новый элемент и атрибуты HTML  

*   `meter` элемент  
*   `picture` элемент  
*   `template` элемент  
*   `image` элемент: `srcset` и `sizes` атрибуты \(запись блога [разработчика](https://blogs.windows.com/msedgedev/2015/06/08)Microsoft Edge ))  
*   `selectionDirection` attribute  
*   `input type=time` и `input type=datetime-local`  

### Object RTC API  

Функция "Объектное временный режим" позволяет передавать файлы с помощью мультимедиа \(аудио или видео\) в режиме реального времени напрямую между веб-браузерами, мобильными устройствами и серверами через Собственный API JavaScript.  Дополнительные сведения о ORTC в Microsoft Edge см. в руководстве [по теме RTC RTC.](https://ortc.org)  

### Режим чтения  

В Microsoft Edge есть режим чтения, чтобы упростить чтение веб-страниц, как благодаря неотвлекающему нежелательному содержимому на странице.  Режим чтения можно включать и выключать с помощью кнопки чтения \(значка книги\) в адресной строке или с `Ctrl` + `Shift` + `R` ней.  Дополнительные сведения см. [в режиме](../browser-features/reading-view.md) чтения.  

### Обнаружение службы поиска  

Интеграция с поддержкой поиска встроена в адресную строку Microsoft Edge, включая предложения для поиска, результаты из Интернета, журнал браузера и избранное.  Microsoft Edge использует [спецификацию OpenSearch 1.1,](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) чтобы найти и использовать поставщики поиска в Интернете.  Если вы являетесь поставщиком поиска, [прочтите дополнительные](../browser-features/search-provider-discovery.md) сведения о том, как убедиться, что Microsoft Edge поддерживает вашу службу.  

### Поддержка API WebKit aPI WebKit  

Для улучшения совместимости Microsoft Edge поддерживает различные `-webkit-` API префикса.  Полный список поддерживаемых `-webkit-` API можно использовать [каталог API.](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit)  

### Аудиозапись  

Microsoft Edge предлагает поддержку спецификации [API веб-аудиоконференции W3C веб-канала W3C.](https://webaudio.github.io/web-audio-api)  Web Audio — это API JavaScript, работающий с интерфейсом JavaScript, который обеспечивает более широкий интерфейс звука и музыкального интерфейса.  Хотя он позволяет воспроизводить потоковую передачу звука, интерфейс API веб-аудиосвязи предоставляет разные возможности aPI, позволяющие воспроизводить несколько звуков с контролем `audio` синхронизации и применять галочки, феймы, переходы и базовые эффекты к смешанному звуку.  Подробнее о [Web Audio](... /multimedia/web-audio.md в руководстве Devide и в [блоге Разработчика Microsoft Edge.](https://blogs.windows.com/msedgedev/2015/05/19)  

### веб-драйвер  

[API WebDriver —](https://w3.org/TR/webdriver) это платформа и интерфейс, неявный интерфейс, и протоколы, позволяющие контролировать работу веб-браузера.  WebDriver позволяет разработчикам создавать автоматизированные тесты, которые хорошо интересуют взаимодействие с пользователем.  Этот процесс отличается от тестов JavaScript unit, так как у WebDriver есть доступ к функциям и сведениям, запущенным в браузере, не и может более точно просматривать события пользователя или события на уровне освобождения.  WebDriver также может управлять тестированием нескольких окон, вкладок и веб-страниц в одном тестовое сеансе.  Дополнительные сведения о том, как начать работу с WebDriver для Microsoft Edge, см. в [веб-диспетчере веб-диспетчера веб-диспетчера веб-диспетчера веб-диспетчера веб-дис](../../webdriver.md)  

## Новый API в Microsoft EdgeHTML 12  

Ниже приведен полный список новых интерфейсов API в Microsoft EdgeHTML 12.  Они указаны в `[interface name].[api name]` формате.  

 > [!NOTE] 
 > Многие из этих API доступны в IE11.  Приведенные ниже данные для EdgeHTML 12 предлагаются в качестве базового плана для сравнения исходных версий EdgeHTML с последующими версиями.  

<iframe height='580' scrolling='no' title='Новый API в Microsoft EdgeHTML 12' src='//codepen.io/MicrosoftEdgeDocumentation/embed/pPOwby/?height=580&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. статью <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'> "Новый API" в Microsoft </a> EdgeHTML 12, используя документы Microsoft Edge <a href='https://codepen.io/MicrosoftEdgeDocumentation'> </a> (@MicrosoftEdgeDocumentation) на <a href='https://codepen.io'> коде Кодировки. </a></iframe>  

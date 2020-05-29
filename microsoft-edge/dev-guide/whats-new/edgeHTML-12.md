---
description: На этой странице представлены общие сведения о новых возможностях EdgeHTML 12.
title: Новые возможности в EdgeHTML 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: f16db0551d4bea3d29b974c2a35fff2adf476c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570889"
---
# Новые возможности в EdgeHTML 12

В Microsoft Edge появился EdgeHTML, новый "живых" обработчик, разработанный для взаимодействия, чтобы гарантировать, что вы всегда получаете новейшую и самую новую веб-платформу Windows. Microsoft EDGE представляет собой четкий перерыв за последнюю, бесплатный из устаревшего кода, необходимого для поддержки элементов управления ActiveX, вспомогательных объектов браузера (BHO) и других методов разработки веб-приложений ByGone. Кроме того, Microsoft EDGE обеспечивает поддержку встроенного PDF-файла. По мере IE11 устаревшие режимы документов устарели, и в Microsoft Edge инфраструктура браузера для их поддержки не существует. Для получения дополнительных сведений ознакомьтесь с [IEBlog](https://go.microsoft.com/fwlink/p/?LinkID=519011) .

Ниже приведены изменения, которые отгружаются с помощью EdgeHTML 12 в первоначальном выпуске [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) (07/2015, сборка 10240). Общие сведения об изменениях, внесенных в общий браузер Microsoft EDGE, можно найти в разделе [перерыв за прошедший: создание нового обработчика веб-отрисовки (Майкрософт](https://blogs.windows.com/msedgedev/2015/02/26/a-break-from-the-past-the-birth-of-microsofts-new-web-rendering-engine/) ) и [перерыв от прошлого, часть 2: как и в случае с элементами ActiveX, VBScript, attachEvent...](https://blogs.windows.com/msedgedev/2015/05/06/a-break-from-the-past-part-2-saying-goodbye-to-activex-vbscript-attachevent/).

Ниже приведен список постоянных [https://aka.ms/devguide_edgehtml_12](https://aka.ms/devguide_edgehtml_12) изменений.


## Новые возможности

### Политика безопасности содержимого 1,0
Microsoft EDGE теперь реализует политику безопасности содержимого (CSP) 1,0. Стандарт безопасности CSP позволяет веб-разработчикам управлять ресурсами (сценариями, CSS, подключаемыми модулями, изображениями и т. д.), в которых определенная страница может получить или выполниться с целью предотвращения атак с помощью межсайтовых сценариев (XSS), clickjacking и других операций внедрения кода для выполнения вредоносного содержимого в контексте надежной веб-страницы. Дополнительные сведения о поставщиках служб шифрования в Microsoft EDGE можно узнать в этой [политике безопасности контента](https://docs.microsoft.com/microsoft-edge/dev-guide/security/content-security-policy) . 

### Эффекты фильтров
Microsoft EDGE обеспечивает простой способ добавления визуальных эффектов к элементам. С помощью `filter` свойства можно добавить размытие, настроить яркость, добавить тени, изменить прозрачность и другие элементы. С помощью чистого CSS можно применить несколько эффектов фильтра к одному элементу и анимировать фильтры. Дополнительные сведения можно найти в разделе [эффекты фильтров](https://docs.microsoft.com/microsoft-edge/dev-guide/css/filter-effects).

### JavaScript
Поддержка JavaScript немного различается между финальной версией Internet Explorer (IE11) и Microsoft Edge. Новые функции в EDGE включают:

| | |
|--|--|
|**Выписки**| [класс](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) (экспериментальный), [for... из](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) |
|**Object**| [Обещание](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise), [прокси](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy), [символ](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [слабый](/scripting/javascript/reference/weakset-object-javascript) |
|**Функции** | [ACOSH](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh), [codePointAt](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat), [fromCodePoint](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint), [hypot](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot), [imul](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul), [целое](/scripting/javascript/reference/number-isinteger-function-number-javascript), [IsNaN](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan), [RAW](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw) |
|**Методы**| [включает в себя](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes) [разделы](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) (массив), [Repeat](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) (строка), [Values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) (массив). |
|**Другие возможности**| [Функции](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) (экспериментальные), [генераторы](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [итераторы](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [ `y` Пометка регулярных выражений](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) (экспериментальные), [строки шаблонов](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals), [escape-символы кодовой точки Юникода](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals) |

Для сравнения поддержки JavaScript через Internet Explorer, Microsoft EDGE и приложения Microsoft Store ознакомьтесь со [*сведениями о версии JavaScript*](./javascript-version-information.md).

### Запись мультимедиа и потоки
Microsoft EDGE обеспечивает поддержку API захвата мультимедиа и потоковых данных на основе спецификаций [захвата мультимедиа W3C и Streams](https://go.microsoft.com/fwlink/p/?LinkID=534096) . Эти API JavaScript разрешают веб-страницам доступ к устройствам захвата мультимедиа, таким как смартфоны или микрофоны, с разрешениями пользователя. Используя API захвата и потоковой передачи мультимедиа, вы можете создавать сценарии, такие как захват фотографий с помощью веб-камеры или захват голосового сообщения с микрофона. Ознакомьтесь с дополнительными сведениями о захвата мультимедиа в Microsoft EDGE в [блоге разработчиков Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/13/announcing-media-capture-functionality-in-microsoft-edge/). 

### Создание HTML-элемента и атрибутов
* `meter` элемент
* `picture` элемент
* `template` элемент
* `image` элемент: `srcset` и `sizes` атрибуты ( [запись блога](https://blogs.windows.com/msedgedev/2015/06/08/introducing-srcset-responsive-images-in-microsoft-edge/)разработчика Microsoft EDGE)
* `selectionDirection` attribute
* `input type=time` и `input type=datetime-local`

### API объекта RTC 
Объектная связь в реальном времени (ORTC) обеспечивает потоковую передачу мультимедиа (звуковых и видеофайлов) в реальном времени напрямую между веб-браузерами, мобильными устройствами и серверами с помощью собственных API JavaScript. Дополнительные сведения о том, как ORTC в Microsoft EDGE, можно найти в руководстве разработчика "раздел" [объект API RTC](https://docs.microsoft.com/microsoft-edge/dev-guide/realtime-communication/object-rtc-api) . 

### Режим чтения
Microsoft Edge предоставляет представление для чтения для более удобной работы с веб-страницами, так же как и без отзыва несвязанных или других вспомогательных материалов на странице. Режим чтения можно включить или отключить из режима чтения (значка книги) в адресной строке (или с помощью сочетания клавиш Ctrl + Shift + R). Дополнительные сведения можно найти в статье [режим чтения](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/reading-view) . 

### Обнаружение поставщика поиска
Расширенная интеграция поиска встроена в адресную строку Microsoft EDGE, в том числе варианты поиска, результаты из Интернета, журнал браузера и Избранное. Microsoft Edge использует спецификацию [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) для поиска и использования веб-служб поиска. Если вы являетесь поставщиком поиска, [Ознакомьтесь с дополнительными](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/search-provider-discovery) сведениями о том, как обеспечить поддержку службой Microsoft Edge. 

### Поддержка API WebKit
Для улучшенной совместимости Microsoft EDGE поддерживает различные предустановленные API с префиксом "-WebKit-". Полный список поддерживаемых API "-WebKit-" можно получить с помощью [каталога API](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit).

### Веб-звук
Microsoft EDGE поддерживает спецификацию [API аудиоподсистемы консорциума W3C](https://go.microsoft.com/fwlink/p/?LinkID=512167) . Веб-звук — это высокоуровневая API JavaScript для обработки и создания звуковых файлов в веб-приложениях, обеспечивающих богатые возможности голосовой и музыкальной связи. Несмотря на то `audio` , что элемент HTML5 поддерживает простое воспроизведение потокового звука, API веб-звука предоставляет широкий набор API, позволяющих воспроизводить несколько звуков с помощью более плотной синхронизации, а также применять функции выигрыша, исчезновения, переходов и базовые эффекты для смешанного звука. Ознакомьтесь с дополнительными сведениями о [веб-звуке](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/web-audio) в руководстве разработчика и в [блоге разработчиков Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/19/bringing-web-audio-to-microsoft-edge-for-interoperable-gaming-and-enthusiast-media/). 

### Веб-драйвер 
API веб- [накопителей W3C](https://w3.org/TR/webdriver/) — это платформа и независимый от языка интерфейс и протокол проводной связи, позволяющая программам и сценариям управлять поведением браузера. С помощью этого устройства разработчики могут создавать автоматические тесты, имитирующие взаимодействие с пользователем. Это отличается от модульных тестов JavaScript, поскольку веб-дисковод имеет доступ к функциональным возможностям и сведениям, которые JavaScript запускается в браузере, и может более точно имитировать события пользователей и события на уровне операционной системы. Кроме того, веб-дисковод также может управлять тестированием между несколькими окнами, вкладками и страницами в одном тестовом сеансе.  Для получения дополнительных сведений о том, как приступить к работе с веб диском Microsoft Edge [, ознакомьтесь со статьей.](https://docs.microsoft.com/microsoft-edge/dev-guide/tools/webdriver) 


## Новые API-интерфейсы в EdgeHTML 12

Ниже приведен полный список новых API-интерфейсов в EdgeHTML 12.  Они указаны в формате **[имя интерфейса]. [ Имя API]**.

 > [!NOTE] 
 > Многие из этих API были доступны в IE11. Приведенные ниже данные для EdgeHTML 12 предлагаются как базовые показатели для сравнения начальной версии EdgeHTML и более поздних версий.

<iframe height='580' scrolling='no' title='Новые API-интерфейсы в EdgeHTML 12' src='//codepen.io/MicrosoftEdgeDocumentation/embed/pPOwby/?height=580&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Ознакомьтесь с <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'> новыми API-интерфейсами в EdgeHTML 12 </a> по Microsoft Edge Docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) на <a href='https://codepen.io'> CodePen </a> .</iframe>

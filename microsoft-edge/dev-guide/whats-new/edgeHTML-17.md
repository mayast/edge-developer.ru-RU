---
title: Новые функции и API-интерфейсы в EdgeHTML 17
description: В этом руководстве вы найдете общие сведения о функциях и стандартах разработчика, включенных в EdgeHTML 17.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: 1359464bfb9ec6f2b84536a11b0fb4bfcce2fb1c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570912"
---
# Новые возможности EdgeHTML 17

Ниже приведен список новых и обновленных функций, выпущенных на веб-платформах [EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/04/30/edgehtml-17-april-2018-update/) в рамках [обновления Windows 10 апреля 2018](https://blogs.windows.com/windowsexperience/2018/04/27/make-the-most-of-your-time-with-the-new-windows-10-update/) (04/2018, сборка 17134). Изменения в конкретных сборках [Insider](https://insider.windows.com/) Preview для Windows можно найти в [журнале изменений Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog/) и [о новых](../whats-new.md)возможностях EdgeHTML.

Ниже приведен список постоянных [https://aka.ms/devguide_edgehtml_17](https://aka.ms/devguide_edgehtml_17) изменений.

## Новые и обновленные функции 

### Роли, состояния и события ARIA 1,1

EdgeHTML 17 добавляет поддержку различных ролей, состояний и свойств из [специальных возможностей Интернет-приложений с богатыми возможностями (помощью ориентиров WAI-ARIA) 1,1](https://w3.org/TR/wai-aria-1.1/), включая [канал](https://www.w3.org/TR/wai-aria-1.1/#feed), [форму](https://www.w3.org/TR/wai-aria-1.1/#form), [aria-haspopup](https://w3.org/TR/wai-aria-1.1/#aria-haspopup), [ARIA-заполнитель](https://w3.org/TR/wai-aria-1.1/#aria-placeholder)и многое другое. Найдите [полный список обновлений ARIA в журнале изменений](https://developer.microsoft.com/microsoft-edge/platform/changelog/desktop/17134/?compareWith=16299). Благодаря этому обновлению EdgeHTML 17 теперь поддерживаются все роли и атрибуты, определенные в помощью ОРИЕНТИРОВ WAI-ARIA 1,1. Дополнительные сведения о специальных возможностях в Microsoft Edge вы узнаете в документах [специальных возможностей](https://docs.microsoft.com/microsoft-edge/accessibility) .

### Маскирование CSS

EdgeHTML 17 включает экспериментальную поддержку для [масок CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking). Частичная реализация содержит свойства " [Маска](https://developer.mozilla.org/docs/Web/CSS/mask-image) CSS" — "изображение" и " [размер маски](https://developer.mozilla.org/docs/Web/CSS/mask-size) ".  Установите флажок Включить Маскирование стилей CSS в разделе about: flags для экспериментов!

### Преобразования CSS для элементов SVG

EdgeHTML 17 теперь поддерживает преобразования CSS для элементов SVG и атрибутов представления. Это позволяет визуально манипулировать элементами SVG, в том числе вращение, масштабирование, перемещение, наклон и сдвиг. 

### Расширения 

Microsoft EDGE теперь поддерживает [API уведомлений](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) , в котором выводятся уведомления из расширений. Теперь разработчики расширений могут создавать различные типы уведомлений (базовый, список, изображение и т. д.), которые поддерживают полную взаимодействие с пользователем. Уведомления также автоматически регистрируются в центре уведомлений. Обратитесь к [примеру уведомлений](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/notifications/notifications) об использовании этого API в расширении.

EdgeHTML 17 теперь также поддерживает `Tabs.reload()` метод как часть стандартного класса API вкладок. Кроме того, Новая возможность в Windows 10 апреля 2018 позволяет пользователям разрешать выполнение расширений во время просмотра InPrivate.

Дополнительные сведения об обновлениях расширений в этом выпуске заголовков в блоге, посвященных новым возможностям, которые можно узнать [в разделе "расширения" в обновлении для Windows 10 апреля 2018](https://blogs.windows.com/msedgedev/2018/05/24/new-extension-features-april-2018-update-notifications-inprivate/).

### DevTools
Этот выпуск DevTools поставляется двумя способами: в качестве традиционных `F12` инструментов для Microsoft EDGE и предварительного просмотра в виде автономного [приложения для Windows 10](../../devtools-guide/whats-new/edgehtml-17.md#microsoft-edge-devtools-app-preview) из Microsoft Store!

![Приложение Microsoft Edge DevTools](../../devtools-protocol/media/microsoft-edge-devtools.png) 

Эти средства также были обновлены с учетом ряда основных функций, в том числе базовой поддержки [удаленной отладки](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol) (с помощью нашего нового [протокола DevTools](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol)), [функций отладки PWA](../../devtools-guide/whats-new/edgehtml-17.md#pwa-debugging), [управления IndexedDB кэша](../../devtools-guide/whats-new/edgehtml-17.md#indexeddb-inspection), [вертикальной стыковки](../../devtools-guide/whats-new/edgehtml-17.md#docking-to-the-right-in-microsoft-edge) и других возможностей. Кроме того, мы постараемся, что все операции [рефакторинга](./edgehtml-16.md) , направленные на Последнее уничтожение, были запущены в рамках текущих инвестиций в производительность и надежность.

Для получения дополнительных сведений посетите [DevTools в новейшем обновлении Windows 10 (EdgeHTML 17)](../../devtools-guide/whats-new/edgehtml-17.md) .

### JavaScript

С помощью EdgeHTML 17 обработчик JavaScript Chakra вводит улучшения производительности в несколько ключевых областей:

**Место для рационального объема памяти**

 - (Повторно) откладывание синтаксического анализа для [функций со стрелками](https://github.com/Microsoft/ChakraCore/pull/4105) и [методов для литеральных объектов](https://github.com/Microsoft/ChakraCore/pull/4136)
 - [Реструктуризация байт-кода RegExp](https://github.com/Microsoft/ChakraCore/pull/3915)

**Более быстрые встроенные надстройки JavaScript**

 - [Ввод общего типа для Object. Create](https://github.com/Microsoft/ChakraCore/pull/3901)
 - [Однострочный кэш с полиморфизмом для объекта. Assign (назначение)](https://github.com/Microsoft/ChakraCore/pull/3792)
 - [Оптимизации JSON. Parse и stringify](https://github.com/Microsoft/ChakraCore/pull/4077)
 - [Перезапись итераторов массивов в JavaScript и более быстрая для... из](https://github.com/Microsoft/ChakraCore/pull/4095)

**Веб-сборка**

 - [Поддержка по поддержке](https://github.com/Microsoft/ChakraCore/pull/3681) 

Ознакомьтесь с [*улучшенной производительностью JavaScript и EdgeHTML для всех данных в разделе 17*](https://blogs.windows.com/msedgedev/2018/06/19/improved-javascript-webassembly-performance-edgehtml-17/#I4vzUJK2va54kSWl.97) .

### Элемент мультимедиа

EdgeHTML 17 включает обновления для [HTMLMediaElement](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) , включая:
* Новый `preload` атрибут [`<media>`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) элемента указывает, какие данные должны быть предварительно загружены.
* [`setSinkId()`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/setSinkId)Метод и [`sinkId`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/sinkId) свойство позволяют разработчикам выбирать Выходное звуковое устройство. (**Примечание**. еще не AVAIABLE в RTC)

### API захвата мультимедиа 
Microsoft EDGE теперь поддерживает функцию захвата экрана на часах через [API захвата мультимедиа](https://w3c.github.io/mediacapture-screen-share/). Эта функция позволяет веб-страницам записывать выходные данные устройства отображения пользователя, обычно используемые для широковещательного показа виртуальных собраний и презентаций на рабочем столе.

### Прогрессивные веб-приложения
Начиная с EdgeHTML 17, сотрудники обслуживания и Push-уведомления включены по умолчанию (Дополнительные сведения об этих функциях можно найти в сотруднике службы записи блога. вы [выходите за пределы страницы](https://blogs.windows.com/msedgedev/2017/12/19/service-workers-going-beyond-page/). Это завершает набор технологий (в том числе получение доступа к сети и API push-и кэша), который содержит техническую основу для последовательного веб-приложения (PWAs) в Windows 10.

PWAs — это веб-приложения, которые [последовательно дополнены](https://en.wikipedia.org/wiki/Progressive_enhancement) функциями поддержки платформ и браузеров, таких как установка/начальная загрузка экрана, Автономная поддержка и Push-уведомления. В Windows 10 с ядром Microsoft EDGE (EdgeHTML) PWAs наслаждайтесь дополнительным преимуществом работы независимо от окна браузера в качестве [универсальных приложений платформы Windows](https://docs.microsoft.com/windows/uwp/get-started/whats-a-uwp) .

Помимо PWAs, сотрудники службы и API кэша позволяют разработчикам перехватывать сетевые запросы и отвечать на них. На веб-сайте не должно быть даже полного предохранителя, чтобы получить доступ к кэшированию рабочих процессов служб для точной и tinedной нагрузки и надежности, а также возможность работать в автономном режиме при отсутствии подключения к Интернету или плохое качество связи.  

Загляните в наши [прогрессивные веб-приложения в документах Windows](../../progressive-web-apps-edgehtml/index.md) , чтобы узнать больше о сотрудниках служб и сведения о PWAs в Windows 10.

### Веб-безопасность
EdgeHTML 17 предоставляет поддержку для обеспечения целостности подресурсов (Шри). [Целостность подресурсов](https://developer.mozilla.org/docs/Web/Security/Subresource_Integrity) — это функция предложенный, которая позволяет браузерам проверять, что извлеченные ресурсы (например, изображения, сценарии, шрифты и т. д.) доставляются без непредвиденных манипуляций. 

Добавьте `integrity` атрибут, содержащий криптографическое хэш-представление ресурса, который вы хотите загрузить на веб-страницу, в `<script>` `<link>` элемент OR, как показано в примере ниже. Затем Microsoft Edge будет сравнивать запрошенный ресурс с хэшем, определенным в `integrity` атрибуте. Если они не совпадают, Microsoft EDGE не будет выполнять ресурс и возвращает ошибку в сеть.

```html
<script src="https://example.com/example-framework.js" 
        integrity="sha384-Li9vy3DqF8tnTXuiaAJuML3ky+er10rcgNR/VqsVpcw+ThHmYcwiB1pbOxEbzJr7" 
        crossorigin="anonymous"></script>
```

Кроме того, в EdgeHTML 17 заголовок запроса " [Обновление — небезопасные запросы](https://developer.mozilla.org/docs/Web/HTTP/Headers/Upgrade-Insecure-Requests) " позволяет браузерам запрашивать безопасный режим работы с Интернет-интерфейсом. Этот заголовок сообщает серверу, что браузер поддерживает обновление любых небезопасных запросов, и пользователь должен перенаправить его в защищенную версию сайта (если она доступна).

### Переменные шрифты
В EdgeHTML 17 поддерживаются все переменные шрифты (в том числе стили CSS [-параметров](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings) и [Шрифт-изменение размера](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings)). Переменные шрифты позволяют разработчикам добиться взгляда на казаться разными шрифтами с одним шрифтом, настраивая различные оси, уменьшая потребность в нескольких файлах шрифтов и повышение производительности.

Присоединяйтесь к нам по [Expedition, чтобы узнать о том, какие переменные шрифты предоставляют веб-разработчики и дизайнеры](https://developer.microsoft.com/microsoft-edge/testdrive/demos/variable-fonts/), и как их использовать на своем сайте. И Читайте больше о переменных шрифтах в записи блога, [применяя выразительный и качественный типографский доступ к Microsoft Edge с переменными шрифтами](https://blogs.windows.com/msedgedev/2018/03/13/bringing-expressive-performant-typography-to-microsoft-edge-with-variable-fonts/).

<iframe height='456' scrolling='no' title='Примеры билетов приливов' src='//codepen.io/MSEdgeDev/embed/dmYvWg/?height=456&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><a href='https://codepen.io/MSEdgeDev/pen/dmYvWg/'>Приливов </a> с MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) в <a href='https://codepen.io'> CodePen, ознакомьтесь с примерами билета </a> .</iframe>

## Новые API-интерфейсы в EdgeHTML 17

Ниже приведен полный список новых API-интерфейсов в EdgeHTML 17. Они указаны в формате [имя интерфейса]. [имя API].

> [!NOTE] 
> Несмотря на то что в DOM используются следующие API-интерфейсы, поведение некоторых из них может по-прежнему находиться в разработке. Для официального приложения Word о поддержке функций вы можете обратиться к [Microsoft Edge Platform Status](https://developer.microsoft.com/microsoft-edge/platform/status/) .

<iframe height='580' scrolling='no' title='Новые API-интерфейсы в EdgeHTML 17' src='//codepen.io/MSEdgeDev/embed/pLxgdj/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Ознакомьтесь с <a href='https://codepen.io/MSEdgeDev/pen/pLxgdj/'> новыми API-интерфейсами EdgeHTML 17 на </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) в <a href='https://codepen.io'> CodePen </a> .</iframe>

> [!TIP]
> Мы [собрались](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) с другими браузерами и веб-сообществом в [MDN веб-документы](https://developer.mozilla.org/) в качестве наиболее удобного места для полезной и несмещенной документации, независимой от браузера, для текущих и новых веб-технологий, основанных на стандартах. Сведения о поддержке API EdgeHTML можно найти непосредственно на каждой странице [библиотеки веб-ссылок MDN](https://developer.mozilla.org/docs/Web). Посетите [состояние платформы](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) Microsoft Edge для получения последних возможностей, поддерживаемых в Microsoft Edge. 

## Предыдущие выпуски EdgeHTML

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)

[EdgeHTML 16/Windows Build 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)

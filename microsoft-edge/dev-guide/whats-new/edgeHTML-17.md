---
title: Новые функции и API в EdgeHTML 17
description: В этом руководстве представлен обзор функций и стандартов для разработчиков, включенных в Microsoft EdgeHTML 17.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 0fc7dda532866e8970003bce2febb7e46fbbc459
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941942"
---
# Новые возможности в EdgeHTML 17  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Ниже приведен список новых и обновленных функций, публикуемых [в веб-платформе Microsoft Edge 17 версии 17(апрель](https://blogs.windows.com/msedgedev/2018/04/30) 2018 г.) в [рамках обновления Windows 10 за апрель 2018](https://blogs.windows.com/windowsexperience/2018/04/27) г.  Сведения об изменениях в конкретных [сборках Windows Insider](https://insider.windows.com) Preview см. в статье ["Изменение журнала изменений Microsoft Edge"](https://developer.microsoft.com/microsoft-edge/platform/changelog) и ["Новые возможности Microsoft EdgeHTML".](../whats-new.md)  

Вот как и вот такая перечень изменений. [https://aka.ms/devguide_edgehtml_17](./edgehtml-17.md)  

## Новые и обновленные функции  

### ARIA 1.1 ролей, штатов и мероприятий  

EdgeHTML 17 добавляет поддержку различных ролей, областей и свойств из спецификации [веб-приложений с поддержкой специальных возможностей (WAI-ARIA) 1.1,](https://w3.org/TR/wai-aria-1.1)включая веб-каналы, [формы,](https://www.w3.org/TR/wai-aria-1.1#form) [aria-haspopup,](https://w3.org/TR/wai-aria-1.1#aria-haspopup) [aria-placeholder](https://w3.org/TR/wai-aria-1.1#aria-placeholder)и многие другие. [feed](https://www.w3.org/TR/wai-aria-1.1#feed) в журнале изменений вы найдете [полный список обновлений ARIA.](https://developer.microsoft.com/microsoft-edge/platform/changelog/desktop/17134/?compareWith=16299)  В этом обновлении EdgeHTML 17 теперь поддерживает все роли и атрибуты, определенные в WAI-ARIA 1.1.  Дополнительные сведения о [специальных возможностях](../../accessibility.md) в Microsoft Edge см. в документах с поддержкой специальных возможностей.  

### Маскирование CSS  

EdgeHTML 17 предлагает экспертовую поддержку для [маски cSS CSS.](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking)  Частичная внедрение описывает свойства [маски](https://developer.mozilla.org/docs/Web/CSS/mask-image) CSS и [свойства](https://developer.mozilla.org/docs/Web/CSS/mask-size) маски размера.  Проверьте флажок "Включить маску CSS" о том, что флаги нужно экспержетизировать!  

### Преобразования CSS в элементы SVG  

EdgeHTML 17 теперь поддерживает преобразование CSS к элементам SVG и атрибутам презентации.  Это позволяет визуально умножать элементы SVG, включая поворот, масштабирование, перемещение, эскиз или перевод.  

### Расширения  

Теперь Microsoft Edge теперь поддерживает [API уведомлений,](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) который отображает уведомления от расширений.  Разработчики расширений теперь могут создавать различные типы уведомлений \(базовые, списки, изображения и т. д.), которые поддерживают полное взаимодействие с полным пользователем.  Уведомления также автоматически вошли в центр уведомлений.  Посетите пример [уведомлений о том,](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/notifications/notifications) как использовать этот API в расширении.  

EdgeHTML 17 теперь также поддерживает `Tabs.reload()` метод в стандартных классах API.  Кроме того, в центре обновления Windows 10 за апрель 2018 г. пользователи теперь могут разрешить выполнять расширения во время просмотра InPrivate.  

Дополнительные сведения об обновлениях в этом выпуске см. в статье "Новые функции для расширений в Windows 10 за апрель [2018 г.](https://blogs.windows.com/msedgedev/2018/05/24)  

### DevTools  

Этот выпуск DevTools пытается использовать двумя способами: как инструменты традиционного режима в \( \) для `F12` Microsoft Edge и предварительный просмотр в виде отдельного приложения Windows [10](../../devtools-guide/whats-new/edgehtml-17.md#microsoft-edge-devtools-app-preview) из Microsoft Store!  

:::image type="complex" source="../../devtools-protocol/media/microsoft-edge-devtools.png" alt-text="Приложение Microsoft Edge DevTools" lightbox="../../devtools-protocol/media/microsoft-edge-devtools.png":::
   Приложение Microsoft Edge DevTools  
:::image-end:::  

Инструменты также были обновлены с помощью ряда основных функций, включая базовую поддержку [удаленного](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol) отладки \(через новый [диспетчер](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol)\), PWA отладки [PWA, управление](../../devtools-guide/whats-new/edgehtml-17.md#pwa-debugging) [индексированными](../../devtools-guide/whats-new/edgehtml-17.md#indexeddb-inspection)док-станциями и т. д. [vertical docking](../../devtools-guide/whats-new/edgehtml-17.md#docking-to-the-right-in-microsoft-edge) Мы также продолжили [refactoring effort](./edgehtml-16.md) реферативное усилие в последнем выпуске в рамках постоянной работы и надежности.  

Дополнительные сведения [см. в последнем обновлении Windows 10 (EdgeHTML 17).](../../devtools-guide/whats-new/edgehtml-17.md)  

### JavaScript  

С EdgeHTML 17 с пулохом Chakra JavaScript появилась улучшена производительность в ряд основных областях.  

:::row:::
   :::column span="1":::
      **Чертеж памяти**  
   :::column-end:::
   :::column span="2":::
      *   \(Re-\)откладывание для [функций](https://github.com/Microsoft/ChakraCore/pull/4105) и [методов объектов](https://github.com/Microsoft/ChakraCore/pull/4136)  
      *   [Регулятор идентифицирование regExp байтов Refactor](https://github.com/Microsoft/ChakraCore/pull/3915)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Встроенные средства JavaScript**
   :::column-end:::
   :::column span="2":::
      *   [Общий доступ к типу для объекта.Создать](https://github.com/Microsoft/ChakraCore/pull/3901)  
      *   [Polymorphic inline кэш для объекта.Assign](https://github.com/Microsoft/ChakraCore/pull/3792)  
      *   [JSON.parse/stringy optimizations](https://github.com/Microsoft/ChakraCore/pull/4077)  
      *   [Перезапись итераций массива в JavaScript и ускоряет для... из](https://github.com/Microsoft/ChakraCore/pull/4095)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Сборки веб-приложений**
   :::column-end:::
   :::column span="2":::
      *   [Поддержка интеллектуальной поддержки](https://github.com/Microsoft/ChakraCore/pull/3681)  
   :::column-end:::
:::row-end:::  

Все параметры можно ознакомиться с [улучшенными средствами JavaScript и Производительностью WebAssemb.](https://blogs.windows.com/msedgedev/2018/06/19)  

### Элемент мультимедиа

EdgeHTML 17 содержит обновления [ДЛЯ HTMLMediaElementElement](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) включают:  

*   Новый `preload` атрибут элемента обозначает, [`<media>`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) какие данные следует предварительно загрузить.
*   Дополнение метода и [`setSinkId()`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/setSinkId) [`sinkId`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/sinkId) свойства позволяют разработчикам выбрать устройство вывода звука.  
    
    > [!NOTE]
    > Эта возможность пока недоступна в rTC.  
    
### Мультимедиа Capture API  

Приложение Microsoft Edge теперь поддерживает снимок экрана в RTC с помощью [API-сбора мультимедиа.](https://w3c.github.io/mediacapture-screen-share)  Эта функция позволяет собирать результаты на устройстве вида пользователя, обычно используя для широковещательного показа рабочего стола для виртуального собрания или презентации.  

### Прогрессивные веб-приложения  

Начиная с Microsoft EdgeHTML 17, работники служб и push-уведомления включены по умолчанию \(подробнее об этих функциях в работнике записей [блога: технический](https://blogs.windows.com/msedgedev/2017/12/19)холст от исходящего со страницы).  Это выполняет набор технологий \(включая лицо сеть, Push-и API-эркипликации кэша\Кэширование\) о том, что техническое сопоставление для прогрессивных веб-приложений \(PWA\) в Windows 10.  

PWA — это просто веб-приложения, которые постепенно повышают эффективность работы в собственных приложениях на поддерживаемых платформах и инженерах браузера, таких как запуск, запуск программы установки, поддержка в автономном режиме и push-уведомлений. [progressively enhanced](https://en.wikipedia.org/wiki/Progressive_enhancement)  В Windows 10 с модулем "\(EdgeHTML\)" PWAs удобно использовать добавленные преимущества независимо от окна браузера как универсальные приложения [платформы Windows.](/windows/uwp/get-started/whats-a-uwp)  

Недалеко пульт транспортных работников, работников служб и API кэша позволяет разработчикам пересылать сетевые запросы и отвечать на них в кэше.  Для использования преимуществ из-за дальнейшей нагрузки страниц не требуется даже в кэше передачи страниц, а также возможность использовать автономный режим в течение периодов без подключения к Интернету или неудовлетворительного качества связи.  

Посмотрите на [прогрессивные веб-приложения для документов Windows, чтобы](../../progressive-web-apps-edgehtml/index.md) узнать больше о работниках по обслуживанию и подробностям работников по Project Web App для Windows 10.  

### Веб-безопасность  

Поддержка EdgeHTML 17 ознакомится с целостностью субтитров \(SRI\).  [Целостность подресурсов](https://developer.mozilla.org/docs/Web/Security/Subresource_Integrity) — это функция безопасности, которая позволяет браузерам проверять, доставляются ли удаленные ресурсы \(изображения, сценарии, шрифты и т. д.) доставляются без непредвиденных средств.  

Добавьте атрибут, содержащий шифрованный хорошооообразный хорошоооооое представление ресурса, который должен загрузить на `integrity` веб-странице `<script>` `<link>` или элемент, как в примере ниже.  Затем Microsoft Edge сравнивает запрошенный ресурс с хэштарм, определенным в `integrity` атрибуте.  Если они не совпадают, Microsoft Edge не будет будет выполнять ресурс и возвращает ошибку в сети.  

```html
<script src="https://example.com/example-framework.js" 
        integrity="sha384-Li9vy3DqF8tnTXuiaAJuML3ky+er10rcgNR/VqsVpcw+ThHmYcwiB1pbOxEbzJr7" 
        crossorigin="anonymous"></script>
```  

Кроме того, в Microsoft [Upgrade-Insecure-Requests](https://developer.mozilla.org/docs/Web/HTTP/Headers/Upgrade-Insecure-Requests) EdgeHTML 17 заголовок запроса на обновление позволяет браузерам запрашивать защищенный просмотр браузеров.  Этот заголовок указывает сервер, что браузер поддерживает обновление любых незащищенных запросов и пользователь следует перенаправиться на защищенную версию сайта (если она доступна).  

### Переменные шрифты
Полная поддержка переменных шрифтов \(включая [CSS-параметры шрифта](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings) и оптическую проверку размера \) доступна в EdgeHTML 17. [font-optical-sizing](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings)  Переменные шрифты обеспечивают вид различных типов с одним шрифтом, изменив различные оси, что уменьшает необходимость для нескольких файлов шрифтов и повышения производительности.  

Присоединяйтесь [к нам по эксперту, чтобы узнать, какие шрифты переменных предоставляют веб-разработчики](https://developer.microsoft.com/microsoft-edge/testdrive/demos/variable-fonts)и разработчики, и как их использовать на сайте.  Кроме того, узнайте больше о переменных шрифтах в записи блога, помощи знакомства с [шрифтами переменных шрифтов.](https://blogs.windows.com/msedgedev/2018/03/13)  

<iframe height='456' scrolling='no' title='Переменные примеры билетов' src='//codepen.io/MSEdgeDev/embed/dmYvWg/?height=456&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Примеры билетов, примеры диктовки пера по <a href='https://codepen.io/MSEdgeDev/pen/dmYvWg/'> </a> программе MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> коде CodePen. </a></iframe>  

## Новый API в EdgeHTML 17  

Ниже приведен полный список новых aPI в EdgeHTML 17.  Они указаны в `[interface name].[api name]` формате.  

> [!NOTE] 
> Хотя в DOM представлены указанные ниже API, конечные точки могут быть настоящими разработками.  Сведения о  [официальном слове](https://developer.microsoft.com/microsoft-edge/platform/status) реализованы в поддержке функций Microsoft Edge.  

<iframe height='580' scrolling='no' title='Новый API в EdgeHTML 17' src='//codepen.io/MSEdgeDev/embed/pLxgdj/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. раздел <a href='https://codepen.io/MSEdgeDev/pen/pLxgdj/'> "Новый API" в EdgeHTML 17 </a> на MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> коде CodePen. </a></iframe>  

> [!TIP]
> Мы [сотрудничали](https://blogs.windows.com/msedgedev/2017/10/18) с другими браузерами и веб-сообществом [веб-сайтов mDN](https://developer.mozilla.org) в качестве определения полезного места для несущественной и несущественной документации в веб-технологиях для текущих и изменений стандартов.  Подробные сведения о поддержке API EdgeHTML можно найти непосредственно на каждой странице [библиотеки справа веб-сайтов MDN.](https://developer.mozilla.org/docs/Web)  Посетите состояние [платформы](https://developer.microsoft.com/microsoft-edge/status) Microsoft Edge, чтобы быть доступна новейшие функции, поддерживаемые в Microsoft Edge.  

## Предыдущие выпуски EdgeHTML  

[EdgeHTML 13 / Windows сборка 10586 (11.11.2015)](https://aka.ms/devguide_edgehtml_13)  

[EdgeHTML 14/ Windows сборка 14393 (8.08.2016)](https://aka.ms/devguide_edgehtml_14)  

[EdgeHTML 15 / Windows сборка 15063 (4.04.2017)](https://aka.ms/devguide_edgehtml_15)  

[EdgeHTML 16/ Сборка 16299 (10.10.2017)](https://aka.ms/devguide_edgehtml_16)  

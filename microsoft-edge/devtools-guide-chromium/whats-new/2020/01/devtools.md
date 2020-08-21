---
title: Новые возможности в DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8e9e6885d04c7ad15a688b51cee4c16440d3ca1e
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942097"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# Новые возможности в средствах разработчиков (Microsoft Edge 81)  

## Объявления от команды разработчиков Microsoft Edge  

В следующих разделах приведен список извещений, которые вы можете пропустить от команды разработчиков Microsoft Edge. Ознакомьтесь с их новыми возможностями в DevTools, расширениях кодов VS и многом другом.  Чтобы быть в курсе всех последних и полезных функций в средствах разработчика, скачайте [каналы microsoft Edge][MicrosoftEdgePreviewChannels] и [отслеживайте нас в Твиттере.][EdgeDevToolsTwitterAccount]  

### Улучшенные специальные возможности в средствах разработчиков  

Меняется 170 на хромомоблю изменилось 170 на Chromium на устранение контрастности цвета, клавиатуры и средства чтения с экрана в средствах разработчиков.  Каждый разработчик, созданный в Интернете, должен использовать DevTools.  

> ##### Рис. 1  
> Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана  
> ![Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

Хотите узнать, как сделать веб-страницу доступным для всех пользователей?  Скачайте [средство "Аналитика][AccessibilityInsights] специальных возможностей" и [расширения][WebhintBrowserExtension] веб-сайта, касающиеся Microsoft Edge для начала работы.  

Если вы используете средства чтения с экрана или клавиатуру для навигации по Разработчикам, отправьте нам свой отзыв, [твитирую щелкая][PostTweetEdgeDevTools] на мнение или щелкнув [значок "Обратная](#getting-in-touch-with-microsoft-edge-devtools-team) связь!".  

Проблема с [#963183][crbug963183]  

### Использование средств разработчиков на других языках  

Многие разработчики используют другие средства разработчика, такие как StackOverflow и VS code, на своем родном языке, а не только на английском языке.  Мы рады сообщать локализацию для разработчиков Разработчиков, которые теперь можно использовать на одном из 10 языков, кроме английского:  

:::row:::
   :::column span="":::
      Китайский \(упрощенное\) -  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Китайский \(традиционное\) -  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Французский (француз&#231;оси)
   :::column-end:::
   :::column span="":::
      Немецкий (отладка)
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Итальный (курсив)
   :::column-end:::
   :::column span="":::
      Японский ( &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Корейский ( &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Португальский (португалия&#234;s)
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Русский ( &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081; русский)
   :::column-end:::
   :::column span="":::
      Испанский (испания&#241;слишком много
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Язык, который вы используете в Microsoft Edge, автоматически соответствует языку, который вы `edge://settings/languages` используете.  

Если вы хотите, чтобы Microsoft Edge оставался на английском языке и язык с разработчиками остался на английском языке, откройте раздел "Параметры" и отключите `F1` язык **соответствия браузера.** [Settings][Settings]  

> ##### Рисунок 2  
> Средства разработчиков на немецком  
> ![Средства разработчиков на немецком][ImageLocalizedGerman]  

**Сообщения консоли не** локализуются.  На языке, который вы используете в Microsoft Edge, отображаются только строки, используемые в языке.  

Если вы хотите использовать разработчики для разработчиков, отличного от того, какие из доступных вам языков вы хотите использовать, [то разговор][PostTweetEdgeDevTools] можно нам или щелкните [значок "Обратная связь".](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема с [хромом#941561][crbug941561]  

### расширение веб-сайта Microsoft Edge  

Расширение Microsoft Edge позволяет легко просматривать веб-страницу и получать отзывы о специальных возможностях, совместимости браузера, безопасности, производительности и т. д. в средствах DevTools.  Дополнительные сведения [https://webhint.io][Webhint] см. в дополнительных случаях.  

> ##### Рисунок3  
> Вкладка «Подсказки» в приложении DevTools при установленном расширении браузера  
> ![Вкладка «Подсказки» в приложении DevTools при установленном расширении браузера][ImageHintsTabWebhintExtension]  

[Попробуйте расширение веб-браузера в Microsoft Edge.][MicrosoftEdgeInsiderAddons]  После установки расширения откройте вкладку DevTools и выберите вкладку "Подсказки".  В этом окне выполните настраиваемое сканирование сайта.  Чтобы узнать [больше webhint.io, нажмите][WebhintBrowserExtension] дополнительные сведения.  

### Трехмерное представление  

Используйте **трехмерное** представление для отладки веб-приложения путем перехода к объектной модели [документов \(DOM\)][MDNDocumentObjectModel] или [стопки z-индекса.][MDNZIndex]  

> ##### Рисунок4  
> Трехмерное представление в средствах разработчиков  
> ![Трехмерное представление в средствах разработчиков][Image3DView]  

Чтобы открыть трехмерное представление, `Ctrl`  +  `Shift`  +  `P` нажмите клавишу в **трехмерном представлении** и выберите **"Показать трехмерное представление".**  

Мы работаем над элементом, который мы работаем над новым элементом, поэтому отправьте [нам](#getting-in-touch-with-microsoft-edge-devtools-team)свой отзыв.  

[Проблема][crbug987787] с #987787 chromium #987787  

### Visual Studio расширения кода  

Команда Разработчиков также выпущена [некоторые расширения для Visual Studio Code \(VS Code\),][VisualStudioCode] которые позволяют использовать возможности DevTools напрямую из текстового редактора! Ознакомьтесь с расширениями ниже.  

#### Элементы Microsoft Edge  

Используйте инструмент "Элементы" в коде VS, добавив расширение ["Элементы" для Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS CodeS.  

> ##### Рисунок 5  
> Инструмент "Элементы" в коде VS с помощью расширения "Элементы" microsoft Edge для Microsoft Edge с помощью расширения "Элементы" для ![ Microsoft Edge][ImageElementsVisualStudioCode]  

Дополнительные сведения см. [в статье "Элементы расширения кода Microsoft Edge VS".][VisualStudioCodeElementEdgeExtension]  

#### Отладка для Microsoft Edge  

С [расширением][VisualStudioMarketplaceDebuggerEdge] отладки для Microsoft Edge VS отладка JavaScript работает в Microsoft Edge непосредственно из кода VS Code!  

> ##### Рисунок6  
> Отладка расширения Microsoft Edge в коде VS  
> ![Отладка расширения Microsoft Edge в коде VS][ImageDebuggerExtensionVisualStudioCode]  

Дополнительные сведения см. в [статье о том, как отладить Microsoft Edge от кода VS.][VisualStudioCodeDebuggerEdgeExtension]  

#### webhint  

[Расширение веб-кода][VisualStudioMarketplaceWebhintExtension] VS используется для `webhint` улучшения веб-страницы во время его письма. Это расширение выполняется, а отчеты диагностики для файлов рабочей области на основе `webhint` анализа.  

> ##### Рисунок7  
> Расширение веб-кода VS с кодом VS  
> ![Расширение веб-кода VS с кодом VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

[Дополнительные сведения о расширении веб-кода VS кода VS.][WebhintVisualStudioCodeExtension]  

### Visual Studio интеграции  

В Visual Studio 2019 г. и более поздних версий используйте отладку Visual Studio для отладки JavaScript в Microsoft Edge.  [Скачайте Visual Studio 2019 г.,][MicrosoftVisualStudioDownloads] чтобы опробовать эту функцию!  

> ##### Рисунок8  
> Visual Studio с возможностью запустить веб-приложение в Microsoft Edge Canary, Dev или бета-версии  
> ![Visual Studio с возможностью запустить веб-приложение в Microsoft Edge Canary, Dev или бета-версии][ImageVisualStudioLaunchWebApp]  

[Подробнее об отладке Microsoft Edge Visual Studio.][MicrosoftVisualStudio]  

### Сообщения консоли отслеживания  

Предотвращение отслеживания — это уникальная функция в Microsoft Edge, которая защищает вас при посещении веб-сайтов, которые вы не посещали.  По умолчанию этот режим предотвращает балансировку сбалансированного отслеживания, который блокирует сторонние средства отслеживания сторонних поставщиков и известные вредоносные отслеживатели для обеспечения балансировки конфиденциальности и совместимости веб-сайтов.  Чтобы получить более подробные сведения о совместимости веб-страницы, когда заблокированы некоторые средства отслеживания, также мы добавили предупреждения в консоль, если средство отслеживания заблокирован.  

> ##### Рисунок9  
> Сообщения в консоли при отслеживании блокируют доступ к хранилищу для отслеживания  
> ![Сообщения в консоли при отслеживании блокируют доступ к хранилищу для отслеживания][ImageTrackingPrevention]  

[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью.][TrackingPrevention]  

## Извещения из проекта Chromium  

В следующих разделах описаны дополнительные функции, доступные в Браузере Microsoft Edge 81, которые были приняли в проекте открытого калерея Chromium.  

### Поддержка Moto G4 в режиме устройства  

После [включения панели][DeviceToolbar]инструментов устройств можно оценить размеры представления Moto G4 из **списка устройств.**  

> ##### Рисунок 10  
> Пример окна просмотра модуля G4  
> ![Пример окна просмотра модуля G4][ImageMotoG4]  

Щелкните ["Показать рамку устройства"][DeviceFrame] для отображения оборудования Moto G4 вокруг портала просмотра.  

> ##### Рисунок11  
> Аппаратное оборудование Moto G4  
> ![Аппаратное оборудование Moto G4][ImageMotoG4Frame]  

Дополнительные возможности  

*   Откройте [меню команд и][CommandMenu] запустите команду, чтобы сделать снимок экрана с оборудованием `Capture screenshot` Moto G4 (после включения **показа фрейма**устройства).  
*   [Регулирование][ThrottleNetworkAndCpu] сети и цпутивенности цикла, чтобы более тщательно оказались условия просмотра веб-сайта для мобильных устройств пользователей.  

Проблема с [#924693][crbug924693]  

### Обновления cookie  

#### Файлы cookie в области "Файлы cookie"  

В области "Файлы cookie" на панели приложений теперь отображаются файлы cookie, на желтый фон.  

> ##### Рисунок12  
> Файлы cookie в области "Файлы cookie" панели приложения  
> ![Файлы cookie в области "Файлы cookie" панели приложения][ImageBlockedCookies]  

Проблема с #1030258 chromium [#1030258][crbug|::ref1::|]  

#### Приоритет cookie в области "Файлы cookie"  

Таблицы cookie на панели "Сети" и "Приложения" теперь содержит **столбец приоритета.**  

> [!CAUTION]
> Браузеры cookie, поддерживаемые браузерами Chromium, например Microsoft Edge, — это единое, поддерживающее приоритет файлов cookie.  

Проблема с [#1026879][crbug1026879]  

#### Изменение всех значений cookie  

На данный момент все ячейки в таблицах Cookie доступны для редактирования, за исключением ячеек в столбце **Size,** так как столбец представляет сетевой размер файла cookie в байтах.  Просмотрите [поля][CookiesFields] для каждого столбца.  

> ##### Рисунок13  
> Изменение значения cookie  
> ![Изменение значения cookie][ImageEditCookie]  

#### Копировать как Node.js лицевой команде для включения данных cookie  

Щелкните сетевой **Copy**запрос правой кнопкой мыши и выберите "Копировать Node.js с помощью лица, чтобы получить выражение с данными  >  **Copy as Node.js fetch** `fetch` cookie".  

> ##### Рисунок14  
> Копировать Node.js обновляется из-за лица, обновляемом для обработки данных  
> ![Копировать Node.js обновляется из-за лица, обновляемом для обработки данных][ImageCopyFetch]  

Проблема с хромом [#1029826][crbug1029826]  

### Более тщательное виде веб-приложения  

Ранее область манифеста на панели приложения отправила собственные запросы для отображения значков манифеста веб-приложения.  В DevTools теперь отображается точный значок манифеста, который используется в Microsoft Edge.  

> ##### Рисунок15  
> Значки в области манифеста  
> ![Значки в области манифеста][ImageManifestIcon]  

Проблема с [#985402][crbug985402]  

### Наведите указатель мыши на свойства содержимого CSS, чтобы увидеть несанкцируемые значения  

Наведите указатель мыши на значение свойства, чтобы увидеть `content` необходимую версию значения.  

Например, в [данном видеоролике,][CSSContentDemo] когда вы просматриваете `p::after` элемент пикоменной элемента, в области "Стили" отображается escaped string:  

> ##### Рисунок16  
> Строка ESCAP  
> ![Строка ESCAP][ImageEscapedString]  

При наведении указателя `content` мыши на необязательное значение:  

> ##### Рисунок17  
> Необязательное значение  
> ![Необязательное значение][ImageUnescapedString]  

### Более подробные ошибки исходной карты в консоли  

Консоль теперь содержит более подробные сведения о причине загрузки исходной карты или связи источника.  Ранее она только что возникает из-за ошибки, в ней не объясняется, почему не так.  

> ##### Рисование 18  
> Ошибка загрузки исходной карты в консоли  
> ![Ошибка загрузки исходной карты в консоли][ImageSourcemapError]  

### Параметр отмены прокрутки в конце файла  

Откройте [меню "Параметры",][Settings] а затем отключите прокрутку в конце файла, чтобы отключить поведение по умолчанию в списке **Preferences**  >  **Sources**  >  **Allow scrolling past end of file** **"Источники".**  

> ##### Рис. 19  
> Выключение функции **прокрутки в** настроек  
> ![Выключение функции прокрутки в прошлом конце файла][ImageSettings]  

> ##### Рис2 20  
> Прокрутка после окончания файла становится неактивной.  
> ![Прокрутка после окончания файла становится неактивной.][ImageScroll]  

## Загрузить каналы с предварительными версиями Microsoft Edge  

Если вы используете Windows или macOS, рекомендуем использовать каналы [предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Каналы с предварительными версиями доступны новейшие функции Разработчиков.  

## Совместная работа с помощью команды разработчиков Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- <<../../_shared/devtools-feedback.md>>  

<<../../_shared/canary.md>>  

<<../../_shared/discover.md>> -->  

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Рис. 1. Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Изображение 2. Разработчики в немецких"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Р. Вкладка "Подсказки" в Microsoft Edge DevTools, если установлено расширение веб-браузера"  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Рис. 4. Представление трехмерных моделей в средствах разработчиков Microsoft Edge"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Рис. 5. Инструмент "Элементы" в коде VS с помощью элементов расширения Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Р. Дебугер для расширения Microsoft Edge в коде VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Рис. Расширение webhint VS-кода, анализирующее TSX-файлы в коде VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Рис. Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Бета-версии"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Р. Сообщения в консоли при блокировке отслеживания блокируют доступ к хранилищу для отслеживания" 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Рис. 10: репликация просмотра порта ладони с G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Рис. 11: оборудование Moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Рис. 12: "Заблокированные файлы cookie" в панели приложений"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Рис. 13: изменение значения cookie"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Рис. 14: копирование Node.js удаленного доступа"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Рис. 15: значки в области манифеста"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Рисование 16: строка escaped"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Рисование 17: неизвестное значение"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Рисунок 18: ошибка загрузки исходной карты в консоли"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Рис. 19. Выключение прокрутки в прошлом конце файла в параметрах"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Рис. Прокрутка в конце файла теперь отключена в панели "Источники""

<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Рекламное представление для мобильных устройств с режимом устройства в режиме разработчика Microsoft Edge"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Выберите "Показать рамку устройства" для отображения физического профиля устройства по порту просмотра."
[CommandMenu]: ../../../command-menu/index.md "Команды с помощью меню «Разработчики» microsoft Edge"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Регулирование сети и цпулу веб-университета, чтобы более тщательно оказались условия просмотра веб-сайта для мобильных устройств пользователей."
[crbug924693]: https://crbug.com/924693 "924693: запрос на добавление модуля G4 в список устройств"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: вкладка Cookie на консоли разработки больше не отображает приоритет"
[CookiesFields]: ../../../storage/cookies.md#fields "Поля в таблице Cookie"
[crbug1029826]: https://crbug.com/1029826 "1029826: вкладка "Сеть" -> щелкните правой кнопкой мыши, чтобы запросить -> копировать > копирования, похожие на копирование, не копируются"
[crbug985402]: https://crbug.com/985402 "985402: строки ошибок манифеста веб-приложения вызывают ошибки в веб-приложении"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Ролик для невольного содержимого CSS"
[Settings]: ../../../customize/index.md#settings "Настройка разработчиков Microsoft Edge с помощью параметров"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема: MicrosoftDocs/edge-разработчики"  
[TheWebWeWant]: https://aka.ms/webwewant "Нужный веб-час"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Отладка расширения кода Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Элементы расширения кода Microsoft Edge VS"  
[crbug963183]: https://crbug.com/963183 "963183 — средства для разработки не совместимо с WCAG"
[crbug941561]: https://crbug.com/941561 "941561 — локализация средств разработчиков"
[crbug987787]: https://crbug.com/987787 "987787 — Dom 3D View"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Сведения о специальных возможностях"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачивание Visual Studio 2019 для Windows \& для Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools твиттер"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio код"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладка для Microsoft Edge — Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \(Chromium\) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение Webhint для браузера | документация веб-хинтертнера"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение веб-кода VS | документация веб-хинтертнера"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение отслеживания исправлений в записях блога Microsoft Edge"

> [!NOTE]
> Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]  
> Исходная страница [here](https://developers.google.com/web/updates/2020/01/devtools/index) находится на сайте [Kayce Basques][KayceBasques] \(технический автор, Chrome DevTools & Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
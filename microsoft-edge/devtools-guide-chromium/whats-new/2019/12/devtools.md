---
title: Новые возможности в DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 03fd78eddf54b68d072ba11401a897ad9f109058
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942143"
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

# Новые возможности в DevTools (Microsoft Edge 80)  

## Объявления от команды разработчиков Microsoft Edge  

В следующих разделах приведен список извещений, которые вы можете пропустить от команды разработчиков Microsoft Edge. Ознакомьтесь с их новыми возможностями в DevTools, расширениях кодов VS и многом другом.  Чтобы быть в курсе всех последних и полезных функций в средствах разработчика, скачайте [каналы microsoft Edge][MicrosoftEdgePreviewChannels] и [отслеживайте нас в Твиттере.][EdgeDevToolsTwitterAccount]  

### Улучшенные специальные возможности в средствах разработчиков  

Меняется 170 на хромомоблю изменилось 170 на Chromium на устранение контрастности цвета, клавиатуры и средства чтения с экрана в средствах разработчиков.  Каждый разработчик, созданный в Интернете, должен использовать DevTools.  

> ##### Рис. 1  
> Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана  
> ![Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

Хотите узнать, как сделать веб-страницу доступным для всех пользователей?  Скачайте [средство "Аналитика][AccessibilityInsights] специальных возможностей" и [расширения][WebhintBrowserExtension] веб-сайта, касающиеся Microsoft Edge для начала работы.  

Если вы используете средства чтения с экрана или клавиатуру для навигации по Разработчикам, отправьте нам свой отзыв, [твитирующий][PostTweetEdgeDevTools] нам или щелкнув [значок "Отправить](#getting-in-touch-with-microsoft-edge-devtools-team) отзыв".  

Проблема с [#963183][crbug963183]  

### Использование средств разработчиков на других языках  

Многие разработчики используют другие средства разработчика, такие как StackOverflow и VS code, на своем родном языке, а не только на английском языке.  Мы рады сообщать локализацию для разработчиков DevTools, который теперь можно использовать на одном из 10 языков, кроме английского:  

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
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Перейдите к `edge://flags` пометке **"Включить локализованные средства разработчика" и** установите для него флаг **"Включить локализованные средства разработчика".**  Также задайте **для флага** экспертов разработчика значение **"Включено".**  Перезапустите Microsoft Edge и откройте DevTools.  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  Язык, который вы используете для Microsoft Edge, соответствующего языку, который вы `edge://settings/languages` используете.  

> ##### Рисунок 2  
> Средства разработчиков на немецком  
> ![Средства разработчиков на немецком][ImageLocalizedGerman]  

Если вы хотите использовать разработчики для разработчиков, отличного от того, какие из доступных вам языков вы хотите использовать, [то разговор][PostTweetEdgeDevTools] можно нам или щелкните [значок "Обратная связь".](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема с [хромом#941561][crbug941561]  

### расширение microsoft Edge  

Расширение веб-сайта Microsoft Edge позволяет легко просматривать веб-страницу и получать отзывы о специальных возможностях, совместимости браузера, безопасности, производительности и т. д. в средствах DevTools.  Дополнительные сведения [https://webhint.io][Webhint] см. в дополнительных случаях.  

> ##### Рисунок3  
> Вкладка «Подсказки» в приложении DevTools при установленном расширении браузера  
> ![Вкладка «Подсказки» в приложении DevTools при установленном расширении браузера][ImageHintsTabWebhintExtension]  

[Попробуйте расширение веб-браузера в Microsoft Edge.][MicrosoftEdgeInsiderAddons]  После установки расширения откройте вкладку DevTools и выберите вкладку "Подсказки".  В этом окне выполните настраиваемое сканирование сайта.  Чтобы узнать [больше webhint.io, нажмите][WebhintBrowserExtension] дополнительные сведения.

### Трехмерное представление  

Используйте **трехмерное** представление для отладки веб-приложения путем перехода к объектной модели [документов \(DOM\)][MDNDocumentObjectModel] или [стопки z-индекса.][MDNZIndex]  

> ##### Рисунок4  
> Трехмерное представление в средствах разработчиков  
> ![Трехмерное представление в средствах разработчиков][Image3DView]  

Для доступа к трехмерному представлению перейдите к трехмерному представлению и убедитесь, что для флага экспертов для `edge://flags` разработчиков **установлено значение "Включено".** **Developer Tools experiments**  Перезапустите Microsoft Edge и откройте DevTools.  Нажмите `F1` в devTools или перейдите в раздел **"Параметры",** перейдите в **раздел "Эксперименты"** и установите **флажок "Включить трехмерное представление".**  Теперь нажмите `Ctrl`  +  `Shift`  +  `P` клавишу ввод в **трехмерном представлении** и выберите **"Показать трехмерное представление".**  

Мы работаем над элементом, и мы добавляем дополнительные функции в трехмерное представление, чтобы отправить [нам свой отзыв.](#getting-in-touch-with-microsoft-edge-devtools-team)  

[Проблема][crbug987787] с #987787 хромом

### Visual Studio расширения кода  

Команда Разработчиков также выпущена [некоторые расширения для Visual Studio Code \(VS Code\),][VisualStudioCode] которые позволяют использовать возможности DevTools напрямую из текстового редактора! Ознакомьтесь с расширениями ниже.  

#### Элементы Microsoft Edge  

Используйте инструмент "Элементы" в коде VS, добавив расширение ["Элементы" для Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS CodeS.  

> ##### Рисунок 5  
> Инструмент "Элементы" в коде VS с использованием расширения "Элементы" для Microsoft Edge  
> ![Инструмент "Элементы" в коде VS с использованием расширения "Элементы" для Microsoft Edge][ImageElementsVisualStudioCode]  

Дополнительные сведения [см. в статье "Элементы расширения кода Microsoft Edge VS".][VisualStudioCodeElementEdgeExtension]  

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

[Прочтите наш блог, чтобы узнать, как отладку Microsoft Edge отладка Microsoft Edge Visual Studio.][MicrosoftVisualStudioBlogDebugJavascript]  

### Сообщения консоли отслеживания  

Предотвращение отслеживания — это уникальная функция в Microsoft Edge, которая защищает вас при посещении веб-сайтов, которые вы не посещали.  По умолчанию этот режим предотвращает балансировку сбалансированного отслеживания, который блокирует сторонние средства отслеживания сторонних средств и известные вредоносные отслеживания для обеспечения балансировки конфиденциальности и совместимости веб-сайтов.  Чтобы получить более подробные сведения о совместимости веб-страницы, когда заблокированы некоторые средства отслеживания, также мы добавили предупреждения в консоль, если средство отслеживания заблокирован.  

> ##### Рисунок9  
> Сообщения в консоли при отслеживании блокируют доступ к хранилищу для отслеживания  
> ![Сообщения в консоли при отслеживании блокируют доступ к хранилищу для отслеживания][ImageTrackingPrevention]  

[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью.][TrackingPrevention]  

## Извещения из проекта Chromium  

В следующих разделах описаны дополнительные функции, доступные в Microsoft Edge 80, которые были внесены в проект Chromium.  

### Поддержка разрешений и объявлений учебных заводов в консоли  

Теперь консоль теперь поддерживает объявления и `let` `class` инструкций.  Невозможность перестать стать часто объявлений для веб-разработчиков, которые используют консоль для эксперимента с новым кодом JavaScript.  

> [!WARNING]
> При объявлении или заполнением отдельных данных консоли или вращения каждого входного `let` консоли по-прежнему `class` приводит к причинам. `SyntaxError`  

Например, при отключении локальной переменной `let` с помощью консоли состоит из следующей ошибки:  

> ##### Рисунок 10  
> Консоль в Microsoft Edge 79 показывает, что возможность отклонения не удается завершить  
> ![Консоль в Microsoft Edge 79 показывает, что возможность отклонения не удается завершить][ImageConsoleRedeclarationFails]  

Теперь консоль позволяет отложить перезаку.  

> ##### Рисунок11  
> Консоль в Microsoft Edge 80 показывает, что разрешение отмены отмены  
> ![Консоль в Microsoft Edge 80 показывает, что разрешение отмены отмены][ImageConsoleRedeclarationSucceeds]  

Проблема с #1004193 chromium [#1004193][crbug1004193]  

### Улучшенный отладка веб-сайта  

DevTools начал поддерживать [стандарт отладки DWARF,][DwarfHome]которая повышает поддержку пошагового кода, настройки остальных точек и устранить расшифровку на локальных языках в разработчиках.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### Обновления панели сети  

#### Запрос инициатора китой на вкладке "Инициатор"  

Теперь вы можете просмотреть инициаторы и зависимости сетевого запроса в виде вложенного списка.  Это поможет понять, почему был запрашивается запрашиваемый ресурс, и какую активность сети выполнялись определенным ресурсом \(например, сценарий\).  

> ##### Рисунок12  
> Цепочка запросов запроса на вкладке "Инициатор"  
> ![Цепочка запросов запроса на вкладке "Инициатор"][ImageRequestInitiatorChain]  

После [ведения журнала действий в сети][DevToolsNetworkIndex]на панели "Сеть" щелкните ресурс и перейдите на вкладку **"Инициатор запроса"** для просмотра крайнего **инициатива запроса:**  

*   **Инвертированный ресурс** выделен полужирным начертанием.  На снимке экрана выше `ai.2.min.js` является проверенный ресурс.  
*   Ресурсами над проверенным ресурсом являются **инициаторы.**  На снимке экрана выше является `https://www.microsoftedgeinsider.com` инициатор. `ai.2.min.js`  Другими словами, `https://www.microsoftedgeinsider.com` вызвано сетевым `ai.2.min.js` запросом.  
*   Ресурсы, которые не будут проверяться, являются **зависимостями.**  На снимке экрана выше `https://dc.services.visualstudio.com/v2/track` представляет собой `ai.2.min.js` зависимость.  Другими словами, `ai.2.min.js` вызвано сетевым `https://dc.services.visualstudio.com/v2/track` запросом.  

> [!NOTE]
> К ним также можно получить доступ к сведениям инициативе и зависимостям, удерживая нажатой кнопку мыши, а затем `Shift` наводя указатель мыши на ресурсы сети.  [Просмотреть инициативив и зависимости.][DevToolsNetworkReferenceViewInitiatorsDependencies]  

Проблема с chromium [#842488][crbug842488]  

#### Выделение выбранного сетевого запроса в обзоре  

После выбора сетевого ресурса для проверки панель сети панель «Сеть» поместит синюю границу вокруг **него в представлении "Обзор".**  Это поможет вам определение того, происходит ли сетевое или позднее, чем ожидалось.  

> ##### Рисунок13  
> Область обзора с проверенным ресурсом  
> ![Область обзора с проверенным ресурсом][ImageOverviewPaneInspectedResource]  

[Проблема][crbug988253] с #988253 chromium #988253  

#### Столбцы URL-адресов и путей на панели сети  

Новые **столбцы "Путь"** **и "URL-адрес"** на панели network (Сетевой ресурс) можно просмотреть абсолютный или полный URL-адрес каждого сетевого ресурса. **Network**  

> ##### Рисунок14  
> Новые столбцы путей и URL-адреса на панели «Сетевой сети»  
> ![Новые столбцы путей и URL-адреса на панели «Сетевой сети»][ImagePathNetworkPanel]  

Щелкните правой кнопкой **мыши заголовок таблицы "Каскадная"** и выберите **путь или** **URL-адрес,** чтобы отобразить новые столбцы.  

Проблема с #993366 chromium [#993366][crbug993366]  

#### Обновленные строки агента пользователя  

DevTools поддерживает установку пользовательской строки агента на вкладке **"Условия сети".**  Строка пользователя влияет на заголовок HTTP, прикрепленный `User-Agent` к сетевым ресурсам, а также `navigator.userAgent` значение.  

Предопределенные строки пользователя агента были обновлены с учептными версиями с овременными версиями браузера.  

> ##### Рисунок15  
> Меню "Агент пользователя" на вкладке "Сетевые условия"  
> ![Меню "Агент пользователя" на вкладке "Сетевые условия"][ImageUserAgentNetworkConditionsTab]  

Для доступа **к сетевому** [условию откройте меню команд][DevToolsCommandMenuIndex] и выполните `Show Network Conditions` команду.  

> [!NOTE]
> Вы также можете [указать строки пользователя-агенты в режиме устройства.][DevToolsDeviceModeIndex]  

Проблема с [#1029031][crbug1029031] хромеум#1029031  

### Обновления панели аудита  

#### Новый элемент управления конфигурацией  

В этом окне конфигурации появилась новый, обязательное дизайн, и параметры регулирования упрощены.  Дополнительные [сведения об][GitHubGoogleChromeDevToolsAuditsPanelThrottling] изменениях в элементе управления регулирования см. в разделе регулирования на панели регулирования.  

> ##### Рисунок16  
> Новый элемент управления конфигурацией  
> ![Новый элемент управления конфигурацией][ImageConfigurationUI]  

### Обновления вкладки по критериев  

#### Режимы охвата для функций или режимы блока на функции  

На [вкладке "Утверждения"][DevToolsCoverageIndex] есть новое раскрывающееся меню, в котором можно указать, следует ли собирать данные о покрытии кода для **каждой функции** или **каждого блока.**  **Перебор по** блоку более подробно, но и дальнейшее собирать его.  По умолчанию в DevTools покрывается **функция,** покрывающая функцию на тот или иной.  

> [!CAUTION]
> В HTML-файлах могут зависеть от того, используется ли функция **или** **режим блокирования.**  При работе **с функциями** встроенные сценарии HTML-файлы воспринимаются как функции.  Если сценарий выполняется во всех, devTools помечает весь сценарий как использовавшийся код.  Только если сценарий выполняется во всех DevTools, помечается сценарием как неиспользуемый код.  

> ##### Рисунок17  
> Раскрывающееся меню режима перекрытия  
> ![Раскрывающееся меню режима перекрытия][ImageCoverageMode]  

#### Кoveroverage теперь должен быть инициировано перезагрузкой страницы  

Переключение кода без перезагрузки страницы была удалена, так как данные покрытия не нарушались.  Например, функция может быть получена как неиспользуемая, если время выполнения была длительное время назад, а сборщик V8 гарбризовала ее.  

Проблема с [хромом#1004203][crbug1004203]  

## Скачивание каналов с предварительными версиями Microsoft Edge  

Если вы используете Windows или macOS, рекомендуем использовать каналы [предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Каналы с предварительными версиями доступны новейшие функции Разработчиков.  

## Совместная работа с помощью команды разработчиков Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2019/12/a11y-performance-tool.msft.gif "Рис. 1. Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана"  
[ImageLocalizedGerman]: ../../images/2019/12/localized-devtools.msft.png "Изображение 2. Разработчики в немецких"  
[ImageHintsTabWebhintExtension]: ../../images/2019/12/webhint-browser-extension.msft.png "Рис. 3. Вкладка "Подсказки" в Microsoft Edge DevTools, если установлено расширение веб-браузера"  
[Image3DView]: ../../images/2019/12/3dview.msft.png "Рис. 4. Трехмерное представление в средствах разработчиков Microsoft Edge"  
[ImageElementsVisualStudioCode]: ../../images/2019/12/elements-for-edge.msft.png "Рис. 5. Инструмент "Элементы" в коде VS с помощью элементов расширения Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2019/12/vscode-debugger.msft.png "Р. Отладка для Расширения Microsoft Edge в коде VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2019/12/webhint-vscode-extension.msft.png "Рис. Расширение webhint VS-кода VS в коде VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2019/12/vs.msft.png "Рис. Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Бета-версии"  
[ImageTrackingPrevention]: ../../images/2019/12/tracking-prevention.msft.png "Р. Сообщения в консоли при блокировке отслеживания блокируют доступ к хранилищу для отслеживания"  
[ImageConsoleRedeclarationFails]: ../../images/2019/12/letbefore.msft.png "Рис. 10: консоль в Microsoft Edge 79, показывающая, что разрешить отказ отклонения не удается"  
[ImageConsoleRedeclarationSucceeds]: ../../images/2019/12/letafter.msft.png "Рис. 11: консоль в Microsoft Edge 80 показывает, что разрешение отклонения разрешено успешно"  
[ImageRequestInitiatorChain]: ../../images/2019/12/initiators.msft.png "Рис. 12: инициатор запросов на вкладке "Инициатор""  
[ImageOverviewPaneInspectedResource]: ../../images/2019/12/overview.msft.png "Рис. 13: область обзора, на ведущей проверенный ресурс"  
[ImagePathNetworkPanel]: ../../images/2019/12/columns.msft.png "Рис. 14: новые столбцы пути и URL-адреса на панели сети"  
[ImageUserAgentNetworkConditionsTab]: ../../images/2019/12/useragent.msft.png "Рис. 15: меню агента пользователя на вкладке "Сетевые условия""  
[ImageConfigurationUI]: ../../images/2019/12/start.msft.png "Рис. 16: новый элемент управления конфигурацией"  
[ImageCoverageMode]: ../../images/2019/12/modes.msft.png "Рис. 17: раскрывающееся меню режима переключения"  

<!--[ImageDwarfPoweredWebAssemblyDebugging]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Команды с помощью меню «Средства разработчика» microsoft Edge"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Поиск кодов JavaScript и CSS с помощью вкладки Coverage в Microsoft Edge DevTools"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Одновременный просмотр для мобильных устройств : одновременный режим устройств с режимом устройств в Microsoft Edge DevTools"  
[DevToolsNetworkIndex]: ../../../network/index.md "Проверка действий с ее сетью в средствах разработчиков Microsoft Edge"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: ../../../network/reference.md#view-initiators-and-dependencies "Просмотр инициатив и зависимостей — справочник по сетевому анализу"  
[DevGuideEdgeHtmlWhatsNew]: ../../../../dev-guide/whats-new.md "Новые возможности Microsoft EdgeHTML"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Отладка расширения кода Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Элементы расширения кода Microsoft Edge VS"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[crbug842488]: https://crbug.com/842488 "842488: добавление поля "Инициатор" на вкладку "Заголовки" — "Морели"."  
[crbug988253]: https://crbug.com/988253 "988253 - ошибка DevTools — Без связи между сетевым запросом и графиком "График" — "Транспорт""  
[crbug993366]: https://crbug.com/993366 "993366. Отобразите путь к URL-адресу в списке запросов на сетевую панель ( произвольный"  
[crbug1004193]: https://crbug.com/1004193 "1004193 — режим REPL для V8 — монor"  
[crbug1004203]: https://crbug.com/1004203 "1004203 — Мондия"  
[crbug1029031]: https://crbug.com/1029031 "1029031 — строки США устарели, — монорский" 
[crbug963183]: https://crbug.com/963183 "963183 — средства для разработки не совместимо с WCAG"
[crbug941561]: https://crbug.com/941561 "941561 — локализация средств разработчиков"
[crbug987787]: https://crbug.com/987787 "987787 — Dom 3D View"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Сведения о специальных возможностях"  

[DwarfHome]: https://dwarfstd.org "Домашняя страница Двуха"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Панель аудита DevTools' на панели регулирования: GoogleChrome/lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема: MicrosoftDocs/edge-разработчики"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Отладка JavaScript в Microsoft Edge с Visual Studio | Visual Studio блог"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачивание Visual Studio 2019 для Windows \& для Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools твиттер"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio код"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладка для Microsoft Edge — Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \(Chromium\) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение Webhint для браузера | документация веб-хинтерской документации"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение веб-кода VS | документация веб-хинтерской документации"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение отслеживания исправлений в записях блога Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Нужный веб-час"

> [!NOTE]
> Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]  
> Исходная страница [here](https://developers.google.com/web/updates/2019/12/devtools/index) находится на сайте [Kayce Basques][KayceBasques] \(технический автор, Chrome DevTools & Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

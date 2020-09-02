---
title: Новые возможности DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4f155a99d28d208bc288e3175b49c221684619a0
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991197"
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

# Новые возможности DevTools (Microsoft Edge 80)  

## Объявления из группы Microsoft Edge DevTools  

В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams! Узнайте, как использовать новые функции в DevTools, расширения кода VS и многое другое.  Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].  

### Улучшение специальных возможностей в DevTools  

Группа DevTools изменила 170 в Chromium для устранения проблем с высокой контрастностью цвета, клавиатуры и средства чтения с экрана в DevTools.  Каждый разработчик, создающий веб-сайт, должен иметь возможность использовать DevTools.  

> ##### Рис. 1  
> Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана  
> ![Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

Сведения о том, как сделать веб-страницу доступной для всех пользователей?  Скачайте [расширения для][WebhintBrowserExtension] Microsoft Edge " [Специальные возможности][AccessibilityInsights] ", чтобы приступить к работе.  

Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) !  

[#963183][crbug963183] проблем с Chromium  

### Использование DevTools на других языках  

Многие разработчики используют другие инструменты разработчика, такие как StackOverflow и код VS, на родном языке, а не только на английском языке.  Мы рады объявить локализацию для DevTools, который теперь вы можете использовать на одном из 10 языков, кроме английского.  

:::row:::
   :::column span="":::
      Китайский (упрощенное письмо) —  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Китайский (традиционное письмо) —  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Французский — Fran&#231;AIS
   :::column-end:::
   :::column span="":::
      Немецкий — Deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Итальянский — Italiano
   :::column-end:::
   :::column span="":::
      Японская  &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Корейский —  &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Португальский (portugu&#234;s)
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Русский —  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Испанская — ESPA&#241;OL
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

Перейдите к разделу `edge://flags` **Включение локализованных средств разработчика** в состояние **включено**и установите для него флажок Включить.  Также установите флажок **эксперименты со средствами разработчика** для **включения**.  Перезапустите Microsoft EDGE и откройте DevTools.  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  DevTools соответствует языку, используемому в Microsoft Edge in `edge://settings/languages` .  

> ##### Рисунок 2  
> DevTools на немецком языке  
> ![DevTools на немецком языке][ImageLocalizedGerman]  

Если вы хотите использовать DevTools на языке, отличном от того, на котором они доступны, [твит][PostTweetEdgeDevTools] в США или щелкните значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#941561][crbug941561] проблем с Chromium  

### Веб – подсказка с расширением Microsoft Edge  

Расширение веб-подсказки Microsoft EDGE позволяет легко находить и получать отзывы о специальных возможностях, совместимости с браузерами, безопасности, производительности и других средствах в DevTools.  Узнайте больше о [https://webhint.io][Webhint] .  

> ##### Рисунок3  
> Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.  
> ![Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.][ImageHintsTabWebhintExtension]  

[Попробуйте расширение браузера веб для подсказки в Microsoft Edge][MicrosoftEdgeInsiderAddons].  После установки расширения откройте DevTools и перейдите на вкладку подсказки.  В этой статье запустите настраиваемое сканирование сайта.  Чтобы получить дополнительные сведения, [заwebhint.IO][WebhintBrowserExtension] в голову.

### Трехмерное представление  

С помощью **трехмерного представления** вы можете выполнять отладку своего веб-приложения, перемещаясь по [объектной модели документов \ (DOM)][MDNDocumentObjectModel] или контексту стека [z-индексов][MDNZIndex] .  

> ##### Рисунок4  
> Трехмерное представление в DevTools  
> ![Трехмерное представление в DevTools][Image3DView]  

Чтобы получить доступ к трехмерному представлению, перейдите в раздел `edge://flags` и убедитесь, что флаг **эксперименты со средствами разработчика** установлен в **разрешено**.  Перезапустите Microsoft EDGE и откройте DevTools.  Нажмите кнопку `F1` DevTools или выберите **Параметры**, перейдите к разделу " **эксперименты** " и установите флажок **включить трехмерное представление** .  Теперь нажмите клавишу `Ctrl`  +  `Shift`  +  `P` Ввод в **3D-представление** и выберите **Показать 3D-представление**.  

Мы работаем над ИНТЕРФЕЙСом и добавляем дополнительные функции в представление 3D, поэтому отправьте нам свой [отзыв](#getting-in-touch-with-microsoft-edge-devtools-team).  

[#987787][crbug987787] проблем с Chromium

### Расширения кода Visual Studio  

Кроме того, Группа DevTools также выпустила некоторые расширения для [кода Visual Studio \ (код VS)][VisualStudioCode] , которые позволяют использовать возможности DevTools прямо из текстового редактора. Ознакомьтесь с приведенными ниже расширениями.  

#### Элементы Microsoft Edge  

С помощью инструмента "элементы" в коде VS добавьте [элементы для расширения кода Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs.  

> ##### Рисунок 5  
> Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge  
> ![Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge][ImageElementsVisualStudioCode]  

Для получения дополнительных сведений изучите [элементы для расширения кода Microsoft Edge VS][VisualStudioCodeElementEdgeExtension].  

#### Отладчик для Microsoft Edge  

С помощью [отладчика для расширения кода Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] , Отладка JavaScript выполняется в Microsoft Edge прямо из кода vs.  

> ##### Рисунок6  
> Отладчик для расширения Microsoft EDGE в коде VS  
> ![Отладчик для расширения Microsoft EDGE в коде VS][ImageDebuggerExtensionVisualStudioCode]  

Дополнительные сведения [об отладке Microsoft Edge из кода VS можно][VisualStudioCodeDebuggerEdgeExtension]найти здесь.  

#### webhint  

Расширение веб- [подсказки][VisualStudioMarketplaceWebhintExtension] и кода используются `webhint` для усовершенствования своей страницы, пока вы пишете ее! Это расширение запускает и сообщает диагностику файлов рабочей области на основе `webhint` анализа.  

> ##### Рисунок7  
> Анализ файла и расширения кода веб-подсказки в коде VS  
> ![Анализ файла и расширения кода веб-подсказки в коде VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

[Узнайте больше о расширении подсказки кода VS][WebhintVisualStudioCodeExtension].  

### Интеграция с Visual Studio
В Visual Studio 2019 версии 16,2 или более поздней Используйте отладчик Visual Studio для отладки JavaScript, который выполняется в Microsoft Edge.  [Загрузите Visual Studio 2019][MicrosoftVisualStudioDownloads] , чтобы попробовать эту функцию!  

> ##### Рисунок8  
> Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta  
> ![Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta][ImageVisualStudioLaunchWebApp]  

[В этой статье рассказывается о том, как отлаживать Microsoft Edge из Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].  

### Сообщения консоли предотвращения отслеживания  

Защита от слежения — это уникальная функция в Microsoft EDGE, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещаете.  Параметр предотвращения отслеживания по умолчанию — это режим балансировки, который блокирует средства отслеживания и известных злоумышленников, чтобы обеспечить баланс конфиденциальности и веб-совместимости.  Чтобы получить более подробную информацию о совместимости веб-страницы, если некоторые средства отслеживания заблокированы, мы также добавили предупреждающие сообщения на консоли, когда средство отслеживания заблокировано.  

> ##### Рисунок9  
> Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания  
> ![Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания][ImageTrackingPrevention]  

[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью][TrackingPrevention].  

## Объявления из проекта Chromium  

В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 80, которые были задействованы в проекте Open Source Chromium.  

### Поддержка повторной декларации Let и Class на консоли  

Теперь консоль поддерживает повторное объявление `let` `class` операторов and.  Невозможность повторного объявления — это распространенный annoyance для веб-разработчиков, использующих консоль для экспериментов с новым кодом JavaScript.  

> [!WARNING]
> При повторном объявлении `let` `class` оператора или в сценарии, находящегося за пределами консоли или при вводе с помощью одного из входных данных в командной консоли возникает проблема `SyntaxError` .  

Например, ранее при повторном объявлении локальной переменной `let` консоль вызвала ошибку:  

> ##### Рисунок 10  
> Консоль в Microsoft Edge 79 показывает, что повторное объявление Let не выполняется  
> ![Консоль в Microsoft Edge 79 показывает, что повторное объявление Let не выполняется][ImageConsoleRedeclarationFails]  

Теперь консоль допускает повторное объявление:  

> ##### Рисунок11  
> Консоль в Microsoft Edge 80, на которой показано, что повторное объявление Let успешно.  
> ![Консоль в Microsoft Edge 80, на которой показано, что повторное объявление Let успешно.][ImageConsoleRedeclarationSucceeds]  

[#1004193][crbug1004193] проблем с Chromium  

### Улучшенная Отладка сборок  

DevTools начал поддерживать [стандарт отладки dwarf][DwarfHome], что означает увеличение поддержки степпинга кода, установки точек останова и разрешения трассировки стека на исходном языке в DevTools.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### Обновления панели сети  

#### Цепочки инициаторов запросов на вкладке инициатора  

Теперь вы можете просмотреть инициаторы и зависимости сетевого запроса как вложенный список.  Это может помочь вам понять, почему был запрошен ресурс, а также о том, какая сетевая активность связана с определенным ресурсом (например, сценарием).  

> ##### Рисунок12  
> Цепочка инициаторов запросов на вкладке инициатора  
> ![Цепочка инициаторов запросов на вкладке инициатора][ImageRequestInitiatorChain]  

После [входа в сеть на панели Network (сеть][DevToolsNetworkIndex]) выберите ресурс и перейдите на вкладку **инициатор** , чтобы просмотреть **цепочку инициаторов запроса**.  

*   **Проверенный ресурс** выделяется полужирным шрифтом.  На снимке экрана выше `ai.2.min.js` показан проверенный ресурс.  
*   Ресурсы, расположенные выше проверенного ресурса, являются **инициаторами**.  На снимке экрана выше `https://www.microsoftedgeinsider.com` — инициатор `ai.2.min.js` .  Другими словами, `https://www.microsoftedgeinsider.com` это привело к сетевому запросу `ai.2.min.js` .  
*   Ресурсы, расположенные под проверенным ресурсом, являются **зависимостями**.  На снимке экрана выше `https://dc.services.visualstudio.com/v2/track` есть зависимость `ai.2.min.js` .  Другими словами, `ai.2.min.js` это привело к сетевому запросу `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> Кроме того, можно получить доступ к сведениям об инициаторе и `Shift` наведении указателя мыши на ресурсы сети.  Просмотр [инициаторов и зависимостей][DevToolsNetworkReferenceViewInitiatorsDependencies].  

[#842488][crbug842488] проблем с Chromium  

#### Выделение выбранного сетевого запроса в обзоре  

После выбора сетевого ресурса для его проверки на панели Network (сеть) размещается синяя рамка вокруг **ресурса.**  Это поможет определить, является ли сетевой запрос более ранней или более поздней, чем ожидалось.  

> ##### Рисунок13  
> Область "Обзор", в которой выделяются проверенные ресурсы  
> ![Область "Обзор", в которой выделяются проверенные ресурсы][ImageOverviewPaneInspectedResource]  

[#988253][crbug988253] проблем с Chromium  

#### URL-адреса и столбцы "путь" на панели "сеть"  

С помощью столбцов «новый **путь** » и « **URL-адрес** » на панели **Network (сеть** ) можно просмотреть абсолютный путь к каждому СЕТЕВОМУ ресурсу или полный URL-адрес.  

> ##### Рисунок14  
> Столбцы "новый путь" и "URL-адрес" на панели "сеть"  
> ![Столбцы "новый путь" и "URL-адрес" на панели "сеть"][ImagePathNetworkPanel]  

Щелкните заголовок **каскадной** таблицы правой кнопкой мыши и выберите команду **путь** или **URL-адрес** , чтобы отобразить новые столбцы.  

[#993366][crbug993366] проблем с Chromium  

#### Обновлены строки агента пользователя  

DevTools поддерживает задание пользовательской строки агента пользователя на вкладке **условия сети** .  Строка агента пользователя влияет на `User-Agent` заголовок HTTP, подключенный к сетевым ресурсам, а также на значение `navigator.userAgent` .  

Предопределенные строки агента пользователя обновлены в соответствии с современными версиями браузера.  

> ##### Рисунок15  
> Меню агента пользователя на вкладке "условия сети"  
> ![Меню агента пользователя на вкладке "условия сети"][ImageUserAgentNetworkConditionsTab]  

Чтобы получить доступ к **сетевым условиям**, [откройте меню команд][DevToolsCommandMenuIndex] и выполните `Show Network Conditions` команду.  

> [!NOTE]
> Вы также можете [задать строки агента пользователя в режиме устройства][DevToolsDeviceModeIndex].  

[#1029031][crbug1029031] проблем с Chromium  

### Обновления панели аудита  

#### Новый пользовательский интерфейс конфигурации  

Пользовательский интерфейс конфигурации имеет новый, реагирующий дизайн и параметры конфигурации регулирования были упрощены.  Дополнительные сведения об изменении пользовательского интерфейса для регулирования приведены в разделе [Аудит][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .  

> ##### Рисунок16  
> Новый пользовательский интерфейс конфигурации  
> ![Новый пользовательский интерфейс конфигурации][ImageConfigurationUI]  

### Обновления вкладок покрытия  

#### Режимы покрытия для отдельных функций или отдельных блоков  

На [вкладке Coverage][DevToolsCoverageIndex] имеется новое раскрывающееся меню, в котором можно указать, нужно ли собирать данные о покрытии кода **для одной функции** или **для каждого блока**.  Покрытие **за блоком** является более подробным, но и более затратным для сбора.  DevTools по умолчанию использует **функцию на уровне отдельных функций** .  

> [!CAUTION]
> В зависимости от того, используется ли **функция** **или режим, в HTML** -файлах могут возблюдаться большие различия в покрытии кода.  При использовании режима " **на функцию** " встроенные сценарии в HTML-файлах рассматриваются как функции.  Если сценарий выполняется, DevTools помечает весь сценарий как использованный код.  Если сценарий не выполняется вообще, DevTools помечает сценарий как неиспользуемый код.  

> ##### Рисунок17  
> Раскрывающееся меню «режим покрытия»  
> ![Раскрывающееся меню «режим покрытия»][ImageCoverageMode]  

#### Теперь покрытие должно быть инициировано перезагрузкой страницы  

Переключение покрытия кода без повторной загрузки страницы удалено, так как данные о покрытии были ненадежны.  Например, функция может быть указана как неиспользуемая, если среда выполнения была длиннее давно, а сборщик мусора V8 удалил его.  

[#1004203][crbug1004203] проблем с Chromium  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge DevTools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2019/12/a11y-performance-tool.msft.gif "Рисунок 1: средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана"  
[ImageLocalizedGerman]: ../../images/2019/12/localized-devtools.msft.png "Рисунок 2: DevTools на немецком языке"  
[ImageHintsTabWebhintExtension]: ../../images/2019/12/webhint-browser-extension.msft.png "Рисунок 3: вкладка "Подсказка" в Microsoft Edge DevTools, когда установлено расширение браузера веб."  
[Image3DView]: ../../images/2019/12/3dview.msft.png "Рисунок 4:3D-представление в Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2019/12/elements-for-edge.msft.png "Рисунок 5. инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2019/12/vscode-debugger.msft.png "Рисунок 6: отладчик для расширения Microsoft EDGE в коде VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2019/12/webhint-vscode-extension.msft.png "Рис. 7: расширение веб-подсказки и кода анализ целевого файла в коде VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2019/12/vs.msft.png "Рисунок 8: Visual Studio с возможностью запуска вашего веб-приложения в Microsoft Edge Канарские, dev или Beta"  
[ImageTrackingPrevention]: ../../images/2019/12/tracking-prevention.msft.png "Рис. 9: сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания."  
[ImageConsoleRedeclarationFails]: ../../images/2019/12/letbefore.msft.png "Рис. 10: консоль в Microsoft Edge 79 показывает, что повторное объявление Let не выполняется"  
[ImageConsoleRedeclarationSucceeds]: ../../images/2019/12/letafter.msft.png "На рисунке 11: консоль в Microsoft Edge 80 показывает, что повторное объявление Let успешно."  
[ImageRequestInitiatorChain]: ../../images/2019/12/initiators.msft.png "Рисунок 12: цепочка инициаторов запросов на вкладке инициатора"  
[ImageOverviewPaneInspectedResource]: ../../images/2019/12/overview.msft.png "Рисунок 13: область "Обзор", в которой выделяются проверенные ресурсы"  
[ImagePathNetworkPanel]: ../../images/2019/12/columns.msft.png "Рисунок 14: столбцы "новый путь" и "URL-адрес" на панели "сеть""  
[ImageUserAgentNetworkConditionsTab]: ../../images/2019/12/useragent.msft.png "Рисунок 15: меню агента пользователя на вкладке условия сети"  
[ImageConfigurationUI]: ../../images/2019/12/start.msft.png "Рисунок 16: новый пользовательский интерфейс конфигурации"  
[ImageCoverageMode]: ../../images/2019/12/modes.msft.png "Рисунок 17: раскрывающееся меню «режим покрытия»"  

<!--[ImageDwarfPoweredWebAssemblyDebugging]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильного просмотра экрана — Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools"  
[DevToolsNetworkIndex]: ../../../network/index.md "Проверка активности сети в Microsoft Edge DevTools"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: ../../../network/reference.md#view-initiators-and-dependencies "Просмотр инициаторов и зависимостей — справочные материалы по анализу сети"  
[DevGuideEdgeHtmlWhatsNew]: ../../../../dev-guide/whats-new.md "Новые возможности EdgeHTML"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Отладчик для расширения кода Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Элементы расширений Microsoft EDGE и кода"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[crbug842488]: https://crbug.com/842488 "842488 — Добавление поля инициатора на вкладку заголовки — Monorail"  
[crbug988253]: https://crbug.com/988253 "988253 — ошибка DevTools — отсутствует связь между сетевым запросом и графом временной шкалы — Monorail"  
[crbug993366]: https://crbug.com/993366 "993366 — часть URL-адреса в списке запросов на панели "сеть" — monorail."  
[crbug1004193]: https://crbug.com/1004193 "1004193-режим REPL для V8-Monorail"  
[crbug1004203]: https://crbug.com/1004203 "1004203-Monorail"  
[crbug1029031]: https://crbug.com/1029031 "Строки 1029031-UA устарели — Monorail" 
[crbug963183]: https://crbug.com/963183 "963183-DevTools не соответствуют требованиям WCAG"
[crbug941561]: https://crbug.com/941561 "941561 – локализуемость DevTools"
[crbug987787]: https://crbug.com/987787 "987787 – трехмерный вид DOM"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Аналитические сведения о специальных возможностях"  

[DwarfHome]: https://dwarfstd.org "Домашняя страница dwarf"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools ' Аудит регулирования панели — GoogleChrome/Lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки Microsoft Edge для участников программы предварительной оценки"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Отладка JavaScript в Microsoft Edge из Visual Studio | Блог Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачайте Visual Studio 2019 для Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Код Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладчик для Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \ (Chromium \) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code ""Подсказка" — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "Подсказка"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузеров веб – подсказок | Документация по подсказкам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение ссылки и кода Документация по подсказкам"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение защиты от слежения в блоге Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2019/12/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

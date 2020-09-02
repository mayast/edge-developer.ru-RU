---
title: Новые возможности DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 10696a49a833475d59a6be1189362fdb0c26a96d
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991150"
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

# Новые возможности DevTools (Microsoft Edge 81)  

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
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

DevTools автоматически соответствует языку, который вы используете для Microsoft Edge in `edge://settings/languages` .  

Если вы хотите, чтобы Microsoft Edge выоставался на одном языке, а DevTools на русском языке, нажмите кнопку `F1` DevTools, чтобы открыть вкладку [Параметры][Settings] и отключить **язык браузера**.  

> ##### Рисунок 2  
> DevTools на немецком языке  
> ![DevTools на немецком языке][ImageLocalizedGerman]  

Сообщения **консоли** не локализуются.  На языке, используемом для Microsoft EDGE, отображаются только строки, используемые в пользовательском интерфейсе DevTools.  

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

Для доступа к трехмерному представлению нажмите клавишу `Ctrl`  +  `Shift`  +  `P` Ввод в **режиме 3D-представления** и выберите **Показать 3D-представление**.  

Мы работаем над ИНТЕРФЕЙСом и добавляем дополнительные функции в 3D-представление, поэтому отправьте нам свой [отзыв](#getting-in-touch-with-microsoft-edge-devtools-team).  

[#987787][crbug987787] проблем с Chromium  

### Расширения кода Visual Studio  

Кроме того, Группа DevTools также выпустила некоторые расширения для [кода Visual Studio \ (код VS)][VisualStudioCode] , которые позволяют использовать возможности DevTools прямо из текстового редактора. Ознакомьтесь с приведенными ниже расширениями.  

#### Элементы Microsoft Edge  

С помощью инструмента "элементы" в коде VS добавьте [элементы для расширения кода Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs.  

> ##### Рисунок 5  
> Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge — ![ инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge][ImageElementsVisualStudioCode]  

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

Дополнительные [сведения об отладке Microsoft Edge из Visual Studio][MicrosoftVisualStudio].  

### Сообщения консоли предотвращения отслеживания  

Защита от слежения — это уникальная функция в Microsoft EDGE, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещаете.  Параметр предотвращения отслеживания по умолчанию — это режим балансировки, который блокирует средства отслеживания и известных злоумышленников, чтобы обеспечить баланс конфиденциальности и веб-совместимости.  Чтобы получить более подробную информацию о совместимости веб-страницы, если некоторые средства отслеживания заблокированы, мы также добавили предупреждающие сообщения на консоли, когда средство отслеживания заблокировано.  

> ##### Рисунок9  
> Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания  
> ![Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания][ImageTrackingPrevention]  

[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью][TrackingPrevention].  

## Объявления из проекта Chromium  

В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 81, которые были задействованы в проекте Open Source Chromium.  

### Поддержка Moto G4 в режиме устройства  

После [включения панели инструментов устройства][DeviceToolbar]имитируйте размеры окна просмотра Moto G4 в списке **устройств** .  

> ##### Рисунок 10  
> Имитация окна просмотра Moto G4  
> ![Имитация окна просмотра Moto G4][ImageMotoG4]  

Щелкните [Показать рамку устройства][DeviceFrame] , чтобы показать аппаратуру Moto G4 в окне просмотра.  

> ##### Рисунок11  
> Аппаратное обеспечение Moto G4  
> ![Аппаратное обеспечение Moto G4][ImageMotoG4Frame]  

Дополнительные возможности:  

*   Откройте [меню команд][CommandMenu] и выполните команду, `Capture screenshot` чтобы сделать снимок экрана просмотра, включающий оборудование Moto G4 (после включения команды **Показать рамку устройства**).  
*   [Регулирование сети и ЦП][ThrottleNetworkAndCpu] для более точной имитации условий просмотра веб-страниц пользователя на мобильном устройстве.  

[#924693][crbug924693] проблем с Chromium  

### Обновления, связанные с файлами cookie  

#### Заблокированные cookie-файлы в области "cookie"  

В области "файлы cookie" на панели приложения теперь отображаются заблокированные файлы cookie с желтым фоном.  

> ##### Рисунок12  
> Заблокированные cookie-файлы в области "cookie" на панели приложения  
> ![Заблокированные cookie-файлы в области "cookie" на панели приложения][ImageBlockedCookies]  

[#1030258][crbug|::ref1::|] проблем с Chromium  

#### Приоритет cookie-файлов в области "cookie"  

Таблицы cookie на панелях сеть и приложения теперь включают столбец **приоритета** .  

> [!CAUTION]
> Chromiumные браузеры, такие как Microsoft EDGE, — это единственные браузеры, поддерживающие приоритет cookie-файлов.  

[#1026879][crbug1026879] проблем с Chromium  

#### Изменение всех значений cookie-файлов  

Все ячейки в таблицах cookie теперь доступны для редактирования, кроме ячеек в столбце **Размер** , так как этот столбец представляет размер файла cookie в байтах.  Просмотрите [поля][CookiesFields] , поясняющие каждый столбец.  

> ##### Рисунок13  
> Изменение значения cookie-файла  
> ![Изменение значения cookie-файла][ImageEditCookie]  

#### Копирование как Node.js выбор для включения данных cookie  

Щелкните правой кнопкой мыши по сетевому запросу и выберите команду **Копировать**  >  **копию как Node.js извлечь** , чтобы получить `fetch` выражение, включающее данные cookie.  

> ##### Рисунок14  
> Копирование как Node.js выборка  
> ![Копирование как Node.js выборка][ImageCopyFetch]  

[#1029826][crbug1029826] проблем с Chromium  

### Более точные значки манифеста веб-приложения  

Ранее область манифеста на панели приложения отправляет свои собственные запросы для отображения значков манифеста веб-приложения.  DevTools теперь показывает тот же значок манифеста, который использует Microsoft Edge.  

> ##### Рисунок15  
> Значки в области «манифест»  
> ![Значки в области «манифест»][ImageManifestIcon]  

[#985402][crbug985402] проблем с Chromium  

### Наведите указатель мыши на свойства содержимого CSS, чтобы увидеть неэкранированные значения  

Наведите указатель мыши на значение `content` свойства, чтобы увидеть неэкранированную версию значения.  

Например, в этой статье вы узнаете [о том,][CSSContentDemo] что на `p::after` панели Стили отображается строка с escape-символами.  

> ##### Рисунок16  
> Строка с escape-символом  
> ![Строка с escape-символом][ImageEscapedString]  

При наведении указателя мыши на значение, которое `content` отображается в неэкранированном значении:  

> ##### Рисунок17  
> Неэкранированное значение  
> ![Неэкранированное значение][ImageUnescapedString]  

### Дополнительные сведения об ошибках на карте исходного кода на консоли  

Теперь консоль содержит более подробные сведения о том, почему не удалось загрузить или проанализировать исходную карту.  Ранее она только что предоставила ошибку, не объясняющую, что пошло не так.  

> ##### Рис. 18  
> Ошибка при загрузке карты исходного кода на консоли  
> ![Ошибка при загрузке карты исходного кода на консоли][ImageSourcemapError]  

### Настройка отключения прокрутки за пределами файла  

Откройте [Параметры][Settings] и выберите Отключить **Preferences**  >  **исходные**настройки.  >  **разрешите прокрутку за** пределами файла, чтобы отключить поведение пользовательского интерфейса по умолчанию, позволяющее прокручивать прокрутку за пределами файла на панели « **источники** ».  

> ##### На рисунке 19  
> Отключение **разрешения на прокрутку за** пределами файла в параметрах  
> ![Отключение разрешения на прокрутку за пределами файла][ImageSettings]  

> ##### Рис. 20  
> Прокрутка за пределами файла теперь отключена на панели «источники»  
> ![Прокрутка за пределами файла теперь отключена на панели «источники»][ImageScroll]  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge DevTools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- <<../../_shared/devtools-feedback.md>>  

<<../../_shared/canary.md>>  

<<../../_shared/discover.md>> -->  

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Рисунок 1: средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Рисунок 2: DevTools на немецком языке"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Рисунок 3: вкладка "Подсказка" в Microsoft Edge DevTools, когда установлено расширение браузера веб."  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Рисунок 4:3D-представление в Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Рисунок 5. инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Рисунок 6: отладчик для расширения Microsoft EDGE в коде VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Рис. 7: расширение веб-подсказки и кода анализ целевого файла в коде VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Рисунок 8: Visual Studio с возможностью запуска вашего веб-приложения в Microsoft Edge Канарские, dev или Beta"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Рис. 9: сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания." 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Рисунок 10: Имитация окна просмотра Moto G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Рисунок 11: демонстрация оборудования Moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Рисунок 12: заблокированные cookie-файлы в области "cookie" на панели приложения"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Рисунок 13: Редактирование значения cookie-файла"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Рисунок 14: копирование как Node.js выборка"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Рисунок 15: значки в области манифеста"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Рисунок 16: строка с escape-символом"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Рисунок 17: Неэкранированное значение"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Рисунок 18: ошибка при загрузке карты исходного кода на консоли"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Рисунок 19: отключение режима "Разрешить прокрутку за конец файла" в параметрах"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Рисунок 20: прокрутка за пределами файла теперь отключена на панели «источники»"

<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильного окна просмотра с помощью режима устройства в Microsoft Edge DevTools"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Нажмите кнопку Показать рамку устройства, чтобы отобразить рамку физического устройства вокруг окна просмотра."
[CommandMenu]: ../../../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Регулирование сети и ЦП для более точной имитации условий просмотра веб-страниц пользователя на мобильном устройстве."
[crbug924693]: https://crbug.com/924693 "924693: запрос компонента: Добавление Moto G4 в список режимов устройства"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: вкладка cookie в консоли разработки больше не показывает приоритет"
[CookiesFields]: ../../../storage/cookies.md#fields "Поля в таблице cookie-файлов"
[crbug1029826]: https://crbug.com/1029826 "1029826: вкладка "сеть" — > щелчок правой кнопкой мыши для запроса на > копирование > копирование в качестве выборке не копирует файлы cookie"
[crbug985402]: https://crbug.com/985402 "985402: ошибки значков в манифесте веб-приложения — это запутанная строка"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Демонстрация для без последовательного содержимого CSS"
[Settings]: ../../../customize/index.md#settings "Настройка Microsoft Edge DevTools с помощью параметров"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  
[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Отладчик для расширения кода Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Элементы расширений Microsoft EDGE и кода"  
[crbug963183]: https://crbug.com/963183 "963183-DevTools не соответствуют требованиям WCAG"
[crbug941561]: https://crbug.com/941561 "941561 – локализуемость DevTools"
[crbug987787]: https://crbug.com/987787 "987787 – трехмерный вид DOM"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Аналитические сведения о специальных возможностях"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки Microsoft Edge для участников программы предварительной оценки"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачайте Visual Studio 2019 для Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Код Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладчик для Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \ (Chromium \) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code ""Подсказка" — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "Подсказка"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузеров веб – подсказок | Документация по подсказкам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение ссылки и кода Документация по подсказкам"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение защиты от слежения в блоге Microsoft Edge"

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/01/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
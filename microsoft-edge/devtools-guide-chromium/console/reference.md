---
title: Справочник по консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601789"
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





# Справочник по консоли   



Эта страница содержит ссылки на возможности, связанные с консолью Microsoft Edge DevTools.  Предполагается, что вы уже знакомы с использованием консоли для просмотра сообщений в журнале и запуска JavaScript.  В противном случае ознакомьтесь [со статьей начало работы с JavaScript на консоли][DevToolsConsoleJavascript] и начните [работу с сообщениями в журнале на консоли][DevToolsConsoleLog].  

Если вы ищете ссылку API на функции, такие как `console.log()` , [Справочник по API консоли][DevToolsConsoleApi].  Дополнительные сведения о функциях, таких как `monitorEvents()` [Справка по API для консольных утилит][DevToolsConsoleUtilities].  

## Открытие консоли   

Вы можете открыть консоль как [панель](#open-the-console-panel) или как [вкладку в ящике](#open-the-console-tab-in-the-drawer).  

### Открытие панели консоли   

Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).  

> ##### Рис. 1  
> Панель консоли  
> ![Панель консоли][ImageConsolePanel]  

Чтобы открыть панель консоли из [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **панели** рядом с ним.  

> ##### Рисунок 2  
> Команда для отображения панели консоли  
> ![Команда для отображения панели консоли][ImageCommandShowConsole]  

### Открытие вкладки "консоль" в ящике   

Нажмите `Escape` или щелкните **настроить DevTools** `...` и выберите пункт **Показать входной ящик консоли**.  

> ##### Рисунок3  
> Показать консольный ящик  
> ![Показать консольный ящик][ImageShowConsoleDrawer]  

Ящик появляется в нижней части окна DevTools и открывается вкладка **консоли** .  

> ##### Рисунок4  
> Вкладка «консоль» в ящике  
> ![Вкладка «консоль» в ящике][ImageDrawerConsole]  

Чтобы открыть вкладку консоль в [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **ящика** рядом с ним.  

> ##### Рисунок 5  
> Команда для отображения вкладки "консоль" в ящике  
> ![Команда для отображения вкладки "консоль" в ящике][ImageShowDrawerCommand]  

### Открытие параметров консоли   

Щелкните Параметры консоли " **Параметры** консоли" ![ ][ImageSettingsButtonIcon] .  

> ##### Рисунок6  
> Параметры консоли  
> ![Параметры консоли][ImageConsoleSettings]  

Ниже описаны ссылки для каждого параметра.  

*   [**Скрыть сеть**](#hide-network-messages)  
*   [**Сохранить журнал**](#persist-messages-across-page-loads)  
*   [**Только выделенный контекст**](#filter-out-messages-from-different-contexts)  
*   [**Одинаковая группа**](#disable-message-grouping)  
*   [**Запись в журнал XmlHttpRequest**](#log-xhr-and-fetch-requests)  
*   [**Упреждающая Оценка**](#disable-eager-evaluation)  
*   [**Автозаполнение из истории**](#disable-autocomplete-from-history)  

### Открытие боковой панели консоли   

Нажмите кнопку **Показать боковую панель консоли** ![ ][ImageShowConsoleSidebarIcon] , чтобы показать боковую панель, что бывает полезно для фильтрации.  

> ##### Рисунок7  
> Боковая панель консоли  
> ![Боковая панель консоли][ImageConsoleSidebar]  

## Просмотр сообщений   

В этом разделе описаны возможности, которые позволят изменить способ представления сообщений на консоли.  В этом пошаговом руководстве показано, как [Просмотреть сообщения][DevToolsConsoleViewMessages] .  

### Отключение группировки сообщений   

[Откройте параметры консоли](#open-console-settings) и отключите **группу, как** отключить поведение группировки сообщений по умолчанию для консоли.  Посмотрите, как [XHR журнал и](#log-xhr-and-fetch-requests) выводит запросы на получение примера.  

### Регистрация запросов XHR и FETCH   

[Откройте параметры консоли](#open-console-settings) и включите в **журнал записи XMLHttpRequest** , чтобы регистрировать все `XMLHttpRequest` и `Fetch` запросы на консоли по мере их появления.  

> ##### Рисунок8  
> Ведение журнала `XMLHttpRequest` и `Fetch` запросы  
> ![Ведение журнала запросов на XMLHttpRequest и выборку][ImageXhrGrouped]  

В верхнем сообщении на [рисунке 8](#figure-8) показано поведение по умолчанию для группировки консоли.  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### Сохранение сообщений на загрузок страниц   

По умолчанию консоль очищается каждый раз, когда вы загружаете новую страницу.  Чтобы сохранить сообщения на нескольких страницах, [откройте параметры консоли](#open-console-settings) и установите флажок **сохранить журнал** .  

### Скрыть сетевые сообщения   

По умолчанию браузер записывает сетевые сообщения на **консоль**.  Например, выбранное сообщение на [рис. 9](#figure-9) представляет код состояния `429` .  

> ##### Рисунок9  
> Сообщение 429 в консоли  
> ! [Сообщение 429 в консоли] [Image429Message]  

Чтобы скрыть сетевые сообщения, выполните указанные ниже действия.  

1.  [Откройте параметры консоли](#open-console-settings).  
1.  Включите флажок **Скрыть сеть** .  

## Фильтрация сообщений   

Есть несколько способов отфильтровать сообщения на консоли.  

### Фильтрация сообщений браузера   

[Откройте панель консоли](#open-the-console-sidebar) и выберите пункт **сообщения пользователя** , чтобы отображались только те сообщения, которые были получены на странице JavaScript.  

> ##### Рисунок 10  
> Просмотр сообщений пользователя  
> ! [Просмотр сообщений пользователей] [ImageUserMessages]  

### Фильтрация по уровню ведения журнала   

DevTools назначает каждому `console.*` методу уровень серьезности.  Существует 4 уровня: `Verbose` ,, `Info` `Warning` , и `Error` .  Например, `console.log()` входит в `Info` группу, в то время как `console.error()` она находится в `Error` группе.  [Справочник по API консоли][DevToolsConsoleApi] описывает уровень важности каждого применимого метода.  Каждое сообщение, которое браузер записывает на консоль, также имеет уровень серьезности.  Вы можете скрыть любые ненужные сообщения.  Например, если вы заинтересованы в `Error` сообщениях, вы можете скрыть другие три группы.  

Щелкните раскрывающийся список **уровни журнала** , чтобы включить или отключить `Verbose` , `Info` `Warning` или `Error` сообщения.  

> ##### Рисунок11  
> Раскрывающийся список **уровней журнала**  
> ! [Раскрывающийся список уровней журнала] [ImageLogLevels]  

Вы также можете отфильтровать по уровню журнала, [открыв боковую панель консоли](#open-the-console-sidebar) и выбрав пункт **ошибки**, **предупреждения**, **сведения**или **подробный**.  

> ##### Рисунок12  
> Использование боковой панели для просмотра предупреждений  
> ! [Использование боковой панели для просмотра предупреждений] [ImageSidebarWarnings]  

### Фильтрация сообщений по URL-адресу   

Введите и `url:` URL-адрес, чтобы просматривать только те сообщения, которые были отправлены из этого URL-адреса.  После ввода `url:` DevTools появятся все нужные URL-адреса.  Домены также работают.  Например, если `https://example.com/a.js` `https://example.com/b.js` сообщения записываются в журнал, `url:https://example.com` вы можете сосредоточиться на сообщениях из этих 2 сценариев.  

> ##### Рисунок13  
> Фильтр URL-адреса  
> ! [Фильтр URL-адреса] [ImageUrlFilter]  

Введите текст `-url:` , чтобы скрыть сообщения от этого URL-адреса.  Это называется фильтром отрицательных URL-адресов.  

> ##### Рисунок14  
> Фильтр отрицательных URL-адресов, который скрывает все сообщения, соответствующие URL-адресу `https://b.wal.co`  
> ! [Фильтр по отрицательному URL-адресу, который скрывает все сообщения, соответствующие URL-адресу https://b.wal.co ] [ImageNegativeUrlFilter1]  

Вы также можете показывать сообщения с одного URL-адреса, [открыв боковую панель консоли](#open-the-console-sidebar), развернув раздел " **пользовательские сообщения** ", а затем щелкнув URL-адрес сценария, содержащего сообщения, на которые нужно обратить внимание.  

> ##### Рисунок15  
> Просмотр сообщений, которые были получены `wp-ad.min.js`  
> ! [Просмотр сообщений, поступивших из WP-AD. min. js] [ImageNegativeUrlFilter2]  

### Фильтрация сообщений в разных контекстах   

Предположим, что у вас есть реклама \ (AD) на вашей странице.  Рекламное объявление встраивается в приложение `<iframe>` и создает большое количество сообщений на консоли.  Так как объявление запущено в другом [контексте JavaScript](#select-javascript-context), один из способов скрыть сообщения — [открыть параметры консоли](#open-console-settings) и установить флажок **только выбранный контекст** .  

### Фильтрация сообщений, не соответствующих шаблону регулярного выражения   

Введите регулярное выражение, например `/[gm][ta][mi]/` в текстовое поле **Фильтр** , чтобы отфильтровать сообщения, которые не соответствуют этому шаблону.  DevTools проверяет, найден ли шаблон в тексте сообщения или сценарий, который привел к занесению в журнал сообщения.  

> ##### Рисунок16  
> Фильтрация несовпадающих сообщений `/[gm][ta][mi]/`  
> ! [Фильтрация сообщений, не соответствующих выражению Regex] [ImageRegExFilter]  

## Запуск JavaScript   

В этом разделе описаны возможности, связанные с выполнением JavaScript на консоли.  В этом пошаговом руководстве показано, как [запускать JavaScript][DevToolsConsoleOverviewJavascript] .  

### Повторное выполнение выражений из истории   

Нажмите клавишу `Up Arrow` для циклического просмотра истории выражений JavaScript, которые выполнялись на консоли раньше.  Нажмите кнопку `Enter` , чтобы выполнить это выражение еще раз.  

### Просмотр значения выражения в режиме реального времени с помощью выражений с реальными данными   

Если вы обнаружите, что один и тот же выражение JavaScript будет вводиться повторно в консоль, возможно, вам будет проще создать **выражение в реальном времени**.  С помощью **выражений в реальном времени** вы вводите выражение один раз, а затем закрепите его в верхней части консоли.  Значение выражения обновляется почти в режиме реального времени.  Просмотрите [значения выражений JavaScript в реальном времени с помощью выражений с реальными данными][DevToolsConsoleLiveExpressions].  

### Отключение безотлагательной оценки   

По мере ввода выражений JavaScript в консоли **упреждающая Оценка** показывает предварительный просмотр возвращаемого значения для этого выражения.  [Откройте параметры консоли](#open-console-settings) и отключите флажок **упреждающая Оценка** , чтобы отключить предварительный просмотр возвращаемых значений.  

### Отключение автозаполнения из истории   

По мере ввода выражения в всплывающем окне для консоли отображаются выражения, которые были выполнены раньше.  Эти выражения добавляются в начале `>` символа.  [Откройте меню Параметры консоли](#open-console-settings) и отключите флажок **Автозаполнение из журнала** , чтобы отключить отображение выражений из истории.  

> [!NOTE]
> На [рис](#figure-17). 17 `document.querySelector('a')` и `document.querySelector('img')` выражения, которые были оценены ранее.  

> ##### Рисунок17  
> Всплывающее окно "Автозаполнение", в котором отображаются выражения из истории  
> ! [Всплывающее окно "Автозаполнение", в котором отображаются выражения из истории] [ImageHistoryAutocomplete]  

### Выбор контекста JavaScript   

По умолчанию раскрывающийся список **контекстов JavaScript** имеет значение **Top**, которое представляет [контекст просмотра][MDNBrowsingContext] основного документа.  

> ##### Рис. 18  
> Раскрывающийся список **контекстов JavaScript**  
> ! [Раскрывающийся список контекстов JavaScript] [ImageJavascriptContext]  

Предположим, что у вас есть реклама на странице, внедренная в `<iframe>` .  Вы хотите запустить JavaScript, чтобы настроить модель DOM рекламы.  Сначала необходимо выбрать контекст обзора рекламы из раскрывающегося списка **контекстов JavaScript** .  

> ##### На рисунке 19  
> Выбор другого контекста JavaScript  
> ! [Выбор другого контекста JavaScript] [ImageSelectContext]  

## Очистка консоли   

Чтобы очистить консоль, вы можете использовать любой из следующих рабочих процессов:  

*   Нажмите кнопку **Очистить консоль** "очистить консоль" ![ ][ImageClearConsoleIcon] .  
*   Щелкните сообщение правой кнопкой мыши и выберите команду **Очистить консоль**.  
*   Введите текст `clear()` на консоли и нажмите клавишу `Enter` .  
*   Вызов `console.clear()` из JavaScript на веб-странице.  
*   Нажимайте кнопку, `Control` + `L` пока фокус находится на консоли.  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Рисунок 1: панель консоли"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Рисунок 2: команда для отображения панели консоли"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Рисунок 3: отображение консольного ящика"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Рисунок 4: вкладка «консоль» в ящике"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Рисунок 5: команда для отображения вкладки "консоль" в ящике"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Рисунок 6: параметры консоли"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Рисунок 7: Боковая панель консоли"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Рисунок 8: регистрация запросов на XMLHttpRequest и выборку данных"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Show-Network.MSFT.png "Рисунок 9: сообщение 429 в консоли"  
[ImageUserMessages]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-sidebar-drawer-User-messages.MSFT.png "Рисунок 10: Просмотр сообщений пользователя"  
[ImageLogLevels]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Log-Level-Default-Levels.MSFT.png "Рисунок 11: раскрывающийся список" уровни журнала ""  
[ImageSidebarWarnings]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-sidebar-Warnings.MSFT.png "Рисунок 12: Использование боковой панели для просмотра предупреждений"  
[ImageUrlFilter]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Filter-Text.MSFT.png "Рисунок 13: фильтр URL-адреса"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Negative-Filter-Text.MSFT.png "Рисунок 14: фильтр отрицательных URL-адресов, который скрывает все сообщения, соответствующие URL-адресу https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Filter-Text-Specified.MSFT.png "Рисунок 15: Просмотр сообщений, поступивших из WP-AD. min. js"  
[ImageRegExFilter]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Filter-Regex.MSFT.png "Рисунок 16: Фильтрация сообщений, не соответствующих выражению Regex"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Filter-Text-AutoFilter-History.MSFT.png "Рисунок 17: всплывающее окно" Автозаполнение ", в котором отображаются выражения из истории"  
[ImageJavascriptContext]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-DOM-Level-Top.MSFT.png "Рисунок 18: раскрывающийся список контекстов JavaScript"  
[ImageSelectContext]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-DOM-Level-Multiple.MSFT.png "Рисунок 19: выбор другого контекста JavaScript"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Просмотр сообщений с запротоколированием — обзор консоли"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Справочник по API консоли"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "Выполнение JavaScript — обзор консоли"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Начало работы с JavaScript на консоли"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Контроль значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с сообщениями журнала на консоли"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Справочник по API для консольных программ"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Контекст просмотра | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

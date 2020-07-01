---
title: Начало работы с сообщениями журнала на консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 4c930caf60af2b5e276e003378546e147c249548
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843969"
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





# Начало работы с сообщениями журнала на консоли   



В этом интерактивном учебнике показано, как записывать и фильтровать сообщения на консоли [Microsoft Edge DevTools][MicrosoftEdgeDevTools] .  

> ##### Рис. 1  
> Сообщения на консоли  
> ![Сообщения на консоли][ImageLogExample]  

Этот учебник предназначен для выполнения в нужном порядке.  Предполагается, что вы знакомы с основами веб-разработки, например с помощью JavaScript для добавления интерактивности на страницу.  

## Настройка ролика и DevTools   

Этот учебник разработан таким образом, чтобы вы могли открыть демонстрацию и попробовать все рабочие процессы самостоятельно.  После того как вы будете физически подписаться на нее, вы, наверное, захотите запомнить рабочие процессы позже.  

1.  Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **примеры журнала консоли** , чтобы открыть ее на новой вкладке.  
    
    [Примеры журнала консоли][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  Чтобы открыть DevTools, сосредоточьте демонстрацию и нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).  По умолчанию DevTools открывается справа от демонстрации.  
    
    > ##### Рисунок 2  
    > DevTools открывается справа от демонстрации  
    > ! [DevTools открывается справа от демонстрации] [ImageDevToolsRight]  
    
    > [!TIP]
    > [Закрепите DevTools в нижней части окна или открепите его в отдельном окне][DevToolsCustomizePlacement].  
    
    > ##### Рисунок3  
    > DevTools закреплено в нижней части демонстрации  
    > ! [DevTools закреплена в нижней части демонстрации] [ImageDevToolsBottom]  
    
    > ##### Рисунок4  
    > Браузер в отдельном окне  
    > ! [Браузер в отдельном окне] [ImageDevToolsSeparateBrowse]  
    
    > ##### Рисунок 5  
    > DevTools отсоединяется в отдельном окне  
    > ! [DevTools открепляются в отдельном окне] [ImageDevToolsSeparateDevTools]  
    
## Просмотр сообщений, записанных из JavaScript   

Большинство сообщений, которые вы видите на консоли, поступают от веб-разработчиков, которые написали JavaScript страницы.  Цель этого раздела — рассказать вам о различных типах сообщений, которые вы, вероятно, видите на консоли, и объясните, как можно вести журнал для каждого типа сообщений.  

1.  Нажмите кнопку " **сведения о журнале** " в демонстрационной версии.  `Hello, Console!` Получает запись в журнал консоли.
    
    > ##### Рисунок6  
    > Консоль после нажатия кнопки " **сведения о журнале** "  
    > ! [Консоль после нажатия кнопки "сведения о журнале"] [ImageLogInfo]  
    
1.  Рядом с `Hello, Console!` сообщением на консоли щелкните **log.js:2**.  Откроется панель источники, в которой выделена строка кода, которая привела к тому, что сообщение будет записано на консоль.  Сообщение было занесено в журнал при выполнении кода JavaScript на странице `console.log('Hello, Console!')` .
    
    > ##### Рисунок7  
    > DevTools открывает панель «источники» после нажатия **log.js:2**  
    > ! [DevTools открывает панель «источники» после нажатия кнопки log.js:2] [ImageSourceLog]  
    
1.  Вернитесь на консоль с помощью одного из следующих рабочих процессов:  
    
    *   Откройте вкладку **консоль** .  
    *   Нажимайте клавиши `Control` + `[` \ (Windows \) или `Command` + `[` \ (macOS \) до тех пор, пока не будет фокус на панели консоли.  
    *   [Откройте меню команд][DevToolsCommandMenu], начните вводить текст `Console` , выберите команду **Показать панель консоли** , а затем нажмите клавишу `Enter` .  
    
1.  Нажмите кнопку **предупреждение журнала** в демонстрационной версии.  `Abandon Hope All Ye Who Enter` Получает запись в журнал консоли.  Сообщения, которые форматируются таким образом, представляют собой предупреждения.  
    
    > ##### Рисунок8  
    > Консоль после нажатия кнопки " **Журнал** "  
    > ! [Консоль после нажатия кнопки Log Warning] [ImageConsoleLogWarning]  
    
    > [!TIP]
    > Если вы хотите просмотреть код, который привел к тому, что сообщение записалось определенным образом, нажмите на сценарий \ (например, `log.js:12` \), чтобы просмотреть код, который привел к форматированию сообщения.  

1.  Щелкните значок **развернуть расширение** ![ ][ImageExpandIcon] перед `Abandon Hope All Ye Who Enter` .  DevTools показывает [трассировку стека][WikiStackTrace] , ведущая к вызову.  
    
    > ##### Рисунок9  
    > Трассировка стека  
    > ! [Трассировка стека] [ImageStackTrace]  
    
    Трассировка стека указывает на то, что вызвана функция с именем `logWarning` , которая, в свою очередь, вызывает функцию с именем `quoteDante` .  Другими словами, вызов, который произошел первым, находится в нижней части трассировки стека.  Вы можете регистрировать трассировку стека в любое время, вызывая `console.trace()` .  

1.  Нажмите " **журнал ошибок**".  Регистрируется следующее сообщение об ошибке: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### Рисунок 10  
    > Сообщение об ошибке  
    > ! [Сообщение об ошибке] [ImageLogError]  
    
1.  Нажмите кнопку **таблица журнала**.  Таблица, посвященная знаменитым исполнителям, записывается на консоль.  
    
    > [!NOTE]
    > `birthday`Столбец заполняется только для одной строки.  Проверьте код, чтобы узнать, почему это так.
    
    > ##### Рисунок11  
    > Таблица в консоли  
    > ! [Таблица на консоли] [ImageConsoleTable]  
    
1.  Нажмите кнопку **Группа журналов**.  Названия четырех знаменитых turtlesных, преступных, группируются под `Adolescent Irradiated Espionage Tortoises` меткой.  
    
    > ##### Рисунок12  
    > Группа сообщений на консоли  
    > ! [Группа сообщений на консоли] [ImageConsoleLogGroup]  
    
1.  Выберите пункт **Журнал настраиваемого**.  Сообщение с красной рамкой и синим фоном записываются в консоль.  
    
    > ##### Рисунок13  
    > Сообщение с настраиваемым форматированием в консоли  
    > ! [Сообщение с настраиваемым форматированием в консоли] [ImageConsoleLogCustomFormatting]  
    
Основная идея здесь заключается в том, что если вы хотите записывать сообщения на консоль из JavaScript, используйте один из этих `console` методов.  Каждый метод форматирует сообщения по-разному.  

В этом разделе есть еще больше методов, чем было показано ниже.  В этом учебнике показано, как ознакомиться с другими методами.  

## Просмотр сообщений, записанных браузером   

Браузер также регистрирует сообщения на консоли.  Обычно это происходит при возникновении проблемы со страницей.  

1.  Нажмите кнопку **причина 404**.  Браузер регистрирует `404` ошибку сети из-за того, что JavaScript пытается получить несуществующий файл.  
    
    > ##### Рисунок14  
    > Ошибка 404 в консоли  
    > ! [Ошибка 404 в консоли] [ImageConsoleLogError]  
    
1.  Нажмите кнопку **Причина ошибки**.  Браузер регистрирует неперехваченные записи, `TypeError` так как JavaScript пытается обновить несуществующий узел DOM.  
    
    > ##### Рисунок15  
    > TypeError на консоли  
    > ! [TypeError на консоли] [ImageConsoleLogTypeError]  
    
1.  Щелкните раскрывающийся список **уровни журнала** и включите параметр **подробный** , если он отключен.  Подробнее о фильтрации можно узнать в следующем разделе.  Это необходимо сделать, чтобы убедиться в том, что следующее сообщение отображается в журнале.  
    **Примечание.** Если раскрывающийся список уровни по умолчанию отключен, может потребоваться закрыть панель консоли. Отфильтровать по источнику сообщения, чтобы получить дополнительные сведения о боковой панели консоли.
    
    > ##### Рисунок16  
    > Включение **подробного** уровня ведения журнала  
    > ! [Включение подробного уровня ведения журнала] [ImageVerboseLogLevel]  
    
1.  Нажмите кнопку **вызвать нарушение**.  Страница перестает отвечать на запросы в течение нескольких секунд, а затем браузер заносит сообщение `[Violation] 'click' handler took 3000ms` на консоль.  Точная длительность может отличаться.  
    
    > ##### Рисунок17  
    > Нарушение в консоли  
    > ! [Нарушение в консоли] [ImageConsoleLogViolation]  
    
## Фильтрация сообщений   

На некоторых страницах вы видите консоль с сообщениями.  DevTools предоставляет множество различных способов фильтрации сообщений, которые не связаны с задачей.  

### Фильтрация по уровню ведения журнала   

Каждому `console` методу назначается уровень серьезности: `Verbose` , `Info` , `Warning` или `Error` .  Например, `console.log()` `Info` сообщение на уровне, в то время как `console.error()` сообщение на `Error` уровне.  

1.  Щелкните раскрывающийся список **уровни журнала** и отключите **ошибки**.  Уровень отключается, если рядом с ним больше нет метки.  `Error`Сообщения на уровне пропадают.  
    
    > ##### Рис. 18  
    > Отключение `Error` сообщений уровня на консоли  
    > ! [Отключение сообщений уровня ошибки на консоли] [ImageConsoleDisablingLogError]  
    
1.  Снова щелкните в раскрывающемся списке **уровни журнала** и повторно включите **ошибки**.  `Error`Снова появятся сообщения уровня.  

### Фильтрация по тексту   

Если вы хотите только просматривать сообщения, содержащие точную строку, введите эту строку в текстовом поле **Фильтр** .  

1.  Введите `Dave` текст в текстовое поле **Фильтр** .  Все сообщения, в которых не указана строка `Dave` , скрыты.  Кроме того, вы можете увидеть `Adolescent Irradiated Espionage Tortoises` метку.  Это ошибка.  
    
    > ##### На рисунке 19  
    > Фильтрация сообщений, которые не включают `Dave`  
    > ! [Фильтрация сообщений, которые не включают Дэйв] [ImageLogTextFiltering]  
    
1.  `Dave`"Удалить" из текстового поля " **Фильтр** ".  Все сообщения снова появятся.  

### Фильтрация по регулярному выражению   

Если вы хотите отобразить все сообщения, которые содержат шаблон текста, а не определенную строку, используйте [регулярное выражение][MDNRegularExpressions].  

1.  Введите `/^[AH]/` текст в текстовое поле **Фильтр** .  Введите этот шаблон в [Regex][|::ref1::|Main] , чтобы узнать, что он делает.  
    
    > ##### Рис. 20  
    > Фильтрация сообщений, не соответствующих шаблону `/^[AH]/`  
    > ! [Фильтрация сообщений, не соответствующих шаблону] [ImageLogRegExFiltering]  
    
1.  `/^[AH]/`"Удалить" из текстового поля " **Фильтр** ".  Все сообщения будут снова видны.  

### Фильтрация по источнику сообщения   

Если вы хотите только просматривать сообщения, поступившие с определенного URL-адреса, используйте **боковую панель**.  

1.  Нажмите кнопку **Показать боковую панель консоли** ![ , чтобы показать боковую панель консоли ][ImageShowConsoleSidebarIcon] .  
    
    > ##### Рисунок 21  
    > Боковая панель  
    > ! [Боковая панель] [ImageConsoleSidebar]  
    
1.  Щелкните значок **развернуть** развернутый ![ ][ImageExpandIcon] рядом с количеством сообщений.  На [рисунке 21](#figure-21)количество сообщений обозначается **13 сообщениями**.  На **боковой панели** отображается список URL-адресов, которые привели к тому, что сообщения записываются в журнал.  Например, это `log.js` связано с 11 сообщениями.  
    
    > ##### Рис. 22  
    > Просмотр источника сообщений на боковой панели  
    > ! [Просмотр источника сообщений на боковой панели] [ImageConsoleSidebarLogSource]  
    
### Фильтрация по пользовательским сообщениям   

Более того, после того, как вы щелкните **сведения журнала**, сценарий вызывается `console.log('Hello, Console!')` для записи сообщения на консоль.  Сообщения, которые регистрируются из сценария JavaScript вроде этого, называются **сообщениями пользователей**.  В отличие от того, когда вы щелкните **Причина ошибки 404**, браузер записал `Error` сообщение о том, что запрошенный ресурс не найден.  Такие сообщения считаются **сообщениями браузера**.  Используйте **боковую панель** , чтобы отфильтровать сообщения браузера и показать только сообщения пользователей.  

1.  Выберите **9 пользовательских сообщений**.  Сообщения браузера скрыты.  
    
    > ##### Рис. 23  
    > Фильтрация сообщений браузера  
    > ! [Фильтрация сообщений браузера] [ImageConsoleLogBrowserFiltering]  
    
1.  Щелкните **13 сообщений** , чтобы снова Показать все сообщения.  

## Использование консоли рядом с любой другой панелью   

Что делать, если стили редактируются, но вам нужно быстро проверить журнал консоли на что-то? Используйте денежный ящик.  

1.  Откройте вкладку **элементы** .  
1.  Нажмите клавишу `Escape` .  Откроется вкладка "консоль" для **ящика** .  У него есть все функции панели консоли, которые использовались в этом учебнике.  
    
    > ##### Рисунок 24  
    > Вкладка «консоль» в ящике  
    > ! [Вкладка "консоль" в ящике] [ImageDrawerConsole]  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Рисунок 1: сообщения на консоли"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-example-devtools-right-console.msft.png "Рисунок 2: DevTools откроется справа от демона"  
[ImageDevToolsBottom]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-example-devtools-bottom-console.msft.png "Рисунок 3: DevTools закреплено в нижней части демона"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-example-devtools-separate-console-browse.msft.png "Рисунок 4: браузер в отдельном окне"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-example-devtools-separate-console-devtools.msft.png "Рисунок 5: DevTools открепляются в отдельном окне"  
[ImageLogInfo]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-log-info.msft.png "Рисунок 6: консоль после нажатия кнопки" сведения о журнале ""  
[ImageSourceLog]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-sources-logjs.msft.png "рис. 7: DevTools открывает панель «источники» после нажатия кнопки log.js:2»  
[ImageConsoleLogWarning]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-log-warning.msft.png "Рисунок 8: консоль после нажатия кнопки" log warning "  
[ImageStackTrace]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-log-warning-expanded.msft.png "Рисунок 9: трассировка стека"  
[ImageLogError]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-log-error.msft.png "рис. 10: сообщение об ошибке"  
[ImageConsoleTable]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-log-table.msft.png "рис. 11: таблица на консоли"  
[ImageConsoleLogGroup]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-log-group.msft.png "Рисунок 12: группа сообщений на консоли"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-log-custom.msft.png "Рисунок 13: сообщение с настраиваемым форматированием в консоли"  
[ImageConsoleLogError]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-cause-404.msft.png "Рисунок 14: ошибка 404 в консоли"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-cause-error.msft.png "рис. 15: TypeError на консоли"  
[ImageVerboseLogLevel]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-cause-error-log-levels.msft.png "Рисунок 16: включение подробного уровня ведения журнала"  
[ImageConsoleLogViolation]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-cause-violation.msft.png "Рисунок 17: нарушение в консоли"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-cause-violation-log-levels.msft.png "Рисунок 18: отключение сообщений уровня ошибки на консоли"  
[ImageLogTextFiltering]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-all-messages-text-filter.msft.png "рис. 19. отфильтровать все сообщения, не содержащие Дэйв"  
[ImageLogRegExFiltering]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-all-messages-regex-filter.msft.png "рис. 20: Фильтрация любого сообщения, не соответствующего шаблону"  
[ImageConsoleSidebar]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-sidebar-all-messages.msft.png "Рисунок 21: Боковая панель"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-sidebar-expanded-all-messages.msft.png "рис. 22: Просмотр источника сообщений на боковой панели"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-sidebar-user-messages.msft.png "рис. 23: Фильтрация сообщений браузера"  
[ImageDrawerConsole]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/console-elements-drawer-console-sidebar-all-messages.msft.png "Рисунок 24: вкладка" консоль "в ящике"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft Edge \ (Chromium \)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Справочник по API консоли"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Справочник по консоли"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Начало работы с сообщениями в журнале | Цепь"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Регулярные выражения | MDN"  

[RegExrMain]: https://regexr.com "Регулярное выражение"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Трассировка стека — Википедии"  


> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/log) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

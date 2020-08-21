---
title: Новые возможности в DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f569414a95336278c93b1bbafd57153ca902df12
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942192"
---
# Новые возможности средств разработчиков (Microsoft Edge 85)  

## Объявления от команды разработчиков Microsoft Edge  

В следующих разделах приведен список извещений, которые вы можете пропустить от команды разработчиков Microsoft Edge DevTools.  Ознакомьтесь с извещениями о новых возможностях DevTools, расширениях кода VS и других возможностях.  Чтобы быть в курсе всех последних и полезных функций в средствах разработчика, скачайте [каналы microsoft Edge и][MicrosoftEdgePreviewChannels] [подписайтесь на группу Microsoft Edge DevTools в Twitter.][EdgeDevToolsTwitterAccount]  

### Возможности отладки CSS-таблицы  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспертальные возможности":::
   Экспертальные возможности  
:::image-end:::  

Команда разработчиков Microsoft Edge DevTools работает в месте совместного использования Chrome DevTools и Chromium для добавления новых функций отладки CSS в разработчики CSS.  Теперь вы можете отображать номера линий сетки, государственные и расширенные линии сетки в виде наложения.  Кроме того, в ближайшее время инструменты сетки станут доступны в ближайшее время.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Возможности отладки CSS-таблицы" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Возможности отладки CSS-таблицы
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперты, см. [раздел "Включение эксперальных возможностей"][DevtoolsExperimentalFeaturesTurnOn] и установите флажок "Включить новые функции отладки **CSS".**  
> 
> Ознакомиться с примером экспертов с примером см. в примере [планировщика CSS.][CodepenRachelweilYzwBzKM]  

Проблема с chromium [#1047356][CR1047356]  

### Изменение и воспроизведение запросов с помощью сетевой консоли  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспертальные возможности":::
   Экспертальные возможности  
:::image-end:::  

Теперь вы можете использовать команду "Изменить **и** воспроизвести воспроизведение при запросах в [сетевом журнале"][DevtoolsNetworkIndexLogActivity] с **помощью сетевой консоли.**  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Изменение и воспроизведение запроса в сети NetworkLog с помощью консоли Network" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Изменение и воспроизведение запроса в [сети NetworkLog][DevtoolsNetworkIndexLogActivity] с **помощью консоли Network**  
:::image-end:::  

В средстве рисования [DevTools][DevtoolsCustomizeIndexDrawer] откроется панель "Сетевой консоль" и автоматически замещаются сведениями для HTTP-запроса. **Network Console**  Чтобы просмотреть ответ, возвращенный с сервера, отредактировайте запрос \(при необходимости\) и нажмите **кнопку "Отправить".**  

Сетевая **консоль** также можно использовать для создания и отправки HTTP-запросов непосредственно в средствах разработки.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Панель "Сетевая консоль"" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   Панель **"Сетевая консоль"**  
:::image-end:::  

> [!TIP]
> Чтобы **просмотреть консоль сети** в основной области \(верхний\) панель \(верхний\) панель [devTools—][DevtoolsCustomizeIndexDrawer]см. инструменты перемещения между [панелями.](#move-tools-between-panels)  

> [!NOTE]
> Чтобы включить эксперт, см. [раздел "Включение эксперальных функций"][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **"Включить сетевую консоль".**  
> 
> Откройте [контекстное][DevtoolsNetworkIndexLogActivity]меню, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **команду "Изменить и воспроизвести".**  

Проблема с #1093687 chromium [#1093687][CR1093687]  

### На вкладке "Время" в личной службе отвечают на сообщения о работе службы  

Вкладка **"Время показа** слайдов" на **панели** network теперь содержит события `respondWith` работников служб.  Событие работника службы отображает срок от времени непосредственного обработчика работника службы до начала его работы с временем, когда устанавливается минимум `respondWith` `fetch` диспетчера `respondWith` `fetch` обработчика.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Событие процедуры обслуживания на вкладке "Время" панели сети" lightbox="../../media/2020/06/timing-tab.msft.png":::
   Событие `respondWith` работника службы на вкладке **"Время показа** слайдов" **панели сети**  
:::image-end:::  

Разверните **полученный ответ, чтобы** просмотреть дополнительные сведения от `fetch` `CacheStorageCacheName` ответа, `serviceWorkerResponseSource` например, `ResponseTime` и.  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Разверните полученный ответ, чтобы просмотреть дополнительные сведения от удаленного ответа" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Развернуть **полученный ответ, чтобы** просмотреть дополнительные сведения `fetch` от ответа  
:::image-end:::  

Проблема с chromium [#1066579][CR1066579]  

### отзыв ы веб-сайта в панели "Проблемы"  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспертальные возможности":::
   Экспертальные возможности  
:::image-end:::  

[webhint][WebhintMain] — это открытый инструмент, в котором вы восприятие удобства использования, совместимости, безопасности, производительности, PWA и других проблем разработки веб-сайтов.  Теперь вы можете просмотреть отзывы веб-хранилища на [панели "Проблемы".][DevtoolsIssues]  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="отзыв ы веб-сайта в панели "Проблемы"" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   отзыв ы веб-сайта в панели "Проблемы"  
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперт, см. [статью "Включение эксперальных возможностей"][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **"Включить веб-хороший веб-сайт".**  
> 
> Откройте [панель "Вопросы"][DevtoolsIssues] для просмотра отзывов веб-хорошего трудозатрат.  

Проблема с [#1070378][CR1070378]  

### Перемещение инструментов между панелями  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспертальные возможности":::
   Экспертальные возможности  
:::image-end:::  

Как обычно, такие инструменты, **Elements** как **Network** Элементы и сеть, могут открываться только в основной панели \(верхней\) панели разработчиков.  Аналогичным причиной таких инструментов, как трехмерное представление и проблемы, можно открыть только в панели \(нижнь\)) панели Средств Разработчиков. **3D View** **Issues**  Теперь вы можете настраивать макет DevTools путем перемещения инструментов между верхними и нижними панелями.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Перемещение вкладок между панелями  
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперт, см. [раздел "Включить экспертные функции"][DevtoolsExperimentalFeaturesTurnOn] и установите флажок "Разрешить поддержку" для перемещения **вкладок между панелями.**  

Проблема с [хромом#897944][CR897944]  

### Улучшенная подсказка инициатора на панели сети  

В Microsoft Edge 83 и 84 подсказки для столбца "Инициатор" для [Network Log][DevtoolsNetworkIndexLogActivity] столбца "Инициатор" с отображением причины запроса ресурса на сетевом журнале с горизонтальной полосой прокрутки.  Вы сможете видеть только стопку звонков, инициировавшую запрос, прокрутив горизонтально в подсказке.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Подсказка инициатора в Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   Подсказка инициатора в Microsoft Edge 84  
:::image-end:::  

Начиная с Microsoft Edge 85, теперь вы можете увидеть стек нужда ть инициатор звонков сигнала в подсказке без прокрутки по горизонтали.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Подсказка инициатора в Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   Подсказка инициатора в Microsoft Edge 85
:::image-end:::  

Проблема с #1069404 chromium [#1069404][CR1069404]  

## Извещения из проекта Chromium  

В следующих разделах описаны дополнительные функции, доступные в Microsoft Edge 85, которые были внесены в проект Chromium.  

### Редактирование стилей для структур структур CSS в JSS  

В **области "Стили"** теперь можно изменять стили, созданные с помощью API-объектной модели [CSS (CSSOM).][CsswgDraftsCssom]  Многие из них инфраструктуры и библиотеки CSS используют API CSSOM под разработчиками.  

Теперь можно изменять стили, добавленные в JavaScript, с помощью [конструкции стилей.][WicgConstructStylesheet]  Конструктивные стили — это новый способ создания и распространения стилей повторно используемых стилей при использовании [тени DOM.][MdnShadowDom]  

Например, `h1` добавленные стили с `CSSStyleSheet` \(CSSOM\) не редактирулись ранее.  Теперь стили можно изменять в области **"Стили".**  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Изменение свойства фона для стилей h1, добавленных с помощью розовой таблицы на светлый" lightbox="../../media/2020/06/css-in-js.msft.png":::
   `background`Измените свойство `h1` стилей, добавленных `CSSStyleSheet` в `pink` `lightblue` список.
:::image-end:::  

Попробовать эту функцию [с образцом, использующим CSS-семи.][CodepenZoherghadyaliAbdgrpz]

Проблема с [#946975][CR946975] хромеум#946975  

### Lighthouse 6 на панели "Молния"  

Панель **"Молуль"** теперь работает на десяти чужих десятках.  Полный список всех изменений см. в [заметках о выпуске 6.0.0.][GithubGoogleChromeLighthouse600]  

В отчет включены три новых показателя: самый большой объем контента: самый большой объем контента (LCP\),интегральная смена макета Shift \(CLS\) и общее время блокирования времени \(TBT\).  

Формула оценки производительности также была удалена, чтобы лучше отразить нагрузку пользователя.  

Проблема с [#772558][CR772558]  

#### First Meaningful Paint  

Первая понятная paint \(FMP\) устарела в Lighthouse 6.0.  FMP также удален с панели **производительности.**  **Самый большой объем контента —** рекомендуемый заменой для FMP.  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

Проблема с [#1096008][CR1096008]  

### Поддержка новых функций JavaScript  

Теперь В DevTools теперь поддерживается поддержка некоторых последних функций языков JavaScript.  

:::row:::
   :::column span="1":::
      [Необязательное][V8DevOptionalChaining] автозавершение синтаксиса  
   :::column-end:::
   :::column span="2":::
      Автозавершение свойств в консоли теперь поддерживает необязательный синтаксис цепочки цепочки, **Console** `name?.` `name.` например `name[` и.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Выделение синтаксиса для [частных полей][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      частные поля класса теперь выделяются правильно, а на **панели источников выделяются прежние** поля.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Выделение синтаксиса [для оператора нули][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      Средства Разработки теперь правильно распечатываются оператор ы операционных шифров абсоллийских операций, на **панели "Источники".**  
   :::column-end:::
:::row-end:::  

Проблемы с [хроме#1073903][CR1073903] [#1083797][CR1083797] #1083214, [#1083797][CR1083214]  

### Предупреждения о новых сочетаниях клавиш приложения в области манифеста  

**Сочетания клавиш для приложений** помогают пользователям быстро начинать типичные или рекомендуемые задачи в веб-приложении.  

<!--todo: add App shortcuts when section is live  -->  

В **области манифеста** теперь отображаются предупреждения для перечисленных ниже условий.  

* Значки сочетаний клавиш приложений меньше 96 x 96 пикселей  
* Значки ярлыков приложений и манифеста не являются квадратными \(так как значки игнорируются\)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Предупреждения о сочетаниях клавиш приложений" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Предупреждения о сочетаниях клавиш приложений  
:::image-end:::  

Проблема с chromium [#955497][CR955497]  

### Единообразный экран области вычисляемой области  

В **области "Элементы"** панель "Элементы" похожна на единообразный список областей просмотра. **Elements**  Ранее, **ранее** созданная в области **"Стили"** в области "Стили" при уменьшении ширины представления DevTools.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Вырезанная область вычисляется постоянно, даже если область "Разработчики" уже сужат" lightbox="../../media/2020/06/computed-pane.msft.png":::
   **Вырезанная область вычисляется** постоянно, даже если узкие для devTools сужаются.
:::image-end:::  

Проблема с [#1073899][CR1073899] хромеум#1073899  

### Смещение байтов для файлов WebAssembly  

В DevTools теперь используются смещения байтов для отображения чисел строк, которые были интегрированы с еженедельными.  
Номера строк делают более четкими, что просматриваетданное двоичные данные и более единообразие использования ссылок на расположения пользователя Временных шкалах.  

Проблема с [#1071432][CR1071432]  

### Построчная копирование и вырезание в области источников  

При копировании или вырезании без выделения в редакторе источников [не][DevtoolsSourcesEditCssJavascript]выбрано, средства DevTools копируют или вырезают текущую строку содержимого.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="При нажатии указателя в конце строки 5 скопируйте всю строку pen.js в devTools и вставьте в код VS-код VS." lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   Скопируйте строку изpen.jsв **средствах** разработчиков и вставьте [в код VS код VS.][VSCode]
:::image-end:::  

Проблема с #800028 Chromium [#800028][CR800028]

### Обновления параметров консоли  

#### Разгруппирование сообщений в консоли  

Параметр **"Группа"** так же, как и в параметрах консоли, теперь применяется для дублированных сообщений.  Ранее применяется к похожим сообщениям.  

Например, ранее devTools не разгруппировал сообщения, хотя похожие на `hello` группы снят. **Group similar**  Теперь сообщения `hello` будут разгруппированы.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Если группа желаемых снята, сообщения приветствия разгруппируются" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Если **похожие флажки** сняты, сообщения `hello` будут отменены.
:::image-end:::  

Попробуйте эту функцию использовать [образец, который отправляет дублирующиеся сообщения в консоль.][CodepenZoherghadyaliZyrjgdJ]  

Проблема с [#1082963][CR1082963]  

### Параметры постоянного контекста  

**Выбранный контекст меню** не удаляется.  Ранее параметры были сброшены каждый раз при закрытии и повторном открытии DevTools.  Изменение вносит изменения в настройки согласованно с другими параметрами консоли.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Только выбранный контекст" lightbox="../../media/2020/06/selected-context.msft.png":::
   **Только выбранный контекст**  
:::image-end:::  

Проблема с [#1055875][CR1055875]  

### Обновления панели производительности  

#### Информация о кэше компиляции для JavaScript на панели производительности  

[Информация о кэше компиляции JavaScript][V8DevCodeCaching] теперь всегда отображается на вкладке "Сводка" панели быстродействия.  Ранее в DevTools не было относительно кэширования кода ничего, связанное с кэшированием кода.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Кэш съемки для JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Кэш съемки для JavaScript  
:::image-end:::  

Проблема с [#912581][CR912581]  

#### Выравнивание время переходов на панели производительности  

На **панели "Производительность"** отображаются временные шкалы на линейках в зависимости от времени начала записи.  Теперь время показа теперь изменилась при переходе по записям, когда пользователь переходит по интерфейсу DevTools теперь отображает таймер таймер относительно навигации.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Выравнивание временных показаслайд по навигации на панели performance" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Выравнивание временных показаслайд по навигации **на панели performance**  
:::image-end:::  

Время, продолжительная первая рисованная питание, первый контент и крупный контент, обновляются относительно начала навигации, то есть соответствует время показа `DOMContentLoaded` `PerformanceObserver` слайдов, полученным.  

Проблема с #974550 chromium [#974550][CR974550]  

### Новые значки для разбиения точек, условных точек и логических точек  

В **области "Источники"** добавлены новые макеты разбивки, условных точек и логических точек.  Разрывы представлены красными кружками, как [и код VS-][VSCode] [и Visual Studio.][VS]  Значки добавляются к различные условные точки и логические точки.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Точки останова" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Точки останова  
:::image-end:::  

Проблема с #1041830 chromium [#1041830][CR1041830]  

## Загрузить каналы с предварительными версиями Microsoft Edge  

Если вы используете Windows или macOS, рекомендуем использовать каналы [предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Каналы с предварительными версиями доступны новейшие функции Разработчиков.  

## Совместная работа с помощью команды разработчиков Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (на базе Chromium) | Документы Майкрософт"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Команды меню "Запуск" в меню Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Рисование — настройка средств разработчиков Microsoft Edge | Документы Майкрософт"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включение экспертальных функций — экспертальные функции | Документы Майкрософт"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Поиск и устранение проблем с средством разработчиков Microsoft Edge | Документы Майкрософт"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Edit CSS and JavaScript — Обзор панели источников | Документы Майкрософт"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Журнал действий с сетью: проверка действий с ее сетью в средствах разработки Microsoft Edge | Документы Майкрософт"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Редактирование стилей для структур в CSS -in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Отправка дубликатов сообщений на консоль | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Пример планировщика CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки на Chromium"  

[CR772558]: https://crbug.com/772558 "Разработчики: обновление до последней версии Lighthouse | Ошибки на Chromium"  
[CR800028]: https://crbug.com/800028 "После обновления Chrome ярлык строки в редакторе средств разработчика не работают? Ошибки на Chromium"  
[CR912581]: https://crbug.com/912581 "Выводит ся, какие сценарии были кэшированы кодированным кодом V8 в DevTools/about:tracing | Ошибки на Chromium"  
[CR946975]: https://crbug.com/946975 "Боковая панель Разработчиков не работает со структурированными таблицами стилей | Ошибки на Chromium"  
[CR955497]: https://crbug.com/955497 "Контекстное меню значка приложения для PWA | Ошибки на Chromium"  
[CR974550]: https://crbug.com/974550 "Несоответствие между панелью Perf и PerformanceObserver | Ошибки на Chromium"  
[CR1041830]: https://crbug.com/1041830 "Улучшены цвета разбивки | Ошибки на Chromium"  
[CR1055875]: https://crbug.com/1055875 "Значение выбранной консоли не удаляется после закрытия и повторного открытия средств разработчика | Ошибки на Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: показать временную шкалу служб fetch TimeLine на запрос на панели Network | Ошибки на Chromium"  
[CR1071432]: https://crbug.com/1071432 "Были опытные возможности для разработчиков | Ошибки на Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка "Вычисляемый стиль" исчезает в режиме респондента | Ошибки на Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: выделение синтаксиса не работает с частными полями | Ошибки на Chromium"  
[CR1082963]: https://crbug.com/1082963 "Невозможно отключить поведение групп ых поведения консоли | Ошибки на Chromium"  
[CR1083214]: https://crbug.com/1083214 "Acorn не поддерживает дополнительную цепочку цепочки | Ошибки на Chromium"  
[CR1083797]: https://crbug.com/1083797 "Напечатать неработающую печать для необычных количества шифрования | Ошибки на Chromium"  
[CR1096008]: https://crbug.com/1096008 "Удалить FMP | Ошибки на Chromium"  
[CR1047356]: https://crbug.com/1047356 "Сетка CSS, Flexbox/инструменты таблиц | Ошибки на Chromium"  
[CR1093687]: https://crbug.com/1093687 "Создание средства для создания и повторного синтаксиса синтаксических запросов | Ошибки на Chromium"  
[CR1070378]: https://crbug.com/1070378 "Интеграция веб-страниц в DevTools | Ошибки на Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Средства разработки] Всплывающие мини-приложения слишком узкими | Ошибки на Chromium"  
[CR897944]: https://crbug.com/897944 "Панели разработчиков | Ошибки на Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "версии 6.0.0–GoogleChrome/lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая проблема: MicrosoftDocs/edge-разработчики"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Использование тени DOM | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Каналы предварительной версии Microsoft Edge"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Visual Studio код"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Объектную модель CSS (CSSOM) | Редактор черновиков группы CSS working Group"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools твиттер"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Частные поля класса — поля "Общие" и "Частное занятие" | 8. Разработка"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Кэширование кодов для разработчиков JavaScript | 8. Разработка"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Неульзя производить необычный количество | 8. Разработка"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Необязательное цепочка | 8. Разработка"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Объекты конструктивной таблицы стилей | Web Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Нужный веб-час"  

> [!NOTE]
> Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]  
> Исходная страница [here](https://developers.google.com/web/updates/2020/06/devtools/index) найдена и находится в динамическом оси Игнатьельской ориентации, и она разрабатывается [Деконом][JecelynYeen] \(Разработчик, Разработчик, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
title: Новые возможности в DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: aa39e5d7811d4a614e055a8e0479c74278efbefd
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942189"
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

# Новые возможности в DevTools (Microsoft Edge 84)  

## Объявления от команды разработчиков Microsoft Edge  

В следующих разделах приведен список извещений, которые вы пропустили от команды разработчиков Microsoft Edge DevTools! Ознакомьтесь с их новыми возможностями в DevTools, расширениях кода VS и многом другом.  Чтобы быть в курсе всех последних и полезных функций в средствах разработчика, скачайте [каналы microsoft Edge][MicrosoftEdgePreviewChannels] и [отслеживайте нас в Твиттере.][EdgeDevToolsTwitterAccount]  

### Использование Средств разработки в режиме высокой контрастности Windows

Средства разработчиков Microsoft Edge теперь отображаются в режиме высокой контрастности, если Windows работает в режиме высокой контрастности.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Разработчики Microsoft Edge в режиме высокой контрастности" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Разработчики Microsoft Edge в режиме высокой контрастности  
:::image-end:::  

[Следуйте инструкциям в windows, чтобы включить режим высокой контрастности.][MicrosoftSupportWindows10HighContrastMode]  Откройте DevTools в Microsoft Edge, нажав `F12` или `Ctrl` + `Shift` + `I` клавишу.  В режиме высокой контрастности отображаются разработчики.  

> [!NOTE]
> В настоящее время в Microsoft Edge DevTools поддерживает режим высокой контрастности для Windows, но не в macOS. 

Проблема с chromium [#1048378][CR1048378]  

### Соответствие сочетаниям клавиш в разработчиках на VS-код  

От отзывов [и](#getting-in-touch-with-microsoft-edge-devtools-team) [общедоступного средства разработчика Chromium][CRIssuesList]команда разработчиков Microsoft Edge заработал собой, что вы хотите настраивать сочетания клавиш в средствах разработчиков.  В Microsoft Edge 84 теперь можно использовать сочетания клавиш в Разработчиках с [кодом VS-кода VS,][VSCode]который над ее помощью работает только для настройки сочетаний клавиш.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Соответствие сочетаниям клавиш в разработчиках на VS-код" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Разработчики Microsoft Edge в режиме высокой контрастности  
:::image-end:::  

Чтобы попробовать эксперимент, откройте параметры DevTools, нажав или `?` щелкнув ![ значок "Параметры DevTools" в правом верхнем углу ][ImageSettingsIcon] средств разработчика.  Перейдите в раздел **"Эксперименты"** и проверьте параметры сочетаний клавиш **(необходимо перезагрузить) на вкладке "Параметры сочетаний клавиш" (потребуется перезагрузить).**  Теперь снова загрузите DevTools, снова откройте параметры и перейдите в раздел **сочетаний клавиш.**  

В **раскрывающемся списке ярлыков "Соответствие" выберите** **пункт Visual Studio Код.** **Match shortcuts from preset**  Сочетания клавиш в разработчиках теперь соответствуют сочетаниям клавиш для эквивалентных действий кода VS-кода.  

Например, сочетание клавиш для привязки или продолжения работы сценария в [коде VS относится][VSCodeShortcuts] к клавише CS. `F5`  В **стандартных средствах DevTools (по умолчанию)** это сочетание клавиш в devTools `F8` **является, но с Visual Studio Code,** теперь это сочетание клавиш `F5` и ярлык.  

Функция в настоящее время доступна в Microsoft Edge 84 в качестве экспертов, поэтому сообщите нам об этом с [коллегами.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема с [хромом#174309][CR174309]  

### Удаленный отладка Surface Duo emulator  

Теперь вы можете удаленно отладки веб-контента работать на [экране эмоблемы Surface Duo][DualScreensAndroidEmulator] с полными возможностями [средств разработчиков Microsoft Edge.][DevToolsChromiumGuide]  

[Эмулуатор Surface Duo][DualScreensAndroidEmulator]помогают проверить, как ваш веб-контент будет выводиться на новом классе сгибом и сдвиганием экрана.  Эмулятор работает под управлением операционной системы Android и предоставляет [приложение Microsoft Edge для Android.][AndroidEdge]  Загрузите веб-контент в [приложении Microsoft Edge][AndroidEdge] и отладьте его с помощью [разработчиков Microsoft Edge.][DevToolsChromiumGuide]  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Приложение Microsoft Edge работает на эмулунере" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   Приложение Microsoft Edge на эмутулу  
:::image-end:::  

На `edge://inspect` странице в экземпляре [Microsoft Edge][DesktopEdge] отображается список открытых вкладок или [PWS,][PwaIndex] которые выполняются на конвейере [Surface Duo.][DualScreensAndroidEmulator] **SurfaceDuoEmulator**  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="На edge://inspect появится список открытых вкладок в приложении Microsoft Edge, запущенной на эмляторе" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   На `edge://inspect` странице отображается список открытых вкладок в приложении Microsoft Edge, запущенном на эмляторе
:::image-end:::  

Если выбрать **поиск вкладки или** PWA, которые нужно отладить, [откроется microsoft Edge DevTools.][DevToolsChromiumGuide]  Следуйте пошаговым инструкциям, чтобы удаленно отладить [веб-контент на эмоблуровsurface.][DevToolsRemoteDebugDuoEmulator]  

### Удобнее изменить размер рисования DevTools  

В Microsoft Edge 83 и более ранних версиях можно изменить размер только средства [рисования DevTools,][DevToolsDrawer] наводя указатель мыши на панель инструментов "Рисование".  Рисование отличается от других элементов управления для областей в разработчиках, если наведите указатель мыши на границу области, чтобы изменить ее размер.  Щелкните на следующем рисунке изображение, чтобы узнать, как изменение рисования, работавшего в версии 83 или более ранних версиях Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Изменение размера средства рисования DevTools в Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Изменение размера средства рисования DevTools в Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Начиная с Microsoft Edge 84, теперь можно изменить размер рисования, наводя указатель мыши на границу документа.  Это изменение отражает поведение размера других областей средств разработчика с помощью средств разработчика.  Щелкните изображение ниже, чтобы увидеть изменения размера в действии в Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Изменение размера средствризов DevTools в Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Изменение размера средствризов DevTools в Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Проблема с chromium [#1076112][CR1076112]  

### Кнопки навигации экрана с фокусом на кнопках навигации  

При удаленном отключении [устройства с Android,][DevToolsRemoteDebugAndroid] [устройства с Windows 10][DevToolsRemoteDebugWindows]или [эмблему Surface Duo][DevToolsRemoteDebugDuoEmulator]вы можете выключать экрансткую выключатель с помощью значка "Выключатель экрана" в левом верхнем углу ![ средств ][ImageScreencastingIcon] DevTools.  Если включена поддержка экрана, вы сможете перемещаться по вкладке в Microsoft Edge на удаленном устройстве из окна Средств DevTools.  В Microsoft Edge 84 эти кнопки навигации теперь доступны и с помощью клавиатуры.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="При нажатии клавиш SHIFT+TAB на панели url-адреса экрана фокус переместится на кнопку "Обновить"" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   При нажатии url-адреса на панели вызова `Shift` + `Tab` отображается фокус на **кнопке "Обновить"**
:::image-end:::  

Проблема с #1081486 chromium [#1081486][CR1081486]  

### Панель сведений о панели сетей теперь доступна  

В области сведений [Details pane][DevToolsNetworkDetails] в Microsoft **Network** Edge 84 фокус перемещается при ее открытии для ресурса в [журнале сети.][DevToolsNetworkLog]  Это изменение позволяет средствам чтения с экрана читать содержимое области **сведений** и работать с ним.  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="В области сведений в панели "Сетевая сеть" фокус перемещается при открытии" lightbox="../../media/2020/05/network-details.msft.png":::
   В **области сведений в** **панели "Сетевая** сеть" фокус перемещается при открытии
:::image-end:::  

Проблема с [#963183][CR963183]  

## Извещения из проекта Chromium  

В следующих разделах описаны дополнительные функции, доступные в Microsoft Edge 84, которые были внесены в проект Chromium.  

### Устранение проблем с новым средством "Проблемы" в средстве рисования DevTools

Новый **инструмент "Проблемы"** в средстве рисования DevTools встроен для уменьшения количества уведомлений и ненужных элементов **консоли.**  В **настоящее** время консоль — это централизованное место для разработчиков веб-сайтов, библиотек, структур и Microsoft Edge для регистрации сообщений, предупреждений и ошибок.  **Средство** "Проблемы" влияет на предупреждения в браузере в структурированном, обобщаемом и поледо конкретном средстве, ссылки на влияние на ресурсы, на которые влияют на ресурсы в microsoft Edge DevTools, и предоставляет рекомендации по их устранению.  Со временем в средстве "Проблемы" в центре проблем важно появляться больше предупреждений в секторе Microsoft Edge, а не **консоли,** что помогает сократить беспорядок в **консоли.** **Issues**  

Чтобы приступить к работе, ознакомьтесь с разделом ["Проблемы с инструментом разработчика Microsoft Edge".][DevtoolsIssuesIndex]  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Средство "Проблемы" в средстве рисования Разработчиков" lightbox="../../media/2020/05/issues.msft.png":::
   Средство **"Проблемы"** в средстве рисования Разработчиков  
:::image-end:::  

Проблема с [#1068116][CR1068116]  

### Просмотр сведений о специальных возможностях в подсказке "Режим проверки"  

В **подсказке** теперь указывается, есть ли у элемента доступные названия и [роль][WebhintHintsAxeNameRoleValue] и есть [клавиатура.][WebhintHintsAxeKeyboard]  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Подсказка в режиме проверки со сведениями о специальных возможностях" lightbox="../../media/2020/05/a11y.msft.png":::
  **Подсказка в режиме** проверки со сведениями о специальных возможностях  
:::image-end:::  

Проблема с #1040025 chromium [#1040025][CR1040025]  

### Обновления панели производительности  

#### Просмотр сведений об итоговом блоке в нижнем колонтитуле  

После записи скорости загрузки на панели "Производительность" отображаются сведения о дате блокирования времени \(TBT\) в нижнем колонтитуле. **Performance**  Срок погрузки — это показатель производительности, которая помогает квадратить, сколько времени занимает страница.  Фактически измеряет, как долго страница будет отображаться в размере \(так как отображается на экране\); Но не является полезным, так как JavaScript блокирует основной цепочку и поэтому страница не отвечает пользователю.  TBT является основной метрикой приблизительных задержек первого ввода.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Чтобы получить сведения о блокировке времени, не используйте значок **обновления страницы** для ![ ][ImageRefreshPageIcon] загрузки страницы.  

Вместо этого выберите **значок записи,** вручную перезагрузите страницу, дождитесь ![ ][ImageRecordIcon] загрузки страницы и остановите запись.  

Если вы видите, Microsoft Edge DevTools не получал требуемые сведения из `Total Blocking Time: Unavailable` внутренних данных профиля в Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Сведения об общем количестве блокировки в нижнем колонтитуле области производительности" lightbox="../../media/2020/05/tbt.msft.png":::
   Сведения об общем количестве блокировки в нижнем колонтитуле **области производительности**  
:::image-end:::  

Проблема с [хромом#1054381][CR1054381]  

#### События макета в новом разделе "Возможности"  

Новый раздел "Производительность" панели "Производительность" поможет обнаружить смены макета. **Experience** **Performance**  Совместимость макета Shift \(CLS\) позволяет квалифицировать нежелательные визуальные элементы.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Выберите **событие "Смена** макета" для просмотра сведений о смене макета в **области "Сводка".**  Наведите указатель мыши **на перемещенные поля** и **"Перемещенные" в** поля, чтобы наглядно представить, где произошло смена макета.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Сведения о смене макета" lightbox="../../media/2020/05/cls.msft.png":::
   Сведения о смене макета  
:::image-end:::  

### Более тщательно промежуточные термины в консоли  

При ведении журнала консоль неправильно предоставлено `Promise` **Console** `PromiseStatus` `resolved` значение.  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Пример консоли с использованием старого определения терминов" lightbox="../../media/2020/05/resolved.msft.png":::
   Пример консоли **с** использованием `resolved` старого термина  
:::image-end:::  

Теперь **в консоли используется** термин `fulfilled` , который выравнивается относительно `Promise` спецификации.  Дополнительные сведения о `Promise` спецификации см. в [разделе "Регионы и сборы" на гитме.](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md)  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Пример консоли с новым терминами" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Пример **консоли** с новым `fulfilled` терминами  
:::image-end:::  

Проблема с [#6751][CRV86751]  

### Обновления области стилей  

#### Поддержка восстановления ключевых слов  

В интерфейсе автозаполнения области **"Стили"** теперь [обнаружение обратного][MDNRevert] ключевого слова CSS, при котором касается касательно вычисленного значения свойства к предыдущему значению.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Отмена значения свойства для отмены" lightbox="../../media/2020/05/revert.msft.png":::
  Отмена значения свойства для отмены  
:::image-end:::  

Проблема с [#1075437][CR1075437]  

#### Предварительный просмотр изображений  

Наведите указатель мыши на `background-image` значение в области **"Стили"** для предварительного просмотра изображения в подсказке.  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="При наведении указателя мыши на значение фонового изображения" lightbox="../../media/2020/05/image-preview.msft.png":::
  Наведение указателя на `background-image` значение  
:::image-end:::  

Проблема с [#1040019][CR1040019]  

#### В средстве выбора цветов теперь используется функция с разделителями, разделенными между пробелами  

[Уровень цветового модуля CSS определяет,][CSSWGDraftsColor4Changes3] что функции цвета `rgb()` (например, должны поддерживать аргументы, разделенные пробелами).  Например, команда `rgb(0, 0, 0)` эквивалентна `rbg(0 0 0)`.  

При выборе цветов [Color Picker][DevtoolsCssReferenceColorPicker] с помощью средства выбора цветов или альтернативного цветового представления в области **"Стили",** удерживая `Shift` нажатой клавишу `background-color` CTRL, вы увидите синтаксис аргументов, разделенных пробелами.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Использование аргументов разделителей между пробелами в области "Стили"" lightbox="../../media/2020/05/color.msft.png":::
  Использование аргументов разделителей между пробелами в **области "Стили"**  
:::image-end:::  

Вы также увидите синтаксис в области **вычисляемого** текста и всплывающую подсказку "Режим проверки". **Inspect Mode**  

В Microsoft Edge DevTools используется новый синтаксис, так как предстоящие функции CSS, [такие как color()][CSSWGDraftsColor4Property] не поддерживают синтаксис устаревшей запятой.  

Синтаксис аргументов с разделителями между пробелами поддерживается в большинстве браузеров.  Дополнительные сведения см. в статье ["Можно ли использовать: функция с разделителями"?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

Проблема с [#1072952][CR1072952] хромом  

### Устаревшее окно "Свойства" в области "Элементы"  

Устаревшая область **"Свойства"** на панели "Элементы" устарела. **Properties**  Вместо `console.dir($0)` этого **запустите консоль.**  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Область свойств устаревшей" lightbox="../../media/2020/05/properties.msft.png":::
   Область свойств **устаревшей**  
:::image-end:::  

#### Ссылок  

*   [console.dir()][DevtoolsConsoleApiDir]  
*   [0 $][DevtoolsConsoleUtilitiesDom]  

### Поддержка сочетаний клавиш приложения в области "Манифест"  

Сочетания клавиш для приложений помогают пользователям быстро начинать типичные или рекомендуемые задачи в веб-приложении.  Меню сочетаний клавиш приложений отображается только для прогрессиональных [веб-приложений,][PwaIndex] установленных на компьютере или мобильном устройстве пользователя.  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Сочетания клавиш приложений в области манифеста" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Сочетания клавиш приложений в **области манифеста**  
:::image-end:::  

## Скачивание каналов с предварительными версиями Microsoft Edge  

Если вы используете Windows или macOS, рекомендуем использовать каналы [предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Каналы с предварительными версиями каналов получают доступ к новейшим функциям DevTools.  

## Совместная работа с помощью команды разработчиков Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Значок "Параметры разработчика""
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/images/toggle-screencast-icon.msft.png "DevTools Togle screencast Screencast"
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png "Значок "Обновить страницу" в области "Производительность""
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png "Значок "Запись" панели "Производительность""

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Майкрософт"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir — Ссылка на консоли API | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Объект "Недавно выбранный элемент или объект JavaScript" — API служебных utilities API | Документы Майкрософт"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цветов с помощью средства выбора цветов — CSS Reference | Документы Майкрософт"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Рисование — настройка | Обзор | Документы Майкрософт"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (на базе Chromium) | Документы Майкрософт"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем с вкладкой "Проблемы разработчиков" в Microsoft Edge | Документы Майкрософт"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленным отладкой с Устройствами Android | Документы Майкрософт"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Начало работы с удаленным демоэропорой Surface Duo | Документы Майкрософт"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленным отладкой устройств с Windows 10 | Документы Майкрософт"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Проверьте сведения о ресурсе | Документы Майкрософт"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Действия в сети | Документы Майкрософт"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Майкрософт"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Приложение Microsoft Edge для Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Нотация с разделителями с разделителями — MDN | Можно ли использовать"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки на Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: разрешение настройки сочетаний клавиш и привязок | Ошибки на Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools не совместимо с WCAG | Ошибки на Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: удобный предварительный просмотр изображений и фоновых изображений в области стилей| Ошибки на Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: показать в свой элемент базовую информацию Ошибки на Chromium"  
[CR1048378]: https://crbug.com/1048378 "Поддержка пользовательского пользовательского образца для режима высокой контрастности | Ошибки на Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Ошибки на Chromium"  
[CR1068116]: https://crbug.com/1068116 "Панель "Проблемы с отправкой" | Ошибки на Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: средство выбора цветов должен создать современный синтаксис цветов CSS | Ошибки на Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: добавление поддержки для ключевого слова и значения | Ошибки на Chromium"  
[CR1076112]: https://crbug.com/1076112 "Персонализация разработки — изменение размера рисования"  
[CR1081486]: https://crbug.com/1081486 "Фокус не отображается для кнопок навигации в режиме экранной шкала | Ошибки на Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus должен быть заполнено, а не соответствует предложению | В8 ошибок v8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Изменения цветов 3 - Модуль цвета CSS уровень 4 | Редактор черновиков группы CSS working Group"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Фон круговый модуль: "цвет" - CSS уровень цвета CSS | Редактор черновиков группы CSS working Group"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Представляем новый браузер Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Штаты и лицы — думанная и промиутбург | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "отмена | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Совместимость браузера | MDN"  

[VSCode]: https://code.visualstudio.com/ "Visual Studio код"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio сочетания клавиш в программах для Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Ось: клавиатура | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Оси: имя роли " | Значение роли | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Включение и отключение режима высокой контрастности в Windows | Поддержка Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools твиттер"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема: MicrosoftDocs/edge-разработчики"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Нужный веб-час"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]  
> Исходная страница [here](https://developers.google.com/web/updates/2020/05/devtools/index) находится на сайте [Kayce Basques][KayceBasques] \(технический автор, Chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

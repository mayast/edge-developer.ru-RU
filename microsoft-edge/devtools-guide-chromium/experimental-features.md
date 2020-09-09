---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: c78e9aa5e0b4d808dd67d607a954b185ddcf54e7
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004043"
---
# Экспериментальные функции  

Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые все еще находятся на стадии разработки.  Вы можете протестировать и[отдать отзыв](#providing-feedback-on-experimental-features) , прежде чем каждый компонент будет выпущен.  

Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.  

## Включение экспериментальных функций  

Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.  

1.  [Откройте DevTools][DevtoolsOpen].  
     *   Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  
1.  Открытие области [параметров][DevToolsCustomizeSettings] .  
    *   Выберите `Shift` + `?` .  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  
1.  В левой части области **параметров** выберите раздел **эксперименты** .  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.msft.png":::
       Список экспериментов в параметрах DevTools  
    :::image-end:::  
    
1.  На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажок рядом с каждым компонентом, который нужно протестировать.  
1.  Закройте и снова откройте Microsoft Edge DevTools.  

> [!NOTE]
> Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.  Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.  

## Выделены экспериментальные функции  

В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.  

| Экспериментальная функция | Версия Microsoft Edge |  
|:--- |:--- |  
| [Вкладка "Включение настраиваемых сочетаний клавиш"](#enable-custom-keyboard-shortcuts-settings-tab) | 84 или более поздняя версия |
| [Эмуляция: поддержка двух режимов экрана](#emulation-support-dual-screen-mode) | 84 или более поздняя версия |  
| [Включение новых функций отладки CSS Grid](#enable-new-css-grid-debugging-features) | 85 или более поздняя версия |  
| [Включение поддержки перемещения вкладок между панелями](#enable-support-to-move-tabs-between-panels) | 85 или более поздняя версия |  
| [Включить подсказку](#enable-webhint) | 85 или более поздняя версия |  
| [Включение сетевой консоли](#enable-network-console) | 85 или более поздняя версия |  
| [Включение средства просмотра заказов исходным кодом](#enable-source-order-viewer) | 86 или более поздняя версия |  

### Вкладка "Включение настраиваемых сочетаний клавиш"  

Предоставляет новую страницу **сочетаний клавиш** в [параметрах DevTools][DevToolsCustomizeSettings] для сопоставления [сочетаний клавиш][DevToolsShortcuts] в [коде DevTools с Microsoft Visual Studio][VisualstudioCode].  

После включения эксперимента снова откройте [Параметры DevTools][DevToolsCustomizeSettings] , нажав кнопку "выбрать" `Shift` + `?` .  Перейдите на страницу новые **сочетания клавиш** .  Выберите **DevTools (по умолчанию)** в раскрывающемся списке **искать сочетания клавиш из предварительной настройки** и выберите **код Visual Studio**.  Сочетания клавиш в DevTools теперь соответствуют сочетаниям клавиш для эквивалентных действий в коде Visual Studio.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="./media/experiments-keyboard-shortcut.msft.png":::
   Соответствие сочетаний клавиш в DevTools с кодом Visual Studio  
:::image-end:::  

Например, в Windows для приостановки или продолжения выполнения сценария в [Visual Studio][VisualstudioCodeShortcutsKeyboardWindows] используется сочетание клавиш `F5` .  В стиле **DevTools (по умолчанию)** в DevTools используется один и тот же ярлык `F8` .  В стиле **кода Visual Studio** ярлык также можно использовать `F5` .  

### Эмуляция: поддержка двух режимов экрана  

Предоставляет дополнительные функции для эмуляции двух новых двух экранов и устройств складная в Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy сгиб][SamsungMobileGalaxyFold]  

Эмулирует устройства и переключаться между следующими элементами.  

*   режим с одним экраном или сложением  
*   возможность установки на два экрана или несложенный  

Используйте [экспериментальные API](#enable-experimental-apis) для расширения вашего веб-сайта (или приложения) для устройства.  Вы также можете использовать [запросы мультимедиа CSS и API перечисления сегмента Windows для JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].  

<!-- This image was taken in Chromium Canary since we don't yet have an Edge Canary that has Stan's changes -->  

:::image type="complex" source="./media/experiments-dual-screen-emulation.msft.png" alt-text="Эмуляция Surface Duo в Microsoft Edge" lightbox="./media/experiments-dual-screen-emulation.msft.png":::  
   Эмуляция Surface Duo в Microsoft Edge  
:::image-end:::  

#### Включение экспериментальных API  

Чтобы [включить этот эксперимент](#turn-on-experimental-features) в Microsoft Edge DevTools, выполните указанные ниже действия.  

1.  Перейдите к `edge://flags` .  
1.  В текстовом поле **Флаги поиска** введите `Experimental Web Platform features` , выберите " **экспериментальные компоненты веб-платформы** ", а затем **Enabled**— " **Отключить** ".  
1.  Перезапустите Microsoft Edge.  

Чтобы улучшить веб-сайт или приложение для двухпроцессорных и складнаяных устройств, перейдите на страницу [запросы CSS и API перечисления сегмента Windows для JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].

[Включите этот эксперимент](#turn-on-experimental-features) в Microsoft Edge DevTools.  

1.  Откройте новую вкладку в Microsoft EDGE и перейдите к `edge://flags` .  
1.  В текстовом поле **Флаги поиска** введите `Experimental Web Platform features` , выберите **экспериментальные функции веб-платформы**и измените значение **отключено** на **разрешено**.  
1.  Перезапустите Microsoft Edge.  

Дополнительные сведения об улучшении веб-сайта (или приложения) для двухпроцессорных и складнаяных устройств можно найти в [запросах CSS Media и API перечисления сегмента Windows для JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Флажок включения функций экспериментальной веб-платформы" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Флажок включения функций экспериментальной веб-платформы  
:::image-end:::  

> [!NOTE]
> Если вы используете запросы на поиск [мультимедиа в каскадных таблицах или API-интерфейс перечисления сегмента Windows (JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables] ) для повышения качества сайта или приложения для служб [Surface Duo][SurfaceDevicesDuo], необходимо также включить флажок **экспериментальные возможности веб-платформы** в [приложении Android Microsoft Edge][GooglePlayMicrosoftEdge] на устройстве [Surface Duo][SurfaceDevicesDuo] .
> 
> Если флажок **"экспериментальные веб-платформа** " включен [в классическом приложении Microsoft][MicrosoftEdge] EDGE и отключен для [приложения Android Microsoft Edge][GooglePlayMicrosoftEdge], поведение вашего веб-сайта или приложения в эмуляторе Lane Duo в классическом приложении Microsoft EDGE не будет совпадать с [приложением Android Microsoft][GooglePlayMicrosoftEdge] EDGE на [Surface Duo][SurfaceDevicesDuo].  Убедитесь в том, что для устройств Android и Desktop Microsoft Edge успешно используются Эмуляторы Surface Duo в классической платформе [Microsoft Edge][MicrosoftEdge].  

#### Тестирование на устройствах складная и на двух экранах  

При эмуляции [Duo Surface][SurfaceDevicesDuo] в Microsoft EDGE на двух экранах, **стык** прорисовывается на своем веб-сайте или в приложении.  

> [!NOTE]
> **Стык** — это расстояние между двумя экранами.  

Симулятор дисплея для вашего веб-сайта \ (или приложения \) является правильным представлением.  Она будет соответствовать экрану [приложения Android Microsoft Edge][GooglePlayMicrosoftEdge] на [Surface Duo][SurfaceDevicesDuo].  Обновите содержимое, чтобы оно лучше отображалось на **стыке**.  Для получения дополнительных сведений о адаптации веб-сайта к **стыку**(или внешнему приложению) перейдите к разделу [Работа с стыком][DualScreenIntroductionHowWorkSeam] в документации Surface Duo.  

На [панели инструментов устройства][DevtoolsDeviceModeIndexSimulateMobileViewport] есть дополнительные функции, с помощью которых можно протестировать веб-сайт или приложение в нескольких элементах управления и ориентации.  **Rotate** ![ ][ImageRotateIcon] Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите поворот на (повернуть). Объедините функцию с **диапазоном** \ ( ![ Span ][ImageSpanIcon] \), чтобы переключаться между одним экраном или сложением, а также с двойным экраном или без сгиба.  Вместе функции позволяют тестировать ваш веб-сайт или приложение во всех четырех возможностях и ориентациях.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Матрица геоуровней и ориентации для двухпроцессорных и складная устройств" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Матрица геоуровней и ориентации для двухпроцессорных и складная устройств  
:::image-end:::  

Значок " **экспериментальные веб-платформы** " \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) отображает состояние флага " **экспериментальные веб-платформы** ".  Если пометка включена, значок выделена.  Если флажок выключен, значок не выделяется.  Чтобы включить параметр \ (или выключить), выберите значок или перейдите к нему `edge://flags` и переключите флажок.  

#### Дополнительные ресурсы  
*   Дополнительные сведения о разработке можно найти на [веб-сайте с двумя экранами][DualScreenWebIndex].  
*   Установите эмулятор Surface Duo.  Он отличается от эмулятора в Microsoft Edge.  Она эмулирует на устройстве Surface Duo с Android и интегрируется с [Android Studio][AndroidDeveloperStudio].  Дополнительные сведения можно найти в [пакете SDK Surface Duo][DualScreenAndroidGetDuoSdk].  

### Включение новых функций отладки CSS Grid  

Улучшена визуализация на странице при отладке веб-сайтов с макетами сетки CSS.  Вы можете настроить перекрытия в DevTools параметров.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.msft.png":::
   Функция отладки сетки каскадных стилей  
:::image-end:::  

Чтобы просмотреть последние экспериментальные функции, выполните указанные ниже действия.  

1.  В разделе **эксперименты** выберите параметр **включить параметры отладки для новой сетки каскадных стилей (элементы конфигурации, доступные в области Макет в элементах после перезапуска)** .  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включение поддержки перемещения вкладок между панелями  

Обычно такие инструменты, как **элементы** и **сеть** , могут открываться только в главной панели, расположенной в верхней части DevTools.  Такие инструменты, как **трехмерные представления** и **проблемы** , которые обычно закрываются на панели **ящика** , которая находится в нижней части DevTools.  После выбора эксперимента вы можете перемещать инструменты между верхней и нижней панелями.  Чтобы переместить инструмент, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **переместить в начало** или **Переместить вниз**.   Этот эксперимент позволяет настроить макет DevTools.  Чтобы показать или скрыть панель **ящика** , нажмите кнопку `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.msft.png":::
   Перемещение вкладок между панелями  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включить подсказку  

веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое предоставляет отзыв в реальном времени для веб-сайтов и локальных веб-страниц.  Тип обратной связи, предоставляемой функцией " [Подсказка][WebhintMain]".  

*   специальные возможности  
*   совместимость с различными браузерами  
*   безопасность"  
*   эффективности  
*   Приложения PWA  
*   другие распространенные проблемы с веб-разработками  

Эксперименты с этой [подсказкой][WebhintMain] отображаются на панели " [вопросы][DevtoolsIssues] " в виде обратной связи.  Выберите вопрос для отображения документации решения и списка уязвимых ресурсов на вашем веб-сайте.  Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="./media/experiments-webhint.msft.png":::
   Обратная связь по этой подсказке на панели " **вопросы** "  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включение сетевой консоли  

**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.  Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.  

После включения эксперимента убедитесь, что вы перезапустите DevTools.  Чтобы использовать **консоль "сеть**", выполните указанные ниже действия.    

1.  Открытие области " **сеть** ".  
1.  Найдите сетевой запрос, который вы хотите изменить и отправить повторно.  
1.  Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).  
1.  Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.  
1.  Нажмите кнопку **Отправить**.  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Сетевая консоль в консольном ящике" lightbox="./media/network-network-console.msft.png":::
   **Сетевая консоль** в **консольном** ящике  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включение средства просмотра заказов исходным кодом  

**Средство просмотра исходного порядка** — это эксперимент, в котором отображается порядок элементов в источнике страницы.  Порядок отображения на экране может отличаться от порядка источников, который в своюмся случае будет использовать средство чтения с экрана и пользователи клавиатуры.  Для поиска различий между порядком отображения на экране и порядком расположения источника используйте эксперимент в **средстве просмотра исходного порядка** .  

После включения эксперимента убедитесь, что вы перезапустите DevTools.  Чтобы использовать средство просмотра заказов исходного кода, выполните указанные ниже действия.  

1.  Откройте область **элементы** .  
1.  Откройте область **Специальные возможности** на панели ящик \ (Нижняя \).  
1.  В разделе **средство просмотра исходного заказа** установите флажок **Показать порядок источников** .  
1.  Выделит любой HTML-элемент, чтобы отобразить наложение, порядок расположения которых указан в источнике страницы.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Средство просмотра исходного порядка на панели "Специальные возможности"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Средство просмотра исходного порядка** на панели " **Специальные возможности** "  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## Предыдущие экспериментальные функции  

*   Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.  

## Отзывы о экспериментальных функциях  

Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.  

*   Отправка отзыва с помощью значка " **Отправить отзыв** " в DevTools  
*   Твит на [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Значок "Отправить отзыв" в Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   Значок " **Отправить отзыв** " в Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Веб-интерфейс на базе двух экранов | Документы Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получение эмулятора Surface Duo | Документы Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с стыками — введение в работу с устройствами с двумя экранами | Документы Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[VisualstudioCode]: https://code.visualstudio.com "Код Microsoft Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows | Код Microsoft Visual Studio"  

[GitHubMicrosoftedgeMsedgeexplainerFoldables]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Примитивы веб-платформ для Грамотногоных функций на складная устройствах | GitHub"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy, сгиб | Samsung"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[WebhintMain]: https://webhint.io "Подсказка"  

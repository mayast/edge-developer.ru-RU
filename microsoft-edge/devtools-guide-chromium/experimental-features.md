---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/21/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: 6b3e1c06d6b8ed79054c28df483fcca93e5751d6
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902858"
---
# Экспериментальные функции  

Вы можете использовать экспериментальные функции, которые все еще находятся на стадии разработки в Microsoft Edge DevTools для тестирования и [предоставления отзывов](#providing-feedback-on-experimental-features) , прежде чем они будут выпущены широко.  

Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.  

## Включение экспериментальных функций  

Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.  

1.  [Откройте DevTools][DevtoolsOpen].  
     *   Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  
1.  Открытие области [параметров][DevToolsCustomizeSettings] .  
    *   Выберите `Shift` + `?` .  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  
1.  В левой части области **параметров** выберите раздел **эксперименты** .  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.png":::
       Список экспериментов в параметрах DevTools  
    :::image-end:::  
    
1.  На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажки рядом с функциями, которые нужно протестировать.  
1.  Закройте и снова откройте Microsoft Edge DevTools.  

> [!NOTE]
> Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.  Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.  

## Выделены экспериментальные функции  

В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.  

| Экспериментальная функция | Версия Microsoft Edge |  
|:--- |:--- |  
| [Вкладка "Включение настраиваемых сочетаний клавиш"](#enable-custom-keyboard-shortcuts-settings-tab) | 84 или более поздняя версия |
| [Включение новых функций отладки CSS Grid](#enable-new-css-grid-debugging-features) | 85 или более поздняя версия |  
| [Включение поддержки перемещения вкладок между панелями](#enable-support-to-move-tabs-between-panels) | 85 или более поздняя версия |  
| [Включить подсказку](#enable-webhint) | 85 или более поздняя версия | 
| [Включение сетевой консоли](#enable-network-console) | 85 или более поздняя версия |

### Вкладка "Включение настраиваемых сочетаний клавиш"

Содержит новую страницу **сочетаний клавиш** в [параметрах DevTools][DevToolsCustomizeSettings] , которая позволяет использовать соответствующие сочетания [клавиш][DevToolsShortcuts] в коде DevTools и [VS][VisualstudioCode].  

После включения эксперимента снова откройте [Параметры DevTools][DevToolsCustomizeSettings] с помощью SELECT `Shift` + `?` .  Перейдите на страницу новые **сочетания клавиш** .  Выберите **DevTools (по умолчанию)** в раскрывающемся списке **искать сочетания клавиш из предварительной настройки** и выберите **код Visual Studio**.  Сочетания клавиш в DevTools теперь соответствуют сочетаниям клавиш для эквивалентных действий в коде VS.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Сопоставление сочетаний клавиш в DevTools с кодом VS" lightbox="./media/experiments-keyboard-shortcut.png":::
   Сопоставление сочетаний клавиш в DevTools с кодом VS
:::image-end:::  

Например, в Windows для приостановки или продолжения выполнения сценария в [коде VS][VisualstudioCodeShortcutsKeyboardWindows] используется сочетание клавиш `F5` .  В стиле **DevTools (по умолчанию)** в DevTools используется один и тот же ярлык `F8` .  В стиле **кода Visual Studio** ярлык также можно использовать `F5` .  

### Включение новых функций отладки CSS Grid  

Улучшена визуализация на странице при отладке веб-сайтов с макетами сетки CSS.  Вы можете настроить перекрытия в DevTools параметров.  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.png":::
   Функция отладки сетки каскадных стилей  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включение поддержки перемещения вкладок между панелями  

Обычно такие инструменты, как **элементы** и **сеть** , можно открывать только на главной панели \ (Top \) DevTools.  Аналогичным образом такие инструменты, как **трехмерный вид** и **проблемы** , можно открывать только на панели ящик \ (Нижняя \) DevTools.  Если вы выберете эксперимент, вы можете перемещать инструменты между верхней и нижней панелями, наведя указатель мыши на вкладку, открыв контекстное меню, а затем выбрав пункты **переместить в начало** или **Переместить вниз**.   Этот эксперимент позволяет настроить макет DevTools.  Чтобы отобразить или скрыть нижнюю панель, нажмите кнопку `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.png":::
   Перемещение вкладок между панелями  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включить подсказку  

веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для обеспечения специальных возможностей, совместимости, безопасности, производительности, PWAs и других распространенных проблем, возникающих при работе в Интернете.  При [эксперименте с DevTools][WebhintMain] на панели " [вопросы][DevtoolsIssues] " появляется обратная связь с помощью подсказки.  Вы можете выбрать проблему, чтобы получить сведения о том, как устранить проблему и список уязвимых ресурсов на вашем веб-сайте.  Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Обратная связь по этой подсказке на панели вопросы" lightbox="./media/experiments-webhint.png":::
   Обратная связь по этой подсказке на панели "вопросы"  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включение сетевой консоли

**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.  Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.  

После включения эксперимента убедитесь, что вы перезапустите DevTools. Чтобы использовать консоль "сеть", выполните указанные ниже действия.
1.  Открытие области " **сеть** ".
1.  Найдите сетевой запрос, который вы хотите изменить и отправить повторно.
1.  Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**). 
1.  Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.
1.  Нажмите кнопку **Отправить**.  

:::image type="complex" source="./media/network-network-console.png" alt-text="Сетевая консоль в консольном ящике" lightbox="./media/network-network-console.png":::
Сетевая консоль в консольном ящике
:::image-end::: 

<!--Available in Microsoft Edge version 85 and later.  --> 

## Предыдущие экспериментальные функции  

*   Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.  

## Отзывы о экспериментальных функциях  

Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.  

*   Отправка отзыва с помощью значка обратной связи в DevTools  
*   Твит на [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Значок обратной связи в Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   Значок обратной связи в Microsoft Edge DevTools  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows | Код Visual Studio"  

[WebhintMain]: https://webhint.io "Подсказка" 

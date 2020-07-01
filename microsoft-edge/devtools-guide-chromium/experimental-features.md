---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: 731a289f555870eeff9cdc160965b59925b70c4d
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843958"
---
# Экспериментальные функции  

Вы можете использовать экспериментальные функции, которые все еще находятся на стадии разработки в Microsoft Edge DevTools для тестирования и [предоставления отзывов](#providing-feedback-on-experimental-features) , прежде чем они будут выпущены широко.  

Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.  

## Включение экспериментальных функций  

Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.  

1.  [Откройте DevTools][DevtoolsOpen].  
     *   Нажмите клавиши `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  
1.  Открытие области **параметров** .  
    *   Нажмите клавишу `Shift` + `?` .  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  
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
| [Включение новых функций отладки CSS Grid](#enable-new-css-grid-debugging-features) | 85 или более поздняя версия |  
| [Включение поддержки перемещения вкладок между панелями](#enable-support-to-move-tabs-between-panels) | 85 или более поздняя версия |  
| [Включить подсказку](#enable-webhint) | 85 или более поздняя версия |  

### Включение новых функций отладки CSS Grid  

Улучшена визуализация на странице при отладке веб-сайтов с макетами сетки CSS.  Вы можете настроить перекрытия в DevTools параметров.  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.png":::
   Функция отладки сетки каскадных стилей  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включение поддержки перемещения вкладок между панелями  

Обычно такие инструменты, как **элементы** и **сеть** , можно открывать только на главной панели \ (Top \) DevTools.  Аналогичным образом такие инструменты, как **трехмерный вид** и **проблемы** , можно открывать только на панели ящик \ (Нижняя \) DevTools.  Если выбрать этот эксперимент, вы можете перемещать инструменты между верхней и нижней панелями, наведя указатель мыши на вкладку, открыв контекстное меню (щелкните правой кнопкой \) и выбрав переместить в **Начало** или **Переместить вниз**.   Этот эксперимент позволяет настроить макет DevTools.  Чтобы отобразить или скрыть нижнюю панель, нажмите `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.png":::
   Перемещение вкладок между панелями  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включить подсказку  

веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для обеспечения специальных возможностей, совместимости, безопасности, производительности, PWAs и других распространенных проблем, возникающих при работе в Интернете.  Этот эксперимент приводит к отклику на DevTools на панели " [вопросы][DevtoolsIssues] ".  Вы можете выбрать проблему, чтобы получить сведения о том, как устранить проблему и список уязвимых ресурсов на вашем веб-сайте.  Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="./media/experiments-webhint.png":::
   Обратная связь по этой подсказке на панели "вопросы"  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

## Предыдущие экспериментальные функции  

*   Теперь [трехмерный вид][Devtools3DView] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.  

## Отзывы о экспериментальных функциях  

Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или что-то еще связано с DevTools, выполните указанные ниже действия.  

*   Отправка отзыва с помощью значка обратной связи в DevTools  
*   Твит на [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Значок обратной связи в Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   Значок обратной связи в Microsoft Edge DevTools  
:::image-end:::  

<!-- links -->  

[Devtools3DView]: ./3D-view.md "Трехмерный вид | Документы Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools — документы Майкрософт"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[WebhintMain]: https://webhint.io "Подсказка" 

---
title: Переключение Microsoft Edge DevTools в режим предварительного просмотра цветовой схемы (CSS предпочитает цветовую схему)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: a83284b676ad388114a4a0ddb7ebdf2203ebcb90
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758118"
---
# Эмуляция темной или светлой цветовой схемы  

В операционных системах можно отобразить любое приложение более темным или более светлым цветом.  Если у вас есть веб-продукт, у которого есть светлая тема в более темном режиме работы, это может привести к проблемам с читаемостью для некоторых пользователей.  В Интернете вы можете использовать запрос в виде " [предпочтительный-Цветная схема][MDNPrefersColorScheme] ", чтобы определить, нужно ли пользователям просматривать ваш продукт более темная или более светлая цветовая схема.  Используйте [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] , чтобы имитировать изменение из темного режима в светлый, не изменяя всей операционной системы.  

1.  Открытие **меню команд**.  
    1.  Нажмите клавишу `Control` + `Shift` + `P` Windows или `Command` + `Shift` + `P` macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           **Меню команд**  
        :::image-end:::   
        
1.  Тип `emulate color` , выберите **Эмуляция предпочтительных цветов в CSS: темная** или **Эмуляция цветовой схемы CSS: светлая** и нажатая `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Выбор цветовой схемы в меню команд" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Выбор цветовой схемы в меню **команд**  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Просто введите `dark` или `light` не раскроете нужный инструмент, так как в этом случае можно [выбрать тему для DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].  Если вы не знаете, что нужно сделать, убедитесь в том, что выбран элемент меню **рендеринга** , а не элемент меню **внешний вид** .  

1.  После того как вы выберете цветовую схему, перезагрузите текущий документ, чтобы увидеть режим имитации.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Имитация светового режима в Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Имитация светового режима в Microsoft Edge DevTools  
    :::image-end:::  
    
    Просмотрите и измените CSS, как любую другую веб-страницу.  Дополнительные сведения можно найти [в разделе Начало просмотра и изменение CSS][DevtoolsGuideChromiumCssIndex].  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft EDGE (Chromium) — Инструменты разработчика Microsoft | Документы Microsoft"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Включить темную тему в Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "предпочтение — цветовая схема | MDN"  

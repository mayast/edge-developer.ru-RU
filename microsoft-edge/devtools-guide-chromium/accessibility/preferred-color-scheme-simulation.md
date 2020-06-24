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
# <span data-ttu-id="dbdf3-103">Эмуляция темной или светлой цветовой схемы</span><span class="sxs-lookup"><span data-stu-id="dbdf3-103">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="dbdf3-104">В операционных системах можно отобразить любое приложение более темным или более светлым цветом.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-104">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="dbdf3-105">Если у вас есть веб-продукт, у которого есть светлая тема в более темном режиме работы, это может привести к проблемам с читаемостью для некоторых пользователей.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-105">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="dbdf3-106">В Интернете вы можете использовать запрос в виде " [предпочтительный-Цветная схема][MDNPrefersColorScheme] ", чтобы определить, нужно ли пользователям просматривать ваш продукт более темная или более светлая цветовая схема.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-106">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to see your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="dbdf3-107">Используйте [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] , чтобы имитировать изменение из темного режима в светлый, не изменяя всей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-107">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="dbdf3-108">Открытие **меню команд**.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-108">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="dbdf3-109">Нажмите клавишу `Control` + `Shift` + `P` Windows или `Command` + `Shift` + `P` macOS.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-109">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="dbdf3-111">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="dbdf3-111">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="dbdf3-112">Тип `emulate color` , выберите **Эмуляция предпочтительных цветов в CSS: темная** или **Эмуляция цветовой схемы CSS: светлая** и нажатая `Enter` .</span><span class="sxs-lookup"><span data-stu-id="dbdf3-112">Type `emulate color`, select either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light**  and then press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Выбор цветовой схемы в меню команд" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="dbdf3-114">Выбор цветовой схемы в меню **команд**</span><span class="sxs-lookup"><span data-stu-id="dbdf3-114">Color scheme selection from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="dbdf3-115">Просто введите `dark` или `light` не раскроете нужный инструмент, так как в этом случае можно [выбрать тему для DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="dbdf3-115">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span></span>  <span data-ttu-id="dbdf3-116">Если вы не знаете, что нужно сделать, убедитесь в том, что выбран элемент меню **рендеринга** , а не элемент меню **внешний вид** .</span><span class="sxs-lookup"><span data-stu-id="dbdf3-116">If you are wondering what to choose, make sure that you are selecting a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="dbdf3-117">После того как вы выберете цветовую схему, перезагрузите текущий документ, чтобы увидеть режим имитации.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-117">After you select a color scheme, reload the current document to see the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Имитация светового режима в Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="dbdf3-119">Имитация светового режима в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="dbdf3-119">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="dbdf3-120">Просмотрите и измените CSS, как любую другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-120">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="dbdf3-121">Дополнительные сведения можно найти [в разделе Начало просмотра и изменение CSS][DevtoolsGuideChromiumCssIndex].</span><span class="sxs-lookup"><span data-stu-id="dbdf3-121">For more information, see [Get Started With Viewing And Changing CSS][DevtoolsGuideChromiumCssIndex].</span></span>  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft EDGE (Chromium) — Инструменты разработчика Microsoft | Документы Microsoft"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Включить темную тему в Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "предпочтение — цветовая схема | MDN"  

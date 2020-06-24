---
title: Переключение Microsoft Edge DevTools в режим предварительного просмотра цветовой схемы (CSS предпочитает цветовую схему)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 94c5369f0eb35059933be7f6202a4f64450629cd
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758112"
---
# <span data-ttu-id="71fde-103">Понижение моделирования движения</span><span class="sxs-lookup"><span data-stu-id="71fde-103">Reduced Motion Simulation</span></span>  

<span data-ttu-id="71fde-104">Анимация в веб-продуктах может представлять собой проблему с читаемостью.</span><span class="sxs-lookup"><span data-stu-id="71fde-104">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="71fde-105">В операционных системах проблему можно решить, добавив параметр, позволяющий отключить анимацию, чтобы избежать путаницы и потенциальных проблем, связанных с работоспособностью, например инициирования захвата.</span><span class="sxs-lookup"><span data-stu-id="71fde-105">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="71fde-106">На веб-сайте вы можете использовать запрос на доступ к материалам CSS с [сокращенными][MDNPrefersReducedMotion] эффектами перемещения, чтобы определить, предпочитаете ли пользователи видеть анимацию.</span><span class="sxs-lookup"><span data-stu-id="71fde-106">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="71fde-107">В вашем продукте вы можете заключить код анимации в тест, чтобы избежать анимаций для затронутых пользователей.</span><span class="sxs-lookup"><span data-stu-id="71fde-107">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
  animation: none;
  }
}
```  

<span data-ttu-id="71fde-108">С помощью [Microsoft Edge DevTools][DevtoolsGuideChromiumMain]вы можете имитировать этот уменьшенный параметр перемещения, не изменяя операционную систему.</span><span class="sxs-lookup"><span data-stu-id="71fde-108">Using the [Microsoft Edge DevTools][DevtoolsGuideChromiumMain], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="71fde-109">Открытие **меню команд**.</span><span class="sxs-lookup"><span data-stu-id="71fde-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="71fde-110">Нажмите клавишу `Control` + `Shift` + `P` Windows или `Command` + `Shift` + `P` macOS.</span><span class="sxs-lookup"><span data-stu-id="71fde-110">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="71fde-112">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="71fde-112">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="71fde-113">Тип `reduced` , чтобы включить или отключить эмуляцию.</span><span class="sxs-lookup"><span data-stu-id="71fde-113">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="71fde-114">Выберите параметр и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="71fde-114">Select the option and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Включение и отключение параметра "предпочтительные уменьшенные перемещения" в меню команд" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="71fde-116">Включение и отключение параметра " **предпочтительные уменьшенные перемещения** " в **меню команд**</span><span class="sxs-lookup"><span data-stu-id="71fde-116">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="71fde-117">Обновите текущую страницу, чтобы убедиться, что анимации выключены или отображаются.</span><span class="sxs-lookup"><span data-stu-id="71fde-117">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Рисунок 1: меню команд"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Рисунок 2: переключение уменьшенного движения из палитры команд"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft EDGE (Chromium) — Инструменты разработчика Microsoft | Документы Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "предпочитать — понижение уровня | MDN"  
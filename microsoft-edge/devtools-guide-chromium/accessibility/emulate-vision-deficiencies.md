---
title: Эмуляция видения deficiencies в Microsoft Edge DevTools (жалюзи цвета)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758121"
---
# <span data-ttu-id="4b38e-103">Эмуляция видения deficiencies</span><span class="sxs-lookup"><span data-stu-id="4b38e-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="4b38e-104">В любой стране мира около 8% от мужчин и 0,5% в женщин имеется [концепция цвета][ColorblindawarenessMain] , которая обычно называется "жалюзи цветов".</span><span class="sxs-lookup"><span data-stu-id="4b38e-104">Worldwide approximately 8% of men and 0.5% of women have a [color vision deficiency][ColorblindawarenessMain] commonly named "Color Blindness".</span></span>  <span data-ttu-id="4b38e-105">[Microsoft Edge DevTools][MicrosoftEdgeDevTools] позволяет эмулировать различные известные deficiencies и предоставлять предварительный просмотр продукта для проверки.</span><span class="sxs-lookup"><span data-stu-id="4b38e-105">[Microsoft Edge DevTools][MicrosoftEdgeDevTools] enables you to emulate various known deficiencies and provide a preview of your product for you to review.</span></span>  

| <span data-ttu-id="4b38e-106">Цветовой недостатк</span><span class="sxs-lookup"><span data-stu-id="4b38e-106">Color Deficiency</span></span> | <span data-ttu-id="4b38e-107">Сведения</span><span class="sxs-lookup"><span data-stu-id="4b38e-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="4b38e-108">Размытое видение</span><span class="sxs-lookup"><span data-stu-id="4b38e-108">Blurred vision</span></span> |  |   
| <span data-ttu-id="4b38e-109">Protanopia</span><span class="sxs-lookup"><span data-stu-id="4b38e-109">Protanopia</span></span> | <span data-ttu-id="4b38e-110">Невозможность воспринимать красный индикатор.</span><span class="sxs-lookup"><span data-stu-id="4b38e-110">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="4b38e-111">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="4b38e-111">Deuteranopia</span></span> | <span data-ttu-id="4b38e-112">Невозможность воспринимать зеленый свет.</span><span class="sxs-lookup"><span data-stu-id="4b38e-112">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="4b38e-113">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="4b38e-113">Tritanopia</span></span> | <span data-ttu-id="4b38e-114">Невозможность воспринимать любой синий индикатор.</span><span class="sxs-lookup"><span data-stu-id="4b38e-114">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="4b38e-115">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="4b38e-115">Achromatopsia</span></span> | <span data-ttu-id="4b38e-116">Невозможность воспринимать любой цвет, кроме оттенков серого.</span><span class="sxs-lookup"><span data-stu-id="4b38e-116">The inability to perceive any color, except for shades of grey.</span></span> |  

## <span data-ttu-id="4b38e-117">Переход к средствам отображения</span><span class="sxs-lookup"><span data-stu-id="4b38e-117">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="4b38e-118">Чтобы протестировать текущий веб-продукт в цвете deficiencies, откройте [инструменты рендеринга][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="4b38e-118">To test your current web product for color deficiencies, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="4b38e-119">Открытие средств рендеринга путем выбора `...` пункта меню на панели инструментов</span><span class="sxs-lookup"><span data-stu-id="4b38e-119">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="4b38e-120">Выбор</span><span class="sxs-lookup"><span data-stu-id="4b38e-120">Select</span></span> `More tools`  
1.  <span data-ttu-id="4b38e-121">Выбор</span><span class="sxs-lookup"><span data-stu-id="4b38e-121">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Открытие средств рендеринга" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="4b38e-123">Открытие **средств рендеринга**</span><span class="sxs-lookup"><span data-stu-id="4b38e-123">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="4b38e-124">В нижней половине DevTools откроется меню **рендеринга** .</span><span class="sxs-lookup"><span data-stu-id="4b38e-124">The **Rendering** menu appears in the bottom half of the DevTools.</span></span>  

1.  <span data-ttu-id="4b38e-125">Прокрутите вниз до `Emulate Vision deficiencies` пункта меню и выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="4b38e-125">Scroll down to the `Emulate Vision deficiencies` menu item and select from the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Меню "эмулятор" deficiencies "инструменты для отрисовки"" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="4b38e-127">Меню " **эмулятор" deficiencies** "инструменты для **отрисовки** "</span><span class="sxs-lookup"><span data-stu-id="4b38e-127">The **Emulate Vision Deficiencies** menu of the **Rendering** tools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b38e-128">Выберите один из вариантов</span><span class="sxs-lookup"><span data-stu-id="4b38e-128">Choose any of the options</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Параметры меню "концепция имитации deficiencies"" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="4b38e-130">Параметры меню " **концепция имитации deficiencies** "</span><span class="sxs-lookup"><span data-stu-id="4b38e-130">The **Emulate Vision Deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b38e-131">Текущая страница отображается в имитации того, как она может выглядеть для пользователя с выбранным недостатком.</span><span class="sxs-lookup"><span data-stu-id="4b38e-131">The current page is displayed in a simulation of how it may appear to a user with the chosen deficiency.</span></span>  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Документация по средствам разработчика Microsoft EDGE в эмуляции размытого видения" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="4b38e-133">Отображается с помощью эмуляции **размытого видения**</span><span class="sxs-lookup"><span data-stu-id="4b38e-133">Displayed using **Blurred Vision** emulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Документация по средствам разработчика Microsoft EDGE в эмуляторе концепции Achromatopsia" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="4b38e-135">Отображение с помощью эмуляции **концепции Achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="4b38e-135">Display using **Achromatopsia Vision** emulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="4b38e-136">Использование меню команд</span><span class="sxs-lookup"><span data-stu-id="4b38e-136">Using the command menu</span></span>  

<span data-ttu-id="4b38e-137">Кроме того, вы можете достичь разных эмуляций, не переходя между различными меню с помощью **меню команд**.</span><span class="sxs-lookup"><span data-stu-id="4b38e-137">You may also reach the different emulations without going through the various menus using the **Command Menu**.</span></span>  

1.  <span data-ttu-id="4b38e-138">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="4b38e-138">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="4b38e-140">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="4b38e-140">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b38e-141">Введите текст `emulate` , который вы хотите имитировать, и нажмите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4b38e-141">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Различные параметры эмуляции, доступные в меню команд" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="4b38e-143">Различные параметры эмуляции, доступные в **меню команд**</span><span class="sxs-lookup"><span data-stu-id="4b38e-143">The different emulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="4b38e-144">Средства эмуляции представляют собой приблизительные сведения о том, как человек с каждым недостатком может видеть ваш продукт.</span><span class="sxs-lookup"><span data-stu-id="4b38e-144">The emulation tools are approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="4b38e-145">У каждого человека разный, поэтому концепция deficiencies по серьезности может варьироваться от человека к человеку.</span><span class="sxs-lookup"><span data-stu-id="4b38e-145">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="4b38e-146">Для более эффективного удовлетворения потребностей пользователей следует избегать цветовых сочетаний, которые могут быть причиной проблем.</span><span class="sxs-lookup"><span data-stu-id="4b38e-146">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="4b38e-147">Средства эмуляции не полностью изменяют доступность вашего продукта, но у вас должен быть лучший первый шаг к устранению незначительных deficiencies.</span><span class="sxs-lookup"><span data-stu-id="4b38e-147">The emulation tools are not a full assessment of the accessibility of your product, but you should have a good first step towards avoiding the biggest deficiencies.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Организация, в которой вы осведомлены о цвете"  
[AmfcbMain]: https://www.amfcb.org "Американская основа для цвета "вслепую" (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Инструменты для отрисовки Microsoft EDGE (Chromium)"  

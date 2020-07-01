---
title: Эмуляция видения deficiencies в Microsoft Edge DevTools (жалюзи цвета)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843923"
---
# <span data-ttu-id="b4fbd-103">Эмуляция видения deficiencies</span><span class="sxs-lookup"><span data-stu-id="b4fbd-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="b4fbd-104">Чтобы лучше удовлетворить потребности пользователей с помощью [цветовой][ColorblindawarenessMain] платформы \ (ослабление цвета \), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] позволяет имитировать определенную концепцию deficiencies.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-104">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="b4fbd-105">Средство **эмуляции deficiencies** имитирует следующие категории.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-105">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="b4fbd-106">Некоторая концепция цвета</span><span class="sxs-lookup"><span data-stu-id="b4fbd-106">Color vision deficiency</span></span> | <span data-ttu-id="b4fbd-107">Сведения</span><span class="sxs-lookup"><span data-stu-id="b4fbd-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b4fbd-108">Размытое видение</span><span class="sxs-lookup"><span data-stu-id="b4fbd-108">Blurred vision</span></span> | <span data-ttu-id="b4fbd-109">У пользователя возникли трудности с детальными сведениями.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-109">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="b4fbd-110">Protanopia</span><span class="sxs-lookup"><span data-stu-id="b4fbd-110">Protanopia</span></span> | <span data-ttu-id="b4fbd-111">Пользователь не может воспринимать красный свет.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-111">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="b4fbd-112">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="b4fbd-112">Deuteranopia</span></span> | <span data-ttu-id="b4fbd-113">Пользователь не может воспринимать зеленый свет.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-113">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="b4fbd-114">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="b4fbd-114">Tritanopia</span></span> | <span data-ttu-id="b4fbd-115">Пользователь не может воспринимать синий свет.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-115">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="b4fbd-116">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="b4fbd-116">Achromatopsia</span></span> | <span data-ttu-id="b4fbd-117">Пользователь не может воспринимать любой цвет, что сокращает цвет до оттенка серого.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-117">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="b4fbd-118">Переход к средствам отображения</span><span class="sxs-lookup"><span data-stu-id="b4fbd-118">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="b4fbd-119">Чтобы смоделировать предметный ряд, применяемый для вашего веб-продукта, откройте [инструменты для подготовки к просмотру][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="b4fbd-119">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="b4fbd-120">Открытие средств рендеринга путем выбора `...` пункта меню на панели инструментов</span><span class="sxs-lookup"><span data-stu-id="b4fbd-120">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="b4fbd-121">Выбор</span><span class="sxs-lookup"><span data-stu-id="b4fbd-121">Select</span></span> `More tools`  
1.  <span data-ttu-id="b4fbd-122">Выбор</span><span class="sxs-lookup"><span data-stu-id="b4fbd-122">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Открытие средств рендеринга" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="b4fbd-124">Открытие **средств рендеринга**</span><span class="sxs-lookup"><span data-stu-id="b4fbd-124">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="b4fbd-125">Меню **рендеринга** появится в ящике.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-125">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="b4fbd-126">Прокрутите вниз до `Emulate vision deficiencies` пункта меню и щелкните раскрывающееся меню, чтобы отобразить параметры.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-126">Scroll down to the `Emulate vision deficiencies` menu item and select the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Меню "симулятор deficiencies видения" в ящике отрисовки" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="b4fbd-128">Меню " **симулятор deficiencies видения** " в ящике **отрисовки**</span><span class="sxs-lookup"><span data-stu-id="b4fbd-128">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b4fbd-129">Выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-129">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Параметры меню "концепция имитации deficiencies"" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="b4fbd-131">Параметры меню " **концепция имитации deficiencies** "</span><span class="sxs-lookup"><span data-stu-id="b4fbd-131">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b4fbd-132">В главном окне будет показана Эмуляция выбранного параметра, примененная к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-132">The main windows displays the simulation of your selected option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Вывод на экран с помощью \* \* имитация размытого видения \* \*" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="b4fbd-134">Отображение с помощью имитации **размытого видения**</span><span class="sxs-lookup"><span data-stu-id="b4fbd-134">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Вывод на экран с помощью функции эмуляции \* \* Achromatopsia \* \*" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="b4fbd-136">Отображение с помощью имитации **Achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="b4fbd-136">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="b4fbd-137">Использование меню команд</span><span class="sxs-lookup"><span data-stu-id="b4fbd-137">Use the Command Menu</span></span>  

<span data-ttu-id="b4fbd-138">Вы также можете использовать **командное меню** для доступа к различным эмуляциям.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-138">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="b4fbd-139">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="b4fbd-139">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="b4fbd-141">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="b4fbd-141">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b4fbd-142">Введите текст `emulate` , который вы хотите имитировать, и нажмите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b4fbd-142">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Различные варианты моделирования, доступные в меню команд" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="b4fbd-144">Различные варианты моделирования, доступные в **меню команд**</span><span class="sxs-lookup"><span data-stu-id="b4fbd-144">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="b4fbd-145">Средства **эмуляции deficiencies** помогают понять, как человек с каждым недостатком может видеть ваш продукт.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-145">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="b4fbd-146">У каждого человека разный, поэтому концепция deficiencies по серьезности может варьироваться от человека к человеку.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-146">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="b4fbd-147">Для более эффективного удовлетворения потребностей пользователей следует избегать цветовых сочетаний, которые могут быть причиной проблем.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-147">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="b4fbd-148">Средства **имитации концепции deficiencies** не являются полным анализом специальных возможностей вашего продукта.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-148">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="b4fbd-149">Вместо этого инструменты **эмуляции deficiencies** должны дать вам хороший первый шаг, чтобы избежать проблем.</span><span class="sxs-lookup"><span data-stu-id="b4fbd-149">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Организация, в которой вы осведомлены о цвете"  
[AmfcbMain]: https://www.amfcb.org "Американская основа для цвета "вслепую" (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Инструменты для отрисовки Microsoft EDGE (Chromium)"  

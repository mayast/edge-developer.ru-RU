---
title: Приступая к просмотру и изменению каскадных таблиц стилей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601819"
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





# <span data-ttu-id="dad04-103">Приступая к просмотру и изменению каскадных таблиц стилей</span><span class="sxs-lookup"><span data-stu-id="dad04-103">Get Started With Viewing And Changing CSS</span></span>   



<span data-ttu-id="dad04-104">Эти интерактивные учебники помогут вам ознакомиться с основными принципами просмотра и изменения CSS для страниц с помощью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="dad04-104">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="dad04-105">Открытие примеров CSS</span><span class="sxs-lookup"><span data-stu-id="dad04-105">Open CSS Examples</span></span>  

1.  <span data-ttu-id="dad04-106">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **примеры CSS** , чтобы открыть их в новом окне.</span><span class="sxs-lookup"><span data-stu-id="dad04-106">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="dad04-107">Примеры CSS</span><span class="sxs-lookup"><span data-stu-id="dad04-107">CSS Examples</span></span>][GlitchDevToolsCssExamples]  

> [!NOTE]
> <span data-ttu-id="dad04-108">Если вы хотите [закрепить окно DevTools][DevToolsCustomizePlacement] справа от окна просмотра \ (на [рис. 1](#figure-1)\), нажмите кнопку **Настройка и управление DevTools** `...` .</span><span class="sxs-lookup"><span data-stu-id="dad04-108">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in [Figure 1](#figure-1)\), click **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="dad04-109">В раскрывающемся меню **Настройка и управление DevTools** в разделе **закрепляемая на стороне** экрана выберите пункт **закрепить по правому**краю.</span><span class="sxs-lookup"><span data-stu-id="dad04-109">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="dad04-110">Просмотр CSS для элемента</span><span class="sxs-lookup"><span data-stu-id="dad04-110">View the CSS for an element</span></span>   

1.  <span data-ttu-id="dad04-111">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="dad04-111">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="dad04-112">Щелкните текст правой кнопкой мыши `Inspect Me!` и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="dad04-112">Right-click the `Inspect Me!` text and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="dad04-113">В DevTools на панели " **элементы** " на вкладке " **дерево DOM** " `Inspect Me!` выделена кнопка "элемент".</span><span class="sxs-lookup"><span data-stu-id="dad04-113">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        > ##### <span data-ttu-id="dad04-114">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="dad04-114">Figure 1</span></span>  
        > <span data-ttu-id="dad04-115">Проверяемый элемент выделен в **дереве DOM**</span><span class="sxs-lookup"><span data-stu-id="dad04-115">The inspected element is highlighted in the **DOM Tree**</span></span>  
        > ![Проверяемый элемент выделен в дереве DOM][ImageInspect]  
        
    1.  <span data-ttu-id="dad04-117">`Inspect Me!`Найдите значение атрибута в элементе `data-message` и скопируйте его.</span><span class="sxs-lookup"><span data-stu-id="dad04-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="dad04-118">На странице в поле **значение `data-message` :** введите значение.</span><span class="sxs-lookup"><span data-stu-id="dad04-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="dad04-119">Щелкните текст правой кнопкой мыши `Inspect Me!` и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="dad04-119">Right-click the `Inspect Me!` text and select **Inspect**.</span></span>  
    
    1.  <span data-ttu-id="dad04-120">В DevTools на панели **элементы** откройте вкладку **стили** .</span><span class="sxs-lookup"><span data-stu-id="dad04-120">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="dad04-121">На вкладке **стили** `Inspect Me!` элемент выделен.</span><span class="sxs-lookup"><span data-stu-id="dad04-121">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="dad04-122">В `Inspect Me!` элементе найдите `aloha` правило класса.</span><span class="sxs-lookup"><span data-stu-id="dad04-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="dad04-123">Вы видите это правило, так как оно применяется к `Inspect Me!` элементу.</span><span class="sxs-lookup"><span data-stu-id="dad04-123">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="dad04-124">В `aloha` классе найдите значение для `padding` стиля и скопируйте его.</span><span class="sxs-lookup"><span data-stu-id="dad04-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        > ##### <span data-ttu-id="dad04-125">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="dad04-125">Figure 2</span></span>  
        > <span data-ttu-id="dad04-126">Классы CSS, примененные к выбранному элементу, такие как `aloha` , отображаются на вкладке " **стили** "</span><span class="sxs-lookup"><span data-stu-id="dad04-126">CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        > ![Классы CSS, примененные к проверяемому элементу, выделяются на вкладке "стили"][ImageAloha]  
        
1.  <span data-ttu-id="dad04-128">На странице в поле **значение `padding` :** введите значение.</span><span class="sxs-lookup"><span data-stu-id="dad04-128">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="dad04-129">Добавление объявления CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="dad04-129">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="dad04-130">Используйте вкладку **стили** , если вы хотите изменить или добавить объявления CSS к элементу.</span><span class="sxs-lookup"><span data-stu-id="dad04-130">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="dad04-131">Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.</span><span class="sxs-lookup"><span data-stu-id="dad04-131">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="dad04-132">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="dad04-132">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="dad04-133">Щелкните текст правой кнопкой мыши `Add A Background Color To Me!` и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="dad04-133">Right-click the `Add A Background Color To Me!` text and select **Inspect**.</span></span>  
1.  <span data-ttu-id="dad04-134">Нажмите кнопку в `element.style` верхней части вкладки **стили** .</span><span class="sxs-lookup"><span data-stu-id="dad04-134">Click `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="dad04-135">Введите текст `background-color` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="dad04-135">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="dad04-136">Введите текст `honeydew` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="dad04-136">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="dad04-137">В **дереве DOM** вы увидите, что к элементу применено объявление встроенного стиля.</span><span class="sxs-lookup"><span data-stu-id="dad04-137">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  

> ##### <span data-ttu-id="dad04-138">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="dad04-138">Figure 3</span></span>  
> <span data-ttu-id="dad04-139">`background-color:honeydew`Объявление применено к элементу с помощью `element.style` раздела вкладки " **стили** "</span><span class="sxs-lookup"><span data-stu-id="dad04-139">The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
> ![Добавление объявления CSS к элементу с помощью вкладки "стили"][ImageDeclaration]  

## <span data-ttu-id="dad04-141">Добавление класса CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="dad04-141">Add a CSS class to an element</span></span>   

<span data-ttu-id="dad04-142">С помощью вкладки " **стили** " можно увидеть, как выглядит элемент, когда класс CSS применяется к элементу или удаляется из него.</span><span class="sxs-lookup"><span data-stu-id="dad04-142">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="dad04-143">Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.</span><span class="sxs-lookup"><span data-stu-id="dad04-143">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="dad04-144">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="dad04-144">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="dad04-145">Щелкните элемент правой кнопкой мыши `Add A Class To Me!` и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="dad04-145">Right-click the `Add A Class To Me!` element and select **Inspect**.</span></span>  
1.  <span data-ttu-id="dad04-146">Щелкните **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="dad04-146">Click **.cls**.</span></span>  <span data-ttu-id="dad04-147">DevTools открывает текстовое поле, в котором можно добавлять классы к выбранному элементу.</span><span class="sxs-lookup"><span data-stu-id="dad04-147">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="dad04-148">Введите `color_me` текст в текстовом поле **Добавить новый класс** и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="dad04-148">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="dad04-149">Флажок отображается под текстовым полем " **Добавить новый класс** ", в котором можно включить или отключить класс.</span><span class="sxs-lookup"><span data-stu-id="dad04-149">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="dad04-150">Если `Add A Class To Me!` к элементу применены другие классы, вы также можете переключаться между ними.</span><span class="sxs-lookup"><span data-stu-id="dad04-150">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  

> ##### <span data-ttu-id="dad04-151">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="dad04-151">Figure 4</span></span>  
> <span data-ttu-id="dad04-152">`color_me`Класс применен к элементу с помощью раздела **. CLS** на вкладке " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="dad04-152">The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
> ![Применение класса color_me к элементу][ImageApplyClass]  

## <span data-ttu-id="dad04-154">Добавление PseudoState в класс</span><span class="sxs-lookup"><span data-stu-id="dad04-154">Add a pseudostate to a class</span></span>   

<span data-ttu-id="dad04-155">С помощью вкладки **стили** вы можете навсегда применить CSS-PseudoState к элементу.</span><span class="sxs-lookup"><span data-stu-id="dad04-155">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="dad04-156">DevTools поддерживает `:active` , `:focus` , `:hover` , и `:visited` .</span><span class="sxs-lookup"><span data-stu-id="dad04-156">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="dad04-157">Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.</span><span class="sxs-lookup"><span data-stu-id="dad04-157">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="dad04-158">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="dad04-158">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="dad04-159">Наведите указатель мыши на `Hover Over Me!` текст.</span><span class="sxs-lookup"><span data-stu-id="dad04-159">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="dad04-160">Цвет фона изменится.</span><span class="sxs-lookup"><span data-stu-id="dad04-160">The background color changes.</span></span>  
1.  <span data-ttu-id="dad04-161">Щелкните текст правой кнопкой мыши `Hover Over Me!` и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="dad04-161">Right-click the `Hover Over Me!` text and select **Inspect**.</span></span>  
1.  <span data-ttu-id="dad04-162">На вкладке **стили** щелкните **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="dad04-162">In the **Styles** tab, click **:hov**.</span></span>  
1.  <span data-ttu-id="dad04-163">Установите флажок **: наведение указателя мыши** .</span><span class="sxs-lookup"><span data-stu-id="dad04-163">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="dad04-164">Цвет фона изменится так же, как и раньше, несмотря на то, что вы не наводите указатель мыши на элемент.</span><span class="sxs-lookup"><span data-stu-id="dad04-164">The background color changes like before, even though you are not actually hovering over the element.</span></span>  

> ##### <span data-ttu-id="dad04-165">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="dad04-165">Figure 5</span></span>  
> <span data-ttu-id="dad04-166">Переключение `:hover` PseudoState для элемента</span><span class="sxs-lookup"><span data-stu-id="dad04-166">Toggling the `:hover` pseudostate on an element</span></span>  
> ![Переключение наведения указателя на PseudoState элемента][ImageSetHover]  

## <span data-ttu-id="dad04-168">Изменение размеров элемента</span><span class="sxs-lookup"><span data-stu-id="dad04-168">Change the dimensions of an element</span></span>   

<span data-ttu-id="dad04-169">С помощью интерактивной схемы **"модель Box** " на вкладке " **стили** " можно изменить ширину, высоту, заполнение, границу или длину границы элемента.</span><span class="sxs-lookup"><span data-stu-id="dad04-169">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="dad04-170">Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.</span><span class="sxs-lookup"><span data-stu-id="dad04-170">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="dad04-171">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="dad04-171">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="dad04-172">Щелкните элемент правой кнопкой мыши `Change My Margin!` и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="dad04-172">Right-click the `Change My Margin!` element and select **Inspect**.</span></span>  
1.  <span data-ttu-id="dad04-173">На схеме **модель Box** на вкладке **стили** наведите указатель мыши на **Заполнение**.</span><span class="sxs-lookup"><span data-stu-id="dad04-173">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="dad04-174">Заполнение элемента выделено в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="dad04-174">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="dad04-175">В зависимости от размера окна DevTools, возможно, потребуется прокрутить в нижнюю часть вкладки **стили** , чтобы увидеть **модель Box**.</span><span class="sxs-lookup"><span data-stu-id="dad04-175">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="dad04-176">Дважды щелкните левое поле в **модели Box**, которое в настоящее время имеет значение `-` , означающее, что у элемента нет левого поля.</span><span class="sxs-lookup"><span data-stu-id="dad04-176">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="dad04-177">Введите текст `100px` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="dad04-177">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="dad04-178">**Модель Box** по умолчанию имеет значения пикселей, но также принимает другие значения, например `25%` или `10vw` .</span><span class="sxs-lookup"><span data-stu-id="dad04-178">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  

> ##### <span data-ttu-id="dad04-179">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="dad04-179">Figure 6</span></span>  
> <span data-ttu-id="dad04-180">Наведение указателя мыши на заполнение элемента</span><span class="sxs-lookup"><span data-stu-id="dad04-180">Hovering over the padding of the element</span></span>  
> ![Наведение указателя мыши на заполнение элемента][ImageShowPadding]  

> ##### <span data-ttu-id="dad04-182">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="dad04-182">Figure 7</span></span>  
> <span data-ttu-id="dad04-183">Изменение левого поля элемента</span><span class="sxs-lookup"><span data-stu-id="dad04-183">Changing the left-margin of the element</span></span>  
> ![Изменение левого поля элемента][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Рисунок 1: в дереве DOM выделено проверенный элемент"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Рисунок 2: классы CSS, примененные к проверяемому элементу, выделяются на вкладке "стили""  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Рисунок 3: Добавление объявления CSS к элементу с помощью вкладки "стили""  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Рисунок 4: применение класса color_me к элементу"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Рис. 5: переключение наведения указателя на элемент PseudoState"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Рисунок 6: наведение указателя мыши на заполнение элемента"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Рисунок 7: изменение левого поля элемента"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Примеры CSS — Microsoft EDGE (Chromium) DevTools | Цепь"  

> [!NOTE]
> <span data-ttu-id="dad04-194">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dad04-194">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dad04-195">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="dad04-195">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dad04-197">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dad04-197">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

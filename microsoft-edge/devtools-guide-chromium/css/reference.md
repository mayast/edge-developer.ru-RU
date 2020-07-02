---
title: Справочник по CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 4f0370b83d8c939476a1ed378dbdf750101c9527
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843972"
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







# <span data-ttu-id="e245a-103">Справочник по CSS</span><span class="sxs-lookup"><span data-stu-id="e245a-103">CSS Reference</span></span>   



<span data-ttu-id="e245a-104">Ознакомьтесь с новыми рабочими процессами в этой полной справке Microsoft Edge DevTools функции, относящиеся к просмотру и изменению каскадных таблиц стилей.</span><span class="sxs-lookup"><span data-stu-id="e245a-104">Discover new workflows in this comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="e245a-105">Ознакомьтесь с основными принципами [просмотра и изменения каскадных таблиц стилей][DevToolsCSSGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="e245a-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="e245a-106">Выбор элемента</span><span class="sxs-lookup"><span data-stu-id="e245a-106">Select an element</span></span>   

<span data-ttu-id="e245a-107">Панель " **элементы** " в DevTools позволяет просматривать или изменять CSS для одного элемента за один раз.</span><span class="sxs-lookup"><span data-stu-id="e245a-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="e245a-108">Выбранный элемент выделится в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="e245a-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="e245a-109">Стили элемента отображаются на панели " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="e245a-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="e245a-110">В разделе [Просмотр CSS для элемента][DevToolsCSSGetStartedTutorial] учебника.</span><span class="sxs-lookup"><span data-stu-id="e245a-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-111">На [рисунке 1](#figure-1) `h1` элемент, выделенный в **дереве DOM** , является выбранным элементом.</span><span class="sxs-lookup"><span data-stu-id="e245a-111">In [Figure 1](#figure-1), the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="e245a-112">Справа в области **стили** отображаются стили элемента.</span><span class="sxs-lookup"><span data-stu-id="e245a-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="e245a-113">В левой части экрана выделяется элемент в окне просмотра, но только потому, что в данный момент указатель мыши наведен на него в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="e245a-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

> ##### <span data-ttu-id="e245a-114">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="e245a-114">Figure 1</span></span>  
> <span data-ttu-id="e245a-115">Пример выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="e245a-115">An example of a selected element</span></span>  
> ![Пример выбранного элемента][ImageSelectedElement]  

<span data-ttu-id="e245a-117">Существует множество способов выбора элемента.</span><span class="sxs-lookup"><span data-stu-id="e245a-117">There are many ways to select an element:</span></span>  

*   <span data-ttu-id="e245a-118">В окне просмотра щелкните элемент правой кнопкой мыши и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="e245a-118">In your viewport, right-click the element and select **Inspect**.</span></span>  
*   <span data-ttu-id="e245a-119">В DevTools щелкните **выбрать элемент** , ![ выберите элемент ][ImageSelectAnElementIcon] или нажмите клавиши `Control` + `Shift` + `C` \ (Windows \) или `Command` + `Shift` + `C` \ (macOS \), а затем щелкните элемент в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="e245a-119">In DevTools, click **Select an element** ![Select an element][ImageSelectAnElementIcon] or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then click the element in the viewport.</span></span>  
*   <span data-ttu-id="e245a-120">В DevTools щелкните элемент в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="e245a-120">In DevTools, click the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="e245a-121">В DevTools выполните запрос, как `document.querySelector('p')` на **консоли**, щелкните результат правой кнопкой мыши и выберите пункт **Показать на панели элементов**.</span><span class="sxs-lookup"><span data-stu-id="e245a-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, right-click the result, and then select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="e245a-122">Просмотр CSS</span><span class="sxs-lookup"><span data-stu-id="e245a-122">View CSS</span></span>   

### <span data-ttu-id="e245a-123">Просмотр внешней таблицы стилей, в которой определено правило</span><span class="sxs-lookup"><span data-stu-id="e245a-123">View the external stylesheet where a rule is defined</span></span>   

<span data-ttu-id="e245a-124">В области **стили** щелкните ссылку рядом с правилом CSS, чтобы открыть внешнюю таблицу стилей, которая определяет правило.</span><span class="sxs-lookup"><span data-stu-id="e245a-124">In the **Styles** pane, click the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="e245a-125">Если таблица стилей minified, ознакомьтесь с тем, [чтобы сделать файл minified читаемым][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="e245a-125">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-126">На [рис. 2](#figure-2), при нажатии кнопки `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` Переход к строке 2 `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , где `.content h1:first-of-type` определено правило CSS.</span><span class="sxs-lookup"><span data-stu-id="e245a-126">In [Figure 2](#figure-2), clicking `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` takes you to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

> ##### <span data-ttu-id="e245a-127">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="e245a-127">Figure 2</span></span>  
> <span data-ttu-id="e245a-128">Просмотр таблицы стилей, в которой определено правило</span><span class="sxs-lookup"><span data-stu-id="e245a-128">Viewing the stylesheet where a rule is defined</span></span>  
> ![Просмотр таблицы стилей, в которой определено правило][ImageViewRuleStylesheet]  

### <span data-ttu-id="e245a-130">Просмотр только CSS, которая фактически применяется к элементу</span><span class="sxs-lookup"><span data-stu-id="e245a-130">View only the CSS that is actually applied to an element</span></span>   

<span data-ttu-id="e245a-131">На вкладке **стили** отображаются все правила, применимые к элементу, включая объявления, которые были переопределены.</span><span class="sxs-lookup"><span data-stu-id="e245a-131">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="e245a-132">Если вы не заинтересованы в переопределенных объявлениях, используйте **вычисляемые** вкладки для просмотра только CSS, которая фактически применяется к элементу.</span><span class="sxs-lookup"><span data-stu-id="e245a-132">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="e245a-133">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-133">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e245a-134">Перейдите на вкладку " **вычисляемые** " на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="e245a-134">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-135">В окне с широкой DevTools **Вычисляемая** вкладка не существует.</span><span class="sxs-lookup"><span data-stu-id="e245a-135">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="e245a-136">Содержимое **вычисляемой** вкладки отображается на вкладке **стили** .</span><span class="sxs-lookup"><span data-stu-id="e245a-136">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="e245a-137">Унаследованные свойства являются непрозрачными.</span><span class="sxs-lookup"><span data-stu-id="e245a-137">Inherited properties are opaque.</span></span>  <span data-ttu-id="e245a-138">Установите флажок **Показать все** , чтобы увидеть все унаследованные значения.</span><span class="sxs-lookup"><span data-stu-id="e245a-138">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-139">На [рисунке 3](#figure-3)на вкладке " **Вычисляемая** вкладка" показаны свойства CSS, применяемые к текущему `h1` элементу.</span><span class="sxs-lookup"><span data-stu-id="e245a-139">In [Figure 3](#figure-3), the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

> ##### <span data-ttu-id="e245a-140">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="e245a-140">Figure 3</span></span>  
> <span data-ttu-id="e245a-141">**Вычисляемая** вкладка</span><span class="sxs-lookup"><span data-stu-id="e245a-141">The **Computed** tab</span></span>  
> ![Вычисляемая вкладка][ImageComputedTab]  

### <span data-ttu-id="e245a-143">Просмотр свойств CSS в алфавитном порядке</span><span class="sxs-lookup"><span data-stu-id="e245a-143">View CSS properties in alphabetical order</span></span>   

<span data-ttu-id="e245a-144">Используйте **вычисляемую** вкладку.  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-144">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="e245a-145">Просмотр унаследованных свойств CSS</span><span class="sxs-lookup"><span data-stu-id="e245a-145">View inherited CSS properties</span></span>   

<span data-ttu-id="e245a-146">Установите флажок **Показать все** на вкладке **вычисляемый** .  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-146">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="e245a-147">Просмотр модели Box для элемента</span><span class="sxs-lookup"><span data-stu-id="e245a-147">View the box model for an element</span></span>   

<span data-ttu-id="e245a-148">Чтобы просмотреть [модель Box][MDNBoxModel] элемента, перейдите на вкладку **стили** .  Если окно DevTools узким, схема **модель Box** находится в нижней части вкладки.</span><span class="sxs-lookup"><span data-stu-id="e245a-148">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="e245a-149">Чтобы изменить значение, дважды щелкните его.</span><span class="sxs-lookup"><span data-stu-id="e245a-149">To change a value, double-click on it.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-150">На [рисунке 4](#figure-4)схема **модель Box** на вкладке **стили** показывает модель Box для элемента, выбранного в данный момент `h1` .</span><span class="sxs-lookup"><span data-stu-id="e245a-150">In [Figure 4](#figure-4), the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

> ##### <span data-ttu-id="e245a-151">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="e245a-151">Figure 4</span></span>  
> <span data-ttu-id="e245a-152">Схема **модели Box**</span><span class="sxs-lookup"><span data-stu-id="e245a-152">The **Box Model** diagram</span></span>  
> ![Схема модели Box][ImageBoxModel]  

### <span data-ttu-id="e245a-154">Поиск и фильтрация CSS элемента</span><span class="sxs-lookup"><span data-stu-id="e245a-154">Search and filter the CSS of an element</span></span>   

<span data-ttu-id="e245a-155">С помощью текстового поля **Фильтр** на вкладках **стили** и **вычисляемые** вкладки можно искать определенные свойства или значения CSS.</span><span class="sxs-lookup"><span data-stu-id="e245a-155">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="e245a-156">Чтобы также искать унаследованные свойства на вкладке **вычисляемые** , установите флажок **Показать все** .</span><span class="sxs-lookup"><span data-stu-id="e245a-156">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-157">На [рисунке 5](#figure-5)вкладка **стили** отфильтрована, чтобы отображались только правила, включающие поисковый запрос `color` .</span><span class="sxs-lookup"><span data-stu-id="e245a-157">In [Figure 5](#figure-5), the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

> ##### <span data-ttu-id="e245a-158">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="e245a-158">Figure 5</span></span>  
> <span data-ttu-id="e245a-159">Фильтрация вкладки " **стили** "</span><span class="sxs-lookup"><span data-stu-id="e245a-159">Filtering the **Styles** tab</span></span>  
> ![Фильтрация вкладки "стили"][ImageStylesFilter]  

> [!NOTE]
> <span data-ttu-id="e245a-161">На [рисунке 6](#figure-6)с помощью **вычисляемой** вкладки отображаются только объявления, включающие поисковый запрос `100%` .</span><span class="sxs-lookup"><span data-stu-id="e245a-161">In [Figure 6](#figure-6), the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

> ##### <span data-ttu-id="e245a-162">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="e245a-162">Figure 6</span></span>  
> <span data-ttu-id="e245a-163">Фильтрация на вкладке " **Вычисляемая** вкладка"</span><span class="sxs-lookup"><span data-stu-id="e245a-163">Filtering the **Computed** tab</span></span>  
> ![Фильтрация на вкладке "вычисляемая вкладка"][ImageComputerFilter]  

### <span data-ttu-id="e245a-165">Переключение на псевдо-класс</span><span class="sxs-lookup"><span data-stu-id="e245a-165">Toggle a pseudo-class</span></span>   

<span data-ttu-id="e245a-166">Чтобы переключить псевдо-класс, например, `:active` `:focus` `:hover` или `:visited` :</span><span class="sxs-lookup"><span data-stu-id="e245a-166">To toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`:</span></span>  

1.  <span data-ttu-id="e245a-167">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-167">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e245a-168">На панели " **элементы** " перейдите на вкладку " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="e245a-168">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="e245a-169">Щелкните **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="e245a-169">Click **:hov**.</span></span>  
1.  <span data-ttu-id="e245a-170">Проверьте псевдо-класс, который вы хотите включить.</span><span class="sxs-lookup"><span data-stu-id="e245a-170">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-171">На [рисунке 7](#figure-7)переключитесь на `:hover` псевдо-класс.</span><span class="sxs-lookup"><span data-stu-id="e245a-171">In [Figure 7](#figure-7), toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="e245a-172">В окне просмотра убедитесь в том, что `background-color: cornflowerblue` объявление применяется к элементу, несмотря на то что элемент фактически не наведен на указатель.</span><span class="sxs-lookup"><span data-stu-id="e245a-172">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

> ##### <span data-ttu-id="e245a-173">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="e245a-173">Figure 7</span></span>  
> <span data-ttu-id="e245a-174">Переключение `:hover` псевдо-класса</span><span class="sxs-lookup"><span data-stu-id="e245a-174">Toggling the `:hover` pseudo-class</span></span>  
> ![Переключение: псевдо-класс для наведения][ImagePseudoClass]  

<span data-ttu-id="e245a-176">Дополнительные сведения о том, как [Добавить PseudoState в класс][DevToolsCSSGetStartedAddPseudoState] для интерактивного учебника.</span><span class="sxs-lookup"><span data-stu-id="e245a-176">See [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState] for an interactive tutorial.</span></span> 

### <span data-ttu-id="e245a-177">Просмотр страницы в режиме печати</span><span class="sxs-lookup"><span data-stu-id="e245a-177">View a page in print mode</span></span>   

<span data-ttu-id="e245a-178">Чтобы просмотреть страницу в режиме печати, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-178">To view a page in print mode:</span></span>  
1.  <span data-ttu-id="e245a-179">[Открытие меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="e245a-179">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="e245a-180">Начните вводить текст `Rendering` и выберите его `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="e245a-180">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="e245a-181">В раскрывающемся списке **Эмуляция мультимедиа в CSS** нажмите кнопку **Печать**.</span><span class="sxs-lookup"><span data-stu-id="e245a-181">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="e245a-182">Просмотр использованной и неиспользуемой CSS с помощью вкладки "покрытие"</span><span class="sxs-lookup"><span data-stu-id="e245a-182">View used and unused CSS with the Coverage tab</span></span>   

<span data-ttu-id="e245a-183">На вкладке Coverage показано, какая страница CSS используется в действительности.</span><span class="sxs-lookup"><span data-stu-id="e245a-183">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="e245a-184">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), когда DevTools в фокусе, чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="e245a-184">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to open the Command Menu.</span></span>  
1.  <span data-ttu-id="e245a-185">Начните вводить текст `coverage` и выберите **Показать покрытие**.</span><span class="sxs-lookup"><span data-stu-id="e245a-185">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="e245a-186">Откроется вкладка покрытие.</span><span class="sxs-lookup"><span data-stu-id="e245a-186">The Coverage tab appears.</span></span>  
    
    > ##### <span data-ttu-id="e245a-187">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="e245a-187">Figure 8</span></span>  
    > <span data-ttu-id="e245a-188">Открытие вкладки "покрытие" в меню команд</span><span class="sxs-lookup"><span data-stu-id="e245a-188">Opening the Coverage tab from the Command Menu</span></span>  
    > ![Открытие вкладки "покрытие" в меню команд][ImageCommandMenu]  
    
    > ##### <span data-ttu-id="e245a-190">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="e245a-190">Figure 9</span></span>  
    > <span data-ttu-id="e245a-191">Вкладка "покрытие"</span><span class="sxs-lookup"><span data-stu-id="e245a-191">The Coverage tab</span></span>  
    > ![Вкладка "покрытие"][ImageCoverageEmpty]  
    
1.  <span data-ttu-id="e245a-193">Нажмите кнопку **начать покрытие и обновите** страницу, чтобы ![ запустить инструментирование, и обновите ее ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="e245a-193">Click **Start instrumenting coverage and refresh the page** ![Start instrumenting coverage and refresh the page][ImageRefreshIcon].</span></span>  <span data-ttu-id="e245a-194">Обновленная страница и вкладка Coverage предоставляют общие сведения о том, сколько стилей CSS и JavaScript используется для каждого файла, загружаемого браузером.</span><span class="sxs-lookup"><span data-stu-id="e245a-194">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="e245a-195">Зеленый представляет используемые CSS.</span><span class="sxs-lookup"><span data-stu-id="e245a-195">Green represents used CSS.</span></span>  <span data-ttu-id="e245a-196">Красный — неиспользуемый CSS.</span><span class="sxs-lookup"><span data-stu-id="e245a-196">Red represents unused CSS.</span></span>  
    
    > ##### <span data-ttu-id="e245a-197">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="e245a-197">Figure 10</span></span>  
    > <span data-ttu-id="e245a-198">Общие сведения о том, какая таблица CSS (и JavaScript) используется и неиспользуемая</span><span class="sxs-lookup"><span data-stu-id="e245a-198">An overview of how much CSS (and JavaScript) is used and unused</span></span>  
    > ![Общие сведения о том, какая таблица CSS (и JavaScript) используется и неиспользуемая][ImageCoverageOverview]  

1.  <span data-ttu-id="e245a-200">Щелкните CSS-файл, чтобы просмотреть разбиение по строкам для используемого CSS.</span><span class="sxs-lookup"><span data-stu-id="e245a-200">Click a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e245a-201">На [рисунке 11](#figure-11)строки 145 в 147 и 149 в 151 из `b66bc881.site-ltr.css` не используются, в то время как используются строки 163 — 166.</span><span class="sxs-lookup"><span data-stu-id="e245a-201">In [Figure 11](#figure-11), lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    > ##### <span data-ttu-id="e245a-202">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="e245a-202">Figure 11</span></span>  
    > <span data-ttu-id="e245a-203">Разбиение по строкам для используемых и неиспользуемых CSS</span><span class="sxs-lookup"><span data-stu-id="e245a-203">A line-by-line breakdown of used and unused CSS</span></span>  
    > ![Разбиение по строкам для используемых и неиспользуемых CSS][ImageCoverageDetail]  
    
### <span data-ttu-id="e245a-205">Принудительная печать в режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="e245a-205">Force print preview mode</span></span>   

<span data-ttu-id="e245a-206">Просмотрите [DevTools в режиме предварительного просмотра][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="e245a-206">See [Force DevTools Into Print Preview Mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="e245a-207">Изменение CSS</span><span class="sxs-lookup"><span data-stu-id="e245a-207">Change CSS</span></span>   

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="e245a-208">Добавление объявления CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="e245a-208">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="e245a-209">Поскольку порядок объявлений влияет на стиль элемента, вы можете добавлять объявления различными способами.</span><span class="sxs-lookup"><span data-stu-id="e245a-209">Since the order of declarations affects how an element is styled, you may add declarations in different ways:</span></span>  

*   <span data-ttu-id="e245a-210">[Добавление встроенного объявления](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="e245a-210">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="e245a-211">Эквивалентно добавлению `style` атрибута в HTML элемента.</span><span class="sxs-lookup"><span data-stu-id="e245a-211">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="e245a-212">[Добавление объявления в правило стиля](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="e245a-212">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="e245a-213">Какой рабочий процесс следует использовать?</span><span class="sxs-lookup"><span data-stu-id="e245a-213">What workflow should you use?</span></span>** <span data-ttu-id="e245a-214">В большинстве сценариев вы, возможно, захотите использовать рабочий процесс объявления на встроенных элементах.</span><span class="sxs-lookup"><span data-stu-id="e245a-214">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="e245a-215">Встроенные объявления имеют более высокие особенности, чем внешние, поэтому встроенный рабочий процесс гарантирует, что изменения вступают в силу в элементе так, как вы ожидали.</span><span class="sxs-lookup"><span data-stu-id="e245a-215">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in the element as you would expect.</span></span>  <span data-ttu-id="e245a-216">Дополнительные сведения о том, как узнать подробности, приведены в разделе [типы Selector][MDNSelectorTypes] .</span><span class="sxs-lookup"><span data-stu-id="e245a-216">See [Selector Types][MDNSelectorTypes] for more on specificity.</span></span>  

<span data-ttu-id="e245a-217">Если при отладке любого стиля элемента требуется специально проверить, что происходит, если объявление определено в разных местах, используйте другой рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="e245a-217">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="e245a-218">Добавление встроенного объявления</span><span class="sxs-lookup"><span data-stu-id="e245a-218">Add an inline declaration</span></span>   

<span data-ttu-id="e245a-219">Чтобы добавить встроенное объявление, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-219">To add an inline declaration:</span></span>  

1.  <span data-ttu-id="e245a-220">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-220">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e245a-221">В области **стили** щелкните между скобками раздела **element. Style** .</span><span class="sxs-lookup"><span data-stu-id="e245a-221">In the **Styles** pane, click between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="e245a-222">Курсор фокусируется на том, что позволяет вводить текст.</span><span class="sxs-lookup"><span data-stu-id="e245a-222">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="e245a-223">Введите имя свойства и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e245a-223">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="e245a-224">Введите допустимое значение для этого свойства и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e245a-224">Enter a valid value for that property and press `Enter`.</span></span>  <span data-ttu-id="e245a-225">Убедитесь, что в **дереве DOM** `style` к элементу добавлен атрибут.</span><span class="sxs-lookup"><span data-stu-id="e245a-225">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-226">На [рисунке 12](#figure-12)к `margin-top` `background-color` выбранному элементу применены свойства и.</span><span class="sxs-lookup"><span data-stu-id="e245a-226">In [Figure 12](#figure-12), the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="e245a-227">В **дереве DOM** убедитесь, что объявления отражены в `style` атрибуте для элемента.</span><span class="sxs-lookup"><span data-stu-id="e245a-227">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

> ##### <span data-ttu-id="e245a-228">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="e245a-228">Figure 12</span></span>  
> <span data-ttu-id="e245a-229">Добавление встроенных объявлений</span><span class="sxs-lookup"><span data-stu-id="e245a-229">Adding inline declarations</span></span>  
> ![Добавление встроенных объявлений][ImageInlineDeclarations]  

#### <span data-ttu-id="e245a-231">Добавление объявления в правило стиля</span><span class="sxs-lookup"><span data-stu-id="e245a-231">Add a declaration to a style rule</span></span>   

<span data-ttu-id="e245a-232">Чтобы добавить объявление к существующему правилу стиля, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-232">To add a declaration to an existing style rule:</span></span>  

1.  <span data-ttu-id="e245a-233">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-233">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e245a-234">В области **стили** щелкните между скобками правила стиля, к которому вы хотите добавить объявление.</span><span class="sxs-lookup"><span data-stu-id="e245a-234">In the **Styles** pane, click between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="e245a-235">Курсор фокусируется на том, что позволяет вводить текст.</span><span class="sxs-lookup"><span data-stu-id="e245a-235">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="e245a-236">Введите имя свойства и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e245a-236">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="e245a-237">Введите допустимое значение для этого свойства и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e245a-237">Enter a valid value for that property and press `Enter`.</span></span>  

> ##### <span data-ttu-id="e245a-238">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="e245a-238">Figure 13</span></span>  
> <span data-ttu-id="e245a-239">Добавление `border-bottom-style:groove` объявления в правило стиля</span><span class="sxs-lookup"><span data-stu-id="e245a-239">Adding the `border-bottom-style:groove` declaration to a style rule</span></span>  
> ![Добавление объявления в правило стиля][ImageAddDeclarationExistingRule]  

### <span data-ttu-id="e245a-241">Изменение имени или значения объявления</span><span class="sxs-lookup"><span data-stu-id="e245a-241">Change a declaration name or value</span></span>   

<span data-ttu-id="e245a-242">Дважды щелкните имя или значение объявления, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="e245a-242">Double-click the name or value of a declaration to change it.</span></span>  <span data-ttu-id="e245a-243">Сочетания клавиш для быстрого увеличения или уменьшения значения (, или единиц) можно найти [в статье изменение значений объявлений](#change-declaration-values-with-keyboard-shortcuts) `0.1` `1` `10` `100` .</span><span class="sxs-lookup"><span data-stu-id="e245a-243">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

> ##### <span data-ttu-id="e245a-244">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="e245a-244">Figure 14</span></span>  
> <span data-ttu-id="e245a-245">Изменение значения</span><span class="sxs-lookup"><span data-stu-id="e245a-245">Changing the value of the</span></span> `border-bottom-style`  
> ![Изменение значения объявления][ImageAddDeclarationExistingRule2]  

### <span data-ttu-id="e245a-247">Изменение значений объявлений с помощью сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="e245a-247">Change declaration values with keyboard shortcuts</span></span>   

<span data-ttu-id="e245a-248">При редактировании значения объявления вы можете использовать следующие сочетания клавиш, чтобы увеличить значение на фиксированную величину.</span><span class="sxs-lookup"><span data-stu-id="e245a-248">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a fixed amount:</span></span>  

*   <span data-ttu-id="e245a-249">Нажмите клавиши `Alt` + `Up` \ (Windows \) или `Option` + `Up` \ (macOS \), чтобы увеличить значение `0.1` .</span><span class="sxs-lookup"><span data-stu-id="e245a-249">Press `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="e245a-250">Нажмите `Up` , чтобы изменить значение на `1` или, `0.1` Если текущее значение находится в диапазоне от `-1` и `1` .</span><span class="sxs-lookup"><span data-stu-id="e245a-250">Press `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="e245a-251">Нажмите, `Shift` + `Up` чтобы увеличить `10` .</span><span class="sxs-lookup"><span data-stu-id="e245a-251">Press `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="e245a-252">Нажмите клавиши `Shift` + `Page Up` \ (Windows \) или `Shift` + `Command` + `Up` \ (macOS \), чтобы увеличить значение на `100` .</span><span class="sxs-lookup"><span data-stu-id="e245a-252">Press `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="e245a-253">Кроме того, выполняется уменьшение.</span><span class="sxs-lookup"><span data-stu-id="e245a-253">Decrementing also works.</span></span>  <span data-ttu-id="e245a-254">Просто замените каждый из `Up` упомянутых выше экземпляров `Down` .</span><span class="sxs-lookup"><span data-stu-id="e245a-254">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="e245a-255">Добавление класса в элемент</span><span class="sxs-lookup"><span data-stu-id="e245a-255">Add a class to an element</span></span>   

<span data-ttu-id="e245a-256">Чтобы добавить класс в элемент, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-256">To add a class to an element:</span></span>  

1.  <span data-ttu-id="e245a-257">[Выберите элемент](#select-an-element) в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="e245a-257">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="e245a-258">Щелкните **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="e245a-258">Click **.cls**.</span></span>  
1.  <span data-ttu-id="e245a-259">Введите имя класса в текстовом поле **Добавить новый класс** .</span><span class="sxs-lookup"><span data-stu-id="e245a-259">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="e245a-260">Нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e245a-260">Press `Enter`.</span></span>  

> ##### <span data-ttu-id="e245a-261">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="e245a-261">Figure 15</span></span>  
> <span data-ttu-id="e245a-262">Область « **классы элементов** »</span><span class="sxs-lookup"><span data-stu-id="e245a-262">The **Element Classes** pane</span></span>  
> ![Область «классы элементов»][ImageElementClasses]  

### <span data-ttu-id="e245a-264">Переключение класса</span><span class="sxs-lookup"><span data-stu-id="e245a-264">Toggle a class</span></span>   

<span data-ttu-id="e245a-265">Чтобы включить или отключить класс для элемента, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-265">To enable or disable a class on an element:</span></span>  

1.  <span data-ttu-id="e245a-266">[Выберите элемент](#select-an-element) в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="e245a-266">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="e245a-267">Откройте область **классы элементов** .</span><span class="sxs-lookup"><span data-stu-id="e245a-267">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="e245a-268">Дополнительные сведения о том, [как добавить класс в элемент](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-268">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="e245a-269">Под текстовым полем **Добавить новый класс** находятся все классы, которые применяются к этому элементу.</span><span class="sxs-lookup"><span data-stu-id="e245a-269">Below the **Add New Class** text box are all of the classes that are being applied to this element.</span></span>  
1.  <span data-ttu-id="e245a-270">Установите флажок рядом с классом, который вы хотите включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="e245a-270">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="e245a-271">Добавление правила стиля</span><span class="sxs-lookup"><span data-stu-id="e245a-271">Add a style rule</span></span>   

<span data-ttu-id="e245a-272">Чтобы добавить новое правило стиля, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-272">To add a new style rule:</span></span>  

1.  <span data-ttu-id="e245a-273">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-273">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e245a-274">Нажмите кнопку **новое** правило стиля ![ ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="e245a-274">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon].</span></span>  <span data-ttu-id="e245a-275">DevTools вставляет новое правило под правилом **element. Style** .</span><span class="sxs-lookup"><span data-stu-id="e245a-275">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-276">На [рисунке 16](#figure-16)DevTools добавляет `h1.devsite-page-title` правило стиля после нажатия кнопки **новое правило стиля**.</span><span class="sxs-lookup"><span data-stu-id="e245a-276">In [Figure 16](#figure-16), DevTools adds the `h1.devsite-page-title` style rule after clicking **New Style Rule**.</span></span>  

> ##### <span data-ttu-id="e245a-277">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="e245a-277">Figure 16</span></span>  
> <span data-ttu-id="e245a-278">Добавление нового правила стиля</span><span class="sxs-lookup"><span data-stu-id="e245a-278">Adding a new style rule</span></span>  
> ![Добавление нового правила стиля][ImageStyleRule]  

#### <span data-ttu-id="e245a-280">Выберите таблицу стилей, к которой нужно добавить правило.</span><span class="sxs-lookup"><span data-stu-id="e245a-280">Choose which stylesheet to add a rule to</span></span>   

<span data-ttu-id="e245a-281">При [добавлении нового правила стиля](#add-a-style-rule)щелкните **и удерживайте новое правило стиля,** чтобы ![ ][ImageNewStyleRuleIcon] выбрать таблицу стилей, к которой нужно добавить правило.</span><span class="sxs-lookup"><span data-stu-id="e245a-281">When [adding a new style rule](#add-a-style-rule), click and hold **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] to choose which stylesheet to add the style rule to.</span></span>  

> ##### <span data-ttu-id="e245a-282">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="e245a-282">Figure 17</span></span>  
> <span data-ttu-id="e245a-283">Выбор таблицы стилей</span><span class="sxs-lookup"><span data-stu-id="e245a-283">Choosing a stylesheet</span></span>  
> ![Выбор таблицы стилей][ImageChooseStylesheet]  

#### <span data-ttu-id="e245a-285">Добавление правила стиля в определенное место</span><span class="sxs-lookup"><span data-stu-id="e245a-285">Add a style rule to a specific location</span></span>   

<span data-ttu-id="e245a-286">Чтобы добавить правило стиля в определенное расположение на вкладке " **стили** ", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-286">To add a style rule to a specific location in the **Styles** tab:</span></span>  

1.  <span data-ttu-id="e245a-287">Наведите указатель мыши на правило стиля, которое находится в том месте, куда вы хотите добавить новое правило стиля.</span><span class="sxs-lookup"><span data-stu-id="e245a-287">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="e245a-288">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e245a-288">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e245a-289">Нажмите кнопку **Вставить правило стиля ниже** ![ , чтобы вставить правило стиля ниже ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="e245a-289">Click **Insert Style Rule Below** ![Insert Style Rule Below][ImageNewStyleRuleIcon].</span></span>  

> ##### <span data-ttu-id="e245a-290">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="e245a-290">Figure 18</span></span>  
> **<span data-ttu-id="e245a-291">Вставить правило стиля ниже</span><span class="sxs-lookup"><span data-stu-id="e245a-291">Insert Style Rule Below</span></span>**  
> ![Вставить правило стиля ниже][ImageInsertStyleRuleBelow]  

### <span data-ttu-id="e245a-293">Панель инструментов "другие действия"</span><span class="sxs-lookup"><span data-stu-id="e245a-293">Reveal the More Actions toolbar</span></span>   

<span data-ttu-id="e245a-294">Панель инструментов " **другие действия** " позволяет:</span><span class="sxs-lookup"><span data-stu-id="e245a-294">The **More Actions** toolbar lets you:</span></span>  

*   <span data-ttu-id="e245a-295">Вставка правила стиля прямо ниже того, на котором вы отправили фокус.</span><span class="sxs-lookup"><span data-stu-id="e245a-295">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="e245a-296">Добавьте в `background-color` `color` `box-shadow` правило стиля, которое `text-shadow` вы хотите включить, или объявление.</span><span class="sxs-lookup"><span data-stu-id="e245a-296">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="e245a-297">Чтобы открыть панель инструментов **Дополнительные действия** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-297">To reveal the **More Actions** toolbar:</span></span>  

1.  <span data-ttu-id="e245a-298">На вкладке **стили** наведите указатель мыши на правило стиля.</span><span class="sxs-lookup"><span data-stu-id="e245a-298">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="e245a-299">**Дополнительные действия** `...` находится в правом нижнем углу раздела "правило стиля".</span><span class="sxs-lookup"><span data-stu-id="e245a-299">**More Actions** `...` is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e245a-300">На [рисунке 19](#figure-19)наведите указатель мыши на `.header-holder.has-default-focus` правило стиля, и в правом нижнем углу раздела правила стиля появится элемент **другие действия** .</span><span class="sxs-lookup"><span data-stu-id="e245a-300">In [Figure 19](#figure-19), hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    > ##### <span data-ttu-id="e245a-301">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="e245a-301">Figure 19</span></span>  
    > <span data-ttu-id="e245a-302">Показать **Дополнительные действия**</span><span class="sxs-lookup"><span data-stu-id="e245a-302">Revealing **More Actions**</span></span>  
    > ![Показать дополнительные действия][ImageRevealMore]  
    
1.  <span data-ttu-id="e245a-304">Наведите указатель мыши на элемент **другие действия** `...` , чтобы открыть описанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-304">Hover over **More Actions** `...` to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e245a-305">**Правило стиля вставки, показанное ниже** , выводится при наведении указателя мыши на **другие действия**.</span><span class="sxs-lookup"><span data-stu-id="e245a-305">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    > ##### <span data-ttu-id="e245a-306">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="e245a-306">Figure 20</span></span>  
    > <span data-ttu-id="e245a-307">Панель инструментов « **другие действия** »</span><span class="sxs-lookup"><span data-stu-id="e245a-307">The **More Actions** toolbar</span></span>  
    > ![Панель инструментов «другие действия»][ImageInsertStyleRuleBelow2]  
    
### <span data-ttu-id="e245a-309">Переключить объявление</span><span class="sxs-lookup"><span data-stu-id="e245a-309">Toggle a declaration</span></span>   

<span data-ttu-id="e245a-310">Чтобы включить или отключить одно объявление, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-310">To toggle a single declaration on or off:</span></span>  

1.  <span data-ttu-id="e245a-311">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-311">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e245a-312">В области **стили** наведите указатель мыши на правило, которое определяет объявление.</span><span class="sxs-lookup"><span data-stu-id="e245a-312">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="e245a-313">Рядом с каждым объявлением отображаются флажки.</span><span class="sxs-lookup"><span data-stu-id="e245a-313">Checkboxes appear next to each declaration.</span></span>  
1.  <span data-ttu-id="e245a-314">Установите или снимите флажок рядом с объявлением.</span><span class="sxs-lookup"><span data-stu-id="e245a-314">Check or uncheck the checkbox next to the declaration.</span></span>  <span data-ttu-id="e245a-315">Если вы снимите флажок объявления, DevTools пересекает его, чтобы показать, что он больше не активен.</span><span class="sxs-lookup"><span data-stu-id="e245a-315">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="e245a-316">На [рисунке 21](#figure-21) `margin-top` свойство для выбранного в данный момент элемента было отключено.</span><span class="sxs-lookup"><span data-stu-id="e245a-316">In [Figure 21](#figure-21), the `margin-top` property for the currently selected element has been toggled off.</span></span>  

> ##### <span data-ttu-id="e245a-317">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="e245a-317">Figure 21</span></span>  
> <span data-ttu-id="e245a-318">Переключение объявления</span><span class="sxs-lookup"><span data-stu-id="e245a-318">Toggling a declaration</span></span>  
> ![Переключение объявления][ImageToggleDeclaration]  

### <span data-ttu-id="e245a-320">Добавление объявления цвета фона</span><span class="sxs-lookup"><span data-stu-id="e245a-320">Add a background-color declaration</span></span>   

<span data-ttu-id="e245a-321">Чтобы добавить `background-color` объявление в элемент, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-321">To add a `background-color` declaration to an element:</span></span>  

1.  <span data-ttu-id="e245a-322">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `background-color` объявление.</span><span class="sxs-lookup"><span data-stu-id="e245a-322">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="e245a-323">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e245a-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e245a-324">Щелкните **добавить цвет фона** ![ добавить цвет фона ][ImageAddBackgroundColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="e245a-324">Click **Add Background Color** ![Add Background Color][ImageAddBackgroundColorIcon].</span></span>  

> ##### <span data-ttu-id="e245a-325">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="e245a-325">Figure 22</span></span>  
> **<span data-ttu-id="e245a-326">Добавление цвета фона</span><span class="sxs-lookup"><span data-stu-id="e245a-326">Add Background Color</span></span>**  
> ![Добавление цвета фона][ImageAddBackgroundColor]  

### <span data-ttu-id="e245a-328">Добавление объявления цвета</span><span class="sxs-lookup"><span data-stu-id="e245a-328">Add a color declaration</span></span>   

<span data-ttu-id="e245a-329">Чтобы добавить `color` объявление в элемент, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-329">To add a `color` declaration to an element:</span></span>  

1.  <span data-ttu-id="e245a-330">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `color` объявление.</span><span class="sxs-lookup"><span data-stu-id="e245a-330">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="e245a-331">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e245a-331">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e245a-332">Нажмите кнопку **Добавить** цвет ![ ][ImageAddColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="e245a-332">Click **Add Color** ![Add Color][ImageAddColorIcon].</span></span>  

> ##### <span data-ttu-id="e245a-333">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="e245a-333">Figure 23</span></span>  
> **<span data-ttu-id="e245a-334">Добавить цвет</span><span class="sxs-lookup"><span data-stu-id="e245a-334">Add Color</span></span>**  
> ![Добавить цвет][ImageAddColor]  

### <span data-ttu-id="e245a-336">Добавление объявления с помощью блочной тени</span><span class="sxs-lookup"><span data-stu-id="e245a-336">Add a box-shadow declaration</span></span>   

<span data-ttu-id="e245a-337">Чтобы добавить `box-shadow` объявление в элемент, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-337">To add a `box-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="e245a-338">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `box-shadow` объявление.</span><span class="sxs-lookup"><span data-stu-id="e245a-338">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="e245a-339">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e245a-339">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e245a-340">Нажмите кнопку Добавить тень надписи "добавить рамку **"** ![ ][ImageAddBoxShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="e245a-340">Click **Add Box Shadow** ![Add Box Shadow][ImageAddBoxShadowIcon].</span></span>  

> ##### <span data-ttu-id="e245a-341">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="e245a-341">Figure 24</span></span>  
> **<span data-ttu-id="e245a-342">Добавление тени для поля</span><span class="sxs-lookup"><span data-stu-id="e245a-342">Add Box Shadow</span></span>**  
> ![Добавление тени для поля][ImageAddBoxShadow]  

### <span data-ttu-id="e245a-344">Добавление объявления тени для текста</span><span class="sxs-lookup"><span data-stu-id="e245a-344">Add a text-shadow declaration</span></span>   

<span data-ttu-id="e245a-345">Чтобы добавить `text-shadow` объявление в элемент, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-345">To add a `text-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="e245a-346">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `text-shadow` объявление.</span><span class="sxs-lookup"><span data-stu-id="e245a-346">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="e245a-347">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e245a-347">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e245a-348">Нажмите кнопку **Добавить** тень текста ![ Добавить тень ][ImageAddTextShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="e245a-348">Click **Add Text Shadow** ![Add Text Shadow][ImageAddTextShadowIcon].</span></span>  

> ##### <span data-ttu-id="e245a-349">Рис. 25</span><span class="sxs-lookup"><span data-stu-id="e245a-349">Figure 25</span></span>  
> **<span data-ttu-id="e245a-350">Добавление тени текста</span><span class="sxs-lookup"><span data-stu-id="e245a-350">Add Text Shadow</span></span>**  
> ![Добавление тени текста][ImageAddTextShadow]  

### <span data-ttu-id="e245a-352">Изменение цвета с помощью палитры цветов</span><span class="sxs-lookup"><span data-stu-id="e245a-352">Change colors with the Color Picker</span></span>   

<span data-ttu-id="e245a-353">В **средстве выбора цвета** есть графический интерфейс для изменения `color` и `background-color` объявлений.</span><span class="sxs-lookup"><span data-stu-id="e245a-353">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="e245a-354">Чтобы открыть окно **выбора цвета**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-354">To open the **Color Picker**:</span></span>  

1.  <span data-ttu-id="e245a-355">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e245a-355">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e245a-356">На вкладке **стили** найдите и щелкните то `color` `background-color` же объявление, которое вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="e245a-356">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="e245a-357">Слева от "," `color` `background-color` или аналогичного значения есть маленький квадрат, который является предварительным просмотром цвета.</span><span class="sxs-lookup"><span data-stu-id="e245a-357">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e245a-358">На [рисунке 26](#figure-26)в маленьком квадрате слева от него `rgba(0, 0, 0, 0.7)` показана эта цветная область.</span><span class="sxs-lookup"><span data-stu-id="e245a-358">In [Figure 26](#figure-26), the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    > ##### <span data-ttu-id="e245a-359">Рис. 26</span><span class="sxs-lookup"><span data-stu-id="e245a-359">Figure 26</span></span>  
    > <span data-ttu-id="e245a-360">Цвет предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="e245a-360">Color preview</span></span>  
    > ![Цвет предварительного просмотра][ImageColorPreview]  
    
1.  <span data-ttu-id="e245a-362">Нажмите кнопку Предварительный просмотр, чтобы открыть окно **выбора цвета**.</span><span class="sxs-lookup"><span data-stu-id="e245a-362">Click the preview to open the **Color Picker**.</span></span>  
    
    > ##### <span data-ttu-id="e245a-363">На рисунке 27</span><span class="sxs-lookup"><span data-stu-id="e245a-363">Figure 27</span></span>  
    > <span data-ttu-id="e245a-364">**Выбор цвета**</span><span class="sxs-lookup"><span data-stu-id="e245a-364">The **Color Picker**</span></span>  
    > ![Выбор цвета][ImageColorPicker]  
    
<span data-ttu-id="e245a-366">Ниже приведено описание каждого элемента пользовательского интерфейса в **средстве выбора цвета**.</span><span class="sxs-lookup"><span data-stu-id="e245a-366">Here is a description of each of the UI elements of the **Color Picker**:</span></span>  

> ##### <span data-ttu-id="e245a-367">Рис. 28</span><span class="sxs-lookup"><span data-stu-id="e245a-367">Figure 28</span></span>  
> <span data-ttu-id="e245a-368">Палитра цветов с заметками</span><span class="sxs-lookup"><span data-stu-id="e245a-368">The Color Picker, annotated</span></span>  
> ![Палитра цветов с заметками][ImageColorPickerAnnotated]  

1.  <span data-ttu-id="e245a-370">**Тени**.</span><span class="sxs-lookup"><span data-stu-id="e245a-370">**Shades**.</span></span>  
1.  <span data-ttu-id="e245a-371">**Пипетка**.</span><span class="sxs-lookup"><span data-stu-id="e245a-371">**Eyedropper**.</span></span>  <span data-ttu-id="e245a-372">Посмотрите [образец цвета на странице с помощью пипетки](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="e245a-372">See [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
1.  <span data-ttu-id="e245a-373">**Копирование в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="e245a-373">**Copy To Clipboard**.</span></span>  <span data-ttu-id="e245a-374">Скопируйте **Отображаемое значение** в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="e245a-374">Copy the **Display Value** to your clipboard.</span></span>  
1.  <span data-ttu-id="e245a-375">**Отображаемое значение**.</span><span class="sxs-lookup"><span data-stu-id="e245a-375">**Display Value**.</span></span>  <span data-ttu-id="e245a-376">Представление RGBA, HSLA или шестнадцатеричного представления цвета.</span><span class="sxs-lookup"><span data-stu-id="e245a-376">The RGBA, HSLA, or Hex representation of the color.</span></span>  
1.  <span data-ttu-id="e245a-377">**Цветовая палитра**.</span><span class="sxs-lookup"><span data-stu-id="e245a-377">**Color Palette**.</span></span>  <span data-ttu-id="e245a-378">Щелкните один из этих квадратов, чтобы изменить цвет на этот квадрат.</span><span class="sxs-lookup"><span data-stu-id="e245a-378">Click one of these squares to change the color to that square.</span></span>  
1.  <span data-ttu-id="e245a-379">**Оттенок**.</span><span class="sxs-lookup"><span data-stu-id="e245a-379">**Hue**.</span></span>  
1.  <span data-ttu-id="e245a-380">**Opacity (прозрачность**).</span><span class="sxs-lookup"><span data-stu-id="e245a-380">**Opacity**.</span></span>  
1.  <span data-ttu-id="e245a-381">**Показать переключатель значения**.</span><span class="sxs-lookup"><span data-stu-id="e245a-381">**Display Value Switcher**.</span></span>  <span data-ttu-id="e245a-382">Переключение между представлениями "RGBA", "HSLA" и "шестнадцатеричный" текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="e245a-382">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
1.  <span data-ttu-id="e245a-383">**Переключатель цветовой палитры**.</span><span class="sxs-lookup"><span data-stu-id="e245a-383">**Color Palette Switcher**.</span></span>  <span data-ttu-id="e245a-384">Переключение между [палитрой «дизайн материала][MaterialDesignColorSystem]», настраиваемой палитрой или палитрой цветов страницы.</span><span class="sxs-lookup"><span data-stu-id="e245a-384">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="e245a-385">DevTools создает цветовую палитру страницы на основе цветов, найденных в стилях.</span><span class="sxs-lookup"><span data-stu-id="e245a-385">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  

#### <span data-ttu-id="e245a-386">Выбор цвета на странице с помощью пипетки</span><span class="sxs-lookup"><span data-stu-id="e245a-386">Sample a color off the page with the Eyedropper</span></span>   

<span data-ttu-id="e245a-387">Когда вы закроете окно **выбора цвета**, **Eyedropper** ![ Пипетка по ][ImageEyedropperIcon] умолчанию будет включена.</span><span class="sxs-lookup"><span data-stu-id="e245a-387">When you open the **Color Picker**, the **Eyedropper** ![Eyedropper][ImageEyedropperIcon] is on by default.</span></span>  <span data-ttu-id="e245a-388">Чтобы изменить выбранный цвет на другой цвет на странице, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e245a-388">To change the selected color to some other color on the page:</span></span>  

1.  <span data-ttu-id="e245a-389">Наведите указатель мыши на целевой цвет в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="e245a-389">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="e245a-390">Щелкните, чтобы подтвердить.</span><span class="sxs-lookup"><span data-stu-id="e245a-390">Click to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e245a-391">На [рисунке 29](#figure-29)в **средстве выбора цвета** отображается текущее цветное значение `rgba(0,0,0,0.7)` , которое близко к черному.</span><span class="sxs-lookup"><span data-stu-id="e245a-391">In [Figure 29](#figure-29), the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="e245a-392">Этот цвет следует изменить на черный, выделенный в окне просмотра, после того как вы щелкните черный.</span><span class="sxs-lookup"><span data-stu-id="e245a-392">This color should change to the black that is currently highlighted in the viewport once the black was clicked.</span></span>  
    
    > ##### <span data-ttu-id="e245a-393">Рис. 29</span><span class="sxs-lookup"><span data-stu-id="e245a-393">Figure 29</span></span>  
    > <span data-ttu-id="e245a-394">Использование пипетки</span><span class="sxs-lookup"><span data-stu-id="e245a-394">Using the Eyedropper</span></span>  
    > ![Использование пипетки][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Рисунок 1: пример выбранного элемента"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Рисунок 2: Просмотр таблицы стилей, в которой определено правило"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Рисунок 3: вычисляемая вкладка"  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Рисунок 4: Схема модели Box"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Рисунок 5: Фильтрация вкладки "стили""  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Рисунок 6: Фильтрация вычисляемой вкладки"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Рисунок 7: переключение: псевдо-класс "наведение""  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Рисунок 8: Открытие вкладки «покрытие» из меню команд"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Рисунок 9: вкладка "покрытие""  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Рисунок 10: Общие сведения о том, сколько CSS (и JavaScript) используется и неиспользуемо"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Рисунок 11: разбиение по строкам использованной и неиспользуемой CSS"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Рисунок 12: Добавление встроенных объявлений"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Рисунок 13: Добавление объявления к правилу стиля"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Рисунок 14: изменение значения объявления"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Рис. 15: область «классы элементов»"  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Рисунок 16: Добавление нового правила стиля"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Рисунок 17: Выбор таблицы стилей"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Рисунок 18: Вставка правила стиля ниже"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "На рисунке 19 показано, как Показать дополнительные действия."  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Рисунок 20: панель инструментов "другие действия""  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Рисунок 21: переключение объявления"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Рисунок 22: Добавление цвета фона"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Рисунок 23: Добавление цвета"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Рисунок 24: Добавление тени поля"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Рисунок 25: Добавление тени текста"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Рисунок 26: предварительный просмотр цвета"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Рисунок 27: палитра цветов"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Рис. 28: палитра цветов с аннотированием"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Рис. 29: Использование пипетки"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Добавление PseudoState в класс — начало работы с просмотром и изменением CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Просмотр CSS для элемента — начало работы с просмотром и изменением CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Создание доступного для чтения файла minified-справочника по отладке JavaScript"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Макет "Цветовая система-материал""  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Модель Box | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Типы выбора — "конкретное |" MDN"  

> [!NOTE]
> <span data-ttu-id="e245a-434">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e245a-434">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e245a-435">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e245a-435">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e245a-437">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e245a-437">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

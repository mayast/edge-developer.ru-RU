---
title: Справочник по CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 908e32140d9deb89489089442055e188cd2d9378
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931462"
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

# <span data-ttu-id="85455-103">Справочник по CSS</span><span class="sxs-lookup"><span data-stu-id="85455-103">CSS reference</span></span>  

<span data-ttu-id="85455-104">Ниже приведен полный справочник по функциям, связанным с просмотром и изменением CSS, в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="85455-104">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="85455-105">Ознакомьтесь с основными принципами [просмотра и изменения каскадных таблиц стилей][DevToolsCSSGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="85455-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="85455-106">Выбор элемента</span><span class="sxs-lookup"><span data-stu-id="85455-106">Select an element</span></span>  

<span data-ttu-id="85455-107">Панель " **элементы** " в DevTools позволяет просматривать или изменять CSS для одного элемента за один раз.</span><span class="sxs-lookup"><span data-stu-id="85455-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="85455-108">Выбранный элемент выделится в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="85455-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="85455-109">Стили элемента отображаются на панели " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="85455-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="85455-110">В разделе [Просмотр CSS для элемента][DevToolsCSSGetStartedTutorial] учебника.</span><span class="sxs-lookup"><span data-stu-id="85455-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-111">На приведенном ниже рисунке `h1` элемент, выделенный в **дереве DOM** , является выбранным элементом.</span><span class="sxs-lookup"><span data-stu-id="85455-111">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="85455-112">Справа в области **стили** отображаются стили элемента.</span><span class="sxs-lookup"><span data-stu-id="85455-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="85455-113">В левой части экрана выделяется элемент в окне просмотра, но только потому, что в данный момент указатель мыши наведен на него в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="85455-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Пример выбранного элемента" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="85455-115">Пример выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="85455-115">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="85455-116">Для выбора элемента используйте одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="85455-116">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="85455-117">В окне просмотра наведите указатель мыши на элемент, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="85455-117">In your viewport, hover on the element, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
*   <span data-ttu-id="85455-118">В DevTools выберите **пункт выбрать** элемент \ (Выбери ![ элемент ][ImageSelectAnElementIcon] \) или SELECT `Control` + `Shift` + `C` \ (Windows \) или `Command` + `Shift` + `C` \ (macOS \), а затем выберите элемент в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="85455-118">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="85455-119">В DevTools выберите элемент в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="85455-119">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="85455-120">В DevTools выполните запрос, как `document.querySelector('p')` на **консоли**, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **Показать на панели элементы**.</span><span class="sxs-lookup"><span data-stu-id="85455-120">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="85455-121">Просмотр CSS</span><span class="sxs-lookup"><span data-stu-id="85455-121">View CSS</span></span>  

### <span data-ttu-id="85455-122">Просмотр внешней таблицы стилей, в которой определено правило</span><span class="sxs-lookup"><span data-stu-id="85455-122">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="85455-123">В области **стили** щелкните ссылку рядом с правилом CSS, чтобы открыть внешнюю таблицу стилей, которая определяет правило.</span><span class="sxs-lookup"><span data-stu-id="85455-123">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="85455-124">Если таблица стилей minified, ознакомьтесь с тем, [чтобы сделать файл minified читаемым][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="85455-124">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-125">На приведенном ниже рисунке после выбора `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` строки 2 `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , где `.content h1:first-of-type` определено правило CSS.</span><span class="sxs-lookup"><span data-stu-id="85455-125">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Просмотр таблицы стилей, в которой определено правило" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="85455-127">Просмотр таблицы стилей, в которой определено правило</span><span class="sxs-lookup"><span data-stu-id="85455-127">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <span data-ttu-id="85455-128">Просмотр только CSS, которая фактически применяется к элементу</span><span class="sxs-lookup"><span data-stu-id="85455-128">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="85455-129">На вкладке **стили** отображаются все правила, применимые к элементу, включая объявления, которые были переопределены.</span><span class="sxs-lookup"><span data-stu-id="85455-129">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="85455-130">Если вы не заинтересованы в переопределенных объявлениях, используйте **вычисляемые** вкладки для просмотра только CSS, которая фактически применяется к элементу.</span><span class="sxs-lookup"><span data-stu-id="85455-130">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="85455-131">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-131">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="85455-132">Перейдите на вкладку " **вычисляемые** " на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="85455-132">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-133">В окне с широкой DevTools **Вычисляемая** вкладка не существует.</span><span class="sxs-lookup"><span data-stu-id="85455-133">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="85455-134">Содержимое **вычисляемой** вкладки отображается на вкладке **стили** .</span><span class="sxs-lookup"><span data-stu-id="85455-134">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="85455-135">Унаследованные свойства являются непрозрачными.</span><span class="sxs-lookup"><span data-stu-id="85455-135">Inherited properties are opaque.</span></span>  <span data-ttu-id="85455-136">Установите флажок **Показать все** , чтобы увидеть все унаследованные значения.</span><span class="sxs-lookup"><span data-stu-id="85455-136">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-137">На приведенном ниже рисунке показана **Вычисляемая** вкладка, на которой ПОКАЗАНЫ свойства CSS, применяемые к текущему `h1` элементу.</span><span class="sxs-lookup"><span data-stu-id="85455-137">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Вычисляемая вкладка" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="85455-139">**Вычисляемая** вкладка</span><span class="sxs-lookup"><span data-stu-id="85455-139">The **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="85455-140">Просмотр свойств CSS в алфавитном порядке</span><span class="sxs-lookup"><span data-stu-id="85455-140">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="85455-141">Используйте **вычисляемую** вкладку.  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-141">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="85455-142">Просмотр унаследованных свойств CSS</span><span class="sxs-lookup"><span data-stu-id="85455-142">View inherited CSS properties</span></span>  

<span data-ttu-id="85455-143">Установите флажок **Показать все** на вкладке **вычисляемый** .  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-143">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="85455-144">Просмотр модели Box для элемента</span><span class="sxs-lookup"><span data-stu-id="85455-144">View the box model for an element</span></span>  

<span data-ttu-id="85455-145">Чтобы просмотреть [модель Box][MDNBoxModel] элемента, перейдите на вкладку **стили** .  Если окно DevTools узким, схема **модель Box** находится в нижней части вкладки.</span><span class="sxs-lookup"><span data-stu-id="85455-145">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="85455-146">Выберите и измените значение, чтобы изменить значение.</span><span class="sxs-lookup"><span data-stu-id="85455-146">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-147">На рисунке ниже показана модель Box на вкладке " **стили** " в **поле** "модель" для элемента, выбранного в данный момент `h1` .</span><span class="sxs-lookup"><span data-stu-id="85455-147">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Схема модели Box" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="85455-149">Схема **модели Box**</span><span class="sxs-lookup"><span data-stu-id="85455-149">The **Box Model** diagram</span></span>  
:::image-end:::  

### <span data-ttu-id="85455-150">Поиск и фильтрация CSS элемента</span><span class="sxs-lookup"><span data-stu-id="85455-150">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="85455-151">С помощью текстового поля **Фильтр** на вкладках **стили** и **вычисляемые** вкладки можно искать определенные свойства или значения CSS.</span><span class="sxs-lookup"><span data-stu-id="85455-151">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="85455-152">Чтобы также искать унаследованные свойства на вкладке **вычисляемые** , установите флажок **Показать все** .</span><span class="sxs-lookup"><span data-stu-id="85455-152">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-153">На приведенном ниже рисунке для вкладки **стили** отображаются только правила, включающие поисковый запрос `color` .</span><span class="sxs-lookup"><span data-stu-id="85455-153">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Фильтрация вкладки "стили"" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="85455-155">Фильтрация вкладки " **стили** "</span><span class="sxs-lookup"><span data-stu-id="85455-155">Filter the **Styles** tab</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="85455-156">На приведенном ниже рисунке отфильтрованная **вкладка** фильтруется так, чтобы отображались только объявления, включающие поисковый запрос `100%` .</span><span class="sxs-lookup"><span data-stu-id="85455-156">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Фильтрация вычисляемой вкладки" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="85455-158">Фильтрация **вычисляемой** вкладки</span><span class="sxs-lookup"><span data-stu-id="85455-158">Filter the **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="85455-159">Переключение на псевдо-класс</span><span class="sxs-lookup"><span data-stu-id="85455-159">Toggle a pseudo-class</span></span>  

<span data-ttu-id="85455-160">Выполните указанные ниже действия, чтобы переключить псевдо-класс, например,, `:active` `:focus` `:hover` или `:visited` .</span><span class="sxs-lookup"><span data-stu-id="85455-160">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="85455-161">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-161">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="85455-162">На панели " **элементы** " перейдите на вкладку " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="85455-162">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="85455-163">Выберите **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="85455-163">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="85455-164">Проверьте псевдо-класс, который вы хотите включить.</span><span class="sxs-lookup"><span data-stu-id="85455-164">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-165">На рисунке ниже показано, как переключается `:hover` псевдо-класс.</span><span class="sxs-lookup"><span data-stu-id="85455-165">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="85455-166">В окне просмотра убедитесь в том, что `background-color: cornflowerblue` объявление применяется к элементу, несмотря на то что элемент фактически не наведен на указатель.</span><span class="sxs-lookup"><span data-stu-id="85455-166">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Переключение: псевдо-класс для наведения" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="85455-168">Переключение `:hover` псевдо-класса</span><span class="sxs-lookup"><span data-stu-id="85455-168">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="85455-169">Интерактивные учебники можно найти в разделе [Добавление PseudoState в класс][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="85455-169">For an interactive tutorial, see [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <span data-ttu-id="85455-170">Просмотр страницы в режиме печати</span><span class="sxs-lookup"><span data-stu-id="85455-170">View a page in print mode</span></span>  

<span data-ttu-id="85455-171">Выполните указанные ниже действия, чтобы просмотреть страницу в режиме печати.</span><span class="sxs-lookup"><span data-stu-id="85455-171">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="85455-172">[Открытие меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="85455-172">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="85455-173">Начните вводить текст `Rendering` и выберите его `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="85455-173">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="85455-174">В раскрывающемся списке **Эмуляция мультимедиа в CSS** нажмите кнопку **Печать**.</span><span class="sxs-lookup"><span data-stu-id="85455-174">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="85455-175">Просмотр использованной и неиспользуемой CSS с помощью вкладки "покрытие"</span><span class="sxs-lookup"><span data-stu-id="85455-175">View used and unused CSS with the Coverage tab</span></span>  

<span data-ttu-id="85455-176">На вкладке Coverage показано, какая страница CSS используется в действительности.</span><span class="sxs-lookup"><span data-stu-id="85455-176">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="85455-177">Выберите `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), когда DevTools находится в фокусе, чтобы [Открыть меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="85455-177">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="85455-178">Начните вводить текст `coverage` и выберите **Показать покрытие**.</span><span class="sxs-lookup"><span data-stu-id="85455-178">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="85455-179">Откроется вкладка покрытие.</span><span class="sxs-lookup"><span data-stu-id="85455-179">The Coverage tab appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Открытие вкладки "покрытие" в меню команд" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="85455-181">Открытие вкладки " **покрытие** " в **меню команд**</span><span class="sxs-lookup"><span data-stu-id="85455-181">Open the **Coverage** tab from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Вкладка "покрытие"" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="85455-183">Вкладка " **покрытие** "</span><span class="sxs-lookup"><span data-stu-id="85455-183">The **Coverage** tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="85455-184">Нажмите кнопку **начать покрытие инструментирования и обновите страницу** \ ( ![ Запуск инструментированного покрытия и обновление страницы ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="85455-184">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="85455-185">Обновленная страница и вкладка Coverage предоставляют общие сведения о том, сколько стилей CSS и JavaScript используется для каждого файла, загружаемого браузером.</span><span class="sxs-lookup"><span data-stu-id="85455-185">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="85455-186">Зеленый представляет используемые CSS.</span><span class="sxs-lookup"><span data-stu-id="85455-186">Green represents used CSS.</span></span>  <span data-ttu-id="85455-187">Красный — неиспользуемый CSS.</span><span class="sxs-lookup"><span data-stu-id="85455-187">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Общие сведения о том, какая таблица CSS (и JavaScript) используется и неиспользуемая" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="85455-189">Общие сведения о том, сколько каскадных таблиц (и JavaScript \) использует и не используется</span><span class="sxs-lookup"><span data-stu-id="85455-189">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="85455-190">Выберите CSS-файл, чтобы просмотреть разбиение по строкам для используемого CSS.</span><span class="sxs-lookup"><span data-stu-id="85455-190">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="85455-191">На приведенном ниже рисунке строки 145 в 147 и 149 в 151 из `b66bc881.site-ltr.css` не используются, в то время как используются строки 163 — 166.</span><span class="sxs-lookup"><span data-stu-id="85455-191">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Разбиение по строкам для используемых и неиспользуемых CSS" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="85455-193">Разбиение по строкам для используемых и неиспользуемых CSS</span><span class="sxs-lookup"><span data-stu-id="85455-193">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="85455-194">Принудительная печать в режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="85455-194">Force print preview mode</span></span>  

<span data-ttu-id="85455-195">Просмотрите [DevTools в режиме предварительного просмотра][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="85455-195">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="85455-196">Изменение CSS</span><span class="sxs-lookup"><span data-stu-id="85455-196">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="85455-197">Добавление объявления CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="85455-197">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="85455-198">Порядок объявлений влияет на стиль элемента с помощью приведенного ниже списка, который поможет вам добавлять объявления различными способами.</span><span class="sxs-lookup"><span data-stu-id="85455-198">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="85455-199">[Добавление встроенного объявления](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="85455-199">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="85455-200">Эквивалентно добавлению `style` атрибута в HTML элемента.</span><span class="sxs-lookup"><span data-stu-id="85455-200">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="85455-201">[Добавление объявления в правило стиля](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="85455-201">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="85455-202">Какой рабочий процесс следует использовать?</span><span class="sxs-lookup"><span data-stu-id="85455-202">What workflow should you use?</span></span>** <span data-ttu-id="85455-203">В большинстве сценариев вы, возможно, захотите использовать рабочий процесс объявления на встроенных элементах.</span><span class="sxs-lookup"><span data-stu-id="85455-203">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="85455-204">Встроенные объявления имеют более высокие особенности, чем внешние, поэтому встроенный рабочий процесс гарантирует, что изменения вступают в силу в ожидаемом элементе.</span><span class="sxs-lookup"><span data-stu-id="85455-204">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="85455-205">Дополнительные сведения о конкретных особенностях можно найти в разделе [типы селекторов][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="85455-205">For more information about specificity, see [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="85455-206">Если при отладке любого стиля элемента требуется специально проверить, что происходит, если объявление определено в разных местах, используйте другой рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="85455-206">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="85455-207">Добавление встроенного объявления</span><span class="sxs-lookup"><span data-stu-id="85455-207">Add an inline declaration</span></span>  

<span data-ttu-id="85455-208">Чтобы добавить встроенное объявление, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="85455-208">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="85455-209">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-209">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="85455-210">В области **стили** выберите между скобками раздела **element. Style** .</span><span class="sxs-lookup"><span data-stu-id="85455-210">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="85455-211">Курсор фокусируется на том, что позволяет вводить текст.</span><span class="sxs-lookup"><span data-stu-id="85455-211">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="85455-212">Введите имя свойства и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="85455-212">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="85455-213">Введите допустимое значение для этого свойства и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="85455-213">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="85455-214">Убедитесь, что в **дереве DOM** `style` к элементу добавлен атрибут.</span><span class="sxs-lookup"><span data-stu-id="85455-214">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-215">На приведенном ниже рисунке к `margin-top` `background-color` выбранному элементу применены свойства и.</span><span class="sxs-lookup"><span data-stu-id="85455-215">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="85455-216">В **дереве DOM** убедитесь, что объявления отражены в `style` атрибуте для элемента.</span><span class="sxs-lookup"><span data-stu-id="85455-216">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Добавление встроенных объявлений" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="85455-218">Добавление встроенных объявлений</span><span class="sxs-lookup"><span data-stu-id="85455-218">Add inline declarations</span></span>  
:::image-end:::  

#### <span data-ttu-id="85455-219">Добавление объявления в правило стиля</span><span class="sxs-lookup"><span data-stu-id="85455-219">Add a declaration to a style rule</span></span>  

<span data-ttu-id="85455-220">Чтобы добавить объявление к существующему правилу стиля, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="85455-220">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="85455-221">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-221">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="85455-222">В области **стили** выберите один из квадратных скобок правила стиля, к которому вы хотите добавить объявление.</span><span class="sxs-lookup"><span data-stu-id="85455-222">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="85455-223">Курсор фокусируется на том, что позволяет вводить текст.</span><span class="sxs-lookup"><span data-stu-id="85455-223">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="85455-224">Введите имя свойства и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="85455-224">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="85455-225">Введите допустимое значение для этого свойства и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="85455-225">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Добавление объявления в правило стиля" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="85455-227">Добавление `border-bottom-style:groove` объявления в правило стиля</span><span class="sxs-lookup"><span data-stu-id="85455-227">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <span data-ttu-id="85455-228">Изменение имени или значения объявления</span><span class="sxs-lookup"><span data-stu-id="85455-228">Change a declaration name or value</span></span>  

<span data-ttu-id="85455-229">Выберите и измените имя или значение объявления, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="85455-229">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="85455-230">Сочетания клавиш для быстрого увеличения или уменьшения значения (, или единиц) можно найти [в статье изменение значений объявлений](#change-declaration-values-with-keyboard-shortcuts) `0.1` `1` `10` `100` .</span><span class="sxs-lookup"><span data-stu-id="85455-230">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Изменение значения объявления" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="85455-232">Изменение значения `border-bottom-style` объявления</span><span class="sxs-lookup"><span data-stu-id="85455-232">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="85455-233">Изменение значений объявлений с помощью сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="85455-233">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="85455-234">При редактировании значения объявления вы можете использовать следующие сочетания клавиш, чтобы увеличить значение на определенную величину.</span><span class="sxs-lookup"><span data-stu-id="85455-234">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="85455-235">Выберите `Alt` + `Up` \ (Windows \) или `Option` + `Up` \ (macOS \), чтобы увеличить его `0.1` .</span><span class="sxs-lookup"><span data-stu-id="85455-235">Select `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="85455-236">Выберите `Up` , чтобы изменить значение `1` , или, `0.1` Если текущее значение находится в диапазоне от `-1` и до `1` .</span><span class="sxs-lookup"><span data-stu-id="85455-236">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="85455-237">Выберите, `Shift` + `Up` чтобы увеличить `10` .</span><span class="sxs-lookup"><span data-stu-id="85455-237">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="85455-238">Выберите `Shift` + `Page Up` \ (Windows \) или `Shift` + `Command` + `Up` \ (macOS \), чтобы увеличить значение `100` .</span><span class="sxs-lookup"><span data-stu-id="85455-238">Select `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="85455-239">Кроме того, выполняется уменьшение.</span><span class="sxs-lookup"><span data-stu-id="85455-239">Decrementing also works.</span></span>  <span data-ttu-id="85455-240">Просто замените каждый из `Up` упомянутых выше экземпляров `Down` .</span><span class="sxs-lookup"><span data-stu-id="85455-240">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="85455-241">Добавление класса в элемент</span><span class="sxs-lookup"><span data-stu-id="85455-241">Add a class to an element</span></span>  

<span data-ttu-id="85455-242">Чтобы добавить класс в элемент, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="85455-242">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="85455-243">[Выберите элемент](#select-an-element) в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="85455-243">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="85455-244">Выберите **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="85455-244">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="85455-245">Введите имя класса в текстовом поле **Добавить новый класс** .</span><span class="sxs-lookup"><span data-stu-id="85455-245">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="85455-246">Выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="85455-246">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Область «классы элементов»" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="85455-248">Область « **классы элементов** »</span><span class="sxs-lookup"><span data-stu-id="85455-248">The **Element Classes** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="85455-249">Переключение класса</span><span class="sxs-lookup"><span data-stu-id="85455-249">Toggle a class</span></span>  

<span data-ttu-id="85455-250">Выполните указанные ниже действия, чтобы включить или отключить класс для элемента.</span><span class="sxs-lookup"><span data-stu-id="85455-250">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="85455-251">[Выберите элемент](#select-an-element) в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="85455-251">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="85455-252">Откройте область **классы элементов** .</span><span class="sxs-lookup"><span data-stu-id="85455-252">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="85455-253">Дополнительные сведения о том, [как добавить класс в элемент](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-253">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="85455-254">Под текстовым полем **Добавить новый класс** находятся все классы, которые применяются к определенному элементу.</span><span class="sxs-lookup"><span data-stu-id="85455-254">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span></span>  
1.  <span data-ttu-id="85455-255">Установите флажок рядом с классом, который вы хотите включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="85455-255">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="85455-256">Добавление правила стиля</span><span class="sxs-lookup"><span data-stu-id="85455-256">Add a style rule</span></span>  

<span data-ttu-id="85455-257">Чтобы добавить новое правило стиля, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="85455-257">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="85455-258">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-258">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="85455-259">Нажмите **новое правило стиля** \ ( ![ новое правило стиля ][ImageNewStyleRuleIcon] ).</span><span class="sxs-lookup"><span data-stu-id="85455-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="85455-260">DevTools вставляет новое правило под правилом **element. Style** .</span><span class="sxs-lookup"><span data-stu-id="85455-260">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-261">На приведенном ниже рисунке DevTools добавляет `h1.devsite-page-title` правило стиля после выбора **нового правила стиля**.</span><span class="sxs-lookup"><span data-stu-id="85455-261">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Добавление нового правила стиля" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="85455-263">Добавление нового правила стиля</span><span class="sxs-lookup"><span data-stu-id="85455-263">Add a new style rule</span></span>  
:::image-end:::  

#### <span data-ttu-id="85455-264">Выберите таблицу стилей, к которой нужно добавить правило.</span><span class="sxs-lookup"><span data-stu-id="85455-264">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="85455-265">При [добавлении нового правила стиля](#add-a-style-rule)нажмите и удерживайте **новое правило** стиля \ ( ![ новое правило стиля), ][ImageNewStyleRuleIcon] чтобы выбрать таблицу стилей, к которой нужно добавить правило.</span><span class="sxs-lookup"><span data-stu-id="85455-265">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Выбор таблицы стилей" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="85455-267">Выбор таблицы стилей</span><span class="sxs-lookup"><span data-stu-id="85455-267">Choose a stylesheet</span></span>  
:::image-end:::  

#### <span data-ttu-id="85455-268">Добавление правила стиля в определенное место</span><span class="sxs-lookup"><span data-stu-id="85455-268">Add a style rule to a specific location</span></span>  

<span data-ttu-id="85455-269">Выполните указанные ниже действия, чтобы добавить правило стиля в конкретное расположение на вкладке " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="85455-269">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span></span>  

1.  <span data-ttu-id="85455-270">Наведите указатель мыши на правило стиля, которое находится в том месте, куда вы хотите добавить новое правило стиля.</span><span class="sxs-lookup"><span data-stu-id="85455-270">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="85455-271">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="85455-271">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="85455-272">Нажмите кнопку **Вставить правило стиля ниже** \ ( ![ Вставить правило стиля ниже ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="85455-272">Choose **Insert Style Rule Below** \(![Insert Style Rule Below][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Вставить правило стиля ниже" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="85455-274">Вставить правило стиля ниже</span><span class="sxs-lookup"><span data-stu-id="85455-274">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <span data-ttu-id="85455-275">Панель инструментов "другие действия"</span><span class="sxs-lookup"><span data-stu-id="85455-275">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="85455-276">На панели инструментов " **другие действия** " можно выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="85455-276">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="85455-277">Вставка правила стиля прямо ниже того, на котором вы отправили фокус.</span><span class="sxs-lookup"><span data-stu-id="85455-277">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="85455-278">Добавьте в `background-color` `color` `box-shadow` правило стиля, которое `text-shadow` вы хотите включить, или объявление.</span><span class="sxs-lookup"><span data-stu-id="85455-278">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="85455-279">Выполните указанные ниже действия, чтобы открыть панель инструментов **Дополнительные действия** .</span><span class="sxs-lookup"><span data-stu-id="85455-279">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="85455-280">На вкладке **стили** наведите указатель мыши на правило стиля.</span><span class="sxs-lookup"><span data-stu-id="85455-280">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="85455-281">**Дополнительные действия** \ ( `...` \) находятся в правом нижнем углу раздела "правило стиля".</span><span class="sxs-lookup"><span data-stu-id="85455-281">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="85455-282">На приведенном ниже рисунке наведите указатель мыши на `.header-holder.has-default-focus` правило стиля и **другие действия** будут отображены в правом нижнем углу раздела "правило стиля".</span><span class="sxs-lookup"><span data-stu-id="85455-282">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Показать дополнительные действия" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="85455-284">Показать **Дополнительные действия** \ ( `...` \)</span><span class="sxs-lookup"><span data-stu-id="85455-284">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="85455-285">Наведите указатель мыши на элемент **Дополнительные действия** , `...` чтобы отобразить указанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="85455-285">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="85455-286">**Правило стиля вставки, показанное ниже** , выводится при наведении указателя мыши на **другие действия**.</span><span class="sxs-lookup"><span data-stu-id="85455-286">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Панель инструментов «другие действия»" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="85455-288">Панель инструментов « **другие действия** »</span><span class="sxs-lookup"><span data-stu-id="85455-288">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="85455-289">Переключить объявление</span><span class="sxs-lookup"><span data-stu-id="85455-289">Toggle a declaration</span></span>  

<span data-ttu-id="85455-290">Выполните действия folllwoing, чтобы переключить одно объявление на \ (или выключить).</span><span class="sxs-lookup"><span data-stu-id="85455-290">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="85455-291">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-291">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="85455-292">В области **стили** наведите указатель мыши на правило, которое определяет объявление.</span><span class="sxs-lookup"><span data-stu-id="85455-292">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="85455-293">Рядом с каждым объявлением появится флажок.</span><span class="sxs-lookup"><span data-stu-id="85455-293">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="85455-294">Установите флажок \ (или снимите) флажок рядом с объявлением.</span><span class="sxs-lookup"><span data-stu-id="85455-294">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="85455-295">Если вы снимите флажок объявления, DevTools пересекает его, чтобы показать, что он больше не активен.</span><span class="sxs-lookup"><span data-stu-id="85455-295">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="85455-296">На приведенном ниже рисунке `margin-top` свойство для выбранного в данный момент элемента было отключено.</span><span class="sxs-lookup"><span data-stu-id="85455-296">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Переключить объявление" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="85455-298">Переключить объявление</span><span class="sxs-lookup"><span data-stu-id="85455-298">Toggle a declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="85455-299">Добавление объявления цвета фона</span><span class="sxs-lookup"><span data-stu-id="85455-299">Add a background-color declaration</span></span>  

<span data-ttu-id="85455-300">Выполните указанные ниже действия, чтобы добавить `background-color` объявление к элементу.</span><span class="sxs-lookup"><span data-stu-id="85455-300">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="85455-301">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `background-color` объявление.</span><span class="sxs-lookup"><span data-stu-id="85455-301">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="85455-302">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="85455-302">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="85455-303">Выберите команду **добавить цвет фона** \ ( ![ добавить цвет фона ][ImageAddBackgroundColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="85455-303">Choose **Add Background Color** \(![Add Background Color][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Добавление цвета фона" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="85455-305">Добавление цвета фона</span><span class="sxs-lookup"><span data-stu-id="85455-305">Add Background Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="85455-306">Добавление объявления цвета</span><span class="sxs-lookup"><span data-stu-id="85455-306">Add a color declaration</span></span>  

<span data-ttu-id="85455-307">Выполните указанные ниже действия, чтобы добавить `color` объявление к элементу.</span><span class="sxs-lookup"><span data-stu-id="85455-307">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="85455-308">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `color` объявление.</span><span class="sxs-lookup"><span data-stu-id="85455-308">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="85455-309">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="85455-309">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="85455-310">Нажмите кнопку **добавить цвет** \ ( ![ добавить цвет ][ImageAddColorIcon] ).</span><span class="sxs-lookup"><span data-stu-id="85455-310">Choose **Add Color** \(![Add Color][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Добавить цвет" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="85455-312">Добавить цвет</span><span class="sxs-lookup"><span data-stu-id="85455-312">Add Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="85455-313">Добавление объявления с помощью блочной тени</span><span class="sxs-lookup"><span data-stu-id="85455-313">Add a box-shadow declaration</span></span>  

<span data-ttu-id="85455-314">Выполните указанные ниже действия, чтобы добавить `box-shadow` объявление к элементу.</span><span class="sxs-lookup"><span data-stu-id="85455-314">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="85455-315">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `box-shadow` объявление.</span><span class="sxs-lookup"><span data-stu-id="85455-315">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="85455-316">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="85455-316">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="85455-317">Нажмите кнопку **Добавить тень поля** \ ( ![ Добавить тень рамки ][ImageAddBoxShadowIcon] ).</span><span class="sxs-lookup"><span data-stu-id="85455-317">Choose **Add Box Shadow** \(![Add Box Shadow][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Добавление тени для поля" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="85455-319">Добавление тени для поля</span><span class="sxs-lookup"><span data-stu-id="85455-319">Add Box Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="85455-320">Добавление объявления тени для текста</span><span class="sxs-lookup"><span data-stu-id="85455-320">Add a text-shadow declaration</span></span>  

<span data-ttu-id="85455-321">Выполните указанные ниже действия, чтобы добавить `text-shadow` объявление к элементу.</span><span class="sxs-lookup"><span data-stu-id="85455-321">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="85455-322">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `text-shadow` объявление.</span><span class="sxs-lookup"><span data-stu-id="85455-322">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="85455-323">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="85455-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="85455-324">Нажмите кнопку **Добавить тень текста** \ ( ![ Добавить тень текста ][ImageAddTextShadowIcon] \).</span><span class="sxs-lookup"><span data-stu-id="85455-324">Choose **Add Text Shadow** \(![Add Text Shadow][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Добавление тени текста" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="85455-326">Добавление тени текста</span><span class="sxs-lookup"><span data-stu-id="85455-326">Add Text Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="85455-327">Изменение цвета с помощью палитры цветов</span><span class="sxs-lookup"><span data-stu-id="85455-327">Change colors with the Color Picker</span></span>  

<span data-ttu-id="85455-328">В **средстве выбора цвета** есть графический интерфейс для изменения `color` и `background-color` объявлений.</span><span class="sxs-lookup"><span data-stu-id="85455-328">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="85455-329">Выполните указанные ниже действия, чтобы открыть окно **выбора цвета**.</span><span class="sxs-lookup"><span data-stu-id="85455-329">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="85455-330">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="85455-330">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="85455-331">На вкладке **стили** найдите и щелкните то `color` `background-color` же объявление, которое вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="85455-331">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="85455-332">Слева от "," `color` `background-color` или аналогичного значения есть маленький квадрат, который является предварительным просмотром цвета.</span><span class="sxs-lookup"><span data-stu-id="85455-332">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="85455-333">На приведенном ниже рисунке небольшой квадрат слева от него `rgba(0, 0, 0, 0.7)` является предварительным просмотром этого цвета.</span><span class="sxs-lookup"><span data-stu-id="85455-333">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Цвет предварительного просмотра" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="85455-335">Цвет предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="85455-335">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="85455-336">Нажмите кнопку Предварительный просмотр, чтобы открыть окно **выбора цвета**.</span><span class="sxs-lookup"><span data-stu-id="85455-336">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Выбор цвета" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="85455-338">**Выбор цвета**</span><span class="sxs-lookup"><span data-stu-id="85455-338">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="85455-339">На приведенном ниже рисунке и списке описывает каждого элемента пользовательского интерфейса в **палитре цветов**.</span><span class="sxs-lookup"><span data-stu-id="85455-339">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Палитра цветов с заметками" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="85455-341">**Палитра цветов**с заметками</span><span class="sxs-lookup"><span data-stu-id="85455-341">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-342">1,1</span><span class="sxs-lookup"><span data-stu-id="85455-342">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-343">Оттенки</span><span class="sxs-lookup"><span data-stu-id="85455-343">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-344">2</span><span class="sxs-lookup"><span data-stu-id="85455-344">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-345">Выбрав</span><span class="sxs-lookup"><span data-stu-id="85455-345">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85455-346">Дополнительные сведения можно найти в разделе [Выбор цвета на странице с помощью пипетки](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="85455-346">For more information, see [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-347">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="85455-347">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-348">Копировать в буфер</span><span class="sxs-lookup"><span data-stu-id="85455-348">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85455-349">Скопируйте **Отображаемое значение** в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="85455-349">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-350">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="85455-350">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-351">Отображаемое значение</span><span class="sxs-lookup"><span data-stu-id="85455-351">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85455-352">Представление RGBA, HSLA или шестнадцатеричного представления цвета.</span><span class="sxs-lookup"><span data-stu-id="85455-352">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-353">5</span><span class="sxs-lookup"><span data-stu-id="85455-353">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-354">Цветовая палитра</span><span class="sxs-lookup"><span data-stu-id="85455-354">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85455-355">Выберите один из квадратов, чтобы изменить цвет на этот квадрат.</span><span class="sxs-lookup"><span data-stu-id="85455-355">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-356">152</span><span class="sxs-lookup"><span data-stu-id="85455-356">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-357">Отношения</span><span class="sxs-lookup"><span data-stu-id="85455-357">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-358">5-7</span><span class="sxs-lookup"><span data-stu-id="85455-358">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-359">Opacity (Прозрачность)</span><span class="sxs-lookup"><span data-stu-id="85455-359">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-360">No8</span><span class="sxs-lookup"><span data-stu-id="85455-360">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-361">Переключатель отображения значений</span><span class="sxs-lookup"><span data-stu-id="85455-361">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85455-362">Переключение между представлениями "RGBA", "HSLA" и "шестнадцатеричный" текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="85455-362">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="85455-363">@</span><span class="sxs-lookup"><span data-stu-id="85455-363">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="85455-364">Переключатель цветовой палитры</span><span class="sxs-lookup"><span data-stu-id="85455-364">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85455-365">Переключение между [палитрой «дизайн материала][MaterialDesignColorSystem]», настраиваемой палитрой или палитрой цветов страницы.</span><span class="sxs-lookup"><span data-stu-id="85455-365">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="85455-366">DevTools создает цветовую палитру страницы на основе цветов, найденных в стилях.</span><span class="sxs-lookup"><span data-stu-id="85455-366">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="85455-367">Выбор цвета на странице с помощью пипетки</span><span class="sxs-lookup"><span data-stu-id="85455-367">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="85455-368">Когда вы откроете окно **выбора цвета**, по умолчанию будет включена **Пипетка** \ ( ![ Пипетка ][ImageEyedropperIcon] \).</span><span class="sxs-lookup"><span data-stu-id="85455-368">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="85455-369">Чтобы изменить выбранный цвет на другой цвет на странице, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="85455-369">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="85455-370">Наведите указатель мыши на целевой цвет в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="85455-370">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="85455-371">Нажмите кнопку подтвердить.</span><span class="sxs-lookup"><span data-stu-id="85455-371">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="85455-372">На приведенном ниже рисунке в **средстве выбора цвета** отображается текущее цветное значение `rgba(0,0,0,0.7)` , которое близко к черному.</span><span class="sxs-lookup"><span data-stu-id="85455-372">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="85455-373">Определенный цвет должен измениться на черную версию, которая выделена в окне просмотра, после того как вы выберете его.</span><span class="sxs-lookup"><span data-stu-id="85455-373">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Использование пипетки" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="85455-375">Использование пипетки</span><span class="sxs-lookup"><span data-stu-id="85455-375">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Добавление PseudoState в класс — начало работы с просмотром и изменением CSS | Документы Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Просмотр CSS для элемента — начало работы с просмотром и изменением CSS | Документы Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS) | Документы Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Создание доступного для чтения файла minified — Справка по отладке JavaScript | Документы Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Макет "Цветовая система-материал""  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Модель Box | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Типы выбора — "конкретное |" MDN"  

> [!NOTE]
> <span data-ttu-id="85455-385">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="85455-385">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="85455-386">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="85455-386">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="85455-388">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="85455-388">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

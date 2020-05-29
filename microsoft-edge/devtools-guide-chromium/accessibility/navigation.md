---
title: Навигация в Microsoft Edge DevTools с помощью специальных возможностей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 5de27e46d20957a1be79f72cf36074291566e6e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571179"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="04b21-103">Навигация в Microsoft Edge DevTools с помощью специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="04b21-103">Navigate Microsoft Edge DevTools With Assistive Technology</span></span>   



<span data-ttu-id="04b21-104">Это руководство помогает пользователям, которые в первую очередь используют специальные возможности, такие как средства чтения с экрана, доступ и использование Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="04b21-104">This guide aims to help users who primarily rely on assistive technology like screen readers access and use Microsoft Edge DevTools.</span></span>  <span data-ttu-id="04b21-105">Microsoft Edge DevTools — это набор средств для веб-разработчиков, встроенных в браузер Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="04b21-105">Microsoft Edge DevTools is a suite of web developer tools built into the Microsoft Edge browser.</span></span>  <!--See [Accessibility Reference][DevtoolsAccessibilityReference] if you are looking for DevTools features related to improving the accessibility of a web page.  -->

<!--todo: add edge devtools index section when available  -->  
<!--todo: add reference (Accessibility Reference) section when available  -->  

<span data-ttu-id="04b21-106">Доступность DevTools — это незавершенная работа.</span><span class="sxs-lookup"><span data-stu-id="04b21-106">The accessibility of DevTools is a work-in-progress.</span></span>  <span data-ttu-id="04b21-107">На некоторых панелях и вкладках удобнее использовать специальные возможности, чем другие.</span><span class="sxs-lookup"><span data-stu-id="04b21-107">Some panels and tabs work better with assistive technology than others.</span></span>  <span data-ttu-id="04b21-108">Это руководство поможет вам просмотреть все доступные и важные проблемы, которые могут возникнуть в ходе работы.</span><span class="sxs-lookup"><span data-stu-id="04b21-108">This guide walks you through the panels which are the most accessible and highlights specific issues you may encounter along the way.</span></span>  

## <span data-ttu-id="04b21-109">Обзор</span><span class="sxs-lookup"><span data-stu-id="04b21-109">Overview</span></span>   

<span data-ttu-id="04b21-110">Перед началом работы он может использовать оценку DevTools пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="04b21-110">Before starting, it helps to have a mental model of how the DevTools UI is structured.</span></span>  <span data-ttu-id="04b21-111">DevTools делится на ряд панелей, организованных в [ARIA `tablist` ][W3CWaiAriaTablist].</span><span class="sxs-lookup"><span data-stu-id="04b21-111">DevTools is divided into a series of panels which are organized into an [ARIA `tablist`][W3CWaiAriaTablist].</span></span>  

<span data-ttu-id="04b21-112">Пример</span><span class="sxs-lookup"><span data-stu-id="04b21-112">For example:</span></span>  

*   <span data-ttu-id="04b21-113">С помощью панели **элементы** вы можете просматривать и изменять узлы DOM или [CSS] [DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="04b21-113">The **Elements** panel lets you view and change DOM nodes or [CSS][DevtoolsCssIndex].</span></span>  
*   <span data-ttu-id="04b21-114">[Панель**консоли** ] [DevtoolsConsoleIndex] позволяет читать журналы JavaScript и объекты Live Edit.</span><span class="sxs-lookup"><span data-stu-id="04b21-114">The [**Console** panel][DevtoolsConsoleIndex] lets you read JavaScript logs and live edit objects.</span></span>  

<!--todo:  add dom nodes (dom nodes) section when available  -->  

<span data-ttu-id="04b21-115">В области содержимого каждой панели находятся различные инструменты, часто называемые вкладками и областями в документации.</span><span class="sxs-lookup"><span data-stu-id="04b21-115">Within the content area of each panel, there are a number of different tools, often referred to as tabs or panes in the documentation.</span></span>  
<span data-ttu-id="04b21-116">Например, на панели **элементы** содержатся дополнительные вкладки для проверки прослушивателей событий, дерева специальных возможностей и многого другого.</span><span class="sxs-lookup"><span data-stu-id="04b21-116">For instance, the **Elements** panel contains additional tabs to inspect event listeners, the accessibility tree, and much more.</span></span>  <span data-ttu-id="04b21-117">Различие между вкладками и областями является несколько произвольным.</span><span class="sxs-lookup"><span data-stu-id="04b21-117">The distinction between tabs and panes is somewhat arbitrary.</span></span>  <span data-ttu-id="04b21-118">Единственная причина, по которой вы можете увидеть один термин, или другую — для обеспечения единообразия с помощью оставшейся части официального DevToolsной документации.</span><span class="sxs-lookup"><span data-stu-id="04b21-118">The only reason you may see one term or the other is to maintain consistency with the rest of the official DevTools documentation.</span></span>  

## <span data-ttu-id="04b21-119">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="04b21-119">Keyboard shortcuts</span></span>   

<span data-ttu-id="04b21-120">[DevTools сочетаний клавиш] [DevtoolsShortcuts] является полезным cheatsheet.</span><span class="sxs-lookup"><span data-stu-id="04b21-120">The [DevTools Keyboard Shortcuts reference][DevtoolsShortcuts] is a helpful cheatsheet.</span></span>  <span data-ttu-id="04b21-121">Запусти закладку и обратись к ней по мере того, как вы изучите различные панели.</span><span class="sxs-lookup"><span data-stu-id="04b21-121">Be sure to bookmark it and refer back to it as you explore the different panels.</span></span>  

## <span data-ttu-id="04b21-122">Открыть DevTools</span><span class="sxs-lookup"><span data-stu-id="04b21-122">Open DevTools</span></span>   

<span data-ttu-id="04b21-123">Чтобы приступить к работе, ознакомьтесь с разделом [открыть Microsoft Edge DevTools] [DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="04b21-123">To get started, read through [Open Microsoft Edge DevTools][DevtoolsOpen].</span></span>  <span data-ttu-id="04b21-124">Открыть DevTools можно несколькими способами с помощью сочетаний клавиш или элементов меню.</span><span class="sxs-lookup"><span data-stu-id="04b21-124">There are a number of ways to open DevTools, either through keyboard shortcuts or menu items.</span></span>  

## <span data-ttu-id="04b21-125">Переход между панелями</span><span class="sxs-lookup"><span data-stu-id="04b21-125">Navigate between panels</span></span>   

### <span data-ttu-id="04b21-126">Навигация с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="04b21-126">Navigate by keyboard</span></span>   

*   <span data-ttu-id="04b21-127">После открытия DevTools нажмите клавиши `Control` + `]` \ (Windows \) или `Command` + `]` \ (macOS \), чтобы сосредоточиться на следующей панели.</span><span class="sxs-lookup"><span data-stu-id="04b21-127">With DevTools open, press `Control`+`]` \(Windows\) or `Command`+`]` \(macOS\) to focus the next panel.</span></span>  
*   <span data-ttu-id="04b21-128">Нажмите клавиши `Control` + `[` \ (Windows \) или `Command` + `[` \ (macOS \), чтобы сосредоточиться на предыдущей панели.</span><span class="sxs-lookup"><span data-stu-id="04b21-128">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) to focus the previous panel.</span></span>  
*   <span data-ttu-id="04b21-129">Кроме того, с помощью `Shift` + `Tab` клавиш со стрелками вы можете переместить фокус на объект [ `tablist` ARIA][W3CWaiAriaTablist] панели и использовать для изменения палитры.</span><span class="sxs-lookup"><span data-stu-id="04b21-129">It is also possible to use `Shift`+`Tab` to move focus into the [ARIA `tablist`][W3CWaiAriaTablist] of a panel and use the arrow keys to change panels, though it may be faster to use the previously mentioned shortcuts.</span></span>  

#### <span data-ttu-id="04b21-130">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="04b21-130">Known issues</span></span>   

*   <span data-ttu-id="04b21-131">Некоторые панели, такие как **консоль** управления и панель **производительности** , могут переместить фокус в область содержимого, как только они будут активированы.</span><span class="sxs-lookup"><span data-stu-id="04b21-131">Some panels, such as the **Console** and **Performance** panels, may move focus into their content area as soon as they are activated.</span></span>  <span data-ttu-id="04b21-132">Это может усложнить навигацию по клавишам со стрелками.</span><span class="sxs-lookup"><span data-stu-id="04b21-132">This may make navigating by arrow keys difficult.</span></span>  
*   <span data-ttu-id="04b21-133">Имя выбранной панели будет объявлено, но только после того, как оно прочитало содержимое, на которое ориентирован элемент, на панели.</span><span class="sxs-lookup"><span data-stu-id="04b21-133">The name of the selected panel is announced, but only after it has read the focused content in the panel.</span></span>  <span data-ttu-id="04b21-134">Это может привести к простому пропуску.</span><span class="sxs-lookup"><span data-stu-id="04b21-134">This may make it very easy to miss.</span></span>  

### <span data-ttu-id="04b21-135">Меню команд навигации</span><span class="sxs-lookup"><span data-stu-id="04b21-135">Navigate by Command Menu</span></span>   

<span data-ttu-id="04b21-136">Чтобы сосредоточиться на определенной панели, используйте [**меню команд**] [DevtoolsCommandMenuIndex]:</span><span class="sxs-lookup"><span data-stu-id="04b21-136">To focus a specific panel, use the [**Command Menu**][DevtoolsCommandMenuIndex]:</span></span>  

1.  <span data-ttu-id="04b21-137">После открытия DevTools нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**.</span><span class="sxs-lookup"><span data-stu-id="04b21-137">With DevTools open, press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    <span data-ttu-id="04b21-138">**Меню команд** — поле со списком автозаполнения для поиска.</span><span class="sxs-lookup"><span data-stu-id="04b21-138">The **Command Menu** is a fuzzy search autocomplete combobox.</span></span>  
1.  <span data-ttu-id="04b21-139">Введите имя панели, которую вы хотите открыть, а затем выберите `Down Arrow` нужный параметр с помощью клавиши на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="04b21-139">Type the name of the panel you want to open, then use the `Down Arrow` on the keyboard to navigate to the correct option.</span></span>  
1.  <span data-ttu-id="04b21-140">Нажмите `Enter` , чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="04b21-140">Press `Enter` to run a command.</span></span>  

<span data-ttu-id="04b21-141">Например, чтобы открыть панель " **элементы** ", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="04b21-141">For example, to open the **Elements** panel:</span></span>  

1.  <span data-ttu-id="04b21-142">Открытие **меню команд**.</span><span class="sxs-lookup"><span data-stu-id="04b21-142">Open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="04b21-143">Введите `E` затем `L` .</span><span class="sxs-lookup"><span data-stu-id="04b21-143">Type `E` then `L`.</span></span>  <span data-ttu-id="04b21-144">Выбран параметр **> Показать элементы панели** .</span><span class="sxs-lookup"><span data-stu-id="04b21-144">The **Panel > Show Elements** option is selected.</span></span>  
1.  <span data-ttu-id="04b21-145">Нажмите `Enter` , чтобы запустить команду, которая открывает панель.</span><span class="sxs-lookup"><span data-stu-id="04b21-145">Press `Enter` to run the command that opens the panel.</span></span>  

<span data-ttu-id="04b21-146">Если открыть панель таким образом, она будет направлять фокус на содержимое панели.</span><span class="sxs-lookup"><span data-stu-id="04b21-146">Opening a panel this way directs focus to the contents of the panel.</span></span>  <span data-ttu-id="04b21-147">В случае панели **элементов** фокус переместится в **дерево DOM**.</span><span class="sxs-lookup"><span data-stu-id="04b21-147">In the case of the **Elements** panel, focus moves into the **DOM Tree**.</span></span>  

## <span data-ttu-id="04b21-148">Панель "элементы"</span><span class="sxs-lookup"><span data-stu-id="04b21-148">Elements panel</span></span>   

### <span data-ttu-id="04b21-149">Проверка элемента на странице</span><span class="sxs-lookup"><span data-stu-id="04b21-149">Inspect an element on the page</span></span>   

1.  <span data-ttu-id="04b21-150">Перейдите к элементу, который вы хотите проанализировать с помощью курсора в средстве чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="04b21-150">Navigate to the element you want to inspect using the cursor in the screen reader.</span></span>  
1.  <span data-ttu-id="04b21-151">Щелкните правой кнопкой мыши элемент, чтобы открыть контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="04b21-151">Simulate a right-mouse click on the element to open the context menu.</span></span>  
1.  <span data-ttu-id="04b21-152">Выберите параметр **проверки** .</span><span class="sxs-lookup"><span data-stu-id="04b21-152">Choose the **Inspect** option.</span></span>  <span data-ttu-id="04b21-153">Откроется панель " **элементы** ", в которой будет соосвещен элемент **дерева DOM**.</span><span class="sxs-lookup"><span data-stu-id="04b21-153">This opens the **Elements** panel and focuses the element in the **DOM Tree**.</span></span>  

<!--todo:  add dom nodes (elements pane) section when available  -->  

<span data-ttu-id="04b21-154">**Дерево DOM** расрасполагается как [ARIA `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="04b21-154">The **DOM Tree** is laid out as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <!--See [Navigate the **DOM Tree** with a keyboard][DevtoolsDomIndexNavigateDomTreeKeyboard] for an example.  -->  

<!--todo: add dom index navigation tree section then available  -->

### <span data-ttu-id="04b21-155">Копирование кода для элемента в дереве DOM</span><span class="sxs-lookup"><span data-stu-id="04b21-155">Copy the code for an element in the DOM Tree</span></span>   

1.  <span data-ttu-id="04b21-156">С помощью фокуса на узле в **дереве DOM**откройте контекстное меню правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="04b21-156">With focus on a node in the **DOM Tree**, bring up the right-click context menu.</span></span>  
1.  <span data-ttu-id="04b21-157">Разверните элемент " **Копировать** ".</span><span class="sxs-lookup"><span data-stu-id="04b21-157">Expand the **Copy** option.</span></span>  
1.  <span data-ttu-id="04b21-158">Нажмите кнопку **Копировать OuterHtml**.</span><span class="sxs-lookup"><span data-stu-id="04b21-158">Select **Copy outerHTML**.</span></span>  

#### <span data-ttu-id="04b21-159">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="04b21-159">Known issues</span></span>   

*   <span data-ttu-id="04b21-160">**Копирование OuterHtml** часто не выделяет текущий узел, а вместо этого выделяет родительский узел.</span><span class="sxs-lookup"><span data-stu-id="04b21-160">**Copy outerHTML** often does not select the current node but instead selects the parent node.</span></span>  <span data-ttu-id="04b21-161">Однако содержимое элемента по-прежнему должно находиться в копируемом outerHTML.</span><span class="sxs-lookup"><span data-stu-id="04b21-161">However, the contents of the element should still be in the copied outerHTML.</span></span>  

### <span data-ttu-id="04b21-162">Изменение атрибутов элемента в дереве DOM</span><span class="sxs-lookup"><span data-stu-id="04b21-162">Modify the attributes of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="04b21-163">Установив фокус на узел в **дереве DOM**, нажмите, `Enter` чтобы сделать его редактируемым.</span><span class="sxs-lookup"><span data-stu-id="04b21-163">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="04b21-164">Нажимайте клавишу `Tab` для перемещения между значениями атрибутов.</span><span class="sxs-lookup"><span data-stu-id="04b21-164">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="04b21-165">Когда вы услышите "место", в пустом текстовом вводе вы можете ввести новое значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="04b21-165">When you hear "space" you are inside of an empty text input and are able to type a new attribute value.</span></span>  
*   <span data-ttu-id="04b21-166">Нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \), чтобы сохранить изменения и прослушать все содержимое элемента.</span><span class="sxs-lookup"><span data-stu-id="04b21-166">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change and hear the entire contents of the element.</span></span>  

#### <span data-ttu-id="04b21-167">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="04b21-167">Known issues</span></span>   

*   <span data-ttu-id="04b21-168">При вводе текста в тексте не получается никаких отзывов.</span><span class="sxs-lookup"><span data-stu-id="04b21-168">When you type into the text input you get no feedback.</span></span>  <span data-ttu-id="04b21-169">Если вы производите опечатку и используете клавиши со стрелками для обзора ваших данных, вы также не получаете обратной связи.</span><span class="sxs-lookup"><span data-stu-id="04b21-169">If you make a typo and use the arrow keys to explore your input you also get no feedback.</span></span>  <span data-ttu-id="04b21-170">Самый простой способ проверить работу — это внести изменения, а затем прослушивать весь элемент, который будет объявлен.</span><span class="sxs-lookup"><span data-stu-id="04b21-170">The easiest way to check your work is to accept the change, then listen for the entire element to be announced.</span></span>  

### <span data-ttu-id="04b21-171">Редактирование HTML-кода элемента в дереве DOM</span><span class="sxs-lookup"><span data-stu-id="04b21-171">Edit the HTML of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="04b21-172">Установив фокус на узел в **дереве DOM**, нажмите, `Enter` чтобы сделать его редактируемым.</span><span class="sxs-lookup"><span data-stu-id="04b21-172">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="04b21-173">Нажимайте клавишу `Tab` для перемещения между значениями атрибутов.</span><span class="sxs-lookup"><span data-stu-id="04b21-173">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="04b21-174">Когда вы услышите имя элемента (например, "H2"), оно находится внутри текстового ввода и может изменить тип элемента.</span><span class="sxs-lookup"><span data-stu-id="04b21-174">When you hear the name of the element, for instance, "h2", you are inside of a text input and may change the type of the element.</span></span>  
*   <span data-ttu-id="04b21-175">Нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \), чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="04b21-175">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change.</span></span>  

<span data-ttu-id="04b21-176">Например, ввод `h3` и нажатие клавиш `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \) изменяет Теги начала и конца элемента на `h3` .</span><span class="sxs-lookup"><span data-stu-id="04b21-176">For example, typing `h3` and pressing `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) changes the start and end tags of the element to `h3`.</span></span>  

## <span data-ttu-id="04b21-177">Вкладки панели элементов</span><span class="sxs-lookup"><span data-stu-id="04b21-177">Elements panel tabs</span></span>   

<span data-ttu-id="04b21-178">Панель " **элементы** " включает дополнительные вкладки для проверки элементов, таких как CSS, примененные к элементу или соответствующему месту в дереве специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="04b21-178">The **Elements** panel contains additional tabs for inspecting things like the CSS applied to an element or the relevant place in the accessibility tree.</span></span>  

*   <span data-ttu-id="04b21-179">Установив фокус на узел в **дереве DOM**, нажимайте кнопку `Tab` , пока не услышите сообщение о том, что выбрана область " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="04b21-179">With focus on a node in the **DOM Tree**, press `Tab` until you hear that the **Styles** pane is selected.</span></span>  
*   <span data-ttu-id="04b21-180">Используйте `Right Arrow` для исследования другие доступные вкладки.</span><span class="sxs-lookup"><span data-stu-id="04b21-180">Use the `Right Arrow` to explore other available tabs.</span></span>  

<span data-ttu-id="04b21-181">**Дерево DOM** превращает элементы с `href` атрибутами в ссылки, поэтому для `Tab` доступа к области **стилей** может потребоваться несколько нажатий клавиши.</span><span class="sxs-lookup"><span data-stu-id="04b21-181">The **DOM Tree** turns elements with `href` attributes into focusable links, so you may need to press `Tab` more than once to reach the **Styles** pane.</span></span>  

### <span data-ttu-id="04b21-182">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="04b21-182">Known issues</span></span>   

<span data-ttu-id="04b21-183">Вкладки " **точки останова** " и " **свойства** " DOM не поддерживают специальные возможности клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="04b21-183">The **DOM Breakpoints** and **Properties** tabs are not keyboard accessible.</span></span>  

### <span data-ttu-id="04b21-184">Область "стили"</span><span class="sxs-lookup"><span data-stu-id="04b21-184">Styles pane</span></span>   

<span data-ttu-id="04b21-185">В области " **стили** " можно найти элементы управления для фильтрации стилей, переключения состояний элементов \ (например [`:active`][MDNActive] , [`:focus`][MDNFocus] \), переключателей классов и добавления новых классов.</span><span class="sxs-lookup"><span data-stu-id="04b21-185">In the **Styles** pane find controls for filtering styles, toggling element states \(such as [`:active`][MDNActive] and [`:focus`][MDNFocus]\), toggling classes, and adding new classes.</span></span>  <span data-ttu-id="04b21-186">Кроме того, существует мощное средство проверки стиля для изучения и изменения стилей, которые в данный момент применены к элементу, который находится в фокусе в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="04b21-186">There is also a powerful style inspection tool to explore and modify styles currently applied to the element that is in focus in the **DOM Tree**.</span></span>  

<span data-ttu-id="04b21-187">Ключевая концепция, указывающая на область **стилей** , заключается в том, что она показывает только стили для выбранного в данный момент узла в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="04b21-187">The key concept to understand about the **Styles** pane is that it only shows styles for the currently-selected node in the **DOM Tree**.</span></span>  <span data-ttu-id="04b21-188">Например, предположим, что вы проверили стили `<header>` узла, и теперь вам нужно просмотреть стили `<footer>` узла.</span><span class="sxs-lookup"><span data-stu-id="04b21-188">For example, suppose you are done inspecting the styles of a `<header>` node, and now you want to look at the styles for a `<footer>` node.</span></span>  <span data-ttu-id="04b21-189">Для этого сначала нужно выбрать `<footer>` узел в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="04b21-189">To do that, you first need to select the `<footer>` node in the **DOM Tree**.</span></span>  <span data-ttu-id="04b21-190">Возможно, вам будет удобнее использовать рабочий процесс [проверки](#inspect-an-element-on-the-page) для проверки узла, находящейся в общей области `footer` (например, ссылки в нижнем колонтитуле \), который специализируется на **дереве DOM**, а затем используйте клавиатуру для перехода на точный узел, в котором он заинтересован.</span><span class="sxs-lookup"><span data-stu-id="04b21-190">You may find it faster to use the [Inspect](#inspect-an-element-on-the-page) workflow to inspect a node that is in the general vicinity of the `footer` node \(such as a link within the footer\), which focuses the **DOM Tree**, and then use your keyboard to navigate to the exact node in which you are interested.</span></span>  

#### <span data-ttu-id="04b21-191">Навигация в области "стили"</span><span class="sxs-lookup"><span data-stu-id="04b21-191">Navigate the Styles pane</span></span>   

<span data-ttu-id="04b21-192">Так как все инструменты стиля подключаются друг к другу, а не в область **стилей** , для этого сначала имеет смысл образец этого инструмента.</span><span class="sxs-lookup"><span data-stu-id="04b21-192">Because all of the style tools connect in one way or another back to the **Styles** pane, it makes sense to master this tool first.</span></span>  

*   <span data-ttu-id="04b21-193">Наведите фокус на область **стили** , нажмите, `Tab` чтобы переместить фокус внутрь и проанализировать содержимое.</span><span class="sxs-lookup"><span data-stu-id="04b21-193">With focus on the **Styles** pane, press `Tab` to move focus inside and explore the contents.</span></span>  
*   <span data-ttu-id="04b21-194">Нажимайте кнопку `Tab` , пока первый стиль не станет активным.</span><span class="sxs-lookup"><span data-stu-id="04b21-194">Press `Tab` until the first style becomes active.</span></span>  <span data-ttu-id="04b21-195">Если вы используете средство чтения с экрана, первый стиль объявляется как "Element. Style {} ".</span><span class="sxs-lookup"><span data-stu-id="04b21-195">If you are using a screen reader this first style is announced as "element.style {}".</span></span>  
*   <span data-ttu-id="04b21-196">Нажмите клавишу `Down Arrow` для перемещения по списку стилей в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="04b21-196">Press `Down Arrow` to navigate the list of styles in order of specificity.</span></span>  <span data-ttu-id="04b21-197">Средство чтения с экрана уведомляет каждый стиль, начиная с имени CSS-файла, номер строки, в которой отображается стиль, и название стиля.</span><span class="sxs-lookup"><span data-stu-id="04b21-197">A screen reader announces each style starting with the name of the CSS file, the line number on which the style appears, and the name of the style.</span></span>  <span data-ttu-id="04b21-198">Например: "Main. CSS: 233. card__img {} "</span><span class="sxs-lookup"><span data-stu-id="04b21-198">For example: "main.css:233 .card__img {}"</span></span>  
*   <span data-ttu-id="04b21-199">`Enter`Более подробное изучение стиля.</span><span class="sxs-lookup"><span data-stu-id="04b21-199">Press `Enter` to inspect a style in more detail.</span></span>  <span data-ttu-id="04b21-200">Фокус начинается с редактируемой версии имени стиля.</span><span class="sxs-lookup"><span data-stu-id="04b21-200">Focus begins on an editable version of the style name.</span></span>  
*   <span data-ttu-id="04b21-201">Нажмите клавишу `Tab` для перемещения между редактируемыми версиями каждого свойства CSS и соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="04b21-201">Press `Tab` to move between editable versions of each CSS property and their corresponding values.</span></span>  <span data-ttu-id="04b21-202">В конце каждого блока Style — пустое Редактируемое текстовое поле, которое можно использовать для добавления дополнительных свойств CSS.</span><span class="sxs-lookup"><span data-stu-id="04b21-202">At the end of each style block is a blank editable text field which you may use to add additional CSS properties.</span></span>  
*   <span data-ttu-id="04b21-203">Вы можете продолжить `Tab` Перемещение по списку стилей или нажать, `Escape` чтобы выйти из этого режима и вернуться к переходу с помощью клавиш со стрелками.</span><span class="sxs-lookup"><span data-stu-id="04b21-203">You may continue to press `Tab` to move through the list of styles, or press `Escape` to exit this mode and go back to navigating by arrow keys.</span></span>  

<span data-ttu-id="04b21-204">Обязательно прочтите вкладку [Справка: клавиатура в области стилей] [DevtoolsShortcutsStylesPaneKeyboard] для получения дополнительных сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="04b21-204">Be sure to read through the [Styles pane keyboard reference][DevtoolsShortcutsStylesPaneKeyboard] for additional shortcuts.</span></span>  

##### <span data-ttu-id="04b21-205">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="04b21-205">Known Issues</span></span>   

*   <span data-ttu-id="04b21-206">Если вы используете Редактируемое текстовое поле **Фильтр** , вы больше не сможете перемещаться по списку стилей.</span><span class="sxs-lookup"><span data-stu-id="04b21-206">If you use the **Filter** editable text field, you are no longer be able to navigate the list of styles.</span></span>  

#### <span data-ttu-id="04b21-207">Переключить состояние элемента</span><span class="sxs-lookup"><span data-stu-id="04b21-207">Toggle element state</span></span>   

<span data-ttu-id="04b21-208">Чтобы переключить состояние элемента (например, или), `:active` `:focus` выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="04b21-208">To toggle the state of an element, such as `:active` or `:focus`:</span></span>  

1.  <span data-ttu-id="04b21-209">Перейдите к области **стили** и нажмите клавишу `Tab` , пока не получит фокус на кнопке **состояния переключаемого элемента** .</span><span class="sxs-lookup"><span data-stu-id="04b21-209">Navigate to the **Styles** pane and press `Tab` until the **Toggle Element State** button has focus.</span></span>  
1.  <span data-ttu-id="04b21-210">Нажмите `Enter` , чтобы развернуть коллекцию состояний элементов.</span><span class="sxs-lookup"><span data-stu-id="04b21-210">Press `Enter` to expand the collection of element states.</span></span>  <span data-ttu-id="04b21-211">Состояния элементов представляются в виде группы флажков.</span><span class="sxs-lookup"><span data-stu-id="04b21-211">The element states are presented as a group of checkboxes.</span></span>  
1.  <span data-ttu-id="04b21-212">Нажимайте клавишу `Tab` до первого состояния, `:active` и фокус.</span><span class="sxs-lookup"><span data-stu-id="04b21-212">Press `Tab` until the first state, `:active`, has focus.</span></span>  
1.  <span data-ttu-id="04b21-213">Нажмите `Space` , чтобы включить его.</span><span class="sxs-lookup"><span data-stu-id="04b21-213">Press `Space` to enable it.</span></span>  <span data-ttu-id="04b21-214">Если элемент, выбранный в дереве DOM `:active` , имеет стиль, он теперь применяется.</span><span class="sxs-lookup"><span data-stu-id="04b21-214">If the currently-selected element in the DOM Tree has an `:active` style, it is now applied.</span></span>  
1.  <span data-ttu-id="04b21-215">Продолжайте нажимать клавишу `Tab` , чтобы ознакомиться со всеми доступными состояниями.</span><span class="sxs-lookup"><span data-stu-id="04b21-215">Continue pressing `Tab` to explore all of the available states.</span></span>  

#### <span data-ttu-id="04b21-216">Добавление существующего класса</span><span class="sxs-lookup"><span data-stu-id="04b21-216">Add an existing class</span></span>   

<span data-ttu-id="04b21-217">Рядом с кнопкой " **включить состояние элемента** " находится кнопка " **классы элементов** ".</span><span class="sxs-lookup"><span data-stu-id="04b21-217">Adjacent to the **Toggle Element State** button is the **Element Classes** button.</span></span>  <span data-ttu-id="04b21-218">Перемещение фокуса на него с помощью клавиши " `Tab` Далее" `Enter` .</span><span class="sxs-lookup"><span data-stu-id="04b21-218">Move focus to it by pressing `Tab` then `Enter`.</span></span>  <span data-ttu-id="04b21-219">Фокус перемещается в поле редактирования текста, помеченное **Добавить новый класс**.</span><span class="sxs-lookup"><span data-stu-id="04b21-219">Focus moves into an edit text field labeled **Add New Class**.</span></span>  

<span data-ttu-id="04b21-220">Кнопка « **классы элементов** » используется преимущественно для добавления в элемент существующих классов.</span><span class="sxs-lookup"><span data-stu-id="04b21-220">The **Element Classes** button is primarily used for adding existing classes to an element.</span></span>  <span data-ttu-id="04b21-221">Например, если ваша таблица стилей содержала вспомогательный класс `.clearfix` , вы можете нажать `.` внутри текстового поля изменить, чтобы просмотреть список предложений, и использовать `Down Arrow` для поиска `.clearfix` вариантов.</span><span class="sxs-lookup"><span data-stu-id="04b21-221">For example, if your stylesheet contained a helper class named `.clearfix` you may press `.` inside of the edit text field to see a suggestion list of classes and use the `Down Arrow` to find the `.clearfix` suggestion.</span></span>  <span data-ttu-id="04b21-222">Или введите имя класса, а затем нажмите `Enter` , чтобы применить его.</span><span class="sxs-lookup"><span data-stu-id="04b21-222">Or type the class name out yourself and press `Enter` to apply it.</span></span>  

#### <span data-ttu-id="04b21-223">Добавление нового правила стиля</span><span class="sxs-lookup"><span data-stu-id="04b21-223">Add a new style rule</span></span>   

<span data-ttu-id="04b21-224">Рядом с кнопкой " **классы элементов** " находится **Новая кнопка "новое правило стиля** ".</span><span class="sxs-lookup"><span data-stu-id="04b21-224">Adjacent to the **Element Classes** button is the **New Style Rule** button.</span></span>  <span data-ttu-id="04b21-225">Перемещение фокуса на него с помощью нажатия `Tab` и нажатия `Enter` .</span><span class="sxs-lookup"><span data-stu-id="04b21-225">Move focus to it by pressing `Tab` and press `Enter`.</span></span>  <span data-ttu-id="04b21-226">Фокус переместится в редактируемое текстовое поле в инспекторе стилей.</span><span class="sxs-lookup"><span data-stu-id="04b21-226">Focus moves into an editable text field inside of the style inspector.</span></span>  <span data-ttu-id="04b21-227">Начальным текстовым содержимым поля является имя тега элемента, выбранного в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="04b21-227">The initial text content of the field is the tag name of the element that is selected in the **DOM Tree**.</span></span>  
<span data-ttu-id="04b21-228">Вы можете ввести имя нужного класса в это поле, а затем нажать `Tab` , чтобы назначить ему свойства CSS.</span><span class="sxs-lookup"><span data-stu-id="04b21-228">You may type any class name you want into this field and then press `Tab` to assign CSS properties to it.</span></span>  

### <span data-ttu-id="04b21-229">Вычисляемая вкладка</span><span class="sxs-lookup"><span data-stu-id="04b21-229">Computed tab</span></span>   

<span data-ttu-id="04b21-230">Наведите фокус на вкладку **вычисляемый** элемент, `Tab` чтобы переместить фокус внутрь и ознакомиться с содержимым, нажмите кнопку.</span><span class="sxs-lookup"><span data-stu-id="04b21-230">With focus on the **Computed** tab, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="04b21-231">В **вычисляемой** вкладке есть элементы управления для изучения того, какие свойства CSS фактически применяются к элементу в порядке их следования.</span><span class="sxs-lookup"><span data-stu-id="04b21-231">Within the **Computed** tab there are controls for exploring which CSS properties are actually applied to an element in order of specificity.</span></span>  

<!--todo: add computed tab section when available  -->  

#### <span data-ttu-id="04b21-232">Ознакомьтесь со всеми вычисляемыми стилями</span><span class="sxs-lookup"><span data-stu-id="04b21-232">Explore all computed styles</span></span>   

<span data-ttu-id="04b21-233">Нажимайте кнопку, `Tab` пока не дойдете до коллекции вычисляемых стилей.</span><span class="sxs-lookup"><span data-stu-id="04b21-233">Press `Tab` until you reach the collection of computed styles.</span></span>  <span data-ttu-id="04b21-234">Они представлены в виде [ARIA `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="04b21-234">These are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="04b21-235">Разворачивание списка ListBox указывает, какие селекторы CSS применяют вычисляемый стиль.</span><span class="sxs-lookup"><span data-stu-id="04b21-235">Expanding a listbox reveals which CSS selectors are applying the computed style.</span></span>  <span data-ttu-id="04b21-236">Эти селекторы упорядочены по определенному принципу.</span><span class="sxs-lookup"><span data-stu-id="04b21-236">These selectors are organized by specificity.</span></span>  <span data-ttu-id="04b21-237">Средство чтения с экрана объявляет вычисленное значение, которое в настоящее время определяет элемент выбора CSS, имя файла таблицы стилей, содержащей селектор, и номер строки для элемента Selector.</span><span class="sxs-lookup"><span data-stu-id="04b21-237">A screen reader announces the computed value, which CSS selector is currently matching, the filename of the stylesheet that contains the selector, and the line number for the selector.</span></span>  

#### <span data-ttu-id="04b21-238">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="04b21-238">Known issues</span></span>   

*   <span data-ttu-id="04b21-239">Если вы используете текстовое поле " **Фильтр** ", вы больше не сможете проверять стили.</span><span class="sxs-lookup"><span data-stu-id="04b21-239">If you use the **Filter** text field, you are no longer able to inspect styles.</span></span>  

### <span data-ttu-id="04b21-240">Вкладка "прослушиватели событий"</span><span class="sxs-lookup"><span data-stu-id="04b21-240">Event listeners tab</span></span>   

<span data-ttu-id="04b21-241">На панели **элементы** можно проверить прослушиватели событий, примененные к элементу, с помощью вкладки **прослушиватели событий** .  В области **стили** нажмите клавишу, `Right Arrow` чтобы перейти на вкладку **прослушиватели событий** .</span><span class="sxs-lookup"><span data-stu-id="04b21-241">From within the **Elements** panel you may inspect the event listeners applied to an element using the **Event Listeners** tab.  With focus on the **Styles** pane, press the `Right Arrow` to navigate to the **Event Listeners** tab.</span></span>  

#### <span data-ttu-id="04b21-242">Анализ прослушивателей событий</span><span class="sxs-lookup"><span data-stu-id="04b21-242">Explore event listeners</span></span>   

<span data-ttu-id="04b21-243">Прослушиватели событий представлены в виде [ARIA `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="04b21-243">Event listeners are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="04b21-244">Вы можете перемещаться с помощью клавиш со стрелками.</span><span class="sxs-lookup"><span data-stu-id="04b21-244">You may use the arrow keys to navigate them.</span></span>  <span data-ttu-id="04b21-245">Средство чтения с экрана объявляет имя объекта DOM, к которому прикреплен прослушиватель событий, а также имя файла, в котором определен прослушиватель событий, и номер строки.</span><span class="sxs-lookup"><span data-stu-id="04b21-245">A screen reader announces the name of the DOM object that the event listener is attached to, as well as the file name where the event listener is defined and the line number.</span></span>  

### <span data-ttu-id="04b21-246">Область специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="04b21-246">Accessibility pane</span></span>   

<span data-ttu-id="04b21-247">Наведите фокус на область **Специальные возможности** , `Tab` чтобы переместить фокус внутрь и ознакомиться с содержимым.</span><span class="sxs-lookup"><span data-stu-id="04b21-247">With focus on the **Accessibility** pane, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="04b21-248">В области **специальных возможностей** есть элементы управления для изучения дерева специальных возможностей, атрибуты ARIA, примененные к элементу, и вычисляемые свойства специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="04b21-248">Within the **Accessibility** pane there are controls for exploring the accessibility tree, the ARIA attributes applied to an element, and the computed accessibility properties.</span></span>  

<!--todo: add reference (Accessibility pane) section when available  -->  

#### <span data-ttu-id="04b21-249">Дерево специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="04b21-249">Accessibility Tree</span></span>   

<span data-ttu-id="04b21-250">**Дерево специальных возможностей** представлено в виде [ARIA `tree` ][W3CWaiAriaTree] , где каждый `treeitem` из них соответствует элементу в DOM.</span><span class="sxs-lookup"><span data-stu-id="04b21-250">The **Accessibility Tree** is presented as an [ARIA `tree`][W3CWaiAriaTree] where each `treeitem` corresponds to an element in the DOM.</span></span>  <span data-ttu-id="04b21-251">Дерево объявляет вычисляемую роль для выбранного узла.</span><span class="sxs-lookup"><span data-stu-id="04b21-251">The tree announces the computed role for the selected node.</span></span>  <span data-ttu-id="04b21-252">Универсальные элементы, такие как `div` и `span` , объявляются как "GenericContainer" в дереве.</span><span class="sxs-lookup"><span data-stu-id="04b21-252">Generic elements like `div` and `span` are announced as "GenericContainer" in the tree.</span></span>  <span data-ttu-id="04b21-253">Используйте клавиши со стрелками для перемещения по дереву и просмотра связей между родительскими и дочерними таблицами.</span><span class="sxs-lookup"><span data-stu-id="04b21-253">Use the arrow keys to traverse the tree and explore parent-child relationships.</span></span>  

#### <span data-ttu-id="04b21-254">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="04b21-254">Known issues</span></span>   

*   <span data-ttu-id="04b21-255">Тип [ `tree` ARIA][W3CWaiAriaTree] , используемый областью **специальных возможностей** , может быть неправильно открыт в Microsoft Edge для средств чтения с экрана macOS, таких как VoiceOver.</span><span class="sxs-lookup"><span data-stu-id="04b21-255">The type of [ARIA `tree`][W3CWaiAriaTree] used by the **Accessibility** pane may not be properly exposed in Microsoft Edge for macOS screen readers like VoiceOver.</span></span>  <span data-ttu-id="04b21-256">Подпишитесь на [вопрос Chromium #868480][ChromiumIssues868480] , чтобы получить информацию о ходе выполнения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="04b21-256">Subscribe to [Chromium issue #868480][ChromiumIssues868480] to be informed about progress on this issue.</span></span>  
*   <span data-ttu-id="04b21-257">Каждый раздел с **атрибутами ARIA** и **вычисляемые свойства** помечается как [ARIA `tree` ][W3CWaiAriaTree], но в настоящее время у каждого из них нет управления фокусом, и это не повлияет на клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="04b21-257">Each of the **ARIA Attributes** and **Computed Properties** sections are marked up as an [ARIA `tree`][W3CWaiAriaTree], but each does not currently have focus management and is not keyboard operable.</span></span>  

## <span data-ttu-id="04b21-258">Панель «аудит»</span><span class="sxs-lookup"><span data-stu-id="04b21-258">Audits panel</span></span>   

<span data-ttu-id="04b21-259">Для проверки распространенных проблем, связанных с производительностью, читаемостью, SEO и другими категориями, необходимо выполнить серию тестов на сайте с помощью панели **аудита** .</span><span class="sxs-lookup"><span data-stu-id="04b21-259">The **Audits** panel you should run a series of tests against a site to check for common issues related to performance, accessibility, SEO, and a number of other categories.</span></span>  

### <span data-ttu-id="04b21-260">Настройка и запуск аудита</span><span class="sxs-lookup"><span data-stu-id="04b21-260">Configure and run an audit</span></span>   

1.  <span data-ttu-id="04b21-261">При первом открытии панели « **аудиты** » фокус помещается на кнопку « **запустить аудит** » в конце формы.</span><span class="sxs-lookup"><span data-stu-id="04b21-261">When the **Audits** panel is first opened, focus is placed on the **Run Audit** button at the end of the form.</span></span>  <span data-ttu-id="04b21-262">По умолчанию форма настроена для выполнения аудита для каждой категории с помощью эмуляции мобильного устройства в имитируемом соединении 3G.</span><span class="sxs-lookup"><span data-stu-id="04b21-262">By default the form is configured to run audits for every category using mobile emulation on a simulated 3G connection.</span></span>  
1.  <span data-ttu-id="04b21-263">Используйте `Shift` + `Tab` или вернитесь в режим просмотра, чтобы изменить параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="04b21-263">Use `Shift`+`Tab` or navigate back in Browse mode to change the audit settings.</span></span>  
1.  <span data-ttu-id="04b21-264">Когда вы будете готовы запустить аудит, вернитесь к кнопке **запустить аудит** и нажмите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="04b21-264">When you are ready to run the audit, navigate back to the **Run Audit** button and press `Enter`.</span></span>  
1.  <span data-ttu-id="04b21-265">Фокус перемещается в модальное окно с помощью кнопки **"Отмена"** , которая позволяет выйти из аудита.</span><span class="sxs-lookup"><span data-stu-id="04b21-265">Focus moves into a modal window with a **Cancel** button which allows you to exit the audit.</span></span>  <span data-ttu-id="04b21-266">Вы можете прослушать серию earconsов в процессе аудита, а также обновить страницу несколько появлений.</span><span class="sxs-lookup"><span data-stu-id="04b21-266">You may hear a series of earcons as the audit runs and refreshes the page multiple times.</span></span>  

#### <span data-ttu-id="04b21-267">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="04b21-267">Known issues</span></span>   

*   <span data-ttu-id="04b21-268">В настоящее время разные разделы формы конфигурации не помечаются `fieldset` элементом.</span><span class="sxs-lookup"><span data-stu-id="04b21-268">The different sections of the configuration form are not currently marked up with a `fieldset` element.</span></span>  <span data-ttu-id="04b21-269">Чтобы узнать, какие элементы управления связаны с каждым разделом, удобнее перейти в режим просмотра.</span><span class="sxs-lookup"><span data-stu-id="04b21-269">It may be easier to navigate them in Browse mode to figure out which controls are associated with each section.</span></span>  
*   <span data-ttu-id="04b21-270">При завершении работы аудита отсутствует объявление earcon или Live Region.</span><span class="sxs-lookup"><span data-stu-id="04b21-270">There is no earcon or live region announcement when the audit is finished running.</span></span>  <span data-ttu-id="04b21-271">Как правило, это займет около 30 секунд, после чего вы сможете перейти к результатам.</span><span class="sxs-lookup"><span data-stu-id="04b21-271">Generally it takes about 30 seconds, after which you should be able to navigate to the results.</span></span>  <span data-ttu-id="04b21-272">Использование режима обзора может быть самым простым способом достичь результатов.</span><span class="sxs-lookup"><span data-stu-id="04b21-272">Using Browse mode may be the easiest way to reach the results.</span></span>  

### <span data-ttu-id="04b21-273">Навигация по отчету аудита</span><span class="sxs-lookup"><span data-stu-id="04b21-273">Navigate the audit report</span></span>   

<span data-ttu-id="04b21-274">Отчет аудита организован в разделы, соответствующие каждой из категорий аудита.</span><span class="sxs-lookup"><span data-stu-id="04b21-274">The audit report is organized into sections that correspond with each of the audit categories.</span></span>  <span data-ttu-id="04b21-275">Откроется отчет со списком оценок для каждой категории.</span><span class="sxs-lookup"><span data-stu-id="04b21-275">The report opens with a list of scores for each category.</span></span>  <span data-ttu-id="04b21-276">Эти баллы также являются ссылками, которые можно использовать для перехода к соответствующим разделам.</span><span class="sxs-lookup"><span data-stu-id="04b21-276">These scores are also links which are able to be used to skip to the relevant sections.</span></span>  <span data-ttu-id="04b21-277">В каждом разделе находятся `details` элементы с расширениями, которые содержат сведения, связанные с прошедших аудитом или сбоем.</span><span class="sxs-lookup"><span data-stu-id="04b21-277">Within each section are expandable `details` elements, which contain information relating to passed or failed audits.</span></span>  <span data-ttu-id="04b21-278">По умолчанию отображаются только ошибки аудита.</span><span class="sxs-lookup"><span data-stu-id="04b21-278">By default, only failing audits are shown.</span></span>  <span data-ttu-id="04b21-279">Каждый раздел завершается с помощью последнего `details` элемента, содержащего все переданные аудиты.</span><span class="sxs-lookup"><span data-stu-id="04b21-279">Each section ends with a final `details` element which contains all of the passed audits.</span></span>  

<span data-ttu-id="04b21-280">Чтобы запустить новый аудит, используйте `Shift` + `Tab` для выхода из него отчет и поиска кнопки **выполнить аудит** .</span><span class="sxs-lookup"><span data-stu-id="04b21-280">To run a new audit, use `Shift`+`Tab` to exit the report and look for the **Perform An Audit** button.</span></span>  

## <span data-ttu-id="04b21-281">Отзыв</span><span class="sxs-lookup"><span data-stu-id="04b21-281">Feedback</span></span>   

*   <span data-ttu-id="04b21-282">Отправка DevToolsных отчетов об ошибках и запросов на функции для [Chromium отслеживания проблем][MonorailChromiumIssues].</span><span class="sxs-lookup"><span data-stu-id="04b21-282">Send DevTools bug reports or feature requests to [Chromium Issue Tracker][MonorailChromiumIssues].</span></span>  
*   <span data-ttu-id="04b21-283">Отправляйте отзывы, связанные с этим документом, в [GitHub][GithubEdgeDeveloperNewIssue].</span><span class="sxs-lookup"><span data-stu-id="04b21-283">Send any feedback related to this document to [GitHub][GithubEdgeDeveloperNewIssue].</span></span>  

<!-- image links -->  

<!-- links -->  

<!--[DevtoolsAccessibilityReference]: reference.md "Accessibility Reference"  -->  
<!--[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "The Accessibility pane - Accessibility Reference"  -->  

<!--[MicrosoftEdgeDevtoolsIndex]: ../index.md "Microsoft Edge DevTools"  -->  
[DevtoolsCommandMenuIndex]: .. /Command-Menu/index.md "запускать команды с помощью меню команд DevTools Microsoft Edge"  
[DevtoolsConsoleIndex]: .. /Console/index.md "Обзор консоли"  
[DevtoolsCssIndex]: .. /CSS/index.md "Начало работы с просмотром и изменением CSS"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get Started With Viewing And Changing The DOM"  -->  
<!--[DevtoolsDomIndexNavigateDomTreeKeyboard]: ../dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get Started With Viewing And Changing The DOM"  -->
[DevtoolsOpen]: .. /open.md "открыть Microsoft Edge DevTools"  
[DevtoolsShortcuts]: .. /shortcuts.md "Microsoft Edge DevTools сочетания клавиш"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.md # Styles (стили) — область — сочетания клавиш в области "стили" — Microsoft Edge DevTools сочетания клавиш "  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Вопрос 868480 – предоставление деревьев ARIA в виде таблиц в специальных возможностях Mac"  
[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Новая ошибка — MicrosoftDocs/Edge-разработчик | GitHub"  
[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": активный | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": фокус | MDN"  
[MonorailChromiumIssues]: https://crbug.com "Проблемы — Chromium-Monorail"  
[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "TabList (роль) — доступные богатые Интернет-приложения (помощью ОРИЕНТИРОВ WAI-ARIA) 1,1 | PNG"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "Tree (роль) — доступные богатые Интернет-приложения (помощью ОРИЕНТИРОВ WAI-ARIA) 1,1 | PNG"  

> [!NOTE]
> <span data-ttu-id="04b21-297">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="04b21-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="04b21-298">[Здесь вы найдете](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) исходную страницу и она была написана [Вадимом Dodson][RobDodson] \ (участники, Google веб-основы.).</span><span class="sxs-lookup"><span data-stu-id="04b21-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) and is authored by [Rob Dodson][RobDodson] \(Contributor, Google WebFundamentals\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="04b21-300">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="04b21-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  

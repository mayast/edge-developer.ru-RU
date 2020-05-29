---
title: Приостановка кода с точки останова в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 2afa4b7dbe96b65747ec17b147f0a82c16efa288
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581805"
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







# <span data-ttu-id="b31af-103">Приостановка кода с точки останова в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b31af-103">How To Pause Your Code With Breakpoints In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="b31af-104">Используйте точки останова для приостановки кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b31af-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="b31af-105">В этом руководстве описаны все типы точек останова, доступные в DevTools, а также способы их использования и настройки каждого типа.</span><span class="sxs-lookup"><span data-stu-id="b31af-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="b31af-106">Практические руководства по отладке можно найти [в разделе Начало отладки JavaScript в Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="b31af-106">For a hands-on tutorial of the debugging process, see [Get Started with Debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="b31af-107">Общие сведения о том, когда использовать каждый тип точки останова</span><span class="sxs-lookup"><span data-stu-id="b31af-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="b31af-108">Наиболее известный тип точки останова — это строка кода.</span><span class="sxs-lookup"><span data-stu-id="b31af-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="b31af-109">Однако точки останова для кода могут быть неэффективными для установки, особенно в том случае, если вы точно не знаете, где искать, или если вы работаете с большой базой кода.</span><span class="sxs-lookup"><span data-stu-id="b31af-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="b31af-110">Вы можете экономить время при отладке, зная, как и когда использовать другие типы точек останова.</span><span class="sxs-lookup"><span data-stu-id="b31af-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="b31af-111">Тип точки останова</span><span class="sxs-lookup"><span data-stu-id="b31af-111">Breakpoint Type</span></span> | <span data-ttu-id="b31af-112">Используйте этот параметр, если вы хотите приостановить...</span><span class="sxs-lookup"><span data-stu-id="b31af-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="b31af-113">Строка кода</span><span class="sxs-lookup"><span data-stu-id="b31af-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="b31af-114">В определенном регионе кода.</span><span class="sxs-lookup"><span data-stu-id="b31af-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="b31af-115">Условный текст</span><span class="sxs-lookup"><span data-stu-id="b31af-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="b31af-116">В определенном регионе кода, но только в том случае, если истинно какое – либо другое условие.</span><span class="sxs-lookup"><span data-stu-id="b31af-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="b31af-117">DOM</span><span class="sxs-lookup"><span data-stu-id="b31af-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="b31af-118">В коде, который изменяет или удаляет определенный узел DOM или дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="b31af-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="b31af-119">XHR</span><span class="sxs-lookup"><span data-stu-id="b31af-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="b31af-120">Если URL-адрес XHR имеет строковый шаблон.</span><span class="sxs-lookup"><span data-stu-id="b31af-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="b31af-121">Прослушиватель событий</span><span class="sxs-lookup"><span data-stu-id="b31af-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="b31af-122">В коде, который выполняется после события, например `click` , выполняется.</span><span class="sxs-lookup"><span data-stu-id="b31af-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="b31af-123">Ошибка</span><span class="sxs-lookup"><span data-stu-id="b31af-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="b31af-124">В строке кода, которая вызывает перехваченное или неперехваченное исключение.</span><span class="sxs-lookup"><span data-stu-id="b31af-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="b31af-125">Функция</span><span class="sxs-lookup"><span data-stu-id="b31af-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="b31af-126">Каждый раз, когда выполняется определенная команда, функция или метод.</span><span class="sxs-lookup"><span data-stu-id="b31af-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="b31af-127">Точки останова в коде строки</span><span class="sxs-lookup"><span data-stu-id="b31af-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="b31af-128">Если вы знаете точную область кода, которую нужно исследовать, используйте точку останова из строки кода.</span><span class="sxs-lookup"><span data-stu-id="b31af-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="b31af-129">DevTools **всегда** задерживается перед выполнением этой строки кода.</span><span class="sxs-lookup"><span data-stu-id="b31af-129">DevTools **always** pauses before this line of code is run.</span></span>  

<span data-ttu-id="b31af-130">Установка точки останова в коде строки в DevTools:</span><span class="sxs-lookup"><span data-stu-id="b31af-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="b31af-131">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="b31af-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b31af-132">Откройте файл с той строкой, в которой вы хотите прервать ее.</span><span class="sxs-lookup"><span data-stu-id="b31af-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="b31af-133">Перейдите к строке кода.</span><span class="sxs-lookup"><span data-stu-id="b31af-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="b31af-134">Слева от строки кода находится столбец номер строки.</span><span class="sxs-lookup"><span data-stu-id="b31af-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="b31af-135">Щелкните по нему.</span><span class="sxs-lookup"><span data-stu-id="b31af-135">Click on it.</span></span>  <span data-ttu-id="b31af-136">Рядом со столбцом номер строки появится красный значок.</span><span class="sxs-lookup"><span data-stu-id="b31af-136">A red icon appears next to the line number column.</span></span>  

> ##### <span data-ttu-id="b31af-137">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="b31af-137">Figure 1</span></span>  
> <span data-ttu-id="b31af-138">Точка останова, установленная на строке 30</span><span class="sxs-lookup"><span data-stu-id="b31af-138">A line-of-code breakpoint set on line 30</span></span>  
> ![Точка останова строки кода][ImageLocBreakpoint]  

### <span data-ttu-id="b31af-140">Точки останова в коде для строк кода</span><span class="sxs-lookup"><span data-stu-id="b31af-140">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="b31af-141">Выполняйте `debugger` метод из вашего кода, чтобы приостановить его на этой линии.</span><span class="sxs-lookup"><span data-stu-id="b31af-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="b31af-142">Это эквивалентно [точке останова строки кода](#line-of-code-breakpoints), за исключением того, что точка останова задается в коде, а не в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="b31af-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="b31af-143">Зависимые точки останова для строк кода</span><span class="sxs-lookup"><span data-stu-id="b31af-143">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="b31af-144">Если вы знаете точную область кода, которую нужно исследовать, но вы хотите приостанавливать только в том случае, если какое-либо другое условие имеет значение true, используйте для нее точку останова в условном коде.</span><span class="sxs-lookup"><span data-stu-id="b31af-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="b31af-145">Установка условной точки останова для строки кода:</span><span class="sxs-lookup"><span data-stu-id="b31af-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="b31af-146">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="b31af-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b31af-147">Откройте файл с той строкой, в которой вы хотите прервать ее.</span><span class="sxs-lookup"><span data-stu-id="b31af-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="b31af-148">Перейдите к строке кода.</span><span class="sxs-lookup"><span data-stu-id="b31af-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="b31af-149">Слева от строки кода находится столбец номер строки.</span><span class="sxs-lookup"><span data-stu-id="b31af-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="b31af-150">Щелкните правой кнопкой мыши номер строки.</span><span class="sxs-lookup"><span data-stu-id="b31af-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="b31af-151">Нажмите кнопку **добавить условную точку останова**.</span><span class="sxs-lookup"><span data-stu-id="b31af-151">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="b31af-152">Под строкой кода появится диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b31af-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="b31af-153">Введите условие в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="b31af-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="b31af-154">Нажмите `Enter` , чтобы активировать точку останова.</span><span class="sxs-lookup"><span data-stu-id="b31af-154">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="b31af-155">Значок рядом со столбцом "номер строки".</span><span class="sxs-lookup"><span data-stu-id="b31af-155">An icon next to the line number column.</span></span>  

> ##### <span data-ttu-id="b31af-156">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="b31af-156">Figure 2</span></span>  
> <span data-ttu-id="b31af-157">В строке 34 задана зависимая точка останова для кода строки.</span><span class="sxs-lookup"><span data-stu-id="b31af-157">A conditional line-of-code breakpoint set on line 34</span></span>  
> ![Условная точка останова для строки кода][ImageConditionalLocBreakpoint]  

### <span data-ttu-id="b31af-159">Управление точками останова для строк кода</span><span class="sxs-lookup"><span data-stu-id="b31af-159">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="b31af-160">С помощью области " **точки останова** " можно отключить или удалить точки останова для строк кода из одного места.</span><span class="sxs-lookup"><span data-stu-id="b31af-160">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

> ##### <span data-ttu-id="b31af-161">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="b31af-161">Figure 3</span></span>  
> <span data-ttu-id="b31af-162">Панель " **точки останова** ", в которой отображаются две точки останова с двумя строками: один на строке `16` `get-started.js` , другой в строке</span><span class="sxs-lookup"><span data-stu-id="b31af-162">The **Breakpoints** panel showing two line-of-code breakpoints: one on line `16` of `get-started.js`, another on line</span></span> `33`  
> ![Панель «точки останова»][ImageBreakpointsPanel]  

*   <span data-ttu-id="b31af-164">Установите флажок рядом с записью, чтобы отключить эту точку останова.</span><span class="sxs-lookup"><span data-stu-id="b31af-164">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="b31af-165">Щелкните правой кнопкой мыши запись для удаления точки останова.</span><span class="sxs-lookup"><span data-stu-id="b31af-165">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="b31af-166">Щелкните правой кнопкой мыши в любом месте области **точки останова** , чтобы отключить все точки останова, отключить все точки останова или удалить все точки останова.</span><span class="sxs-lookup"><span data-stu-id="b31af-166">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="b31af-167">Отключение всех точек останова эквивалентно депроверке каждого из них.</span><span class="sxs-lookup"><span data-stu-id="b31af-167">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="b31af-168">Отключение всех точек останова дает указание DevTools игнорировать все точки останова для строк кода, а также поддерживать состояние включения, чтобы каждый из них нав одном и том же состоянии до повторной активации каждой из них.</span><span class="sxs-lookup"><span data-stu-id="b31af-168">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  

> ##### <span data-ttu-id="b31af-169">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="b31af-169">Figure 4</span></span>  
> <span data-ttu-id="b31af-170">Деактивированные точки останова на панели " **точки останова** " отключены и прозрачны</span><span class="sxs-lookup"><span data-stu-id="b31af-170">Deactivated breakpoints in the **Breakpoints** pane are disabled and transparent</span></span>  
> ![Деактивированные точки останова на панели "точки останова"][ImageDeactivatedBreakpoints]  

## <span data-ttu-id="b31af-172">Точки останова по изменению модели DOM</span><span class="sxs-lookup"><span data-stu-id="b31af-172">DOM change breakpoints</span></span>   

<span data-ttu-id="b31af-173">Чтобы приостановить выполнение кода, который изменяет узел DOM или дочерние элементы, используйте точку останова изменения модели DOM.</span><span class="sxs-lookup"><span data-stu-id="b31af-173">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="b31af-174">Настройка точки останова для изменения модели DOM.</span><span class="sxs-lookup"><span data-stu-id="b31af-174">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="b31af-175">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="b31af-175">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="b31af-176">Перейдите к элементу, для которого вы хотите установить точку останова.</span><span class="sxs-lookup"><span data-stu-id="b31af-176">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="b31af-177">Щелкните элемент правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="b31af-177">Right-click the element.</span></span>  
1.  <span data-ttu-id="b31af-178">Наведите указатель мыши **на пункт разрыв**, а затем выберите **изменения поддерева**, **изменения атрибутов**или **Удаление узла**.</span><span class="sxs-lookup"><span data-stu-id="b31af-178">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  

> ##### <span data-ttu-id="b31af-179">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="b31af-179">Figure 5</span></span>  
> <span data-ttu-id="b31af-180">Контекстное меню для создания точки останова по изменению модели DOM</span><span class="sxs-lookup"><span data-stu-id="b31af-180">The context menu for creating a DOM change breakpoint</span></span>  
> ![Контекстное меню для создания точки останова по изменению модели DOM][ImageDomChangeBreakpoint]  

### <span data-ttu-id="b31af-182">Типы точек останова для изменения модели DOM</span><span class="sxs-lookup"><span data-stu-id="b31af-182">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="b31af-183">**Изменения поддерева**.</span><span class="sxs-lookup"><span data-stu-id="b31af-183">**Subtree modifications**.</span></span>  <span data-ttu-id="b31af-184">Вызывается при удалении или добавлении дочернего узла, выбранного в данный момент, или изменении содержимого дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="b31af-184">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="b31af-185">Не инициируется для изменений атрибутов дочернего узла или при любых изменениях в выбранном в данный момент узле.</span><span class="sxs-lookup"><span data-stu-id="b31af-185">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  

*   <span data-ttu-id="b31af-186">**Изменения атрибутов**: активируется при добавлении или удалении атрибута на текущем выбранном узле или изменении значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="b31af-186">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  

*   <span data-ttu-id="b31af-187">**Удаление узла**: активируется при удалении текущего выбранного узла.</span><span class="sxs-lookup"><span data-stu-id="b31af-187">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  

## <span data-ttu-id="b31af-188">Точки останова XHR и FETCH</span><span class="sxs-lookup"><span data-stu-id="b31af-188">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="b31af-189">Используйте точку останова XHR, когда нужно прервать, когда URL-адрес запроса XHR содержат указанную строку.</span><span class="sxs-lookup"><span data-stu-id="b31af-189">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="b31af-190">DevTools приостанавливается на строке кода, где XHR запускает `send()` метод.</span><span class="sxs-lookup"><span data-stu-id="b31af-190">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="b31af-191">Эта функция также работает для запросов [API FETCH][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="b31af-191">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="b31af-192">Это может быть полезно, если вы видите, что ваша страница запрашивает неверный URL-адрес, и вам нужно быстро найти исходный код AJAX или FETCH, вызывающий неверный запрос.</span><span class="sxs-lookup"><span data-stu-id="b31af-192">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="b31af-193">Чтобы установить точку останова XHR, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b31af-193">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="b31af-194">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="b31af-194">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b31af-195">Разверните область **точки останова XHR** .</span><span class="sxs-lookup"><span data-stu-id="b31af-195">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="b31af-196">Нажмите кнопку **Добавить точку останова**.</span><span class="sxs-lookup"><span data-stu-id="b31af-196">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="b31af-197">Введите строку, на которой вы хотите приостановить.</span><span class="sxs-lookup"><span data-stu-id="b31af-197">Enter the string which you want to break on.</span></span>  <span data-ttu-id="b31af-198">DevTools приостанавливает работу, когда эта строка отображается в любом месте URL-адреса запроса XHR.</span><span class="sxs-lookup"><span data-stu-id="b31af-198">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="b31af-199">Нажмите кнопку `Enter` , чтобы подтвердить.</span><span class="sxs-lookup"><span data-stu-id="b31af-199">Press `Enter` to confirm.</span></span>  

> ##### <span data-ttu-id="b31af-200">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="b31af-200">Figure 6</span></span>  
> <span data-ttu-id="b31af-201">Создание точки останова XHR в **точках останова XHR** для любого запроса, содержащегося `org` в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="b31af-201">Creating an XHR breakpoint in the **XHR Breakpoints** for any request that contains `org` in the URL</span></span>  
> ![Создание точки останова XHR][ImageXhrBreakpoint]  

## <span data-ttu-id="b31af-203">Точки останова прослушивателя событий</span><span class="sxs-lookup"><span data-stu-id="b31af-203">Event listener breakpoints</span></span> 

<span data-ttu-id="b31af-204">Используйте точки останова прослушивателя событий, когда необходимо приостановить выполнение кода прослушивателя событий, который выполняется после срабатывания события.</span><span class="sxs-lookup"><span data-stu-id="b31af-204">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="b31af-205">Вы можете выбрать определенные события, такие как `click` или категории событий, например все события мыши.</span><span class="sxs-lookup"><span data-stu-id="b31af-205">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="b31af-206">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="b31af-206">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b31af-207">Разверните область **точки останова для прослушивателя событий** .</span><span class="sxs-lookup"><span data-stu-id="b31af-207">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="b31af-208">DevTools отображает список категорий событий, например **анимацию**.</span><span class="sxs-lookup"><span data-stu-id="b31af-208">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="b31af-209">Отметьте одну из этих категорий, чтобы приостановить любое событие из этой категории, или развернуть категорию и проверить определенное событие.</span><span class="sxs-lookup"><span data-stu-id="b31af-209">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  

> ##### <span data-ttu-id="b31af-210">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="b31af-210">Figure 7</span></span>  
> <span data-ttu-id="b31af-211">Создание точки останова прослушивателя событий для</span><span class="sxs-lookup"><span data-stu-id="b31af-211">Creating an event listener breakpoint for</span></span> `deviceorientation`  
> ![Создание точки останова для прослушивателя событий][ImageEventListenerBreakpoint]  

## <span data-ttu-id="b31af-213">Точки останова для исключений</span><span class="sxs-lookup"><span data-stu-id="b31af-213">Exception breakpoints</span></span>   

<span data-ttu-id="b31af-214">Используйте точки останова, когда нужно приостановить выполнение в строке кода, которая вызывает перехваченное или неперехваченное исключение.</span><span class="sxs-lookup"><span data-stu-id="b31af-214">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="b31af-215">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="b31af-215">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b31af-216">Нажмите кнопку **Пауза на** вкладке исключения ![ приостановить выполнение ][ImagePauseOnExceptionsIcon] .</span><span class="sxs-lookup"><span data-stu-id="b31af-216">Click **Pause on exceptions** ![Pause on exceptions][ImagePauseOnExceptionsIcon].</span></span>  <span data-ttu-id="b31af-217">При включении значок становится синей.</span><span class="sxs-lookup"><span data-stu-id="b31af-217">The icon turns blue when enabled.</span></span>  
    
    > ##### <span data-ttu-id="b31af-218">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="b31af-218">Figure 8</span></span>  
    > <span data-ttu-id="b31af-219">Кнопка " **Пауза при исключениях** "</span><span class="sxs-lookup"><span data-stu-id="b31af-219">The **Pause on exceptions** button</span></span>  
    > ![Кнопка "Пауза при исключениях"][ImagePauseExceptionsHighlight]  

1.  <span data-ttu-id="b31af-221">**Необязательный**.</span><span class="sxs-lookup"><span data-stu-id="b31af-221">**Optional**.</span></span> <span data-ttu-id="b31af-222">Установите флажок **приостановить на перехваченных исключениях** , если вы также хотите приостанавливать на перехваченных исключениях помимо неперехваченных.</span><span class="sxs-lookup"><span data-stu-id="b31af-222">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  

> ##### <span data-ttu-id="b31af-223">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="b31af-223">Figure 9</span></span>  
> <span data-ttu-id="b31af-224">Приостановлено при неперехваченном исключении</span><span class="sxs-lookup"><span data-stu-id="b31af-224">Paused on an uncaught exception</span></span>  
> ![Приостановлено при неперехваченном исключении][ImageUncaughtException]  

## <span data-ttu-id="b31af-226">Точки останова по функциям</span><span class="sxs-lookup"><span data-stu-id="b31af-226">Function breakpoints</span></span>   

<span data-ttu-id="b31af-227">Выполняйте `debug(method)` метод, где `method` — команда, функция или метод, для которого нужно выполнить отладку, когда вы хотите приостановить каждый раз при запуске определенной функции.</span><span class="sxs-lookup"><span data-stu-id="b31af-227">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="b31af-228">Вы можете вставить `debug()` в код (например, `console.log()` инструкцию) или запустить метод из консоли DevTools.</span><span class="sxs-lookup"><span data-stu-id="b31af-228">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="b31af-229">эквивалентно установке [точки останова строки кода](#line-of-code-breakpoints) в первой строке функции.</span><span class="sxs-lookup"><span data-stu-id="b31af-229">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="b31af-230">Проверка того, что Целевая функция находится в области</span><span class="sxs-lookup"><span data-stu-id="b31af-230">Make sure the target function is in scope</span></span>   

<span data-ttu-id="b31af-231">DevTools создает исключение, `ReferenceError` Если функция, которую вы хотите отладить, не находится в области действия.</span><span class="sxs-lookup"><span data-stu-id="b31af-231">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

<span data-ttu-id="b31af-232">Убедитесь в том, что Целевая функция находится в области действия, если вы запускаете `debug()` метод из консоли DevTools.</span><span class="sxs-lookup"><span data-stu-id="b31af-232">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="b31af-233">Ниже описана одна из стратегий.</span><span class="sxs-lookup"><span data-stu-id="b31af-233">Here is one strategy:</span></span>  

1.  <span data-ttu-id="b31af-234">Установите [точку останова для строки кода](#line-of-code-breakpoints) , где находится функция в области.</span><span class="sxs-lookup"><span data-stu-id="b31af-234">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="b31af-235">Активация точки останова.</span><span class="sxs-lookup"><span data-stu-id="b31af-235">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="b31af-236">Выполняйте `debug()` метод на консоли DevTools, когда код по-прежнему придерживается в точке останова кода.</span><span class="sxs-lookup"><span data-stu-id="b31af-236">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  

 



<!-- image links -->  

[ImagePauseOnExceptionsIcon]: /microsoft-edge/devtools-guide-chromium/media/pause-on-exceptions-icon.msft.png  

[ImageLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoint-30.msft.png "Рисунок 1: точка останова в коде строки"  
[ImageConditionalLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-conditional-breakpoint.msft.png "Рисунок 2: точка останова, которая является зависимой от строки кода"  
[ImageBreakpointsPanel]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-16-33.msft.png "Рисунок 3: панель «точки останова»"  
[ImageDeactivatedBreakpoints]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png "Рисунок 4: отключенные точки останова в области "точки останова""  
[ImageDomChangeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-elements-break-on-subtree-modifications.msft.png "Рисунок 5: контекстное меню для создания точки останова по изменению модели DOM"  
[ImageXhrBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png "Рисунок 6: создание точки останова XHR"  
[ImageEventListenerBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png "Рисунок 7: создание точки останова для прослушивателя событий"  
[ImagePauseExceptionsHighlight]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-pause-on-exceptions.msft.png "Рисунок 8: кнопка "Пауза при исключениях""  
[ImageUncaughtException]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-paused-on-exception.msft.png "Рис. 9: приостанавливается на неперехваченном исключении"  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Получить API | MDN"  

> [!NOTE]
> <span data-ttu-id="b31af-248">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b31af-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b31af-249">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) и [Kayce Basques][KayceBasques] \ (технический писатель, хром DevTools & Lighthouse).</span><span class="sxs-lookup"><span data-stu-id="b31af-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b31af-251">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b31af-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

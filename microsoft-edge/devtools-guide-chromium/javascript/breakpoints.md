---
title: Приостановка кода с точки останова в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8eefea3fad894af6b66a6d7f595c5b663c03a0dc
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991187"
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







# <span data-ttu-id="e0c64-103">Приостановка кода с точки останова в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e0c64-103">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="e0c64-104">Используйте точки останова для приостановки кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e0c64-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="e0c64-105">В этом руководстве описаны все типы точек останова, доступные в DevTools, а также способы их использования и настройки каждого типа.</span><span class="sxs-lookup"><span data-stu-id="e0c64-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="e0c64-106">Практические руководства по отладке можно найти [в разделе Начало отладки JavaScript в Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="e0c64-106">For a hands-on tutorial of the debugging process, see [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="e0c64-107">Общие сведения о том, когда использовать каждый тип точки останова</span><span class="sxs-lookup"><span data-stu-id="e0c64-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="e0c64-108">Наиболее известный тип точки останова — это строка кода.</span><span class="sxs-lookup"><span data-stu-id="e0c64-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="e0c64-109">Однако точки останова для кода могут быть неэффективными для установки, особенно в том случае, если вы точно не знаете, где искать, или если вы работаете с большой базой кода.</span><span class="sxs-lookup"><span data-stu-id="e0c64-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="e0c64-110">Вы можете экономить время при отладке, зная, как и когда использовать другие типы точек останова.</span><span class="sxs-lookup"><span data-stu-id="e0c64-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="e0c64-111">Тип точки останова</span><span class="sxs-lookup"><span data-stu-id="e0c64-111">Breakpoint Type</span></span> | <span data-ttu-id="e0c64-112">Используйте этот параметр, если вы хотите приостановить...</span><span class="sxs-lookup"><span data-stu-id="e0c64-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="e0c64-113">Строка кода</span><span class="sxs-lookup"><span data-stu-id="e0c64-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="e0c64-114">В определенном регионе кода.</span><span class="sxs-lookup"><span data-stu-id="e0c64-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="e0c64-115">Условный текст</span><span class="sxs-lookup"><span data-stu-id="e0c64-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="e0c64-116">В определенном регионе кода, но только в том случае, если истинно какое – либо другое условие.</span><span class="sxs-lookup"><span data-stu-id="e0c64-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="e0c64-117">DOM</span><span class="sxs-lookup"><span data-stu-id="e0c64-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="e0c64-118">В коде, который изменяет или удаляет определенный узел DOM или дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="e0c64-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="e0c64-119">XHR</span><span class="sxs-lookup"><span data-stu-id="e0c64-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="e0c64-120">Если URL-адрес XHR имеет строковый шаблон.</span><span class="sxs-lookup"><span data-stu-id="e0c64-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="e0c64-121">Прослушиватель событий</span><span class="sxs-lookup"><span data-stu-id="e0c64-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="e0c64-122">В коде, который выполняется после события, например `click` , выполняется.</span><span class="sxs-lookup"><span data-stu-id="e0c64-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="e0c64-123">Ошибка</span><span class="sxs-lookup"><span data-stu-id="e0c64-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="e0c64-124">В строке кода, которая вызывает перехваченное или неперехваченное исключение.</span><span class="sxs-lookup"><span data-stu-id="e0c64-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="e0c64-125">Функция</span><span class="sxs-lookup"><span data-stu-id="e0c64-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="e0c64-126">Каждый раз, когда выполняется определенная команда, функция или метод.</span><span class="sxs-lookup"><span data-stu-id="e0c64-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="e0c64-127">Точки останова в коде строки</span><span class="sxs-lookup"><span data-stu-id="e0c64-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="e0c64-128">Если вы знаете точную область кода, которую нужно исследовать, используйте точку останова из строки кода.</span><span class="sxs-lookup"><span data-stu-id="e0c64-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="e0c64-129">DevTools всегда задерживается перед выполнением этой строки кода.</span><span class="sxs-lookup"><span data-stu-id="e0c64-129">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="e0c64-130">Установка точки останова в коде строки в DevTools:</span><span class="sxs-lookup"><span data-stu-id="e0c64-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="e0c64-131">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="e0c64-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e0c64-132">Откройте файл с той строкой, в которой вы хотите прервать ее.</span><span class="sxs-lookup"><span data-stu-id="e0c64-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="e0c64-133">Перейдите к строке кода.</span><span class="sxs-lookup"><span data-stu-id="e0c64-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="e0c64-134">Слева от строки кода находится столбец номер строки.</span><span class="sxs-lookup"><span data-stu-id="e0c64-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="e0c64-135">Щелкните по нему.</span><span class="sxs-lookup"><span data-stu-id="e0c64-135">Click on it.</span></span>  <span data-ttu-id="e0c64-136">Рядом со столбцом номер строки появится красный значок.</span><span class="sxs-lookup"><span data-stu-id="e0c64-136">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="e0c64-138">Точка останова строки кода</span><span class="sxs-lookup"><span data-stu-id="e0c64-138">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e0c64-139">Точки останова в коде для строк кода</span><span class="sxs-lookup"><span data-stu-id="e0c64-139">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="e0c64-140">Выполняйте `debugger` метод из вашего кода, чтобы приостановить его на этой линии.</span><span class="sxs-lookup"><span data-stu-id="e0c64-140">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="e0c64-141">Это эквивалентно [точке останова строки кода](#line-of-code-breakpoints), за исключением того, что точка останова задается в коде, а не в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="e0c64-141">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="e0c64-142">Зависимые точки останова для строк кода</span><span class="sxs-lookup"><span data-stu-id="e0c64-142">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="e0c64-143">Если вы знаете точную область кода, которую нужно исследовать, но вы хотите приостанавливать только в том случае, если какое-либо другое условие имеет значение true, используйте для нее точку останова в условном коде.</span><span class="sxs-lookup"><span data-stu-id="e0c64-143">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="e0c64-144">Установка условной точки останова для строки кода:</span><span class="sxs-lookup"><span data-stu-id="e0c64-144">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="e0c64-145">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="e0c64-145">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e0c64-146">Откройте файл с той строкой, в которой вы хотите прервать ее.</span><span class="sxs-lookup"><span data-stu-id="e0c64-146">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="e0c64-147">Перейдите к строке кода.</span><span class="sxs-lookup"><span data-stu-id="e0c64-147">Go the line of code.</span></span>  
1.  <span data-ttu-id="e0c64-148">Слева от строки кода находится столбец номер строки.</span><span class="sxs-lookup"><span data-stu-id="e0c64-148">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="e0c64-149">Щелкните правой кнопкой мыши номер строки.</span><span class="sxs-lookup"><span data-stu-id="e0c64-149">Right-click the line number.</span></span>  
1.  <span data-ttu-id="e0c64-150">Нажмите кнопку **добавить условную точку останова**.</span><span class="sxs-lookup"><span data-stu-id="e0c64-150">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="e0c64-151">Под строкой кода появится диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e0c64-151">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="e0c64-152">Введите условие в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e0c64-152">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="e0c64-153">Нажмите `Enter` , чтобы активировать точку останова.</span><span class="sxs-lookup"><span data-stu-id="e0c64-153">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="e0c64-154">Значок рядом со столбцом "номер строки".</span><span class="sxs-lookup"><span data-stu-id="e0c64-154">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Условная точка останова для строки кода" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="e0c64-156">Условная точка останова для строки кода</span><span class="sxs-lookup"><span data-stu-id="e0c64-156">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e0c64-157">Управление точками останова для строк кода</span><span class="sxs-lookup"><span data-stu-id="e0c64-157">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="e0c64-158">С помощью области " **точки останова** " можно отключить или удалить точки останова для строк кода из одного места.</span><span class="sxs-lookup"><span data-stu-id="e0c64-158">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Панель «точки останова»" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="e0c64-160">Панель « **точки останова** »</span><span class="sxs-lookup"><span data-stu-id="e0c64-160">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="e0c64-161">Установите флажок рядом с записью, чтобы отключить эту точку останова.</span><span class="sxs-lookup"><span data-stu-id="e0c64-161">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="e0c64-162">Щелкните правой кнопкой мыши запись для удаления точки останова.</span><span class="sxs-lookup"><span data-stu-id="e0c64-162">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="e0c64-163">Щелкните правой кнопкой мыши в любом месте области **точки останова** , чтобы отключить все точки останова, отключить все точки останова или удалить все точки останова.</span><span class="sxs-lookup"><span data-stu-id="e0c64-163">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="e0c64-164">Отключение всех точек останова эквивалентно депроверке каждого из них.</span><span class="sxs-lookup"><span data-stu-id="e0c64-164">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="e0c64-165">Отключение всех точек останова дает указание DevTools игнорировать все точки останова для строк кода, а также поддерживать состояние включения, чтобы каждый из них нав одном и том же состоянии до повторной активации каждой из них.</span><span class="sxs-lookup"><span data-stu-id="e0c64-165">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Деактивированные точки останова на панели "точки останова"" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="e0c64-167">Деактивированные точки останова на панели " **точки останова** "</span><span class="sxs-lookup"><span data-stu-id="e0c64-167">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0c64-168">Точки останова по изменению модели DOM</span><span class="sxs-lookup"><span data-stu-id="e0c64-168">DOM change breakpoints</span></span>   

<span data-ttu-id="e0c64-169">Чтобы приостановить выполнение кода, который изменяет узел DOM или дочерние элементы, используйте точку останова изменения модели DOM.</span><span class="sxs-lookup"><span data-stu-id="e0c64-169">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="e0c64-170">Настройка точки останова для изменения модели DOM.</span><span class="sxs-lookup"><span data-stu-id="e0c64-170">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="e0c64-171">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="e0c64-171">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="e0c64-172">Перейдите к элементу, для которого вы хотите установить точку останова.</span><span class="sxs-lookup"><span data-stu-id="e0c64-172">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="e0c64-173">Щелкните элемент правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="e0c64-173">Right-click the element.</span></span>  
1.  <span data-ttu-id="e0c64-174">Наведите указатель мыши **на пункт разрыв**, а затем выберите **изменения поддерева**, **изменения атрибутов**или **Удаление узла**.</span><span class="sxs-lookup"><span data-stu-id="e0c64-174">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Контекстное меню для создания точки останова по изменению модели DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="e0c64-176">Контекстное меню для создания точки останова по изменению модели DOM</span><span class="sxs-lookup"><span data-stu-id="e0c64-176">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e0c64-177">Типы точек останова для изменения модели DOM</span><span class="sxs-lookup"><span data-stu-id="e0c64-177">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="e0c64-178">**Изменения поддерева**.</span><span class="sxs-lookup"><span data-stu-id="e0c64-178">**Subtree modifications**.</span></span>  <span data-ttu-id="e0c64-179">Вызывается при удалении или добавлении дочернего узла, выбранного в данный момент, или изменении содержимого дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="e0c64-179">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="e0c64-180">Не инициируется для изменений атрибутов дочернего узла или при любых изменениях в выбранном в данный момент узле.</span><span class="sxs-lookup"><span data-stu-id="e0c64-180">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="e0c64-181">**Изменения атрибутов**: активируется при добавлении или удалении атрибута на текущем выбранном узле или изменении значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="e0c64-181">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="e0c64-182">**Удаление узла**: активируется при удалении текущего выбранного узла.</span><span class="sxs-lookup"><span data-stu-id="e0c64-182">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="e0c64-183">Точки останова XHR и FETCH</span><span class="sxs-lookup"><span data-stu-id="e0c64-183">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="e0c64-184">Используйте точку останова XHR, когда нужно прервать, когда URL-адрес запроса XHR содержат указанную строку.</span><span class="sxs-lookup"><span data-stu-id="e0c64-184">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="e0c64-185">DevTools приостанавливается на строке кода, где XHR запускает `send()` метод.</span><span class="sxs-lookup"><span data-stu-id="e0c64-185">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="e0c64-186">Эта функция также работает для запросов [API FETCH][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="e0c64-186">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="e0c64-187">Это может быть полезно, если вы видите, что ваша страница запрашивает неверный URL-адрес, и вам нужно быстро найти исходный код AJAX или FETCH, вызывающий неверный запрос.</span><span class="sxs-lookup"><span data-stu-id="e0c64-187">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="e0c64-188">Чтобы установить точку останова XHR, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e0c64-188">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="e0c64-189">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="e0c64-189">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e0c64-190">Разверните область **точки останова XHR** .</span><span class="sxs-lookup"><span data-stu-id="e0c64-190">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="e0c64-191">Нажмите кнопку **Добавить точку останова**.</span><span class="sxs-lookup"><span data-stu-id="e0c64-191">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="e0c64-192">Введите строку, на которой вы хотите приостановить.</span><span class="sxs-lookup"><span data-stu-id="e0c64-192">Enter the string which you want to break on.</span></span>  <span data-ttu-id="e0c64-193">DevTools приостанавливает работу, когда эта строка отображается в любом месте URL-адреса запроса XHR.</span><span class="sxs-lookup"><span data-stu-id="e0c64-193">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="e0c64-194">Нажмите кнопку `Enter` , чтобы подтвердить.</span><span class="sxs-lookup"><span data-stu-id="e0c64-194">Press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Создание точки останова XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="e0c64-196">Создание точки останова XHR</span><span class="sxs-lookup"><span data-stu-id="e0c64-196">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0c64-197">Точки останова прослушивателя событий</span><span class="sxs-lookup"><span data-stu-id="e0c64-197">Event listener breakpoints</span></span> 

<span data-ttu-id="e0c64-198">Используйте точки останова прослушивателя событий, когда необходимо приостановить выполнение кода прослушивателя событий, который выполняется после срабатывания события.</span><span class="sxs-lookup"><span data-stu-id="e0c64-198">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="e0c64-199">Вы можете выбрать определенные события, такие как `click` или категории событий, например все события мыши.</span><span class="sxs-lookup"><span data-stu-id="e0c64-199">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="e0c64-200">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="e0c64-200">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e0c64-201">Разверните область **точки останова для прослушивателя событий** .</span><span class="sxs-lookup"><span data-stu-id="e0c64-201">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="e0c64-202">DevTools отображает список категорий событий, например **анимацию**.</span><span class="sxs-lookup"><span data-stu-id="e0c64-202">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="e0c64-203">Отметьте одну из этих категорий, чтобы приостановить любое событие из этой категории, или развернуть категорию и проверить определенное событие.</span><span class="sxs-lookup"><span data-stu-id="e0c64-203">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Создание точки останова для прослушивателя событий" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="e0c64-205">Создание точки останова для прослушивателя событий</span><span class="sxs-lookup"><span data-stu-id="e0c64-205">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0c64-206">Точки останова для исключений</span><span class="sxs-lookup"><span data-stu-id="e0c64-206">Exception breakpoints</span></span>   

<span data-ttu-id="e0c64-207">Используйте точки останова, когда нужно приостановить выполнение в строке кода, которая вызывает перехваченное или неперехваченное исключение.</span><span class="sxs-lookup"><span data-stu-id="e0c64-207">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="e0c64-208">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="e0c64-208">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e0c64-209">Нажмите кнопку **Pause on Exceptions** \ ( ![ Pause on Exceptions ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e0c64-209">Click **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="e0c64-210">При включении значок становится синей.</span><span class="sxs-lookup"><span data-stu-id="e0c64-210">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Кнопка "Пауза при исключениях"" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="e0c64-212">Кнопка " **Пауза при исключениях** "</span><span class="sxs-lookup"><span data-stu-id="e0c64-212">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0c64-213">**Необязательный**.</span><span class="sxs-lookup"><span data-stu-id="e0c64-213">**Optional**.</span></span>  <span data-ttu-id="e0c64-214">Установите флажок **приостановить на перехваченных исключениях** , если вы также хотите приостанавливать на перехваченных исключениях помимо неперехваченных.</span><span class="sxs-lookup"><span data-stu-id="e0c64-214">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Приостановлено при неперехваченном исключении" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="e0c64-216">Приостановлено при неперехваченном исключении</span><span class="sxs-lookup"><span data-stu-id="e0c64-216">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0c64-217">Точки останова по функциям</span><span class="sxs-lookup"><span data-stu-id="e0c64-217">Function breakpoints</span></span>   

<span data-ttu-id="e0c64-218">Выполняйте `debug(method)` метод, где `method` — команда, функция или метод, для которого нужно выполнить отладку, когда вы хотите приостановить каждый раз при запуске определенной функции.</span><span class="sxs-lookup"><span data-stu-id="e0c64-218">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="e0c64-219">Вы можете вставить `debug()` в код (например, `console.log()` инструкцию) или запустить метод из консоли DevTools.</span><span class="sxs-lookup"><span data-stu-id="e0c64-219">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="e0c64-220">эквивалентно установке [точки останова строки кода](#line-of-code-breakpoints) в первой строке функции.</span><span class="sxs-lookup"><span data-stu-id="e0c64-220">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="e0c64-221">Проверка того, что Целевая функция находится в области</span><span class="sxs-lookup"><span data-stu-id="e0c64-221">Make sure the target function is in scope</span></span>   

<span data-ttu-id="e0c64-222">DevTools создает исключение, `ReferenceError` Если функция, которую вы хотите отладить, не находится в области действия.</span><span class="sxs-lookup"><span data-stu-id="e0c64-222">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="e0c64-223">Убедитесь в том, что Целевая функция находится в области действия, если вы запускаете `debug()` метод из консоли DevTools.</span><span class="sxs-lookup"><span data-stu-id="e0c64-223">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="e0c64-224">Ниже описана одна из стратегий.</span><span class="sxs-lookup"><span data-stu-id="e0c64-224">Here is one strategy:</span></span>  

1.  <span data-ttu-id="e0c64-225">Установите [точку останова для строки кода](#line-of-code-breakpoints) , где находится функция в области.</span><span class="sxs-lookup"><span data-stu-id="e0c64-225">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="e0c64-226">Активация точки останова.</span><span class="sxs-lookup"><span data-stu-id="e0c64-226">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="e0c64-227">Выполняйте `debug()` метод на консоли DevTools, когда код по-прежнему придерживается в точке останова кода.</span><span class="sxs-lookup"><span data-stu-id="e0c64-227">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools | Документы Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Получить API | MDN"  

> [!NOTE]
> <span data-ttu-id="e0c64-230">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e0c64-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e0c64-231">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e0c64-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e0c64-233">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e0c64-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

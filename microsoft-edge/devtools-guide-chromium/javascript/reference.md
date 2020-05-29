---
title: Справочник по отладке JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 1d361bb39523e9b039500f46da54e60b82adbda6
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581742"
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







# <span data-ttu-id="679e4-103">Справочник по отладке JavaScript</span><span class="sxs-lookup"><span data-stu-id="679e4-103">JavaScript Debugging Reference</span></span>   



<span data-ttu-id="679e4-104">Вы узнаете о новых рабочих процессах отладки с полным справочником по функциям отладки Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="679e4-104">Discover new debugging workflows with this comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="679e4-105">Подробнее об отладке можно найти [в статье Начало работы с отладкой JavaScript в Microsoft Edge DevTools][DevToolsJavascriptGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="679e4-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="679e4-106">Приостановка кода с точки останова</span><span class="sxs-lookup"><span data-stu-id="679e4-106">Pause code with breakpoints</span></span>   

<span data-ttu-id="679e4-107">Установите точку останова, чтобы можно было приостановить выполнение кода в середине среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="679e4-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="679e4-108">Сведения о том, как задавать точки останова, можно найти в разделе [приостановка кода с точки останова][DevToolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="679e4-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Приостановка кода с точки останова в Microsoft Edge DevTools"  

## <span data-ttu-id="679e4-110">Пошаговое руководство по коду</span><span class="sxs-lookup"><span data-stu-id="679e4-110">Step through code</span></span>   

<span data-ttu-id="679e4-111">Когда код приостанавливается, проведите по одной строке за раз, изменяя поток управления и значения свойств по своему пути.</span><span class="sxs-lookup"><span data-stu-id="679e4-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="679e4-112">Шаг с заходом в строке кода</span><span class="sxs-lookup"><span data-stu-id="679e4-112">Step over line of code</span></span>   

<span data-ttu-id="679e4-113">При приостановке на строке, содержащей функцию, не относящуюся к проблеме, которую вы отлаживается, щелкните значок " **шаг за** ![ шагом", ][ImageStepOverIcon] чтобы запустить функцию без пошаговой отладки.</span><span class="sxs-lookup"><span data-stu-id="679e4-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click on the **Step over** ![Step over][ImageStepOverIcon] icon to run the function without stepping into it.</span></span>  

> ##### <span data-ttu-id="679e4-114">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="679e4-114">Figure 1</span></span>  
> <span data-ttu-id="679e4-115">Выбор **пункта "шаг за шагом** "</span><span class="sxs-lookup"><span data-stu-id="679e4-115">Selecting **Step over**</span></span>  
> ![Выбор пункта "шаг за шагом"][ImageSelectingStepOver]  

<span data-ttu-id="679e4-117">Например, предположим, что выполняется отладка следующего кода:</span><span class="sxs-lookup"><span data-stu-id="679e4-117">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

<span data-ttu-id="679e4-118">Вы приостанавливаете `A` .</span><span class="sxs-lookup"><span data-stu-id="679e4-118">You are paused on `A`.</span></span>  <span data-ttu-id="679e4-119">Нажимая клавишу " **шаг за шагом**", DevTools запускает весь код в функции, для которой выполняется пошаговое выполнение, `B` а именно `C` .</span><span class="sxs-lookup"><span data-stu-id="679e4-119">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="679e4-120">Затем DevTools приостанавливает `D` .</span><span class="sxs-lookup"><span data-stu-id="679e4-120">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="679e4-121">Шаг с заходом в строку кода</span><span class="sxs-lookup"><span data-stu-id="679e4-121">Step into line of code</span></span>   

<span data-ttu-id="679e4-122">При приостановке в строке кода, содержащей вызов функции, связанный с проблемой, в которой выполняется отладка, щелкните значок **шаг** с заходом, ![ ][ImageStepIntoIcon] чтобы более подробно изучить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="679e4-122">When paused on a line of code containing a function call that is related to the problem you are debugging, click on the **Step into** ![Step into][ImageStepIntoIcon] icon to investigate that function further.</span></span>  

> ##### <span data-ttu-id="679e4-123">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="679e4-123">Figure 2</span></span>  
> <span data-ttu-id="679e4-124">Выбор **шага**</span><span class="sxs-lookup"><span data-stu-id="679e4-124">Selecting **Step into**</span></span>  
> ![Выбор шага][ImageSelectingStepInto]  

<span data-ttu-id="679e4-126">Например, предположим, что выполняется отладка следующего кода:</span><span class="sxs-lookup"><span data-stu-id="679e4-126">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

<span data-ttu-id="679e4-127">Вы приостанавливаете `A` .</span><span class="sxs-lookup"><span data-stu-id="679e4-127">You are paused on `A`.</span></span>  <span data-ttu-id="679e4-128">Нажимая кнопку " **Шаг с заходом**", DevTools запускает эту строку кода, а затем приостанавливает выполнение `B` .</span><span class="sxs-lookup"><span data-stu-id="679e4-128">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="679e4-129">Пошаговое руководство из строки кода</span><span class="sxs-lookup"><span data-stu-id="679e4-129">Step out of line of code</span></span>   

<span data-ttu-id="679e4-130">При приостановке внутри функции, которая не связана с проблемой, которую вы выполняете Отладка, щелкните значок **шаг** с выходом, ![ ][ImageStepOutIcon] чтобы выполнить оставшуюся часть кода функции.</span><span class="sxs-lookup"><span data-stu-id="679e4-130">When paused inside of a function that is not related to the problem you are debugging, click on the **Step out** ![Step out][ImageStepOutIcon] icon to run the rest of the code of the function.</span></span>  

> ##### <span data-ttu-id="679e4-131">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="679e4-131">Figure 3</span></span>  
> <span data-ttu-id="679e4-132">Выбор **пункта "шаг с выходом** "</span><span class="sxs-lookup"><span data-stu-id="679e4-132">Selecting **Step out**</span></span>  
> ![Выбор пункта "шаг с выходом"][ImageSelectingStepOut]  

<span data-ttu-id="679e4-134">Например, предположим, что выполняется отладка следующего кода:</span><span class="sxs-lookup"><span data-stu-id="679e4-134">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

<span data-ttu-id="679e4-135">Вы приостанавливаете `A` .</span><span class="sxs-lookup"><span data-stu-id="679e4-135">You are paused on `A`.</span></span>  <span data-ttu-id="679e4-136">Нажимая кнопку " **Шаг с выходом**", DevTools запускает оставшуюся часть кода в `getName()` `B` этом примере, а затем приостанавливает выполнение `C` .</span><span class="sxs-lookup"><span data-stu-id="679e4-136">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="679e4-137">Выполнение всего кода до определенной строки</span><span class="sxs-lookup"><span data-stu-id="679e4-137">Run all code up to a specific line</span></span>   

<span data-ttu-id="679e4-138">При отладке длительных функций может возникнуть большой объем кода, не относящегося к той проблеме, которую вы размещаете в отладке.</span><span class="sxs-lookup"><span data-stu-id="679e4-138">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="679e4-139">Вы можете пошагово пройти все строки, но это утомительно.</span><span class="sxs-lookup"><span data-stu-id="679e4-139">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="679e4-140">Вы можете указать точку останова для строки кода в строке, в которой вы заинтересованы, и нажать на значок возобновления сценария "возобновить **выполнение** скрипта" ![ ][ImageResumeScriptExecutionIcon] , но это быстрее.</span><span class="sxs-lookup"><span data-stu-id="679e4-140">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon, but there is a faster way.</span></span>  

<span data-ttu-id="679e4-141">Щелкните правой кнопкой мыши строку кода, в которой вы хотите заинтересовать, и выберите команду **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="679e4-141">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="679e4-142">DevTools запускает весь код до этого момента, а затем приостанавливает выполнение на этой линии.</span><span class="sxs-lookup"><span data-stu-id="679e4-142">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

> ##### <span data-ttu-id="679e4-143">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="679e4-143">Figure 4</span></span>  
> <span data-ttu-id="679e4-144">Выбор варианта **"перейти сюда"**</span><span class="sxs-lookup"><span data-stu-id="679e4-144">Selecting **Continue to here**</span></span>  
> ![Выбор варианта "перейти сюда"][ImageSelectingContinueToHere]  

### <span data-ttu-id="679e4-146">Перезапустить функцию TOP в стеке вызовов</span><span class="sxs-lookup"><span data-stu-id="679e4-146">Restart the top function of the call stack</span></span>   

<span data-ttu-id="679e4-147">Наведя указатель на строку кода, щелкните правой кнопкой мыши в любом месте области **стека звонков** и выберите команду **перезапустить кадр** , чтобы приостановить работу на первой строке функции Top в стеке вызовов.</span><span class="sxs-lookup"><span data-stu-id="679e4-147">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="679e4-148">Функция Top — это последняя вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="679e4-148">The top function is the last function that was called.</span></span>  

<span data-ttu-id="679e4-149">Например, предположим, что выполняется пошаговое выполнение следующего кода:</span><span class="sxs-lookup"><span data-stu-id="679e4-149">For example, suppose you are stepping through the following code:</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="679e4-150">Вы приостанавливаете `A` .</span><span class="sxs-lookup"><span data-stu-id="679e4-150">You are paused on `A`.</span></span>  <span data-ttu-id="679e4-151">После нажатия кнопки **перезапустить**вы должны быть приостановлены `B` , пока не задана точка останова или нажата клавиша **возобновления выполнения сценария**.</span><span class="sxs-lookup"><span data-stu-id="679e4-151">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

> ##### <span data-ttu-id="679e4-152">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="679e4-152">Figure 5</span></span>  
> <span data-ttu-id="679e4-153">Выбор **перезапуска кадра**</span><span class="sxs-lookup"><span data-stu-id="679e4-153">Selecting **Restart Frame**</span></span>  
> ![Выбор перезапуска кадра][ImageSelectingRestartFrame]  

### <span data-ttu-id="679e4-155">Среда выполнения сценария возобновления</span><span class="sxs-lookup"><span data-stu-id="679e4-155">Resume script runtime</span></span>   

<span data-ttu-id="679e4-156">Чтобы продолжить выполнение после паузы в сценарии, щелкните значок "возобновить **сценарий запуска сценария** " ![ ][ImageResumeScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="679e4-156">To continue the runtime after a pause of your script, click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon.</span></span>  <span data-ttu-id="679e4-157">DevTools запускает сценарий до следующей точки останова (при наличии).</span><span class="sxs-lookup"><span data-stu-id="679e4-157">DevTools runs the script up until the next breakpoint, if any.</span></span>  

> ##### <span data-ttu-id="679e4-158">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="679e4-158">Figure 6</span></span>  
> <span data-ttu-id="679e4-159">Выбор **выполнения скрипта возобновления**</span><span class="sxs-lookup"><span data-stu-id="679e4-159">Selecting **Resume script execution**</span></span>  
> ![Выбор выполнения скрипта возобновления][ImageSelectingResumeScriptExecution]  

#### <span data-ttu-id="679e4-161">Выполнение принудительного выполнения сценария</span><span class="sxs-lookup"><span data-stu-id="679e4-161">Force script runtime</span></span>   

<span data-ttu-id="679e4-162">Чтобы пропустить все точки останова и принудительно возобновить выполнение сценария, нажмите и удерживайте значок возобновления **сценария "возобновить выполнение** скрипта", ![ ][ImageResumeScriptExecutionIcon] а затем выберите команду **принудительное** ![ выполнение сценария принудительной обработки ][ImageForceScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="679e4-162">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon and then select **Force script execution** ![Force script execution][ImageForceScriptExecutionIcon].</span></span>  

> ##### <span data-ttu-id="679e4-163">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="679e4-163">Figure 7</span></span>  
> <span data-ttu-id="679e4-164">Выбор **принудительного выполнения сценария**</span><span class="sxs-lookup"><span data-stu-id="679e4-164">Selecting **Force script execution**</span></span>  
> ![Выбор принудительного выполнения сценария][ImageSelectingForceScriptExecution]  

### <span data-ttu-id="679e4-166">Изменить контекст потока</span><span class="sxs-lookup"><span data-stu-id="679e4-166">Change thread context</span></span>   

<span data-ttu-id="679e4-167">При работе с веб-сотрудниками или сотрудниками служб щелкните контекст, указанный в области **потоки** , чтобы переключиться на этот контекст.</span><span class="sxs-lookup"><span data-stu-id="679e4-167">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="679e4-168">Синий значок стрелки соответствует контексту, выбранному в данный момент.</span><span class="sxs-lookup"><span data-stu-id="679e4-168">The blue arrow icon represents which context is currently selected.</span></span>  

> ##### <span data-ttu-id="679e4-169">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="679e4-169">Figure 8</span></span>  
> <span data-ttu-id="679e4-170">Область « **потоки** »</span><span class="sxs-lookup"><span data-stu-id="679e4-170">The **Threads** pane</span></span>  
> ![Область «потоки»][ImageThreadsPane]  

<span data-ttu-id="679e4-172">Например, предположим, что вы придерживаетесь точки останова как в основном, так и на рабочем скрипте службы.</span><span class="sxs-lookup"><span data-stu-id="679e4-172">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="679e4-173">Вы хотите просмотреть локальные и глобальные свойства для контекста рабочего процесса службы, но на панели **источники** отображается контекст основного сценария.</span><span class="sxs-lookup"><span data-stu-id="679e4-173">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="679e4-174">Нажимая кнопку "сервисный рабочий процесс" на панели " **потоки** ", вы сможете перейти в этот контекст.</span><span class="sxs-lookup"><span data-stu-id="679e4-174">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="679e4-175">Просмотр и изменение локальных, закрытых и глобальных свойств</span><span class="sxs-lookup"><span data-stu-id="679e4-175">View and edit local, closure, and global properties</span></span>   

<span data-ttu-id="679e4-176">При приостановке в строке кода используйте область **область** для просмотра и изменения значений свойств и переменных в локальных, закрытых и глобальных областях.</span><span class="sxs-lookup"><span data-stu-id="679e4-176">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="679e4-177">Дважды щелкните значение свойства, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="679e4-177">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="679e4-178">Неперечислимые свойства затенены.</span><span class="sxs-lookup"><span data-stu-id="679e4-178">Non-enumerable properties are greyed out.</span></span>  

> ##### <span data-ttu-id="679e4-179">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="679e4-179">Figure 9</span></span>  
> <span data-ttu-id="679e4-180">Область " **область** "</span><span class="sxs-lookup"><span data-stu-id="679e4-180">The **Scope** pane</span></span>  
> ![Область "область"][ImageScopePane]  

## <span data-ttu-id="679e4-182">Просмотр текущего стека вызовов</span><span class="sxs-lookup"><span data-stu-id="679e4-182">View the current call stack</span></span>   

<span data-ttu-id="679e4-183">При приостановке на строке кода используйте область **Стек вызовов** для просмотра стека вызовов, в котором вы набрались этим моментом.</span><span class="sxs-lookup"><span data-stu-id="679e4-183">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="679e4-184">Щелкните запись, чтобы перейти к строке кода, в которой была вызвана эта функция.</span><span class="sxs-lookup"><span data-stu-id="679e4-184">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="679e4-185">Синий значок стрелки показывает, какая функция DevTools выделяется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="679e4-185">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

> ##### <span data-ttu-id="679e4-186">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="679e4-186">Figure 10</span></span>  
> <span data-ttu-id="679e4-187">Область « **Стек вызовов** »</span><span class="sxs-lookup"><span data-stu-id="679e4-187">The **Call Stack** pane</span></span>  
> ![Область «стек вызовов»][ImageCallStackPane]  

> [!NOTE]
> <span data-ttu-id="679e4-189">Если в строке кода не присвоена значение, область **стека вызовов** пуста.</span><span class="sxs-lookup"><span data-stu-id="679e4-189">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="679e4-190">Копирование трассировки стека</span><span class="sxs-lookup"><span data-stu-id="679e4-190">Copy stack trace</span></span>   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="679e4-191">Щелкните правой кнопкой мыши в любом месте области **стека звонков** и выберите команду **Копировать трассировку стека** , чтобы скопировать текущий стек вызовов в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="679e4-191">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

> ##### <span data-ttu-id="679e4-192">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="679e4-192">Figure 11</span></span>  
> <span data-ttu-id="679e4-193">Выбор пункта « **Копировать трассировку стека** »</span><span class="sxs-lookup"><span data-stu-id="679e4-193">Selecting **Copy Stack Trace**</span></span>  
> ![Выбор пункта «Копировать трассировку стека»][ImageSelectingCopyStackTrace]  

<span data-ttu-id="679e4-195">Ниже приведен пример выходных данных.</span><span class="sxs-lookup"><span data-stu-id="679e4-195">Below is an example of the output:</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="679e4-196">Игнорировать сценарий или шаблон сценариев</span><span class="sxs-lookup"><span data-stu-id="679e4-196">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="679e4-197">Помечайте сценарий как код библиотеки, если вы хотите пропустить этот сценарий во время отладки.</span><span class="sxs-lookup"><span data-stu-id="679e4-197">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="679e4-198">При пометке в виде кода библиотеки сценарий скрывается в области **стека вызовов** , и вы никогда не просматриваете функции сценария при пошаговом выполнении кода.</span><span class="sxs-lookup"><span data-stu-id="679e4-198">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="679e4-199">Например, предположим, что выполняется пошаговое выполнение следующего кода:</span><span class="sxs-lookup"><span data-stu-id="679e4-199">For example, suppose you are stepping through this code:</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="679e4-200">— это библиотека стороннего поставщика, которой вы доверяете.</span><span class="sxs-lookup"><span data-stu-id="679e4-200">is a third-party library that you trust.</span></span>  <span data-ttu-id="679e4-201">Если вы уверены, что проблема, выполняемая при отладке, не связана с библиотекой стороннего поставщика, имеет смысл помечать сценарий как **код библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="679e4-201">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="679e4-202">Пометка сценария как кода библиотеки в области "редактор"</span><span class="sxs-lookup"><span data-stu-id="679e4-202">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="679e4-203">Чтобы помечать сценарий как **код библиотеки** на панели " **Редактор** ", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="679e4-203">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="679e4-204">Откройте файл.</span><span class="sxs-lookup"><span data-stu-id="679e4-204">Open the file.</span></span>  
1.  <span data-ttu-id="679e4-205">Щелкните правой кнопкой мыши в любом месте.</span><span class="sxs-lookup"><span data-stu-id="679e4-205">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="679e4-206">Нажмите кнопку **помечать как код библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="679e4-206">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="679e4-207">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="679e4-207">Figure 12</span></span>  
> <span data-ttu-id="679e4-208">Пометка сценария как **кода библиотеки** в области " **Редактор** "</span><span class="sxs-lookup"><span data-stu-id="679e4-208">Marking a script as **Library code** from the **Editor** pane</span></span>  
> ![Пометка сценария как кода библиотеки в области "редактор"][ImageMarkEditorPane]  

### <span data-ttu-id="679e4-210">Пометка сценария как кода библиотеки на панели «стек вызовов»</span><span class="sxs-lookup"><span data-stu-id="679e4-210">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="679e4-211">Чтобы помечать сценарий как **код библиотеки** на панели « **стек звонков** », выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="679e4-211">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="679e4-212">Щелкните правой кнопкой мыши функцию в сценарии.</span><span class="sxs-lookup"><span data-stu-id="679e4-212">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="679e4-213">Нажмите кнопку **помечать как код библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="679e4-213">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="679e4-214">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="679e4-214">Figure 13</span></span>  
> <span data-ttu-id="679e4-215">Пометка сценария как **кода библиотеки** на панели « **Стек вызовов** »</span><span class="sxs-lookup"><span data-stu-id="679e4-215">Marking a script as **Library code** from the **Call Stack** pane</span></span>  
> ![Пометка сценария как кода библиотеки на панели «стек вызовов»][ImageMarkCallStackPane]  

### <span data-ttu-id="679e4-217">Пометка сценария как кода библиотеки из параметров</span><span class="sxs-lookup"><span data-stu-id="679e4-217">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="679e4-218">Чтобы помечать один сценарий или шаблон сценариев из параметров, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="679e4-218">To mark a single script or pattern of scripts from Settings:</span></span>  

1.  <span data-ttu-id="679e4-219">Откройте [Параметры][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="679e4-219">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="679e4-220">Перейдите на вкладку **код библиотеки** .</span><span class="sxs-lookup"><span data-stu-id="679e4-220">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="679e4-221">Нажмите кнопку **Добавить узор**.</span><span class="sxs-lookup"><span data-stu-id="679e4-221">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="679e4-222">Введите имя сценария или шаблон регулярного выражения для имен сценариев, чтобы помечать его как **код библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="679e4-222">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="679e4-223">Щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="679e4-223">Click **Add**.</span></span>  

> ##### <span data-ttu-id="679e4-224">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="679e4-224">Figure 14</span></span>  
> <span data-ttu-id="679e4-225">Пометка сценария как **кода библиотеки** из параметров</span><span class="sxs-lookup"><span data-stu-id="679e4-225">Marking a script as **Library code** from Settings</span></span>  
> ![Пометка сценария как кода библиотеки из параметров][ImageMarkScriptSettings]  

## <span data-ttu-id="679e4-227">Выполнение фрагментов кода отладки на любой странице</span><span class="sxs-lookup"><span data-stu-id="679e4-227">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="679e4-228">Если вы обнаружите, что вы используете один и тот же код отладки в консоли, рассматривайте фрагменты кода.</span><span class="sxs-lookup"><span data-stu-id="679e4-228">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="679e4-229">Фрагменты — это сценарии среды выполнения, созданные, сохраняемые и выполняемые в DevTools.</span><span class="sxs-lookup"><span data-stu-id="679e4-229">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="679e4-230">Дополнительные сведения можно найти в разделе [выполнение фрагментов кода на любой странице][DevToolsJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="679e4-230">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="679e4-231">Просмотр значений настраиваемых выражений JavaScript</span><span class="sxs-lookup"><span data-stu-id="679e4-231">Watch the values of custom JavaScript expressions</span></span>   

<span data-ttu-id="679e4-232">Используйте область **контрольных** значений для просмотра значений настраиваемых выражений.</span><span class="sxs-lookup"><span data-stu-id="679e4-232">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="679e4-233">Вы можете просмотреть любое допустимое выражение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="679e4-233">You may watch any valid JavaScript expression.</span></span>  

> ##### <span data-ttu-id="679e4-234">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="679e4-234">Figure 15</span></span>  
> <span data-ttu-id="679e4-235">Область **контрольных значений**</span><span class="sxs-lookup"><span data-stu-id="679e4-235">The **Watch** pane</span></span>  
> ![Область контрольных значений][ImageWatchPane]  

*   <span data-ttu-id="679e4-237">Щелкните значок Добавить **выражение** ![ Добавить выражение ][ImageAddExpressionIcon] , чтобы создать новое выражение контрольного значения.</span><span class="sxs-lookup"><span data-stu-id="679e4-237">Click on the **Add Expression** ![Add Expression][ImageAddExpressionIcon] icon to create a new watch expression.</span></span>  
*   <span data-ttu-id="679e4-238">Щелкните значок **обновления** обновления ![ ][ImageRefreshIcon] , чтобы обновить значения всех существующих выражений.</span><span class="sxs-lookup"><span data-stu-id="679e4-238">Click on the **Refresh** ![Refresh][ImageRefreshIcon] icon to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="679e4-239">Значения автоматически обновляются при пошаговом выполнении кода.</span><span class="sxs-lookup"><span data-stu-id="679e4-239">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="679e4-240">Наведите указатель мыши на выражение и щелкните значок **Удалить** выражение удаления выражения, ![ ][ImageDeleteExpressionIcon] чтобы удалить его.</span><span class="sxs-lookup"><span data-stu-id="679e4-240">Hover over an expression and click on the **Delete Expression** ![Delete Expression][ImageDeleteExpressionIcon] icon to delete it.</span></span>  

## <span data-ttu-id="679e4-241">Создание читаемого файла minified</span><span class="sxs-lookup"><span data-stu-id="679e4-241">Make a minified file readable</span></span>   

<span data-ttu-id="679e4-242">Щелкните значок формата **формата** ![ ][ImageFormatIcon] , чтобы сделать файл minified удобным для чтения.</span><span class="sxs-lookup"><span data-stu-id="679e4-242">Click on the **Format** ![Format][ImageFormatIcon] icon to make a minified file human-readable.</span></span>  

> ##### <span data-ttu-id="679e4-243">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="679e4-243">Figure 16</span></span>  
> <span data-ttu-id="679e4-244">Кнопка " **Формат** "</span><span class="sxs-lookup"><span data-stu-id="679e4-244">The **Format** button</span></span>  
> ![Кнопка "формат"][ImageFormat]  

## <span data-ttu-id="679e4-246">Изменение сценария</span><span class="sxs-lookup"><span data-stu-id="679e4-246">Edit a script</span></span>   

<span data-ttu-id="679e4-247">При исправлении ошибки часто требуется протестировать некоторые изменения в коде JavaScript.</span><span class="sxs-lookup"><span data-stu-id="679e4-247">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="679e4-248">Вам не нужно вносить изменения в внешний редактор или интегрированную среду разработки и повторно загрузить страницу.</span><span class="sxs-lookup"><span data-stu-id="679e4-248">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="679e4-249">Вы можете редактировать сценарий в DevTools.</span><span class="sxs-lookup"><span data-stu-id="679e4-249">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="679e4-250">Чтобы изменить сценарий, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="679e4-250">To edit a script:</span></span>  

1.  <span data-ttu-id="679e4-251">Откройте файл в области " **Редактор** " на панели " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="679e4-251">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="679e4-252">Внесите изменения в область " **Редактор** ".</span><span class="sxs-lookup"><span data-stu-id="679e4-252">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="679e4-253">Чтобы сохранить, нажмите клавиши `Ctrl` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="679e4-253">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="679e4-254">DevTools заменяет весь JS – файл в механизме JavaScript Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="679e4-254">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  

> ##### <span data-ttu-id="679e4-255">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="679e4-255">Figure 17</span></span>  
> <span data-ttu-id="679e4-256">Область " **Редактор** "</span><span class="sxs-lookup"><span data-stu-id="679e4-256">The **Editor** pane</span></span>  
> ![Область "редактор"][ImageEditorPane]  

## <span data-ttu-id="679e4-258">Отключение JavaScript</span><span class="sxs-lookup"><span data-stu-id="679e4-258">Disable JavaScript</span></span>   

<span data-ttu-id="679e4-259">[В разделе Отключение JavaScript с Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="679e4-259">See [Disable JavaScript With Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageStepIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageStepOutIcon]: /microsoft-edge/devtools-guide-chromium/media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-expression-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  

[ImageSelectingStepOver]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-over-next-function-call.msft.png "Рисунок 1: выбор пункта "шаг за шагом""  
[ImageSelectingStepInto]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-into-next-function-call.msft.png "Рисунок 2: выбор пункта "шаг""  
[ImageSelectingStepOut]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-out-of-current-function.msft.png "Рисунок 3: выбор пункта "шаг с выходом""  
[ImageSelectingContinueToHere]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-continue-to-here.msft.png "Рисунок 4: выбор варианта перейти сюда"  
[ImageSelectingRestartFrame]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-restart-frame.msft.png "Рисунок 5: выбор перезапуска кадра"  
[ImageSelectingResumeScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-resume-script-runtime.msft.png "Рисунок 6: выбор выполнения сценария возобновления"  
[ImageSelectingForceScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-force-script-runtime.msft.png "Рисунок 7: выбор принудительного выполнения сценария"  
[ImageThreadsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-main-min-js-threads.msft.png "Рисунок 8: область "потоки""  
[ImageScopePane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-scope.msft.png "Рисунок 9: область "область""  
[ImageCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png "Рисунок 10: область стека звонков"  
[ImageSelectingCopyStackTrace]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png "Рисунок 11: выбор пункта "Копировать трассировку стека""  
[ImageMarkEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png "Рисунок 12: Пометка сценария как кода библиотеки в области "редактор""  
[ImageMarkCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png "Рис. 13: Пометка сценария как кода библиотеки в области стека вызовов"  
[ImageMarkScriptSettings]: /microsoft-edge/devtools-guide-chromium/media/javascript-framework-library-code.msft.png "Рисунок 14: Пометка сценария как кода библиотеки из параметров"  
[ImageWatchPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-watch.msft.png "Рисунок 15: область контрольных значений"  
[ImageFormat]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-non-minified.msft.png "Рисунок 16: кнопка "формат""  
[ImageEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-minified.msft.png "Рисунок 17: область "редактор""  

<!-- links -->  

[DevToolsJavascriptDisable]: disable.md "Отключение JavaScript с помощью Microsoft Edge DevTools"  
[DevToolsJavascriptGetStarted]: index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  
[DevToolsJavascriptSnippets]: snippets.md "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools"  

[DevToolsCustomize]: ../customize/index.md "Настройка Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="679e4-281">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="679e4-281">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="679e4-282">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="679e4-282">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="679e4-284">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="679e4-284">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

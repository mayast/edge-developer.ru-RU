---
title: Начало работы с отладкой JavaScript в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 06df1fd4d6457a3f02be85b95959bdc353865495
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581826"
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







# <span data-ttu-id="49bbe-103">Начало работы с отладкой JavaScript в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="49bbe-103">Get Started with Debugging JavaScript in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="49bbe-104">В этом учебнике вы научитесь основным рабочим процессом для отладки проблем JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="49bbe-104">This tutorial teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="49bbe-105">Шаг 1: воспроизведение ошибки</span><span class="sxs-lookup"><span data-stu-id="49bbe-105">Step 1: Reproduce the bug</span></span>   

<span data-ttu-id="49bbe-106">Поиск серии действий, которые постоянно воспроизводит ошибки, всегда является первым этапом отладки.</span><span class="sxs-lookup"><span data-stu-id="49bbe-106">Finding a series of actions that consistently reproduces a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="49bbe-107">Нажмите кнопку **Открыть демонстрацию**.</span><span class="sxs-lookup"><span data-stu-id="49bbe-107">Click **Open Demo**.</span></span>  <span data-ttu-id="49bbe-108">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и открывайте демонстрацию на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="49bbe-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and open the demo in a new tab.</span></span>  

    <span data-ttu-id="49bbe-109">[Открыть демонстрацию] [OpenDebugJSDemo]</span><span class="sxs-lookup"><span data-stu-id="49bbe-109">[Open Demo][OpenDebugJSDemo]</span></span>  

1.  <span data-ttu-id="49bbe-110">Введите `5` текст в текстовом поле **число 1** .</span><span class="sxs-lookup"><span data-stu-id="49bbe-110">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="49bbe-111">Введите `1` текст в текстовое поле **число 2** .</span><span class="sxs-lookup"><span data-stu-id="49bbe-111">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="49bbe-112">Нажмите кнопку **Добавить номер 1 и номер 2**.</span><span class="sxs-lookup"><span data-stu-id="49bbe-112">Click **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="49bbe-113">Надпись под кнопкой содержит сообщение `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-113">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="49bbe-114">Результат должен быть `6` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-114">The result should be `6`.</span></span>  <span data-ttu-id="49bbe-115">Это ошибка, которую вы собираетесь исправить.</span><span class="sxs-lookup"><span data-stu-id="49bbe-115">This is the bug you are going to fix.</span></span>  
    
    > ##### <span data-ttu-id="49bbe-116">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="49bbe-116">Figure 1</span></span>  
    > <span data-ttu-id="49bbe-117">Результат состоит в `5 + 1` том `51` , что</span><span class="sxs-lookup"><span data-stu-id="49bbe-117">The result of `5 + 1` is `51`, but should be</span></span> `6`  
    > ![Результатом 5 + 1 является 51, а должно быть 6.][ImageJSBugs]  

## <span data-ttu-id="49bbe-119">Шаг 2: знакомство с пользовательским интерфейсом панели «источники»</span><span class="sxs-lookup"><span data-stu-id="49bbe-119">Step 2: Get familiar with the Sources panel UI</span></span>   

<span data-ttu-id="49bbe-120">DevTools предоставляет множество различных инструментов для различных задач, таких как изменение CSS, профилирование нагрузки страниц и мониторинг сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="49bbe-120">DevTools provides a lot of different tools for different tasks, such as changing CSS, profiling page load performance, and monitoring network requests.</span></span>  <span data-ttu-id="49bbe-121">На панели « **источники** » можно выполнить отладку JavaScript.</span><span class="sxs-lookup"><span data-stu-id="49bbe-121">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="49bbe-122">Откройте DevTools, нажав клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="49bbe-122">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) .</span></span>  <span data-ttu-id="49bbe-123">С помощью этого ярлыка открывается панель **консоли** .</span><span class="sxs-lookup"><span data-stu-id="49bbe-123">This shortcut opens the **Console** panel.</span></span>  
    
    > ##### <span data-ttu-id="49bbe-124">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="49bbe-124">Figure 2</span></span>  
    > <span data-ttu-id="49bbe-125">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="49bbe-125">The **Console** panel</span></span>  
    > ![Панель консоли][ImageJSConsole]  

1.  <span data-ttu-id="49bbe-127">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="49bbe-127">Click the **Sources** tab.</span></span>  
    
    > ##### <span data-ttu-id="49bbe-128">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="49bbe-128">Figure 3</span></span>  
    > <span data-ttu-id="49bbe-129">Панель « **источники** »</span><span class="sxs-lookup"><span data-stu-id="49bbe-129">The **Sources** panel</span></span>  
    > ![Панель «источники»][ImageJSSources]  

<span data-ttu-id="49bbe-131">Пользовательский интерфейс панели « **источники** » состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="49bbe-131">The **Sources** panel UI has 3 parts:</span></span>  

> ##### <span data-ttu-id="49bbe-132">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="49bbe-132">Figure 4</span></span>  
> <span data-ttu-id="49bbe-133">3 части пользовательского интерфейса панели « **источники** »</span><span class="sxs-lookup"><span data-stu-id="49bbe-133">The 3 parts of the **Sources** panel UI</span></span>  
> ![3 части пользовательского интерфейса панели «источники»][ImageJSSourcesAnnotated]  

1.  <span data-ttu-id="49bbe-135">Область " **Навигатор файлов** " \ (раздел 1 на [рис. 4](#figure-4)).</span><span class="sxs-lookup"><span data-stu-id="49bbe-135">The **File Navigator** pane \(Section 1 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="49bbe-136">Здесь перечислены все файлы, на которые поступают запросы страниц.</span><span class="sxs-lookup"><span data-stu-id="49bbe-136">Every file that the page requests is listed here.</span></span>  
1.  <span data-ttu-id="49bbe-137">Область **редактора кода** \ (раздел 2 на [рисунке 4](#figure-4)).</span><span class="sxs-lookup"><span data-stu-id="49bbe-137">The **Code Editor** pane \(Section 2 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="49bbe-138">После того как вы выберете файл в области **навигатора по файлам** , здесь отображается содержимое этого файла.</span><span class="sxs-lookup"><span data-stu-id="49bbe-138">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="49bbe-139">Область **отладки JavaScript** \ (раздел 3 на [рис. 4](#figure-4)).</span><span class="sxs-lookup"><span data-stu-id="49bbe-139">The **JavaScript Debugging** pane \(Section 3 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="49bbe-140">Различные инструменты для проверки JavaScript на странице.</span><span class="sxs-lookup"><span data-stu-id="49bbe-140">Various tools for inspecting the JavaScript for the page.</span></span>  <span data-ttu-id="49bbe-141">Если окно DevTools имеет ширину, эта область отображается справа от области **редактора кода** .</span><span class="sxs-lookup"><span data-stu-id="49bbe-141">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  

## <span data-ttu-id="49bbe-142">Шаг 3: Приостановка кода с помощью точки останова</span><span class="sxs-lookup"><span data-stu-id="49bbe-142">Step 3: Pause the code with a breakpoint</span></span>   

<span data-ttu-id="49bbe-143">Наиболее распространенный способ отладки такого сбоя — Вставка в код большого количества инструкций для `console.log()` проверки значений по мере выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="49bbe-143">A common method for debugging a problem like this is to insert a lot of `console.log()` statements into the code, in order to inspect values as the script runs.</span></span>  <span data-ttu-id="49bbe-144">Пример</span><span class="sxs-lookup"><span data-stu-id="49bbe-144">For example:</span></span>  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

<span data-ttu-id="49bbe-145">Этот `console.log()` метод может быть выполнен, но **точки останова** могут сделать ее более быстрой.</span><span class="sxs-lookup"><span data-stu-id="49bbe-145">The `console.log()` method may get the job done, but **breakpoints** are able to get it done faster.</span></span>  <span data-ttu-id="49bbe-146">С помощью точки останова можно приостановить выполнение кода в середине среды выполнения и проанализировать все значения в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="49bbe-146">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="49bbe-147">В методе точки останова есть несколько преимуществ `console.log()` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-147">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="49bbe-148">Кроме `console.log()` того, необходимо вручную открыть исходный код, найти нужный код, вставить `console.log()` инструкции, а затем снова загрузить страницу, чтобы просмотреть сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="49bbe-148">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then reload the page in order to see the messages in the Console.</span></span>  <span data-ttu-id="49bbe-149">С помощью точек останова вы можете приостановить выполнение нужного кода, даже не зная структуру кода.</span><span class="sxs-lookup"><span data-stu-id="49bbe-149">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="49bbe-150">В `console.log()` инструкции Вам необходимо явным образом указать каждое значение, которое нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="49bbe-150">In your `console.log()` statements you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="49bbe-151">С помощью точек останова DevTools показывает значения всех переменных в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="49bbe-151">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="49bbe-152">Иногда есть переменные, влияющие на ваш код, на который вы еще не осведомлены.</span><span class="sxs-lookup"><span data-stu-id="49bbe-152">Sometimes there are variables affecting your code that you are not even aware of.</span></span>  

<span data-ttu-id="49bbe-153">Короче говоря, точки останова могут помочь вам находить и устранять ошибки быстрее, чем `console.log()` метод.</span><span class="sxs-lookup"><span data-stu-id="49bbe-153">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="49bbe-154">Если вы перейдете на шаг назад и хотите подумать о том, как работает приложение, вы можете сделать обоснованную оценку того, что в `5 + 1 = 51` `click` прослушиватель событий, связанный с кнопкой " **добавить число 1" и "номер 2** ", вычисляется неправильное значение Sum ().</span><span class="sxs-lookup"><span data-stu-id="49bbe-154">If you take a step back and think about how the app works, you are able to make an educated guess that the incorrect sum (`5 + 1 = 51`) gets computed in the `click` event listener that is associated to the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="49bbe-155">Таким образом, вам, возможно, потребуется приостановить код на время `click` выполнения слушателя.</span><span class="sxs-lookup"><span data-stu-id="49bbe-155">Therefore, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="49bbe-156">**Точки останова для прослушивателей событий** позволяют точно так:</span><span class="sxs-lookup"><span data-stu-id="49bbe-156">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="49bbe-157">В области **Отладка JavaScript** щелкните **точки останова прослушивателя событий** , чтобы развернуть раздел.</span><span class="sxs-lookup"><span data-stu-id="49bbe-157">In the **JavaScript Debugging** pane, click **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="49bbe-158">DevTools открывает список категорий расширяемых событий, таких как **анимация** и **буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="49bbe-158">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="49bbe-159">Рядом с категорией событие **мыши** нажмите кнопку **развернуть** значок "развернуть" ![ ][ImageExpandIcon] .</span><span class="sxs-lookup"><span data-stu-id="49bbe-159">Next to the **Mouse** event category, click **Expand** ![Expand icon][ImageExpandIcon].</span></span>  <span data-ttu-id="49bbe-160">DevTools открывает список событий мыши, например **Click** и **MouseDown**.</span><span class="sxs-lookup"><span data-stu-id="49bbe-160">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="49bbe-161">Рядом с каждым событием установлен флажок.</span><span class="sxs-lookup"><span data-stu-id="49bbe-161">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="49bbe-162">Установите флажок **щелкнуть** .</span><span class="sxs-lookup"><span data-stu-id="49bbe-162">Check the **click** checkbox.</span></span>  <span data-ttu-id="49bbe-163">DevTools теперь настроен на автоматическую приостановку при запуске *любого* `click` прослушивателя событий.</span><span class="sxs-lookup"><span data-stu-id="49bbe-163">DevTools is now set up to automatically pause when *any* `click` event listener runs.</span></span>  
    
    > ##### <span data-ttu-id="49bbe-164">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="49bbe-164">Figure 5</span></span>  
    > <span data-ttu-id="49bbe-165">Флажок " **Нажатие кнопки** " включен</span><span class="sxs-lookup"><span data-stu-id="49bbe-165">The **click** checkbox is enabled</span></span>  
    > ![Флажок "нажатие кнопки" включен][ImageJSClickCheckbox]  
    
1.  <span data-ttu-id="49bbe-167">Вернитесь на демонстрацию, нажмите кнопку **Добавить номер 1 и номер 2** еще раз.</span><span class="sxs-lookup"><span data-stu-id="49bbe-167">Back on the demo, click **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="49bbe-168">DevTools приостанавливает демонстрацию и выделяет строку кода на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="49bbe-168">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="49bbe-169">DevTools должен быть приостановлен в строке 16 `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-169">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="49bbe-170">Если вы наведите указатель мыши на другую строку кода, нажмите кнопку **возобновить выполнение** сценария, ![ пока вы не нажмете указатель мыши ][ImageResumeIcon] на нужной строке.</span><span class="sxs-lookup"><span data-stu-id="49bbe-170">If you pause on a different line of code, press **Resume Script Execution** ![Resume Script Execution][ImageResumeIcon] until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="49bbe-171">Если вы приостановили другую строку, у вас есть расширение браузера, которое регистрирует `click` прослушиватель событий на каждой странице, которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="49bbe-171">If you paused on a different line, you have a browser extension that registers a `click` event listener on every page that you visit.</span></span>  <span data-ttu-id="49bbe-172">Вы приостановили `click` прослушиватель расширения.</span><span class="sxs-lookup"><span data-stu-id="49bbe-172">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="49bbe-173">Если вы используете режим InPrivate для **просмотра личных**данных, который отключает все расширения, вы можете увидеть, что вы приостанавливаете каждую из них в нужной строке кода.</span><span class="sxs-lookup"><span data-stu-id="49bbe-173">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="49bbe-174">**Точки останова для прослушивателей событий** — это только один из многих типов точек останова, доступных в DevTools.</span><span class="sxs-lookup"><span data-stu-id="49bbe-174">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="49bbe-175">Стоит запомнить все различные типы, поскольку каждый из них в конечном итоге поможет вам быстрее отлаживать различные сценарии.</span><span class="sxs-lookup"><span data-stu-id="49bbe-175">It is worth memorizing all the different types, because each type ultimately helps you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="49bbe-176">Шаг 4: пошаговое руководство по коду</span><span class="sxs-lookup"><span data-stu-id="49bbe-176">Step 4: Step through the code</span></span>   

<span data-ttu-id="49bbe-177">Одной из распространенных причин ошибок является то, что сценарий выполняется в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="49bbe-177">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="49bbe-178">Пошаговое выполнение кода позволяет проанализировать исполняющую среду вашего кода, по одной строке и точно определить, в каком порядке она работает, не превышающие ожидаемый.</span><span class="sxs-lookup"><span data-stu-id="49bbe-178">Stepping through your code enables you to walk through the runtime of your code, one line at a time, and figure out exactly where it is running in a different order than you expected.</span></span>  <span data-ttu-id="49bbe-179">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="49bbe-179">Try it now:</span></span>  

1.  <span data-ttu-id="49bbe-180">Нажмите кнопку **Перейти к следующей функции** ![ , чтобы перейти к следующему вызову функции ][ImageOverIcon] .</span><span class="sxs-lookup"><span data-stu-id="49bbe-180">Click **Step over next function call** ![Step over next function call][ImageOverIcon].</span></span>  <span data-ttu-id="49bbe-181">DevTools запускает следующий код без пошагового выполнения.</span><span class="sxs-lookup"><span data-stu-id="49bbe-181">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  

    > [!NOTE]
    > <span data-ttu-id="49bbe-182">DevTools пропускает несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="49bbe-182">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="49bbe-183">Это происходит из-за того `inputsAreEmpty()` , что результатом вычисления является значение ложь, поэтому блок кода для `if` инструкции не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49bbe-183">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  

1.  <span data-ttu-id="49bbe-184">На панели **источники** DevTools нажмите кнопку **шаг** с заходом в следующий вызов функции ![ ][ImageIntoIcon] , чтобы пошагово пройти среду выполнения `updateLabel()` функции, по одной строке за раз.</span><span class="sxs-lookup"><span data-stu-id="49bbe-184">On the **Sources** panel of DevTools, click **Step into next function call** ![Step into next function call][ImageIntoIcon] to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  

<span data-ttu-id="49bbe-185">Это основная идея пошагового выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="49bbe-185">That is the basic idea of stepping through code.</span></span>  <span data-ttu-id="49bbe-186">Если посмотреть на код в `get-started.js` , вы увидите, что ошибка может находиться где-то в `updateLabel()` функции.</span><span class="sxs-lookup"><span data-stu-id="49bbe-186">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="49bbe-187">Вместо того чтобы пошагово пройти все строки кода, вы можете использовать другой тип точки останова, чтобы приостановить код ближе к вероятному расположению ошибки.</span><span class="sxs-lookup"><span data-stu-id="49bbe-187">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="49bbe-188">Шаг 5. Установка точки останова в коде строки</span><span class="sxs-lookup"><span data-stu-id="49bbe-188">Step 5: Set a line-of-code breakpoint</span></span>   

<span data-ttu-id="49bbe-189">Точки останова по строкам кода — это наиболее распространенный тип точки останова.</span><span class="sxs-lookup"><span data-stu-id="49bbe-189">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="49bbe-190">Когда вы получаете определенную строку кода, которую вы хотите приостановить, используйте точку останова для строки кода:</span><span class="sxs-lookup"><span data-stu-id="49bbe-190">When you get the specific line of code that you want to pause on, use a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="49bbe-191">Рассмотрим последнюю строку кода `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="49bbe-191">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="49bbe-192">Слева от кода отображается номер строки данной строки кода, **33**.</span><span class="sxs-lookup"><span data-stu-id="49bbe-192">To the left of the code you see the line number of this particular line of code, which is **33**.</span></span>  <span data-ttu-id="49bbe-193">Щелкните **33**.</span><span class="sxs-lookup"><span data-stu-id="49bbe-193">Click on **33**.</span></span>  <span data-ttu-id="49bbe-194">DevTools помещает красный значок слева от **33**.</span><span class="sxs-lookup"><span data-stu-id="49bbe-194">DevTools puts a red icon to the left of **33**.</span></span>  <span data-ttu-id="49bbe-195">Это означает, что в этой строке есть точка останова из строки кода.</span><span class="sxs-lookup"><span data-stu-id="49bbe-195">This means that there is a line-of-code breakpoint on this line.</span></span>  <span data-ttu-id="49bbe-196">DevTools теперь всегда задерживается перед выполнением этой строки кода.</span><span class="sxs-lookup"><span data-stu-id="49bbe-196">DevTools now always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="49bbe-197">Нажмите кнопку **возобновить** ![ выполнение скрипта ][ImageResumeIcon] .</span><span class="sxs-lookup"><span data-stu-id="49bbe-197">Click **Resume script execution** ![Resume script execution][ImageResumeIcon].</span></span>  <span data-ttu-id="49bbe-198">Сценарий продолжит работу, пока не достигнет строки 33.</span><span class="sxs-lookup"><span data-stu-id="49bbe-198">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="49bbe-199">В строках с 30, 31 и 32 DevTools распечатывает значения и `addend1` `addend2` `sum` справа от точки с запятой в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="49bbe-199">On lines 30, 31, and 32, DevTools prints out the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    > ##### <span data-ttu-id="49bbe-200">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="49bbe-200">Figure 6</span></span>  
    > <span data-ttu-id="49bbe-201">DevTools приостанавливается на точке останова строки кода в строке 32</span><span class="sxs-lookup"><span data-stu-id="49bbe-201">DevTools pauses on the line-of-code breakpoint on line 32</span></span>  
    > ![DevTools приостанавливается на точке останова строки кода в строке 32][ImageJSLineOfCodeBreakpoint]  

## <span data-ttu-id="49bbe-203">Шаг 6: Проверка значений переменной</span><span class="sxs-lookup"><span data-stu-id="49bbe-203">Step 6: Check variable values</span></span>   

<span data-ttu-id="49bbe-204">Значения `addend1` `addend2` и `sum` вид подозрительных.</span><span class="sxs-lookup"><span data-stu-id="49bbe-204">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="49bbe-205">Они заключены в кавычки, что означает, что они являются строками.</span><span class="sxs-lookup"><span data-stu-id="49bbe-205">They are wrapped in quotes, which means that they are strings.</span></span>  <span data-ttu-id="49bbe-206">Это хорошая гипотеза, объясняющая причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="49bbe-206">This is a good hypothesis for the explaining the cause of the bug.</span></span>  <span data-ttu-id="49bbe-207">Теперь пора собрать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="49bbe-207">Now it is time to gather more information.</span></span>  <span data-ttu-id="49bbe-208">DevTools предоставляет множество инструментов для проверки значений переменных.</span><span class="sxs-lookup"><span data-stu-id="49bbe-208">DevTools provides a lot of tools for examining variable values.</span></span>  

### <span data-ttu-id="49bbe-209">Способ 1: область "область"</span><span class="sxs-lookup"><span data-stu-id="49bbe-209">Method 1: The Scope pane</span></span>   

<span data-ttu-id="49bbe-210">Когда вы наводите указатель на строку кода, область " **область** " показывает, какие локальные и глобальные переменные определяются в настоящее время, а также значения каждой переменной.</span><span class="sxs-lookup"><span data-stu-id="49bbe-210">When you pause on a line of code, the **Scope** pane shows you what local and global variables are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="49bbe-211">Кроме того, при необходимости отображаются переменные замыкания.</span><span class="sxs-lookup"><span data-stu-id="49bbe-211">It also shows closure variables, when applicable.</span></span>  <span data-ttu-id="49bbe-212">Дважды щелкните значение переменной, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="49bbe-212">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="49bbe-213">Если вы не надерживаетесь в строке кода, область " **область** " пуста.</span><span class="sxs-lookup"><span data-stu-id="49bbe-213">When you are not paused on a line of code, the **Scope** pane is empty.</span></span>  

> ##### <span data-ttu-id="49bbe-214">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="49bbe-214">Figure 7</span></span>  
> <span data-ttu-id="49bbe-215">Область " **область** "</span><span class="sxs-lookup"><span data-stu-id="49bbe-215">The **Scope** pane</span></span>  
> ![Область "область"][ImageJSScope]  

### <span data-ttu-id="49bbe-217">Способ 2: контрольные выражения</span><span class="sxs-lookup"><span data-stu-id="49bbe-217">Method 2: Watch Expressions</span></span>   

<span data-ttu-id="49bbe-218">С помощью вкладки " **выражения контрольного значения** " можно отслеживать значения переменных с течением времени.</span><span class="sxs-lookup"><span data-stu-id="49bbe-218">The **Watch Expressions** tab lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="49bbe-219">Как и названия, выражения контрольного значения не ограничиваются только переменными.</span><span class="sxs-lookup"><span data-stu-id="49bbe-219">As the name implies, Watch Expressions are not just limited to variables.</span></span>  <span data-ttu-id="49bbe-220">Вы можете хранить любое допустимое выражение JavaScript в выражении Watch.</span><span class="sxs-lookup"><span data-stu-id="49bbe-220">You are able to store any valid JavaScript expression in a Watch Expression.</span></span>  <span data-ttu-id="49bbe-221">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="49bbe-221">Try it now:</span></span>  

1.  <span data-ttu-id="49bbe-222">Откройте вкладку **Контрольные значения** .</span><span class="sxs-lookup"><span data-stu-id="49bbe-222">Click the **Watch** tab.</span></span>  
1.  <span data-ttu-id="49bbe-223">Нажмите кнопку **Добавить** выражение ![ ][ImageAddIcon] .</span><span class="sxs-lookup"><span data-stu-id="49bbe-223">Click **Add Expression** ![Add Expression][ImageAddIcon].</span></span>  
1.  <span data-ttu-id="49bbe-224">Введите `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="49bbe-224">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="49bbe-225">Нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-225">Press `Enter`.</span></span>  <span data-ttu-id="49bbe-226">DevTools показан `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-226">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="49bbe-227">Значение справа от двоеточия является результатом вашего выражения контрольного значения.</span><span class="sxs-lookup"><span data-stu-id="49bbe-227">The value to the right of the colon is the result of your Watch Expression.</span></span>  

> [!NOTE]
> <span data-ttu-id="49bbe-228">На панели "выражение для контрольного значения \" (внизу справа) на [рисунке 8](#figure-8) `typeof sum` отображается выражение Watch.</span><span class="sxs-lookup"><span data-stu-id="49bbe-228">In the Watch Expression pane \(bottom-right\) in [Figure 8](#figure-8), the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="49bbe-229">Если окно DevTools велико, область выражения контрольных значений находится справа над областью **точки останова прослушивателя событий** .</span><span class="sxs-lookup"><span data-stu-id="49bbe-229">If your DevTools window is large, the Watch Expression pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

> ##### <span data-ttu-id="49bbe-230">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="49bbe-230">Figure 8</span></span>  
> <span data-ttu-id="49bbe-231">Область "выражение контрольного значения"</span><span class="sxs-lookup"><span data-stu-id="49bbe-231">The Watch Expression pane</span></span>  
> ![Область "выражение контрольного значения"][ImageJSWatchExpression]  

<span data-ttu-id="49bbe-233">Как и `sum` предполагается, вычисляется как строка, когда она должна быть числом.</span><span class="sxs-lookup"><span data-stu-id="49bbe-233">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="49bbe-234">Теперь вы подтверждаете, что это причина ошибки.</span><span class="sxs-lookup"><span data-stu-id="49bbe-234">You have now confirmed that this is the cause of the bug.</span></span>  

### <span data-ttu-id="49bbe-235">Способ 3: консоль</span><span class="sxs-lookup"><span data-stu-id="49bbe-235">Method 3: The Console</span></span>   

<span data-ttu-id="49bbe-236">Помимо просмотра `console.log()` сообщений, вы также можете использовать консоль для оценки произвольных операторов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="49bbe-236">In addition to viewing `console.log()` messages, you may also use the Console to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="49bbe-237">С точки зрения отладки вы можете использовать консоль для проверки возможных исправлений ошибок.</span><span class="sxs-lookup"><span data-stu-id="49bbe-237">In terms of debugging, you may use the Console to test out potential fixes for bugs.</span></span>  <span data-ttu-id="49bbe-238">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="49bbe-238">Try it now:</span></span>  

1.  <span data-ttu-id="49bbe-239">Если вы не открыли ящик консоли, нажмите, `Escape` чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="49bbe-239">If you do not have the Console drawer open, press `Escape` to open it.</span></span>  <span data-ttu-id="49bbe-240">Она откроется в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="49bbe-240">It opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="49bbe-241">В окне консоли введите `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-241">In the Console, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="49bbe-242">Эта инструкция работает, так как вы придерживаетесь к строке кода, `addend1` в которой и `addend2` находятся в области.</span><span class="sxs-lookup"><span data-stu-id="49bbe-242">This statement works because you are paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="49bbe-243">Нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-243">Press `Enter`.</span></span>  <span data-ttu-id="49bbe-244">DevTools оценивает оператор и печатает `6` результаты, что является результатом, который вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="49bbe-244">DevTools evaluates the statement and prints out `6`, which is the result you expect the demo to produce.</span></span>  

> ##### <span data-ttu-id="49bbe-245">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="49bbe-245">Figure 9</span></span>  
> <span data-ttu-id="49bbe-246">Входной ящик консоли после оценки</span><span class="sxs-lookup"><span data-stu-id="49bbe-246">The Console drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
> ![Входной ящик консоли после оценки parseInt (addend1) + parseInt (addend2)][ImageJSConsoleEvaluated]  

## <span data-ttu-id="49bbe-248">Шаг 7: применение исправления</span><span class="sxs-lookup"><span data-stu-id="49bbe-248">Step 7: Apply a fix</span></span>   

<span data-ttu-id="49bbe-249">Если вы нашли исправление ошибки, исправьте его, изменив код и повторно выполнив демонстрацию.</span><span class="sxs-lookup"><span data-stu-id="49bbe-249">If you find a fix for the bug, try out your fix by editing the code and re-running the demo.</span></span>  <span data-ttu-id="49bbe-250">Для применения исправления вам не нужно выходить из DevTools.</span><span class="sxs-lookup"><span data-stu-id="49bbe-250">You do not need to leave DevTools to apply the fix.</span></span>  <span data-ttu-id="49bbe-251">Вы можете редактировать код JavaScript прямо в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="49bbe-251">You are able to edit JavaScript code directly within the DevTools UI.</span></span>  <span data-ttu-id="49bbe-252">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="49bbe-252">Try it now:</span></span>  

1.  <span data-ttu-id="49bbe-253">Нажмите кнопку **возобновить** ![ выполнение скрипта ][ImageResumeIcon] .</span><span class="sxs-lookup"><span data-stu-id="49bbe-253">Click **Resume script execution** ![Resume script execution][ImageResumeIcon].</span></span>  
1.  <span data-ttu-id="49bbe-254">В **редакторе кода**замените строку 32, `var sum = addend1 + addend2` с `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="49bbe-254">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="49bbe-255">`Control` + `S` Чтобы сохранить изменения, нажмите клавиши \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="49bbe-255">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="49bbe-256">Щелкните **отключить точки останова** ![ , чтобы отключить точки останова ][ImageDeactivateIcon] .</span><span class="sxs-lookup"><span data-stu-id="49bbe-256">Click **Deactivate breakpoints** ![Deactivate breakpoints][ImageDeactivateIcon].</span></span>  <span data-ttu-id="49bbe-257">Она изменится на синий, чтобы показать, что она активна.</span><span class="sxs-lookup"><span data-stu-id="49bbe-257">It changes blue to indicate that it is active.</span></span>  <span data-ttu-id="49bbe-258">Несмотря на то, что этот параметр установлен, DevTools игнорирует любые точки останова, заданные вами.</span><span class="sxs-lookup"><span data-stu-id="49bbe-258">While this is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="49bbe-259">Попробуйте использовать демонстрационную версию с разными значениями.</span><span class="sxs-lookup"><span data-stu-id="49bbe-259">Try out the demo with different values.</span></span>  <span data-ttu-id="49bbe-260">Демонстрация будет правильно рассчитывается.</span><span class="sxs-lookup"><span data-stu-id="49bbe-260">The demo now calculates correctly.</span></span>  

> [!CAUTION]
> <span data-ttu-id="49bbe-261">Этот рабочий процесс применяет исправление только к коду, который выполняется в браузере.</span><span class="sxs-lookup"><span data-stu-id="49bbe-261">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="49bbe-262">Она не исправляет код для всех пользователей, которые посещает страницу.</span><span class="sxs-lookup"><span data-stu-id="49bbe-262">It does not fix the code for all users that visit your page.</span></span>  <span data-ttu-id="49bbe-263">Для этого вам нужно исправить код, который находится на сервере.</span><span class="sxs-lookup"><span data-stu-id="49bbe-263">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="49bbe-264">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="49bbe-264">Next steps</span></span>   

<span data-ttu-id="49bbe-265">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="49bbe-265">Congratulations!</span></span>  <span data-ttu-id="49bbe-266">Теперь вы знаете, как максимально эффективно использовать Microsoft Edge DevTools при отладке JavaScript.</span><span class="sxs-lookup"><span data-stu-id="49bbe-266">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="49bbe-267">Средства и методы, описанные в этом учебнике, помогут вам сэкономить бесчисленные часы.</span><span class="sxs-lookup"><span data-stu-id="49bbe-267">The tools and methods you learned in this tutorial may save you countless hours.</span></span>  

<span data-ttu-id="49bbe-268">В этом учебнике показано два способа задания точек останова.</span><span class="sxs-lookup"><span data-stu-id="49bbe-268">This tutorial only showed you two ways to set breakpoints.</span></span>  <span data-ttu-id="49bbe-269">DevTools обладает многими другими способами, в том числе:</span><span class="sxs-lookup"><span data-stu-id="49bbe-269">DevTools offers many other ways, including:</span></span>  

*   <span data-ttu-id="49bbe-270">Условные точки останова, которые запускаются только в случае, если предоставленное условие истинно.</span><span class="sxs-lookup"><span data-stu-id="49bbe-270">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="49bbe-271">Точки останова в перехваченных или неперехваченных исключениях.</span><span class="sxs-lookup"><span data-stu-id="49bbe-271">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="49bbe-272">XHR точки останова, которые инициируются, когда запрашиваемый URL-адрес соответствует подстроке, которую вы задаете.</span><span class="sxs-lookup"><span data-stu-id="49bbe-272">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  

<!-- See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

<!--There are a couple of code stepping controls that were not explained in this tutorial.  See [Step over line of code][JSReferenceStepping] to learn more.  -->  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: /microsoft-edge/devtools-guide-chromium/media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageResumeIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  

[ImageJSBugs]: /microsoft-edge/devtools-guide-chromium/media/javascript-js-demo-bad.msft.png "Рисунок 1: результат 5 + 1 — 51, а должен быть 6"  
[ImageJSConsole]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-empty.msft.png "Рисунок 2: панель консоли"  
[ImageJSSources]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections.msft.png "Рисунок 3: панель «источники»"  
[ImageJSSourcesAnnotated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections-annotated.msft.png "Рисунок 4:3 части пользовательского интерфейса панели «источники»"  
[ImageJSClickCheckbox]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png "Рисунок 5: установлен флажок "щелкнуть"."  
[ImageJSLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused.msft.png "Рисунок 6: DevTools приостанавливается на точке останова кода строки в 32"  
[ImageJSScope]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-scope.msft.png "Рисунок 7: область "область""  
[ImageJSWatchExpression]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-watch.msft.png "Рисунок 8: область "выражение контрольного значения""  
[ImageJSConsoleEvaluated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-console.msft.png "Входной ящик консоли после оценки parseInt (addend1) + parseInt (addend2)"  

<!-- links -->  

<!--[JSBreakpoints]: breakpoints.md "JavaScript Breakpoints"  -->  
<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->
[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Открыть демонстрацию"  
<!--[JSReferenceStepping]: reference.md#stepping "Reference Stepping"  -->

> [!NOTE]
> <span data-ttu-id="49bbe-283">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49bbe-283">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="49bbe-284">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="49bbe-284">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="49bbe-286">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49bbe-286">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

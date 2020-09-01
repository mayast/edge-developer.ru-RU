---
title: Начало работы с отладкой JavaScript в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 204d3033b65f82c6160a0d2c41a15d8eb62b4530
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982882"
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







# <span data-ttu-id="3dc98-103">Начало работы с отладкой JavaScript в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3dc98-103">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="3dc98-104">В этом учебнике вы научитесь основным рабочим процессом для отладки проблем JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3dc98-104">This tutorial teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="3dc98-105">Шаг 1: воспроизведение ошибки</span><span class="sxs-lookup"><span data-stu-id="3dc98-105">Step 1: Reproduce the bug</span></span>   

<span data-ttu-id="3dc98-106">Поиск серии действий, которые постоянно воспроизводит ошибки, всегда является первым этапом отладки.</span><span class="sxs-lookup"><span data-stu-id="3dc98-106">Finding a series of actions that consistently reproduces a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="3dc98-107">Нажмите кнопку **Открыть демонстрацию**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-107">Click **Open Demo**.</span></span>  <span data-ttu-id="3dc98-108">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и открывайте демонстрацию на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="3dc98-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and open the demo in a new tab.</span></span>  
    
    [<span data-ttu-id="3dc98-109">Открыть демонстрацию</span><span class="sxs-lookup"><span data-stu-id="3dc98-109">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="3dc98-110">Введите `5` текст в текстовом поле **число 1** .</span><span class="sxs-lookup"><span data-stu-id="3dc98-110">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="3dc98-111">Введите `1` текст в текстовое поле **число 2** .</span><span class="sxs-lookup"><span data-stu-id="3dc98-111">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="3dc98-112">Нажмите кнопку **Добавить номер 1 и номер 2**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-112">Click **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="3dc98-113">Надпись под кнопкой содержит сообщение `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-113">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="3dc98-114">Результат должен быть `6` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-114">The result should be `6`.</span></span>  <span data-ttu-id="3dc98-115">Это ошибка, которую вы собираетесь исправить.</span><span class="sxs-lookup"><span data-stu-id="3dc98-115">This is the bug you are going to fix.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-js-demo-bad.msft.png":::
       <span data-ttu-id="3dc98-117">Результат состоит в `5 + 1` том `51` , что</span><span class="sxs-lookup"><span data-stu-id="3dc98-117">The result of `5 + 1` is `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="3dc98-118">Шаг 2: знакомство с пользовательским интерфейсом панели «источники»</span><span class="sxs-lookup"><span data-stu-id="3dc98-118">Step 2: Get familiar with the Sources panel UI</span></span>   

<span data-ttu-id="3dc98-119">DevTools предоставляет множество различных инструментов для различных задач, таких как изменение CSS, профилирование нагрузки страниц и мониторинг сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="3dc98-119">DevTools provides a lot of different tools for different tasks, such as changing CSS, profiling page load performance, and monitoring network requests.</span></span>  <span data-ttu-id="3dc98-120">На панели « **источники** » можно выполнить отладку JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3dc98-120">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="3dc98-121">Откройте DevTools, нажав клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3dc98-121">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) .</span></span>  <span data-ttu-id="3dc98-122">С помощью этого ярлыка открывается панель **консоли** .</span><span class="sxs-lookup"><span data-stu-id="3dc98-122">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Панель консоли" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="3dc98-124">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="3dc98-124">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3dc98-125">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="3dc98-125">Click the **Sources** tab.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Панель «источники»" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="3dc98-127">Панель « **источники** »</span><span class="sxs-lookup"><span data-stu-id="3dc98-127">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3dc98-128">В пользовательском интерфейсе панели « **источники** » есть 3 части.</span><span class="sxs-lookup"><span data-stu-id="3dc98-128">The **Sources** panel UI has 3 parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="3 части пользовательского интерфейса панели «источники»" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="3dc98-130">3 части пользовательского интерфейса панели « **источники** »</span><span class="sxs-lookup"><span data-stu-id="3dc98-130">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="3dc98-131">Область " **Навигатор файлов** " \ (раздел 1 на предыдущем рисунке).</span><span class="sxs-lookup"><span data-stu-id="3dc98-131">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="3dc98-132">Здесь перечислены все файлы, на которые поступают запросы страниц.</span><span class="sxs-lookup"><span data-stu-id="3dc98-132">Every file that the page requests is listed here.</span></span>  
1.  <span data-ttu-id="3dc98-133">Область **редактора кода** \ (раздел 2 на предыдущем рисунке).</span><span class="sxs-lookup"><span data-stu-id="3dc98-133">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="3dc98-134">После того как вы выберете файл в области **навигатора по файлам** , здесь отображается содержимое этого файла.</span><span class="sxs-lookup"><span data-stu-id="3dc98-134">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="3dc98-135">Область **отладки JavaScript** \ (раздел 3 на предыдущем рисунке).</span><span class="sxs-lookup"><span data-stu-id="3dc98-135">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="3dc98-136">Различные инструменты для проверки JavaScript на странице.</span><span class="sxs-lookup"><span data-stu-id="3dc98-136">Various tools for inspecting the JavaScript for the page.</span></span>  <span data-ttu-id="3dc98-137">Если окно DevTools имеет ширину, эта область отображается справа от области **редактора кода** .</span><span class="sxs-lookup"><span data-stu-id="3dc98-137">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="3dc98-138">Шаг 3: Приостановка кода с помощью точки останова</span><span class="sxs-lookup"><span data-stu-id="3dc98-138">Step 3: Pause the code with a breakpoint</span></span>   

<span data-ttu-id="3dc98-139">Наиболее распространенный способ отладки такого сбоя — Вставка в код большого количества инструкций для `console.log()` проверки значений по мере выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="3dc98-139">A common method for debugging a problem like this is to insert a lot of `console.log()` statements into the code, in order to inspect values as the script runs.</span></span>  <span data-ttu-id="3dc98-140">Например:</span><span class="sxs-lookup"><span data-stu-id="3dc98-140">For example:</span></span>  

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

<span data-ttu-id="3dc98-141">Этот `console.log()` метод может быть выполнен, но **точки останова** могут сделать ее более быстрой.</span><span class="sxs-lookup"><span data-stu-id="3dc98-141">The `console.log()` method may get the job done, but **breakpoints** are able to get it done faster.</span></span>  <span data-ttu-id="3dc98-142">С помощью точки останова можно приостановить выполнение кода в середине среды выполнения и проанализировать все значения в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="3dc98-142">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="3dc98-143">В методе точки останова есть несколько преимуществ `console.log()` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-143">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="3dc98-144">Кроме `console.log()` того, необходимо вручную открыть исходный код, найти нужный код, вставить `console.log()` инструкции, а затем снова загрузить страницу, чтобы просмотреть сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="3dc98-144">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then reload the page in order to see the messages in the Console.</span></span>  <span data-ttu-id="3dc98-145">С помощью точек останова вы можете приостановить выполнение нужного кода, даже не зная структуру кода.</span><span class="sxs-lookup"><span data-stu-id="3dc98-145">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="3dc98-146">В `console.log()` инструкции Вам необходимо явным образом указать каждое значение, которое нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="3dc98-146">In your `console.log()` statements you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="3dc98-147">С помощью точек останова DevTools показывает значения всех переменных в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="3dc98-147">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="3dc98-148">Иногда есть переменные, влияющие на ваш код, на который вы еще не осведомлены.</span><span class="sxs-lookup"><span data-stu-id="3dc98-148">Sometimes there are variables affecting your code that you are not even aware of.</span></span>  

<span data-ttu-id="3dc98-149">Короче говоря, точки останова могут помочь вам находить и устранять ошибки быстрее, чем `console.log()` метод.</span><span class="sxs-lookup"><span data-stu-id="3dc98-149">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="3dc98-150">Если вы перейдете на шаг назад и хотите подумать о том, как работает приложение, вы можете сделать обоснованную оценку того, что в `5 + 1 = 51` `click` прослушиватель событий, связанный с кнопкой " **добавить число 1" и "номер 2** ", вычисляется неправильное значение Sum ().</span><span class="sxs-lookup"><span data-stu-id="3dc98-150">If you take a step back and think about how the app works, you are able to make an educated guess that the incorrect sum (`5 + 1 = 51`) gets computed in the `click` event listener that is associated to the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="3dc98-151">Таким образом, вам, возможно, потребуется приостановить код на время `click` выполнения слушателя.</span><span class="sxs-lookup"><span data-stu-id="3dc98-151">Therefore, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="3dc98-152">**Точки останова для прослушивателей событий** позволяют точно так:</span><span class="sxs-lookup"><span data-stu-id="3dc98-152">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="3dc98-153">В области **Отладка JavaScript** щелкните **точки останова прослушивателя событий** , чтобы развернуть раздел.</span><span class="sxs-lookup"><span data-stu-id="3dc98-153">In the **JavaScript Debugging** pane, click **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="3dc98-154">DevTools открывает список категорий расширяемых событий, таких как **анимация** и **буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-154">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="3dc98-155">Рядом с категорией событие **мыши** нажмите кнопку **развернуть** \ ( ![ развернуть значок ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3dc98-155">Next to the **Mouse** event category, click **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="3dc98-156">DevTools открывает список событий мыши, например **Click** и **MouseDown**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-156">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="3dc98-157">Рядом с каждым событием установлен флажок.</span><span class="sxs-lookup"><span data-stu-id="3dc98-157">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="3dc98-158">Установите флажок **щелкнуть** .</span><span class="sxs-lookup"><span data-stu-id="3dc98-158">Check the **click** checkbox.</span></span>  <span data-ttu-id="3dc98-159">DevTools теперь настроен на автоматическую приостановку при запуске *любого* `click` прослушивателя событий.</span><span class="sxs-lookup"><span data-stu-id="3dc98-159">DevTools is now set up to automatically pause when *any* `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Флажок "нажатие кнопки" включен" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="3dc98-161">Флажок " **Нажатие кнопки** " включен</span><span class="sxs-lookup"><span data-stu-id="3dc98-161">The **click** checkbox is enabled</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3dc98-162">Вернитесь на демонстрацию, нажмите кнопку **Добавить номер 1 и номер 2** еще раз.</span><span class="sxs-lookup"><span data-stu-id="3dc98-162">Back on the demo, click **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="3dc98-163">DevTools приостанавливает демонстрацию и выделяет строку кода на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="3dc98-163">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="3dc98-164">DevTools должен быть приостановлен в строке 16 `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-164">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="3dc98-165">Если наведите указатель мыши на другую строку кода, нажмите кнопку **возобновить выполнение сценария** и ( ![ возобновить выполнение сценария ][ImageResumeIcon] ), пока вы не нажмете указатель мыши на нужной строке.</span><span class="sxs-lookup"><span data-stu-id="3dc98-165">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3dc98-166">Если вы приостановили другую строку, у вас есть расширение браузера, которое регистрирует `click` прослушиватель событий на каждой странице, которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="3dc98-166">If you paused on a different line, you have a browser extension that registers a `click` event listener on every page that you visit.</span></span>  <span data-ttu-id="3dc98-167">Вы приостановили `click` прослушиватель расширения.</span><span class="sxs-lookup"><span data-stu-id="3dc98-167">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="3dc98-168">Если вы используете режим InPrivate для **просмотра личных**данных, который отключает все расширения, вы можете увидеть, что вы приостанавливаете каждую из них в нужной строке кода.</span><span class="sxs-lookup"><span data-stu-id="3dc98-168">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="3dc98-169">**Точки останова для прослушивателей событий** — это только один из многих типов точек останова, доступных в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3dc98-169">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="3dc98-170">Стоит запомнить все различные типы, поскольку каждый из них в конечном итоге поможет вам быстрее отлаживать различные сценарии.</span><span class="sxs-lookup"><span data-stu-id="3dc98-170">It is worth memorizing all the different types, because each type ultimately helps you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="3dc98-171">Шаг 4: пошаговое руководство по коду</span><span class="sxs-lookup"><span data-stu-id="3dc98-171">Step 4: Step through the code</span></span>   

<span data-ttu-id="3dc98-172">Одной из распространенных причин ошибок является то, что сценарий выполняется в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="3dc98-172">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="3dc98-173">Пошаговое выполнение кода позволяет проанализировать исполняющую среду вашего кода, по одной строке и точно определить, в каком порядке она работает, не превышающие ожидаемый.</span><span class="sxs-lookup"><span data-stu-id="3dc98-173">Stepping through your code enables you to walk through the runtime of your code, one line at a time, and figure out exactly where it is running in a different order than you expected.</span></span>  <span data-ttu-id="3dc98-174">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="3dc98-174">Try it now:</span></span>  

1.  <span data-ttu-id="3dc98-175">Нажмите кнопку " **Перейти к следующему вызову функции** " ( ![ шаг за следующий вызов функции ][ImageOverIcon] ).</span><span class="sxs-lookup"><span data-stu-id="3dc98-175">Click **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="3dc98-176">DevTools запускает следующий код без пошагового выполнения.</span><span class="sxs-lookup"><span data-stu-id="3dc98-176">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="3dc98-177">DevTools пропускает несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="3dc98-177">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="3dc98-178">Это происходит из-за того `inputsAreEmpty()` , что результатом вычисления является значение ложь, поэтому блок кода для `if` инструкции не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3dc98-178">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="3dc98-179">На панели **источники** DevTools выберите команду Шаг с **заходом к следующей функции** \ ( ![ Шаг с заходом в следующую функцию ][ImageIntoIcon] ), чтобы пошагово пройти все `updateLabel()` время выполнения функции, по одной строке за раз.</span><span class="sxs-lookup"><span data-stu-id="3dc98-179">On the **Sources** panel of DevTools, click **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="3dc98-180">Это основная идея пошагового выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="3dc98-180">That is the basic idea of stepping through code.</span></span>  <span data-ttu-id="3dc98-181">Если посмотреть на код в `get-started.js` , вы увидите, что ошибка может находиться где-то в `updateLabel()` функции.</span><span class="sxs-lookup"><span data-stu-id="3dc98-181">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="3dc98-182">Вместо того чтобы пошагово пройти все строки кода, вы можете использовать другой тип точки останова, чтобы приостановить код ближе к вероятному расположению ошибки.</span><span class="sxs-lookup"><span data-stu-id="3dc98-182">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="3dc98-183">Шаг 5. Установка точки останова в коде строки</span><span class="sxs-lookup"><span data-stu-id="3dc98-183">Step 5: Set a line-of-code breakpoint</span></span>   

<span data-ttu-id="3dc98-184">Точки останова по строкам кода — это наиболее распространенный тип точки останова.</span><span class="sxs-lookup"><span data-stu-id="3dc98-184">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="3dc98-185">Когда вы получаете определенную строку кода, которую вы хотите приостановить, используйте точку останова для строки кода:</span><span class="sxs-lookup"><span data-stu-id="3dc98-185">When you get the specific line of code that you want to pause on, use a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="3dc98-186">Рассмотрим последнюю строку кода `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="3dc98-186">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="3dc98-187">Слева от кода отображается номер строки данной строки кода, **33**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-187">To the left of the code you see the line number of this particular line of code, which is **33**.</span></span>  <span data-ttu-id="3dc98-188">Щелкните **33**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-188">Click on **33**.</span></span>  <span data-ttu-id="3dc98-189">DevTools помещает красный значок слева от **33**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-189">DevTools puts a red icon to the left of **33**.</span></span>  <span data-ttu-id="3dc98-190">Это означает, что в этой строке есть точка останова из строки кода.</span><span class="sxs-lookup"><span data-stu-id="3dc98-190">This means that there is a line-of-code breakpoint on this line.</span></span>  <span data-ttu-id="3dc98-191">DevTools теперь всегда задерживается перед выполнением этой строки кода.</span><span class="sxs-lookup"><span data-stu-id="3dc98-191">DevTools now always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="3dc98-192">Нажмите кнопку **возобновить выполнение сценария** ( ![ возобновить выполнение сценария ][ImageResumeIcon] ).</span><span class="sxs-lookup"><span data-stu-id="3dc98-192">Click **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="3dc98-193">Сценарий продолжит работу, пока не достигнет строки 33.</span><span class="sxs-lookup"><span data-stu-id="3dc98-193">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="3dc98-194">В строках с 30, 31 и 32 DevTools распечатывает значения и `addend1` `addend2` `sum` справа от точки с запятой в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="3dc98-194">On lines 30, 31, and 32, DevTools prints out the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools приостанавливается на точке останова строки кода в строке 32" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="3dc98-196">DevTools приостанавливается на точке останова строки кода в строке 32</span><span class="sxs-lookup"><span data-stu-id="3dc98-196">DevTools pauses on the line-of-code breakpoint on line 32</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3dc98-197">Шаг 6: Проверка значений переменной</span><span class="sxs-lookup"><span data-stu-id="3dc98-197">Step 6: Check variable values</span></span>   

<span data-ttu-id="3dc98-198">Значения `addend1` `addend2` и `sum` вид подозрительных.</span><span class="sxs-lookup"><span data-stu-id="3dc98-198">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="3dc98-199">Они заключены в кавычки, что означает, что они являются строками.</span><span class="sxs-lookup"><span data-stu-id="3dc98-199">They are wrapped in quotes, which means that they are strings.</span></span>  <span data-ttu-id="3dc98-200">Это хорошая гипотеза, объясняющая причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="3dc98-200">This is a good hypothesis for the explaining the cause of the bug.</span></span>  <span data-ttu-id="3dc98-201">Теперь пора собрать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3dc98-201">Now it is time to gather more information.</span></span>  <span data-ttu-id="3dc98-202">DevTools предоставляет множество инструментов для проверки значений переменных.</span><span class="sxs-lookup"><span data-stu-id="3dc98-202">DevTools provides a lot of tools for examining variable values.</span></span>  

### <span data-ttu-id="3dc98-203">Способ 1: область "область"</span><span class="sxs-lookup"><span data-stu-id="3dc98-203">Method 1: The Scope pane</span></span>   

<span data-ttu-id="3dc98-204">Когда вы наводите указатель на строку кода, область " **область** " показывает, какие локальные и глобальные переменные определяются в настоящее время, а также значения каждой переменной.</span><span class="sxs-lookup"><span data-stu-id="3dc98-204">When you pause on a line of code, the **Scope** pane shows you what local and global variables are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="3dc98-205">Кроме того, при необходимости отображаются переменные замыкания.</span><span class="sxs-lookup"><span data-stu-id="3dc98-205">It also shows closure variables, when applicable.</span></span>  <span data-ttu-id="3dc98-206">Дважды щелкните значение переменной, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="3dc98-206">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="3dc98-207">Если вы не надерживаетесь в строке кода, область " **область** " пуста.</span><span class="sxs-lookup"><span data-stu-id="3dc98-207">When you are not paused on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Область "область"" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="3dc98-209">Область " **область** "</span><span class="sxs-lookup"><span data-stu-id="3dc98-209">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="3dc98-210">Способ 2: контрольные выражения</span><span class="sxs-lookup"><span data-stu-id="3dc98-210">Method 2: Watch Expressions</span></span>   

<span data-ttu-id="3dc98-211">С помощью вкладки " **выражения контрольного значения** " можно отслеживать значения переменных с течением времени.</span><span class="sxs-lookup"><span data-stu-id="3dc98-211">The **Watch Expressions** tab lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="3dc98-212">Как и названия, выражения контрольного значения не ограничиваются только переменными.</span><span class="sxs-lookup"><span data-stu-id="3dc98-212">As the name implies, Watch Expressions are not just limited to variables.</span></span>  <span data-ttu-id="3dc98-213">Вы можете хранить любое допустимое выражение JavaScript в выражении Watch.</span><span class="sxs-lookup"><span data-stu-id="3dc98-213">You are able to store any valid JavaScript expression in a Watch Expression.</span></span>  <span data-ttu-id="3dc98-214">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="3dc98-214">Try it now:</span></span>  

1.  <span data-ttu-id="3dc98-215">Откройте вкладку **Контрольные значения** .</span><span class="sxs-lookup"><span data-stu-id="3dc98-215">Click the **Watch** tab.</span></span>  
1.  <span data-ttu-id="3dc98-216">Нажмите кнопку **Добавить выражение** \ ( ![ Добавить выражение ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3dc98-216">Click **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="3dc98-217">Введите `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="3dc98-217">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="3dc98-218">Нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-218">Press `Enter`.</span></span>  <span data-ttu-id="3dc98-219">DevTools показан `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-219">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="3dc98-220">Значение справа от двоеточия является результатом вашего выражения контрольного значения.</span><span class="sxs-lookup"><span data-stu-id="3dc98-220">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="3dc98-221">В области выражения для контрольных значений \ (внизу справа) на рисунке ниже `typeof sum` показано выражение Watch.</span><span class="sxs-lookup"><span data-stu-id="3dc98-221">In the Watch Expression pane \(bottom-right\) in in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="3dc98-222">Если окно DevTools велико, область выражения контрольных значений находится справа над областью **точки останова прослушивателя событий** .</span><span class="sxs-lookup"><span data-stu-id="3dc98-222">If your DevTools window is large, the Watch Expression pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Область "выражение контрольного значения"" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="3dc98-224">Область " **выражение контрольного значения** "</span><span class="sxs-lookup"><span data-stu-id="3dc98-224">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="3dc98-225">Как и `sum` предполагается, вычисляется как строка, когда она должна быть числом.</span><span class="sxs-lookup"><span data-stu-id="3dc98-225">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="3dc98-226">Теперь вы подтверждаете, что это причина ошибки.</span><span class="sxs-lookup"><span data-stu-id="3dc98-226">You have now confirmed that this is the cause of the bug.</span></span>  

### <span data-ttu-id="3dc98-227">Способ 3: консоль</span><span class="sxs-lookup"><span data-stu-id="3dc98-227">Method 3: The Console</span></span>   

<span data-ttu-id="3dc98-228">Помимо просмотра `console.log()` сообщений, вы также можете использовать консоль для оценки произвольных операторов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3dc98-228">In addition to viewing `console.log()` messages, you may also use the Console to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="3dc98-229">С точки зрения отладки вы можете использовать консоль для проверки возможных исправлений ошибок.</span><span class="sxs-lookup"><span data-stu-id="3dc98-229">In terms of debugging, you may use the Console to test out potential fixes for bugs.</span></span>  <span data-ttu-id="3dc98-230">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="3dc98-230">Try it now:</span></span>  

1.  <span data-ttu-id="3dc98-231">Если вы не открыли ящик консоли, нажмите, `Escape` чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="3dc98-231">If you do not have the Console drawer open, press `Escape` to open it.</span></span>  <span data-ttu-id="3dc98-232">Она откроется в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="3dc98-232">It opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="3dc98-233">В окне консоли введите `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-233">In the Console, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="3dc98-234">Эта инструкция работает, так как вы придерживаетесь к строке кода, `addend1` в которой и `addend2` находятся в области.</span><span class="sxs-lookup"><span data-stu-id="3dc98-234">This statement works because you are paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="3dc98-235">Нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-235">Press `Enter`.</span></span>  <span data-ttu-id="3dc98-236">DevTools оценивает оператор и печатает `6` результаты, что является результатом, который вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="3dc98-236">DevTools evaluates the statement and prints out `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Входной ящик консоли после оценки parseInt (addend1) + parseInt (addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="3dc98-238">Входной ящик **консоли** после оценки</span><span class="sxs-lookup"><span data-stu-id="3dc98-238">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="3dc98-239">Шаг 7: применение исправления</span><span class="sxs-lookup"><span data-stu-id="3dc98-239">Step 7: Apply a fix</span></span>   

<span data-ttu-id="3dc98-240">Если вы нашли исправление ошибки, исправьте его, изменив код и повторно выполнив демонстрацию.</span><span class="sxs-lookup"><span data-stu-id="3dc98-240">If you find a fix for the bug, try out your fix by editing the code and re-running the demo.</span></span>  <span data-ttu-id="3dc98-241">Для применения исправления вам не нужно выходить из DevTools.</span><span class="sxs-lookup"><span data-stu-id="3dc98-241">You do not need to leave DevTools to apply the fix.</span></span>  <span data-ttu-id="3dc98-242">Вы можете редактировать код JavaScript прямо в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="3dc98-242">You are able to edit JavaScript code directly within the DevTools UI.</span></span>  <span data-ttu-id="3dc98-243">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="3dc98-243">Try it now:</span></span>  

1.  <span data-ttu-id="3dc98-244">Нажмите кнопку **возобновить выполнение сценария** ( ![ возобновить выполнение сценария ][ImageResumeIcon] ).</span><span class="sxs-lookup"><span data-stu-id="3dc98-244">Click **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="3dc98-245">В **редакторе кода**замените строку 32, `var sum = addend1 + addend2` с `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="3dc98-245">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="3dc98-246">`Control` + `S` Чтобы сохранить изменения, нажмите клавиши \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3dc98-246">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="3dc98-247">Щелкните **отключить точки останова** \ ( ![ отключить точки останова ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3dc98-247">Click **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="3dc98-248">Она изменится на синий, чтобы показать, что она активна.</span><span class="sxs-lookup"><span data-stu-id="3dc98-248">It changes blue to indicate that it is active.</span></span>  <span data-ttu-id="3dc98-249">Несмотря на то, что этот параметр установлен, DevTools игнорирует любые точки останова, заданные вами.</span><span class="sxs-lookup"><span data-stu-id="3dc98-249">While this is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="3dc98-250">Попробуйте использовать демонстрационную версию с разными значениями.</span><span class="sxs-lookup"><span data-stu-id="3dc98-250">Try out the demo with different values.</span></span>  <span data-ttu-id="3dc98-251">Демонстрация будет правильно рассчитывается.</span><span class="sxs-lookup"><span data-stu-id="3dc98-251">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="3dc98-252">Этот рабочий процесс применяет исправление только к коду, который выполняется в браузере.</span><span class="sxs-lookup"><span data-stu-id="3dc98-252">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="3dc98-253">Она не исправляет код для всех пользователей, которые посещает страницу.</span><span class="sxs-lookup"><span data-stu-id="3dc98-253">It does not fix the code for all users that visit your page.</span></span>  <span data-ttu-id="3dc98-254">Для этого вам нужно исправить код, который находится на сервере.</span><span class="sxs-lookup"><span data-stu-id="3dc98-254">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="3dc98-255">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="3dc98-255">Next steps</span></span>   

<span data-ttu-id="3dc98-256">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="3dc98-256">Congratulations!</span></span>  <span data-ttu-id="3dc98-257">Теперь вы знаете, как максимально эффективно использовать Microsoft Edge DevTools при отладке JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3dc98-257">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="3dc98-258">Средства и методы, описанные в этом учебнике, помогут вам сэкономить бесчисленные часы.</span><span class="sxs-lookup"><span data-stu-id="3dc98-258">The tools and methods you learned in this tutorial may save you countless hours.</span></span>  

<span data-ttu-id="3dc98-259">В этом учебнике показано два способа задания точек останова.</span><span class="sxs-lookup"><span data-stu-id="3dc98-259">This tutorial only showed you two ways to set breakpoints.</span></span>  <span data-ttu-id="3dc98-260">DevTools включает в себя множество других способов, включая следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="3dc98-260">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="3dc98-261">Условные точки останова, которые запускаются только в случае, если предоставленное условие истинно.</span><span class="sxs-lookup"><span data-stu-id="3dc98-261">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="3dc98-262">Точки останова в перехваченных или неперехваченных исключениях.</span><span class="sxs-lookup"><span data-stu-id="3dc98-262">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="3dc98-263">XHR точки останова, которые инициируются, когда запрашиваемый URL-адрес соответствует подстроке, которую вы задаете.</span><span class="sxs-lookup"><span data-stu-id="3dc98-263">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="3dc98-264">Для получения дополнительных сведений о том, когда и как использовать каждый из типов, перейдите к разделу [Остановка кода с точки останова][DevtoolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="3dc98-264">For more information about when and how to use each type, go to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="3dc98-265">В этом учебнике описаны несколько элементов управления пошаговым выполнением кода.</span><span class="sxs-lookup"><span data-stu-id="3dc98-265">There are a couple of code stepping controls that were not explained in this tutorial.</span></span>  <span data-ttu-id="3dc98-266">Дополнительные сведения можно найти на странице [Шаг с заходом в строке кода][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="3dc98-266">For more information, go to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Приостановка кода с точки останова в Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Пошаговое руководство по отладке кода-JavaScript | Документы Microsoft"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Открыть демонстрацию | Цепь"  

> [!NOTE]
> <span data-ttu-id="3dc98-270">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3dc98-270">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3dc98-271">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3dc98-271">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3dc98-273">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3dc98-273">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

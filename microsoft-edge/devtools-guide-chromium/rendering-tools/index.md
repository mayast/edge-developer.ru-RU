---
title: Анализ производительности среды выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 7705428dba2ca368eb8f61b13bb96901756b081f
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611866"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="ce825-103">Анализ производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="ce825-103">Analyze Runtime Performance</span></span>   




<span data-ttu-id="ce825-104">Пользователи ожидают интерактивные и плавные страницы.</span><span class="sxs-lookup"><span data-stu-id="ce825-104">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="ce825-105">Каждый этап конвейера на пиксельах представляет возможность введения Jank.</span><span class="sxs-lookup"><span data-stu-id="ce825-105">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="ce825-106">Узнайте о средствах и стратегиях, позволяющих выявить и устранить распространенные проблемы, которые замедляют производительность во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce825-106">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <span data-ttu-id="ce825-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ce825-107">Summary</span></span>  

*   <span data-ttu-id="ce825-108">Не записывайте JavaScript, который заставляет браузер обновить макет.</span><span class="sxs-lookup"><span data-stu-id="ce825-108">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="ce825-109">Разделяйте функции чтения и записи, а затем выполняйте операции чтения первыми.</span><span class="sxs-lookup"><span data-stu-id="ce825-109">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="ce825-110">Не переусложняйте CSS.</span><span class="sxs-lookup"><span data-stu-id="ce825-110">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="ce825-111">Используйте меньший CSS, чтобы сделать селекторы CSS простыми.</span><span class="sxs-lookup"><span data-stu-id="ce825-111">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="ce825-112">Старайтесь не использовать разметку максимально возможной.</span><span class="sxs-lookup"><span data-stu-id="ce825-112">Avoid layout as much as possible.</span></span>  <span data-ttu-id="ce825-113">Выберите CSS, для которого не запущен макет.</span><span class="sxs-lookup"><span data-stu-id="ce825-113">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="ce825-114">Рисование может занимать больше времени, чем любые другие действия рендеринга.</span><span class="sxs-lookup"><span data-stu-id="ce825-114">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="ce825-115">Посмотрите, как узкие места закрашивания закраски.</span><span class="sxs-lookup"><span data-stu-id="ce825-115">Watch out for paint bottlenecks.</span></span>  

## <span data-ttu-id="ce825-116">JavaScript</span><span class="sxs-lookup"><span data-stu-id="ce825-116">JavaScript</span></span>  

<span data-ttu-id="ce825-117">Вычисления JavaScript, особенно те, которые вызывают сложные визуальные изменения, могут привести к снижению производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="ce825-117">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="ce825-118">Не разрешать неправильное или долгое выполнение JavaScript, мешая взаимодействию с пользователем.</span><span class="sxs-lookup"><span data-stu-id="ce825-118">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <span data-ttu-id="ce825-119">JavaScript: инструменты</span><span class="sxs-lookup"><span data-stu-id="ce825-119">JavaScript: Tools</span></span>  

<span data-ttu-id="ce825-120">Сделайте запись на панели " **производительность** " и найдите подозрительные `Evaluate Script` события.</span><span class="sxs-lookup"><span data-stu-id="ce825-120">Take a recording in the **Performance** panel and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="ce825-121">е, что вы проjankе в JavaScript, вам может потребоваться выполнить анализ следующего уровня и собрать профиль ЦП JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ce825-121">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="ce825-122">В профилях ЦП показано, где в функциях страницы потратила среда выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce825-122">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="ce825-123">В этой статье объясняется, как создавать профили ЦП с использованием [ускорения выполнения JavaScript][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="ce825-123">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <span data-ttu-id="ce825-124">JavaScript: проблемы</span><span class="sxs-lookup"><span data-stu-id="ce825-124">JavaScript: Problems</span></span>  

<span data-ttu-id="ce825-125">В приведенной ниже таблице описаны некоторые распространенные проблемы JavaScript и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="ce825-125">The following table describes some common JavaScript problems and potential solutions:</span></span>  

| <span data-ttu-id="ce825-126">Проблема</span><span class="sxs-lookup"><span data-stu-id="ce825-126">Problem</span></span> | <span data-ttu-id="ce825-127">Пример.</span><span class="sxs-lookup"><span data-stu-id="ce825-127">Example</span></span> | <span data-ttu-id="ce825-128">Решение</span><span class="sxs-lookup"><span data-stu-id="ce825-128">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ce825-129">Ресурсоемкие обработчики входных данных, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-129">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="ce825-130">Сенсор, параллакс прокрутку.</span><span class="sxs-lookup"><span data-stu-id="ce825-130">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="ce825-131">Разрешите браузеру управлять сенсорными и прокруткой или привяжите прослушиватель как можно позже.</span><span class="sxs-lookup"><span data-stu-id="ce825-131">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="ce825-132">Просмотр [ресурсоемких обработчиков ввода в контрольном списке производительности в пол Lewis and "][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="ce825-132">See [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="ce825-133">Некорректное применение JavaScript, которое влияет на отклик, анимацию, загрузку.</span><span class="sxs-lookup"><span data-stu-id="ce825-133">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="ce825-134">Пользователь выполняет прокрутку сразу после загрузки страницы, setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="ce825-134">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="ce825-135">Оптимизация среды выполнения JavaScript: использование `requestAnimationFrame` , распространение управления DOM на кадры и использование [веб-рабочих процессов][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="ce825-135">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="ce825-136">Длительное выполнение ответа на JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ce825-136">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="ce825-137">[Событие DOMContentLoaded][MDNUsingWebWorkers] останавливается, так как оно вашего удобства с помощью JS.</span><span class="sxs-lookup"><span data-stu-id="ce825-137">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="ce825-138">Перевод чистых вычислительных трудозатрат на [веб-рабочие процессы][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="ce825-138">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="ce825-139">Если вам нужен доступ DOM, используйте `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="ce825-139">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="ce825-140">Сценарии сборки мусора, влияющие на ответ или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-140">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="ce825-141">Сбор мусора может происходить везде, где бы вы ни находились</span><span class="sxs-lookup"><span data-stu-id="ce825-141">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="ce825-142">Создавать менее сценарии сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="ce825-142">Write less garbage-y scripts.</span></span>  <span data-ttu-id="ce825-143">Ознакомьтесь со [сборкой мусора в анимации в контрольном списке производительности в пол Lewis and "][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="ce825-143">See [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <span data-ttu-id="ce825-144">Стиль</span><span class="sxs-lookup"><span data-stu-id="ce825-144">Style</span></span>  

<span data-ttu-id="ce825-145">Изменение стиля — это дорогостоящие особенности, особенно если эти изменения влияют на более чем один элемент в DOM.</span><span class="sxs-lookup"><span data-stu-id="ce825-145">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="ce825-146">Каждый раз, когда к элементу применяются стили, браузер отражает влияние на все связанные элементы, пересчитывать макет и перекрашивать.</span><span class="sxs-lookup"><span data-stu-id="ce825-146">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <span data-ttu-id="ce825-147">Стиль: инструменты</span><span class="sxs-lookup"><span data-stu-id="ce825-147">Style: Tools</span></span>  

<span data-ttu-id="ce825-148">Сделайте запись на панели " **производительность** ".</span><span class="sxs-lookup"><span data-stu-id="ce825-148">Take a recording in the **Performance** panel.</span></span>  <span data-ttu-id="ce825-149">Проверка записи для больших `Recalculate Style` событий (отображается фиолетовым).</span><span class="sxs-lookup"><span data-stu-id="ce825-149">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="ce825-150">Щелкните событие, `Recalculate Style` чтобы просмотреть дополнительные сведения о нем в области **сведений** .</span><span class="sxs-lookup"><span data-stu-id="ce825-150">Click on a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="ce825-151">Если изменение стиля занимает много времени, это снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="ce825-151">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="ce825-152">Если вычисления стиля влияют на большое количество элементов, это еще одна область с комнатой для улучшения.</span><span class="sxs-lookup"><span data-stu-id="ce825-152">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

> ##### <span data-ttu-id="ce825-153">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="ce825-153">Figure 1</span></span>  
> <span data-ttu-id="ce825-154">Длинный стиль пересчета</span><span class="sxs-lookup"><span data-stu-id="ce825-154">Long recalculate style</span></span>  
> ![Длинный стиль пересчета][ImageLongRecalculateStyle]

<span data-ttu-id="ce825-156">Чтобы уменьшить влияние событий, `Recalculate Style` сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="ce825-156">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="ce825-157">Используйте [триггеры CSS][CssTriggers] , чтобы выяснить, какие свойства CSS активируют макет, Paint и Composite.</span><span class="sxs-lookup"><span data-stu-id="ce825-157">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="ce825-158">Эти свойства имеют наихудшее влияние на производительность отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ce825-158">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="ce825-159">Переключиться на свойства с меньшим влиянием.</span><span class="sxs-lookup"><span data-stu-id="ce825-159">Switch to properties that have less impact.</span></span>  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <span data-ttu-id="ce825-160">Стиль: проблемы</span><span class="sxs-lookup"><span data-stu-id="ce825-160">Style: Problems</span></span>  

<span data-ttu-id="ce825-161">В таблице ниже описаны некоторые распространенные проблемы стиля и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="ce825-161">The following table describes some common style problems and potential solutions:</span></span>  

| <span data-ttu-id="ce825-162">Проблема</span><span class="sxs-lookup"><span data-stu-id="ce825-162">Problem</span></span> | <span data-ttu-id="ce825-163">Пример.</span><span class="sxs-lookup"><span data-stu-id="ce825-163">Example</span></span> | <span data-ttu-id="ce825-164">Решение</span><span class="sxs-lookup"><span data-stu-id="ce825-164">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ce825-165">Дорогостоящие расчеты стиля, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-165">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="ce825-166">Любое свойство CSS, которое изменяет геометрию элемента, например ширину, высоту или расположение; Браузер проверяет все другие элементы и пересчитывает макет.</span><span class="sxs-lookup"><span data-stu-id="ce825-166">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="ce825-167">Старайтесь не использовать CSS, которые инициируют макеты</span><span class="sxs-lookup"><span data-stu-id="ce825-167">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="ce825-168">Сложные селекторы, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-168">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="ce825-169">Вложенные элементы выбора заставляют браузер знать все о всех остальных элементах, включая родительские и дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="ce825-169">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="ce825-170">Сослаться на элемент в таблице CSS только с помощью класса.</span><span class="sxs-lookup"><span data-stu-id="ce825-170">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <span data-ttu-id="ce825-171">Макет</span><span class="sxs-lookup"><span data-stu-id="ce825-171">Layout</span></span>  

<span data-ttu-id="ce825-172">Макет (или перекомпоновка в Firefox) — это процесс, с помощью которого браузер вычисляет позиции и размеры всех элементов на странице.</span><span class="sxs-lookup"><span data-stu-id="ce825-172">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="ce825-173">Модель макета веба означает, что один элемент может повлиять на других пользователей; Например, ширина `<body>` элемента обычно влияет на ширину дочерних элементов и т. д., так же, как и вниз по дереву.</span><span class="sxs-lookup"><span data-stu-id="ce825-173">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="ce825-174">Процесс может быть довольно вовлеченным в браузер.</span><span class="sxs-lookup"><span data-stu-id="ce825-174">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="ce825-175">Как правило, если вы запрашиваете значение геометрического значения из DOM перед завершением кадра, вы собираетесь найти себя с помощью принудительно синхронных макетов, что может привести к значительному снижению производительности, если часто приходится создавать большое дерево DOM.</span><span class="sxs-lookup"><span data-stu-id="ce825-175">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <span data-ttu-id="ce825-176">Макет: инструменты</span><span class="sxs-lookup"><span data-stu-id="ce825-176">Layout: Tools</span></span>  

<span data-ttu-id="ce825-177">Область **производительности** определяет, когда страница вызывает принудительно синхронные макеты.</span><span class="sxs-lookup"><span data-stu-id="ce825-177">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="ce825-178">Эти `Layout` события помечены красными отрезками.</span><span class="sxs-lookup"><span data-stu-id="ce825-178">These `Layout` events are marked with red bars.</span></span>  

> ##### <span data-ttu-id="ce825-179">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="ce825-179">Figure 2</span></span>  
> <span data-ttu-id="ce825-180">Принудительно синхронный макет</span><span class="sxs-lookup"><span data-stu-id="ce825-180">Forced synchronous layout</span></span>  
> ![Принудительно синхронный макет][ImageForcedSynchronousLayout]  

<span data-ttu-id="ce825-182">"Макет Thrashing" — это повторение принудительно синхронно заданных условий макета.</span><span class="sxs-lookup"><span data-stu-id="ce825-182">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="ce825-183">Это происходит, когда JavaScript пишет и считывает из DOM многократно, что приводит к пересчету макета в браузере.</span><span class="sxs-lookup"><span data-stu-id="ce825-183">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="ce825-184">Чтобы определить макет Thrashing, найдите шаблон с несколькими принудительно синхронными предупреждениями макета.</span><span class="sxs-lookup"><span data-stu-id="ce825-184">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="ce825-185">Смотрите [Рисунок 2](#figure-2).</span><span class="sxs-lookup"><span data-stu-id="ce825-185">See [Figure 2](#figure-2).</span></span>  

### <span data-ttu-id="ce825-186">Макет: проблемы</span><span class="sxs-lookup"><span data-stu-id="ce825-186">Layout: Problems</span></span>  

<span data-ttu-id="ce825-187">В таблице ниже описаны некоторые типичные проблемы с макетами и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="ce825-187">The following table describes some common layout problems and potential solutions:</span></span>  

| <span data-ttu-id="ce825-188">Проблема</span><span class="sxs-lookup"><span data-stu-id="ce825-188">Problem</span></span> | <span data-ttu-id="ce825-189">Пример.</span><span class="sxs-lookup"><span data-stu-id="ce825-189">Example</span></span> | <span data-ttu-id="ce825-190">Решение</span><span class="sxs-lookup"><span data-stu-id="ce825-190">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ce825-191">Принудительно синхронный макет, влияющий на ответ или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-191">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="ce825-192">Принудительное выполнение браузером более ранней версии в конвейере пикселей, что приводит к повторяющимся действиям в процессе отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ce825-192">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="ce825-193">Предварительно заполните свой стиль, а затем выполните все операции записи.</span><span class="sxs-lookup"><span data-stu-id="ce825-193">Batch your style reads first, then do any writes.</span></span>  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="ce825-194">Макет Thrashing влияет на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-194">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="ce825-195">Цикл, покрывающий браузер, в цикле чтения и записи-чтения, который принудительно пересчитывает макет, переключаясь в браузер.</span><span class="sxs-lookup"><span data-stu-id="ce825-195">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="ce825-196">Автоматическая обработка пакетных операций чтения и записи с помощью [библиотеки FastDom][GitHubWilsonpageFastdom].</span><span class="sxs-lookup"><span data-stu-id="ce825-196">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <span data-ttu-id="ce825-197">Рисование и совмещение цветов</span><span class="sxs-lookup"><span data-stu-id="ce825-197">Paint and composite</span></span>  

<span data-ttu-id="ce825-198">Заливка — это процесс заполнения пикселов.</span><span class="sxs-lookup"><span data-stu-id="ce825-198">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="ce825-199">Это часто является наиболее дорогостоящей частью процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ce825-199">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="ce825-200">Если вы заметили, что ваша страница janky, возможно, у вас возникли проблемы с окрашиванием.</span><span class="sxs-lookup"><span data-stu-id="ce825-200">If you noticed that your page is janky in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="ce825-201">Композиция — это область, в которой окрашенные части страницы размещаются вместе для отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="ce825-201">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="ce825-202">В большинстве случаев, если вы перейдете на свойства, предназначенные только для компоновщика, и не можете вообще обрисовываться, вы увидите значительную улучшенность в производительности, но вам нужно пронаблюдать за избыточными счетчиками слоев.</span><span class="sxs-lookup"><span data-stu-id="ce825-202">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should see a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <span data-ttu-id="ce825-203">Рисование и совмещение: инструменты</span><span class="sxs-lookup"><span data-stu-id="ce825-203">Paint and composite: Tools</span></span>  

<span data-ttu-id="ce825-204">Хотите узнать, как долго рисуются и как часто происходит рисование?</span><span class="sxs-lookup"><span data-stu-id="ce825-204">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="ce825-205">Установите флажок [включить дополнительные возможности инструментирования Paint][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] на панели **производительности** и сделайте запись.</span><span class="sxs-lookup"><span data-stu-id="ce825-205">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="ce825-206">Если большая часть времени отрисовки потратила на рисование, у вас возникли проблемы с рисованием.</span><span class="sxs-lookup"><span data-stu-id="ce825-206">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
> ##### Old Figure 3  
> Long paint times in timeline recording  
> ![Long paint times in timeline recording][ImageLongPaintTimes]  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <span data-ttu-id="ce825-207">Раскрашивание и совмещение: проблемы</span><span class="sxs-lookup"><span data-stu-id="ce825-207">Paint and composite: Problems</span></span>  

<span data-ttu-id="ce825-208">В таблице ниже описаны некоторые распространенные проблемы, возникающие при работе с закрасками и комплексными решениями.</span><span class="sxs-lookup"><span data-stu-id="ce825-208">The following table describes some common paint and composite problems and potential solutions:</span></span>  

| <span data-ttu-id="ce825-209">Проблема</span><span class="sxs-lookup"><span data-stu-id="ce825-209">Problem</span></span> | <span data-ttu-id="ce825-210">Пример.</span><span class="sxs-lookup"><span data-stu-id="ce825-210">Example</span></span> | <span data-ttu-id="ce825-211">Решение</span><span class="sxs-lookup"><span data-stu-id="ce825-211">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ce825-212">Эффекты рисования влияют на реакцию или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-212">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="ce825-213">Большие области или дорогостоящие краски влияют на реакцию или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-213">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="ce825-214">Избегайте рисования, продвижение элементов, которые перемещаются в собственный слой, использование преобразований и непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="ce825-214">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="ce825-215">Развертывание слоев влияет на анимацию.</span><span class="sxs-lookup"><span data-stu-id="ce825-215">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="ce825-216">Превышение избыточного продвижения слишком большого количества элементов `translateZ(0)` заметно влияет на производительность анимации.</span><span class="sxs-lookup"><span data-stu-id="ce825-216">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="ce825-217">Придвигайте к слоям экономно и только в том случае, если вы знаете, что она содержит существенные улучшения.</span><span class="sxs-lookup"><span data-stu-id="ce825-217">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageLongRecalculateStyle]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-performance-recalculate-style-summary.msft.png "Рисунок 1: длинный пересчет стиля"  
[ImageForcedSynchronousLayout]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-jank-performance-recalculate-style-summary.msft.png "Рисунок 2: принудительно синхронный макет"  
<!--[ImageLongPaintTimes]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png "Old Figure 3: Long paint times in timeline recording"  -->  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Ускорение выполнения JavaScript"  

[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#enable-advanced-paint-instrumentation "Включение расширенного инструментария рисования — справочные материалы по анализу производительности"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: /microsoft-edge/devtools-guide-chromium/rendering-tools/forced-synchronous-layouts "Diagnose Forced Synchronous Layouts"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Триггеры CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-сотрудников | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Контрольный список производительности во время выполнения — Календарь веб-производительности"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="ce825-226">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ce825-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ce825-227">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="ce825-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ce825-229">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ce825-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

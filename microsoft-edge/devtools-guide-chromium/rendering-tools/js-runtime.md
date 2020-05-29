---
title: Ускорение выполнения JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 0e198be3e1cef53590a24bfaa2382746ced299ed
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611873"
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
   limitations under the License. -->





# <span data-ttu-id="69867-103">Ускорение выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="69867-103">Speed Up JavaScript Runtime</span></span>   




<span data-ttu-id="69867-104">Нахождение ресурсоемких функций с помощью панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="69867-104">Identify expensive functions using the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="69867-105">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="69867-105">Figure 1</span></span>  
> <span data-ttu-id="69867-106">Профили выборки</span><span class="sxs-lookup"><span data-stu-id="69867-106">Sampling Profiles</span></span>  
> ![Профили выборки][ImageCpuProfile]  

### <span data-ttu-id="69867-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="69867-108">Summary</span></span>  

*   <span data-ttu-id="69867-109">Записывайте именно те функции, которые были вызваны, и объем памяти, необходимый для выделения ресурсов, на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="69867-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="69867-110">Визуализируйте свои профили как flameную диаграмму.</span><span class="sxs-lookup"><span data-stu-id="69867-110">Visualize your profiles as a flame chart.</span></span>  

## <span data-ttu-id="69867-111">Запись профиля выборки</span><span class="sxs-lookup"><span data-stu-id="69867-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="69867-112">Если вы заметили, что Jank в коде JavaScript, соберите профиль выборки.</span><span class="sxs-lookup"><span data-stu-id="69867-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="69867-113">Профили выборки показывают, где на странице потратило время выполнения.</span><span class="sxs-lookup"><span data-stu-id="69867-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="69867-114">Откройте панель **память** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="69867-114">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="69867-115">Установите переключатель **выборка распределения** .</span><span class="sxs-lookup"><span data-stu-id="69867-115">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="69867-116">Нажмите кнопку **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="69867-116">Select **Start**.</span></span>  
1.  <span data-ttu-id="69867-117">В зависимости от того, что вы пытаетесь проанализировать, вы можете либо повторно загрузить страницу, взаимодействовать со страницей, либо просто разрешить выполнение страницы.</span><span class="sxs-lookup"><span data-stu-id="69867-117">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="69867-118">Когда все будет готово, нажмите кнопку **остановить** .</span><span class="sxs-lookup"><span data-stu-id="69867-118">Select the **Stop** button when you are finished.</span></span>  

> [!NOTE]
> <span data-ttu-id="69867-119">Вы также можете использовать [API консольных утилит][DevtoolsConsoleUtilities] для записи и группировки профилей из командной строки.</span><span class="sxs-lookup"><span data-stu-id="69867-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="69867-120">Просмотр профиля выборки</span><span class="sxs-lookup"><span data-stu-id="69867-120">View Sampling Profile</span></span>  

<span data-ttu-id="69867-121">Когда вы закончите запись, DevTools автоматически заполнит панель **памяти** в разделе **Профили выборки** с данными из записи.</span><span class="sxs-lookup"><span data-stu-id="69867-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="69867-122">Представление по умолчанию имеет **большой вид \ (снизу вверх)**.</span><span class="sxs-lookup"><span data-stu-id="69867-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="69867-123">Это представление позволяет узнать, какие функции приводили к снижению производительности и как проанализировать пути вызова для этих функций.</span><span class="sxs-lookup"><span data-stu-id="69867-123">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="69867-124">Изменение порядка сортировки</span><span class="sxs-lookup"><span data-stu-id="69867-124">Change sort order</span></span>   

<span data-ttu-id="69867-125">Чтобы изменить порядок сортировки, щелкните раскрывающееся меню рядом с **выбранным** ![ значком функции фокус выделения, ][ImageFocusIcon] а затем выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="69867-125">To change the sorting order, select the dropdown menu next to the **focus selected function** ![focus selected function][ImageFocusIcon] icon and then choose one of the following options.</span></span>

<span data-ttu-id="69867-126">**Диаграмма**.</span><span class="sxs-lookup"><span data-stu-id="69867-126">**Chart**.</span></span>  <span data-ttu-id="69867-127">Диаграмма, на которой показана Хронология записи.</span><span class="sxs-lookup"><span data-stu-id="69867-127">Displays a chronological chart of the recording.</span></span>  

> ##### <span data-ttu-id="69867-128">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="69867-128">Figure 2</span></span>  
> <span data-ttu-id="69867-129">Flame диаграмма</span><span class="sxs-lookup"><span data-stu-id="69867-129">Flame chart</span></span>  
> ![Flame диаграмма][ImageFlameChart]  

<span data-ttu-id="69867-131">**Тяжелая – (снизу вверх)**.</span><span class="sxs-lookup"><span data-stu-id="69867-131">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="69867-132">Перечисление функций, влияющих на производительность, и позволяет исследовать пути вызова функций.</span><span class="sxs-lookup"><span data-stu-id="69867-132">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="69867-133">Это представление по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69867-133">This is the default view.</span></span>  

> ##### <span data-ttu-id="69867-134">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="69867-134">Figure 3</span></span>  
> <span data-ttu-id="69867-135">Тяжелая диаграмма</span><span class="sxs-lookup"><span data-stu-id="69867-135">Heavy chart</span></span>  
> ![Тяжелая диаграмма][ImageHeavyChart]  

<span data-ttu-id="69867-137">**Дерево \ (сверху вниз)**.</span><span class="sxs-lookup"><span data-stu-id="69867-137">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="69867-138">Показывает общую картину структуры вызова, начиная с верхней части стека вызова.</span><span class="sxs-lookup"><span data-stu-id="69867-138">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

> ##### <span data-ttu-id="69867-139">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="69867-139">Figure 4</span></span>  
> <span data-ttu-id="69867-140">Древовидная диаграмма</span><span class="sxs-lookup"><span data-stu-id="69867-140">Tree chart</span></span>  
> ![Древовидная диаграмма][ImageTreeChart]  

### <span data-ttu-id="69867-142">Исключить функции</span><span class="sxs-lookup"><span data-stu-id="69867-142">Exclude functions</span></span>   

<span data-ttu-id="69867-143">Чтобы исключить функцию из профиля с выборочными тестами, выделите ее, а затем выберите значок исключить **выбранную функцию** ![ исключить выбранный элемент ][ImageExcludeIcon] .</span><span class="sxs-lookup"><span data-stu-id="69867-143">To exclude a function from your Sampling Profile, select it to select it and then select the **exclude selected function** ![exclude selected function][ImageExcludeIcon] icon.</span></span>  <span data-ttu-id="69867-144">Функция запроса \ (родительский элемент) исключенной функции \ (дочерней) оценивается выделенной памятью, назначенной исключенной функции \ (дочерняя).</span><span class="sxs-lookup"><span data-stu-id="69867-144">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="69867-145">Нажмите кнопку **восстановить** все функции ![ восстановить все функции ][ImageRestoreIcon] , чтобы восстановить все исключенные функции, возвращенные в запись.</span><span class="sxs-lookup"><span data-stu-id="69867-145">Select the **restore all functions** ![restore all functions][ImageRestoreIcon] icon to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="69867-146">Просмотр профиля выборки как диаграммы</span><span class="sxs-lookup"><span data-stu-id="69867-146">View Sampling Profile as Chart</span></span>   

<span data-ttu-id="69867-147">Представление Диаграмма обеспечивает визуальное представление профиля выборки с течением времени.</span><span class="sxs-lookup"><span data-stu-id="69867-147">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="69867-148">После [записи профиля выборочной](#record-a-sampling-profile)настройки просмотрите запись в виде Flame диаграммы, [изменив порядок сортировки](#change-sort-order) на **Chart**.</span><span class="sxs-lookup"><span data-stu-id="69867-148">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

> ##### <span data-ttu-id="69867-149">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="69867-149">Figure 5</span></span>  
> <span data-ttu-id="69867-150">Flame представления диаграммы</span><span class="sxs-lookup"><span data-stu-id="69867-150">Flame chart view</span></span>  
> ![Flame представления диаграммы][ImageFlameChartView]  

<span data-ttu-id="69867-152">Flame диаграмма делится на две части.</span><span class="sxs-lookup"><span data-stu-id="69867-152">The flame chart is split into two parts.</span></span>  

| | <span data-ttu-id="69867-153">Составляющая</span><span class="sxs-lookup"><span data-stu-id="69867-153">Part</span></span> | <span data-ttu-id="69867-154">Описание</span><span class="sxs-lookup"><span data-stu-id="69867-154">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="69867-155">1,1</span><span class="sxs-lookup"><span data-stu-id="69867-155">1</span></span> | <span data-ttu-id="69867-156">Обзор</span><span class="sxs-lookup"><span data-stu-id="69867-156">Overview</span></span> | <span data-ttu-id="69867-157">Представление всей записи в Birds взгляда.</span><span class="sxs-lookup"><span data-stu-id="69867-157">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="69867-158">Высота отрезков соответствует глубине стека вызова.</span><span class="sxs-lookup"><span data-stu-id="69867-158">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="69867-159">Таким образом, чем выше отрезок, тем глубже стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="69867-159">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="69867-160">2</span><span class="sxs-lookup"><span data-stu-id="69867-160">2</span></span> | <span data-ttu-id="69867-161">Стеки вызовов</span><span class="sxs-lookup"><span data-stu-id="69867-161">Call Stacks</span></span> | <span data-ttu-id="69867-162">Это подробное представление функций, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="69867-162">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="69867-163">Горизонтальная ось — это время и вертикальная ось — стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="69867-163">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="69867-164">Стеки организованы сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="69867-164">The stacks are organized top-down.</span></span>  <span data-ttu-id="69867-165">Таким образом, функция сверху вызывается под ней и т. д.</span><span class="sxs-lookup"><span data-stu-id="69867-165">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="69867-166">Функции окрашены в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="69867-166">Functions are colored randomly.</span></span>  <span data-ttu-id="69867-167">Нет связи с цветами, используемыми в других панелях.</span><span class="sxs-lookup"><span data-stu-id="69867-167">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="69867-168">Однако функции всегда выделяются одинаково во всех вызовах, чтобы можно было видеть закономерности в каждой среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="69867-168">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

> ##### <span data-ttu-id="69867-169">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="69867-169">Figure 6</span></span>  
> <span data-ttu-id="69867-170">Диаграмма с аннотированными Flame</span><span class="sxs-lookup"><span data-stu-id="69867-170">Annotated flame chart</span></span>  
> ![Диаграмма с аннотированными Flame][ImageAnnotatedFlameChart]  

<span data-ttu-id="69867-172">Высокий стек вызовов не обязательно важен, это означает, что было вызвано много функций.</span><span class="sxs-lookup"><span data-stu-id="69867-172">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="69867-173">Но широкий отрезок означает, что выполнение функции заняло много времени.</span><span class="sxs-lookup"><span data-stu-id="69867-173">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="69867-174">Они являются кандидатами для оптимизации.</span><span class="sxs-lookup"><span data-stu-id="69867-174">These are candidates for optimization.</span></span>  

### <span data-ttu-id="69867-175">Масштабирование отдельных частей записи</span><span class="sxs-lookup"><span data-stu-id="69867-175">Zoom in on specific parts of recording</span></span>   

<span data-ttu-id="69867-176">Выберите, удерживайте и перетащите указатель мыши по левому краю обзора и проведите по экрану, чтобы увеличить масштаб отдельных частей стека вызова.</span><span class="sxs-lookup"><span data-stu-id="69867-176">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="69867-177">После масштабирования стек вызовов автоматически отображает выбранную часть записи.</span><span class="sxs-lookup"><span data-stu-id="69867-177">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

> ##### <span data-ttu-id="69867-178">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="69867-178">Figure 7</span></span>  
> <span data-ttu-id="69867-179">Диаграмма с увеличенным масштабом</span><span class="sxs-lookup"><span data-stu-id="69867-179">Chart zoomed</span></span>  
> ![Диаграмма с увеличенным масштабом][ImageFlameChartZoomed]  

### <span data-ttu-id="69867-181">Просмотр сведений о функции</span><span class="sxs-lookup"><span data-stu-id="69867-181">View function details</span></span>   

<span data-ttu-id="69867-182">Выберите функцию, чтобы просмотреть ее определение на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="69867-182">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="69867-183">Наведите указатель мыши на функцию, чтобы отобразить имя и данные о времени.</span><span class="sxs-lookup"><span data-stu-id="69867-183">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="69867-184">Ниже приведены сведения.</span><span class="sxs-lookup"><span data-stu-id="69867-184">The following information is provided.</span></span>  

| <span data-ttu-id="69867-185">Подробнее</span><span class="sxs-lookup"><span data-stu-id="69867-185">Detail</span></span> | <span data-ttu-id="69867-186">Описание</span><span class="sxs-lookup"><span data-stu-id="69867-186">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="69867-187">Name</span><span class="sxs-lookup"><span data-stu-id="69867-187">Name</span></span>** | <span data-ttu-id="69867-188">Имя функции.</span><span class="sxs-lookup"><span data-stu-id="69867-188">The name of the function.</span></span>  |  
| **<span data-ttu-id="69867-189">Сам размер</span><span class="sxs-lookup"><span data-stu-id="69867-189">Self size</span></span>** | <span data-ttu-id="69867-190">Размер текущего вызова функции, включая только инструкции в функции.</span><span class="sxs-lookup"><span data-stu-id="69867-190">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="69867-191">Общий размер</span><span class="sxs-lookup"><span data-stu-id="69867-191">Total size</span></span>** | <span data-ttu-id="69867-192">Размер текущего вызова функции и всех ее вызываемых функций.</span><span class="sxs-lookup"><span data-stu-id="69867-192">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="69867-193">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="69867-193">URL</span></span>** | <span data-ttu-id="69867-194">Расположение определения функции в форме `base.js:261` Where `base.js` — имя файла, в котором определена функция, и `261` является номером строки определения.</span><span class="sxs-lookup"><span data-stu-id="69867-194">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

> ##### <span data-ttu-id="69867-195">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="69867-195">Figure 8</span></span>  
> <span data-ttu-id="69867-196">Просмотр сведений о функциях на диаграмме</span><span class="sxs-lookup"><span data-stu-id="69867-196">Viewing functions details in chart</span></span>  
> ![Просмотр сведений о функциях на диаграмме][ImageFunctionsDetails]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageExcludeIcon]: /microsoft-edge/devtools-guide-chromium/media/exclude-icon.msft.png  
[ImageFocusIcon]: /microsoft-edge/devtools-guide-chromium/media/images/focus-icon.msft.png  
[ImageRestoreIcon]: /microsoft-edge/devtools-guide-chromium/media/images/restore-icon.msft.png  

[ImageCpuProfile]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Рисунок 1: профили выборки"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Рисунок 2: Flame диаграмма"  
[ImageHeavyChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Рисунок 3: диаграмма высокой плотности"  
[ImageTreeChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png "Рисунок 4: иерархическая диаграмма"  
[ImageFlameChartView]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Рисунок 5: представление диаграммы Flame"  
[ImageAnnotatedFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png "Рисунок 6: Flame диаграмма с примечаниями"  
[ImageFlameChartZoomed]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png "Рисунок 7: диаграмма с увеличенным масштабом"  
[ImageFunctionsDetails]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png "Рисунок 8: Просмотр сведений о функциях на диаграмме"  

<!-- links -->  

[DevtoolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Справочник по API для консольных программ"  
[DevtoolsConsoleUtilitiesProfile]: /microsoft-edge/devtools-guide-chromium/console/utilities#profile "Справочник по API для служебных программ на консоли"  
[DevtoolsConsoleUtilitiesProfileEnd]: /microsoft-edge/devtools-guide-chromium/console/utilities#profileend "Справочник по API для служебных программ на консоли profileEnd"  

> [!NOTE]
> <span data-ttu-id="69867-209">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="69867-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="69867-210">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="69867-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="69867-212">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="69867-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

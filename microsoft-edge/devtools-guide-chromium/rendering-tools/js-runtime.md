---
title: Ускорение среды выполнения JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2f05ef2911c855df39d60fa732ff5f784ab49473
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984885"
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





# <span data-ttu-id="42cbd-103">Ускорение выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="42cbd-103">Speed up JavaScript runtime</span></span>   




<span data-ttu-id="42cbd-104">Нахождение ресурсоемких функций с помощью панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="42cbd-104">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Профили выборки" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="42cbd-106">Профили выборки</span><span class="sxs-lookup"><span data-stu-id="42cbd-106">Sampling Profiles</span></span>  
:::image-end:::  

### <span data-ttu-id="42cbd-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="42cbd-107">Summary</span></span>  

*   <span data-ttu-id="42cbd-108">Записывайте именно те функции, которые были вызваны, и объем памяти, необходимый для выделения ресурсов, на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="42cbd-108">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="42cbd-109">Визуализируйте свои профили как flameную диаграмму.</span><span class="sxs-lookup"><span data-stu-id="42cbd-109">Visualize your profiles as a flame chart.</span></span>  
    
## <span data-ttu-id="42cbd-110">Запись профиля выборки</span><span class="sxs-lookup"><span data-stu-id="42cbd-110">Record a Sampling Profile</span></span>  

<span data-ttu-id="42cbd-111">Если вы заметили, что Jank в коде JavaScript, соберите профиль выборки.</span><span class="sxs-lookup"><span data-stu-id="42cbd-111">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="42cbd-112">Профили выборки показывают, где на странице потратило время выполнения.</span><span class="sxs-lookup"><span data-stu-id="42cbd-112">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="42cbd-113">Откройте панель **память** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="42cbd-113">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="42cbd-114">Установите переключатель **выборка распределения** .</span><span class="sxs-lookup"><span data-stu-id="42cbd-114">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="42cbd-115">Нажмите кнопку **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="42cbd-115">Select **Start**.</span></span>  
1.  <span data-ttu-id="42cbd-116">В зависимости от того, что вы пытаетесь проанализировать, вы можете либо повторно загрузить страницу, взаимодействовать со страницей, либо просто разрешить выполнение страницы.</span><span class="sxs-lookup"><span data-stu-id="42cbd-116">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="42cbd-117">Когда все будет готово, нажмите кнопку **остановить** .</span><span class="sxs-lookup"><span data-stu-id="42cbd-117">Select the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="42cbd-118">Вы также можете использовать [API консольных утилит][DevtoolsConsoleUtilities] для записи и группировки профилей из командной строки.</span><span class="sxs-lookup"><span data-stu-id="42cbd-118">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="42cbd-119">Просмотр профиля выборки</span><span class="sxs-lookup"><span data-stu-id="42cbd-119">View Sampling Profile</span></span>  

<span data-ttu-id="42cbd-120">Когда вы закончите запись, DevTools автоматически заполнит панель **памяти** в разделе **Профили выборки** с данными из записи.</span><span class="sxs-lookup"><span data-stu-id="42cbd-120">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="42cbd-121">Представление по умолчанию имеет **большой вид \ (снизу вверх)**.</span><span class="sxs-lookup"><span data-stu-id="42cbd-121">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="42cbd-122">Это представление позволяет узнать, какие функции приводили к снижению производительности и как проанализировать пути вызова для этих функций.</span><span class="sxs-lookup"><span data-stu-id="42cbd-122">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="42cbd-123">Изменение порядка сортировки</span><span class="sxs-lookup"><span data-stu-id="42cbd-123">Change sort order</span></span>   

<span data-ttu-id="42cbd-124">Чтобы изменить порядок сортировки, щелкните раскрывающееся меню рядом с **выделенной функцией фокуса** , ![ ][ImageFocusIcon] а затем выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="42cbd-124">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="42cbd-125">**Диаграмма**.</span><span class="sxs-lookup"><span data-stu-id="42cbd-125">**Chart**.</span></span>  <span data-ttu-id="42cbd-126">Диаграмма, на которой показана Хронология записи.</span><span class="sxs-lookup"><span data-stu-id="42cbd-126">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Flame диаграмма" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="42cbd-128">Flame диаграмма</span><span class="sxs-lookup"><span data-stu-id="42cbd-128">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="42cbd-129">**Тяжелая – (снизу вверх)**.</span><span class="sxs-lookup"><span data-stu-id="42cbd-129">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="42cbd-130">Перечисление функций, влияющих на производительность, и позволяет исследовать пути вызова функций.</span><span class="sxs-lookup"><span data-stu-id="42cbd-130">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="42cbd-131">Это представление по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42cbd-131">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Тяжелая диаграмма" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="42cbd-133">Тяжелая диаграмма</span><span class="sxs-lookup"><span data-stu-id="42cbd-133">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="42cbd-134">**Дерево \ (сверху вниз)**.</span><span class="sxs-lookup"><span data-stu-id="42cbd-134">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="42cbd-135">Показывает общую картину структуры вызова, начиная с верхней части стека вызова.</span><span class="sxs-lookup"><span data-stu-id="42cbd-135">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Древовидная диаграмма" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="42cbd-137">Древовидная диаграмма</span><span class="sxs-lookup"><span data-stu-id="42cbd-137">Tree chart</span></span>  
:::image-end:::  

### <span data-ttu-id="42cbd-138">Исключить функции</span><span class="sxs-lookup"><span data-stu-id="42cbd-138">Exclude functions</span></span>   

<span data-ttu-id="42cbd-139">Чтобы исключить функцию из профиля с выборочными тестами, выделите ее, а затем нажмите значок **исключить выбранную функцию** \ (исключить выбранную функцию \ ![ ][ImageExcludeIcon] ).</span><span class="sxs-lookup"><span data-stu-id="42cbd-139">To exclude a function from your Sampling Profile, select it to select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) icon.</span></span>  <span data-ttu-id="42cbd-140">Функция запроса \ (родительский элемент) исключенной функции \ (дочерней) оценивается выделенной памятью, назначенной исключенной функции \ (дочерняя).</span><span class="sxs-lookup"><span data-stu-id="42cbd-140">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="42cbd-141">Щелкните значок **восстановить все функции** \ ( ![ восстановить все функции ][ImageRestoreIcon] \), чтобы восстановить все исключенные функции, возвращенные в запись.</span><span class="sxs-lookup"><span data-stu-id="42cbd-141">Select the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) icon to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="42cbd-142">Просмотр профиля выборки как диаграммы</span><span class="sxs-lookup"><span data-stu-id="42cbd-142">View Sampling Profile as Chart</span></span>   

<span data-ttu-id="42cbd-143">Представление Диаграмма обеспечивает визуальное представление профиля выборки с течением времени.</span><span class="sxs-lookup"><span data-stu-id="42cbd-143">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="42cbd-144">После [записи профиля выборочной](#record-a-sampling-profile)настройки просмотрите запись в виде Flame диаграммы, [изменив порядок сортировки](#change-sort-order) на **Chart**.</span><span class="sxs-lookup"><span data-stu-id="42cbd-144">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Flame представления диаграммы" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="42cbd-146">Flame представления диаграммы</span><span class="sxs-lookup"><span data-stu-id="42cbd-146">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="42cbd-147">Flame диаграмма делится на две части.</span><span class="sxs-lookup"><span data-stu-id="42cbd-147">The flame chart is split into two parts.</span></span>  

| | <span data-ttu-id="42cbd-148">Составляющая</span><span class="sxs-lookup"><span data-stu-id="42cbd-148">Part</span></span> | <span data-ttu-id="42cbd-149">Описание</span><span class="sxs-lookup"><span data-stu-id="42cbd-149">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="42cbd-150">1,1</span><span class="sxs-lookup"><span data-stu-id="42cbd-150">1</span></span> | <span data-ttu-id="42cbd-151">Обзор</span><span class="sxs-lookup"><span data-stu-id="42cbd-151">Overview</span></span> | <span data-ttu-id="42cbd-152">Представление всей записи в Birds взгляда.</span><span class="sxs-lookup"><span data-stu-id="42cbd-152">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="42cbd-153">Высота отрезков соответствует глубине стека вызова.</span><span class="sxs-lookup"><span data-stu-id="42cbd-153">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="42cbd-154">Таким образом, чем выше отрезок, тем глубже стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="42cbd-154">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="42cbd-155">2</span><span class="sxs-lookup"><span data-stu-id="42cbd-155">2</span></span> | <span data-ttu-id="42cbd-156">Стеки вызовов</span><span class="sxs-lookup"><span data-stu-id="42cbd-156">Call Stacks</span></span> | <span data-ttu-id="42cbd-157">Это подробное представление функций, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="42cbd-157">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="42cbd-158">Горизонтальная ось — это время и вертикальная ось — стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="42cbd-158">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="42cbd-159">Стеки организованы сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="42cbd-159">The stacks are organized top-down.</span></span>  <span data-ttu-id="42cbd-160">Таким образом, функция сверху вызывается под ней и т. д.</span><span class="sxs-lookup"><span data-stu-id="42cbd-160">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="42cbd-161">Функции окрашены в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="42cbd-161">Functions are colored randomly.</span></span>  <span data-ttu-id="42cbd-162">Нет связи с цветами, используемыми в других панелях.</span><span class="sxs-lookup"><span data-stu-id="42cbd-162">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="42cbd-163">Однако функции всегда выделяются одинаково во всех вызовах, чтобы можно было видеть закономерности в каждой среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="42cbd-163">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Диаграмма с аннотированными Flame" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="42cbd-165">Диаграмма с аннотированными Flame</span><span class="sxs-lookup"><span data-stu-id="42cbd-165">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="42cbd-166">Высокий стек вызовов не обязательно важен, это означает, что было вызвано много функций.</span><span class="sxs-lookup"><span data-stu-id="42cbd-166">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="42cbd-167">Но широкий отрезок означает, что выполнение функции заняло много времени.</span><span class="sxs-lookup"><span data-stu-id="42cbd-167">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="42cbd-168">Они являются кандидатами для оптимизации.</span><span class="sxs-lookup"><span data-stu-id="42cbd-168">These are candidates for optimization.</span></span>  

### <span data-ttu-id="42cbd-169">Масштабирование отдельных частей записи</span><span class="sxs-lookup"><span data-stu-id="42cbd-169">Zoom in on specific parts of recording</span></span>   

<span data-ttu-id="42cbd-170">Выберите, удерживайте и перетащите указатель мыши по левому краю обзора и проведите по экрану, чтобы увеличить масштаб отдельных частей стека вызова.</span><span class="sxs-lookup"><span data-stu-id="42cbd-170">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="42cbd-171">После масштабирования стек вызовов автоматически отображает выбранную часть записи.</span><span class="sxs-lookup"><span data-stu-id="42cbd-171">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Диаграмма с увеличенным масштабом" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="42cbd-173">Диаграмма с увеличенным масштабом</span><span class="sxs-lookup"><span data-stu-id="42cbd-173">Chart zoomed</span></span>  
:::image-end:::  

### <span data-ttu-id="42cbd-174">Просмотр сведений о функции</span><span class="sxs-lookup"><span data-stu-id="42cbd-174">View function details</span></span>   

<span data-ttu-id="42cbd-175">Выберите функцию, чтобы просмотреть ее определение на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="42cbd-175">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="42cbd-176">Наведите указатель мыши на функцию, чтобы отобразить имя и данные о времени.</span><span class="sxs-lookup"><span data-stu-id="42cbd-176">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="42cbd-177">Ниже приведены сведения.</span><span class="sxs-lookup"><span data-stu-id="42cbd-177">The following information is provided.</span></span>  

| <span data-ttu-id="42cbd-178">Подробнее</span><span class="sxs-lookup"><span data-stu-id="42cbd-178">Detail</span></span> | <span data-ttu-id="42cbd-179">Описание</span><span class="sxs-lookup"><span data-stu-id="42cbd-179">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="42cbd-180">Name</span><span class="sxs-lookup"><span data-stu-id="42cbd-180">Name</span></span>** | <span data-ttu-id="42cbd-181">Имя функции.</span><span class="sxs-lookup"><span data-stu-id="42cbd-181">The name of the function.</span></span>  |  
| **<span data-ttu-id="42cbd-182">Сам размер</span><span class="sxs-lookup"><span data-stu-id="42cbd-182">Self size</span></span>** | <span data-ttu-id="42cbd-183">Размер текущего вызова функции, включая только инструкции в функции.</span><span class="sxs-lookup"><span data-stu-id="42cbd-183">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="42cbd-184">Общий размер</span><span class="sxs-lookup"><span data-stu-id="42cbd-184">Total size</span></span>** | <span data-ttu-id="42cbd-185">Размер текущего вызова функции и всех ее вызываемых функций.</span><span class="sxs-lookup"><span data-stu-id="42cbd-185">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="42cbd-186">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="42cbd-186">URL</span></span>** | <span data-ttu-id="42cbd-187">Расположение определения функции в форме `base.js:261` Where `base.js` — имя файла, в котором определена функция, и `261` является номером строки определения.</span><span class="sxs-lookup"><span data-stu-id="42cbd-187">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Просмотр сведений о функциях на диаграмме" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="42cbd-189">Просмотр сведений о функциях на диаграмме</span><span class="sxs-lookup"><span data-stu-id="42cbd-189">Viewing functions details in chart</span></span>  
:::image-end:::  

<!--  
## Feedback   


-->  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Profile — Справочник по API для служебных программ консоли | Документы Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "Справочник по API для служебных программ на консоли profileEnd | Документы Microsoft"  

> [!NOTE]
> <span data-ttu-id="42cbd-193">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42cbd-193">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="42cbd-194">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="42cbd-194">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="42cbd-196">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42cbd-196">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

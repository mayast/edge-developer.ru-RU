---
title: Использование инструментирования выделения на временной шкале
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: ab7a270e1d599e254aaaf4515b6898cb1d9782fc
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611736"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# <span data-ttu-id="e1889-103">Использование инструментирования выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="e1889-103">How to Use Allocation Instrumentation on Timeline</span></span>  



<span data-ttu-id="e1889-104">Используйте **Инструментирование выделения на временной шкале** , чтобы найти объекты, которые не будут собираться сборщиком мусора, и продолжайте удерживать память.</span><span class="sxs-lookup"><span data-stu-id="e1889-104">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <span data-ttu-id="e1889-105">Как работает Инструментарий выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="e1889-105">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="e1889-106">**Инструмент выделения на временной шкале** объединяет подробные сведения о снимке **профилировщика кучи** с помощью добавочного обновления и отслеживания на панели **производительности** .</span><span class="sxs-lookup"><span data-stu-id="e1889-106">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="e1889-107">Аналогичным образом отслеживание выделения кучи для объектов включает в себя запуск записи, выполнение последовательности действий и остановку записи для анализа.</span><span class="sxs-lookup"><span data-stu-id="e1889-107">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="e1889-108">**Инструментарий выделения на временной шкале** периодически берет моментальные снимки кучи во время записи \ (как обычно каждые 50 MS! \) и один финальный снимок в конце записи.</span><span class="sxs-lookup"><span data-stu-id="e1889-108">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms!\) and one final snapshot at the end of the recording.</span></span>  

> ##### <span data-ttu-id="e1889-109">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="e1889-109">Figure 1</span></span>  
> **<span data-ttu-id="e1889-110">Инструментирование выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="e1889-110">Allocation instrumentation on timeline</span></span>**  
> ![Инструментирование выделения на временной шкале][ImageObjectTracker]  

> [!NOTE]
> <span data-ttu-id="e1889-112">Число после a `@` — это идентификатор объекта, который сохраняется во многих снимках, сделанных в ходе сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="e1889-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="e1889-113">Постоянный идентификатор объекта обеспечивает точное сравнение состояний кучи.</span><span class="sxs-lookup"><span data-stu-id="e1889-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="e1889-114">Объекты перемещаются во время сборки мусора, поэтому отображение адреса объекта не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="e1889-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <span data-ttu-id="e1889-115">Включение инструментирования выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="e1889-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="e1889-116">Выполните эти действия, чтобы приступить к работе с **инструментированием выделения на временной шкале**.</span><span class="sxs-lookup"><span data-stu-id="e1889-116">Follow these steps to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="e1889-117">[Откройте DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="e1889-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="e1889-118">Откройте панель **память** и выберите переключатель **Инструментирование выделения на временной шкале** .</span><span class="sxs-lookup"><span data-stu-id="e1889-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="e1889-119">Start recording.</span><span class="sxs-lookup"><span data-stu-id="e1889-119">Start recording.</span></span>  

> ##### <span data-ttu-id="e1889-120">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="e1889-120">Figure 2</span></span>  
> <span data-ttu-id="e1889-121">Профилировщик записи для выделения кучи</span><span class="sxs-lookup"><span data-stu-id="e1889-121">Record heap allocations profiler</span></span>  
> ![Профилировщик записи для выделения кучи][ImageRecordHeap]  

## <span data-ttu-id="e1889-123">Чтение временной шкалы выделения кучи</span><span class="sxs-lookup"><span data-stu-id="e1889-123">Read a heap allocation timeline</span></span>  

<span data-ttu-id="e1889-124">Временная шкала выделения кучи показывает, где создаются объекты и определяет путь сохранения.</span><span class="sxs-lookup"><span data-stu-id="e1889-124">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="e1889-125">На [рисунке 3](#figure-3)на верхней панели обозначаются новые объекты, найденные в куче.</span><span class="sxs-lookup"><span data-stu-id="e1889-125">In [Figure 3](#figure-3), the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="e1889-126">Высота каждой линии соответствует размеру недавно выделенных объектов, а цвет отрезков показывает, будут ли эти объекты по-прежнему находиться в последнем снимке кучи.</span><span class="sxs-lookup"><span data-stu-id="e1889-126">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="e1889-127">Синие отрезки указывают на объекты, которые по-прежнему находятся в конце временной шкалы, а серые — на объекты, которые были выделены на временной шкале, но с момента сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="e1889-127">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

> ##### <span data-ttu-id="e1889-128">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="e1889-128">Figure 3</span></span>  
> <span data-ttu-id="e1889-129">**Инструментирование выделения для снимка временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="e1889-129">**Allocation instrumentation on timeline** snapshot</span></span>  
> ![Инструментирование выделения для снимка временной шкалы][ImageCollected]  

<!--In [Figure 4](#figure-4), an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

<span data-ttu-id="e1889-131">Вы можете использовать ползунки на временной шкале выше, чтобы увеличить этот конкретный снимок и просмотреть объекты, которые были недавно выделены в данный момент.</span><span class="sxs-lookup"><span data-stu-id="e1889-131">You are able to use the sliders in the timeline above to zoom into that particular snapshot and see the objects that were recently allocated at that point:</span></span>  

> ##### <span data-ttu-id="e1889-132">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="e1889-132">Figure 4</span></span>  
> <span data-ttu-id="e1889-133">Изменение размера снимка</span><span class="sxs-lookup"><span data-stu-id="e1889-133">Zoom into snapshot</span></span>  
> ![Изменение размера снимка][ImageSliders]  

<span data-ttu-id="e1889-135">Если щелкнуть конкретный объект в куче, появится дерево сохранения в нижней части снимка кучи.</span><span class="sxs-lookup"><span data-stu-id="e1889-135">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="e1889-136">Проверка пути сохранения для объекта позволяет понять, почему объект не был собран, и необходимо внести необходимые изменения в код, чтобы удалить ненужную ссылку.</span><span class="sxs-lookup"><span data-stu-id="e1889-136">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <span data-ttu-id="e1889-137">Просмотр выделения памяти по функциям</span><span class="sxs-lookup"><span data-stu-id="e1889-137">View memory allocation by function</span></span>   

<span data-ttu-id="e1889-138">Вы можете просматривать выделение памяти функцией JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1889-138">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="e1889-139">Дополнительные сведения [можно найти в разделе изучение выделения памяти по функциям][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] .</span><span class="sxs-lookup"><span data-stu-id="e1889-139">See [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] for more information.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageObjectTracker]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png "Рисунок 1: инструментирование выделения на временной шкале"  
[ImageRecordHeap]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png "Рисунок 2: запись профилировщика выделения кучи"  
[ImageCollected]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timelines-snapshot.msft.png "Рисунок 3: инструментирование выделения для снимка временной шкалы"  
[ImageSliders]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png "Рисунок 4: изменение размера снимка"  

<!-- links -->  

[DevToolsOpenIndex]: /microsoft-edge/devtools-guide-chromium/open "Откройте Microsoft EDGE (Chromium) DevTools"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: /microsoft-edge/devtools-guide-chromium/memory-problems/index#investigate-memory-allocation-by-function "Исследование выделения памяти функцией — устранение проблем с памятью"  

<!--[HeapProfiler]: ../profile/memory-problems/heap-snapshots ""  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Скачайте канал Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="e1889-147">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e1889-147">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e1889-148">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) и была написана с помощью [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="e1889-148">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e1889-150">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e1889-150">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

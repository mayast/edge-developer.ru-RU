---
title: Запись моментальных снимков кучи
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 183482660ed5fc50862dfd2cce7209384fee93e3
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986173"
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
   limitations under the License.  -->

# <span data-ttu-id="bb4f0-103">Запись моментальных снимков кучи</span><span class="sxs-lookup"><span data-stu-id="bb4f0-103">How to record heap snapshots</span></span>  

<span data-ttu-id="bb4f0-104">Узнайте, как записывать моментальные снимки кучи с помощью профилировщика Microsoft Edge DevTools и поиска утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-104">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="bb4f0-105">Профилировщик кучи Microsoft Edge DevTools показывает распределение памяти по объектам JavaScript и связанным узлам DOM на странице.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-105">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="bb4f0-106">Используйте его для создания моментальных снимков JavaScript \ (JS-файлов, кучи и т. д.), анализа графов памяти, сравнения снимков и поиска утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-106">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="bb4f0-107">Смотрите также [объекты][DevtoolsMemoryProblems101ObjectsRetainingTree], которые хранятся в дереве.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-107">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="bb4f0-108">Создание снимка</span><span class="sxs-lookup"><span data-stu-id="bb4f0-108">Take a snapshot</span></span>  

<span data-ttu-id="bb4f0-109">На панели **память** выберите команду **сделать снимок**, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-109">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="bb4f0-110">Вы также можете нажать клавиши `Ctrl` + `E` \ (Windows \) или `Cmd` + `E` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="bb4f0-110">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="bb4f0-112">Выбор типа профилирования</span><span class="sxs-lookup"><span data-stu-id="bb4f0-112">Select profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="bb4f0-113">**Моментальные снимки** первоначально хранятся в памяти процесса обработчика.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-113">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="bb4f0-114">При необходимости снимки переносятся в DevTools по запросу, если щелкнуть значок снимка, чтобы просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-114">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="bb4f0-115">После того как вы загрузили моментальный снимок в DevTools и проанализируете его, появится число под заголовком снимка, в котором будет показан [Общий размер достижимых объектов JavaScript][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="bb4f0-115">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Общий размер достижимых объектов" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="bb4f0-117">Общий размер достижимых объектов</span><span class="sxs-lookup"><span data-stu-id="bb4f0-117">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="bb4f0-118">В снимки включаются только достижимые объекты.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-118">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="bb4f0-119">Кроме того, создание моментального снимка всегда начинается со сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-119">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="bb4f0-120">Очистка снимков</span><span class="sxs-lookup"><span data-stu-id="bb4f0-120">Clear snapshots</span></span>  

<span data-ttu-id="bb4f0-121">Нажмите кнопку **Очистить все профили** , чтобы удалить снимки \ (как из DevTools, так и из памяти, связанной с процессом рендеринга \).</span><span class="sxs-lookup"><span data-stu-id="bb4f0-121">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Удаление снимков" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="bb4f0-123">Удаление снимков</span><span class="sxs-lookup"><span data-stu-id="bb4f0-123">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="bb4f0-124">Закрытие окна DevTools не приводит к удалению профилей из памяти, связанной с процессом рендеринга.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-124">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="bb4f0-125">При повторном открытии DevTools все ранее созданные моментальные снимки снова появляются в списке снимков.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-125">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="bb4f0-126">Попробуйте этот пример [геоточечных объектов][GlitchDevtoolsMemoryExample03] и пропрофилировать его с помощью профилировщика кучи.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-126">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="bb4f0-127">Вы увидите число выделений элементов \ (объект \).</span><span class="sxs-lookup"><span data-stu-id="bb4f0-127">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="bb4f0-128">Просмотр снимков</span><span class="sxs-lookup"><span data-stu-id="bb4f0-128">View snapshots</span></span>  

<span data-ttu-id="bb4f0-129">Просмотр снимков с разных точек зрения для разных задач.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-129">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="bb4f0-130">В **представлении "Сводка** " отображаются объекты, сгруппированные по имени конструктора.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-130">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="bb4f0-131">Используйте его для поиска объектов \ (и использование памяти \) в зависимости от типа, сгруппированного по имени конструктора.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-131">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="bb4f0-132">Это особенно полезно для **отслеживания УТЕЧЕК DOM**.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-132">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="bb4f0-133">**Представление сравнения**.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-133">**Comparison view**.</span></span>  <span data-ttu-id="bb4f0-134">Показывает разницу между двумя снимками.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-134">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="bb4f0-135">Используйте его для сравнения двух (или более) моментальных снимков памяти от до и после выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-135">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="bb4f0-136">Проверка дельты в освобожденной памяти и счетчике ссылок позволяет вам подтвердить присутствие и причину утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-136">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="bb4f0-137">**Представление "вложение**".</span><span class="sxs-lookup"><span data-stu-id="bb4f0-137">**Containment view**.</span></span>  <span data-ttu-id="bb4f0-138">Позволяет исследовать содержимое кучи.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-138">Allows exploration of heap contents.</span></span>  <span data-ttu-id="bb4f0-139">**Представление "вложение** " обеспечивает более эффективное представление структуры объектов, помогая анализировать объекты, на которые ссылается глобальное пространство имен \ (окно \), чтобы узнать, что такое хранение объектов.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-139">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="bb4f0-140">Используйте его для анализа замыканий и пошагового углубления объектов на низком уровне.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-140">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="bb4f0-141">Для переключения между представлениями Используйте селектор в верхней части представления.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-141">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Переключатель выбора представлений" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="bb4f0-143">Переключатель выбора представлений</span><span class="sxs-lookup"><span data-stu-id="bb4f0-143">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="bb4f0-144">Не все свойства хранятся в куче JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-144">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="bb4f0-145">Свойства, реализованные с помощью методов доступа, которые выполняют машинный код, не фиксируются.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-145">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="bb4f0-146">Кроме того, не записываются значения, не являющиеся строками, например числа.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-146">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="bb4f0-147">Представление сводки</span><span class="sxs-lookup"><span data-stu-id="bb4f0-147">Summary view</span></span>  

<span data-ttu-id="bb4f0-148">Изначально в представлении сводки открывается моментальный снимок, в котором отображаются итоговые объекты, которые могут быть развернуты для отображения экземпляров.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-148">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Представление сводки" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="bb4f0-150">Представление **сводки**</span><span class="sxs-lookup"><span data-stu-id="bb4f0-150">**Summary** view</span></span>  
:::image-end:::  

<span data-ttu-id="bb4f0-151">Элементы верхнего уровня — строки "Итого".</span><span class="sxs-lookup"><span data-stu-id="bb4f0-151">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="bb4f0-152">Элементы верхнего уровня</span><span class="sxs-lookup"><span data-stu-id="bb4f0-152">Top-level entries</span></span> | <span data-ttu-id="bb4f0-153">Описание</span><span class="sxs-lookup"><span data-stu-id="bb4f0-153">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="bb4f0-154">Конструктор</span><span class="sxs-lookup"><span data-stu-id="bb4f0-154">Constructor</span></span>** | <span data-ttu-id="bb4f0-155">Представляет все объекты, созданные с помощью этого конструктора.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-155">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="bb4f0-156">Расстояние</span><span class="sxs-lookup"><span data-stu-id="bb4f0-156">Distance</span></span>** | <span data-ttu-id="bb4f0-157">показывает расстояние до корня с минимальным простым путем к узлам.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-157">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="bb4f0-158">Неглубокий размер</span><span class="sxs-lookup"><span data-stu-id="bb4f0-158">Shallow size</span></span>** | <span data-ttu-id="bb4f0-159">Отображает сумму мелких размеров всех объектов, созданных с помощью определенной функции конструктора.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-159">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="bb4f0-160">Неглубокий размер — это размер памяти, занимаемой объектом, (обычно массивы и строки имеют более мелких размеров).</span><span class="sxs-lookup"><span data-stu-id="bb4f0-160">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="bb4f0-161">Смотрите также [размеры объектов][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="bb4f0-161">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="bb4f0-162">Сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="bb4f0-162">Retained size</span></span>** | <span data-ttu-id="bb4f0-163">Отображение максимального размера в одном наборе объектов.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-163">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="bb4f0-164">Объем памяти, который вы можете освобождать после удаления объекта \ (а зависимые элементы становятся недостижимыми \), называется сохраненным размером.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-164">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="bb4f0-165">Смотрите также [размеры объектов][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="bb4f0-165">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="bb4f0-166">После того как вы разворачиваете итоговую строку в верхнем представлении, отобразятся все экземпляры.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-166">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="bb4f0-167">Для каждого экземпляра в соответствующих столбцах отображаются неполные и удержанные размеры.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-167">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="bb4f0-168">Число после `@` символа является уникальным идентификатором объекта, что позволяет сравнивать моментальные снимки кучи на отдельных объектах.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-168">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="bb4f0-169">Обратите внимание, что желтые объекты содержат ссылки на JavaScript, а красные объекты — это отсоединенные узлы, на которые ссылается один из них с желтым фоном.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-169">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="bb4f0-170">Что в профилировщике кучи соотносятся различные элементы конструктора \ (Group \)?</span><span class="sxs-lookup"><span data-stu-id="bb4f0-170">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Группы конструкторов" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="bb4f0-172">Группы **конструкторов**</span><span class="sxs-lookup"><span data-stu-id="bb4f0-172">**Constructor** groups</span></span>  
:::image-end:::  

| <span data-ttu-id="bb4f0-173">Элемент Конструктор \ (группировка)</span><span class="sxs-lookup"><span data-stu-id="bb4f0-173">Constructor \(group\) entry</span></span> | <span data-ttu-id="bb4f0-174">Описание</span><span class="sxs-lookup"><span data-stu-id="bb4f0-174">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="bb4f0-175">\ (глобальное свойство)</span><span class="sxs-lookup"><span data-stu-id="bb4f0-175">\(global property\)</span></span>** | <span data-ttu-id="bb4f0-176">Промежуточные объекты между глобальным объектом (например, `window` \) и объектом, на который ссылается этот объект.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-176">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="bb4f0-177">Если объект создается с помощью конструктора `Person` и удерживается глобальным объектом, путь сохранения будет выглядеть так, как нужно `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="bb4f0-177">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="bb4f0-178">Это отличается от нормы, где объекты непосредственно ссылаются друг на друга.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-178">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="bb4f0-179">Промежуточные объекты существуют для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-179">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="bb4f0-180">Глобальные объекты регулярно изменяются, а оптимизации доступа к свойствам являются хорошим заданием для неглобальных объектов, неприменимо для глобальных.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-180">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="bb4f0-181">\ (корни \)</span><span class="sxs-lookup"><span data-stu-id="bb4f0-181">\(roots\)</span></span>** | <span data-ttu-id="bb4f0-182">Корневые элементы в представлении в виде дерева сохраняются как сущности, которые содержат ссылки на выбранный объект.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-182">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="bb4f0-183">Записи могут также содержать ссылки, созданные ядром для целей, специфических для ядра.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-183">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="bb4f0-184">Ядро содержит кэш, в котором есть ссылки на объекты, но все такие ссылки являются слабыми и не запрещают сбору объекта с учетом того, что нет действительно строгой ссылки.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-184">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="bb4f0-185">\ (замыкание)</span><span class="sxs-lookup"><span data-stu-id="bb4f0-185">\(closure\)</span></span>** | <span data-ttu-id="bb4f0-186">Количество ссылок на группу объектов с помощью замыкания функций.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-186">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="bb4f0-187">\ (массив, строка, число, regexp)</span><span class="sxs-lookup"><span data-stu-id="bb4f0-187">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="bb4f0-188">Список типов объектов со свойствами, которые ссылаются на массив, строку, число или регулярное выражение.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-188">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="bb4f0-189">\ (скомпилированный код)</span><span class="sxs-lookup"><span data-stu-id="bb4f0-189">\(compiled code\)</span></span>** | <span data-ttu-id="bb4f0-190">Все, что связано с компилированным кодом.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-190">Everything related to compiled code.</span></span>  <span data-ttu-id="bb4f0-191">Сценарий похож на функцию, но соответствует `<script>` телу.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-191">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="bb4f0-192">SharedFunctionInfos \ (SFI \) — объекты, зафиксированные между функциями и скомпилированным кодом.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-192">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="bb4f0-193">У функций обычно есть контекст, а не SFIs.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-193">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="bb4f0-194">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**и т. д.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-194">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="bb4f0-195">Ссылки на элементы или объекты документа определенного типа, на которые ссылается ваш код.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-195">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="bb4f0-196">Представление "Сравнение"</span><span class="sxs-lookup"><span data-stu-id="bb4f0-196">Comparison view</span></span>  

<span data-ttu-id="bb4f0-197">Находить потерянные объекты, сравнивая несколько моментальных снимков друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-197">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="bb4f0-198">Чтобы убедиться в том, что определенная операция приложения не создает утечки \ (например, при открытии документа, а затем его закрытии), не следует оставлять все сборки мусора, вы можете воспользоваться приведенным ниже сценарием.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-198">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="bb4f0-199">Сделайте снимок кучи, прежде чем выполнять операцию.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-199">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="bb4f0-200">Выполнение операции \ (взаимодействие с страницей в некоторых условиях, когда вы считаете, что она вызывает утечку).</span><span class="sxs-lookup"><span data-stu-id="bb4f0-200">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="bb4f0-201">Выполните обратную операцию, чтобы (выполнить обратное взаимодействие и повторить ее несколько раз).</span><span class="sxs-lookup"><span data-stu-id="bb4f0-201">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="bb4f0-202">Сделайте второй снимок кучи и измените его представление на **Сравнение**, сравнив его с **снимком 1**.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-202">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="bb4f0-203">В представлении **Сравнение** отображается разница между двумя снимками.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-203">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="bb4f0-204">При развертывании элемента общего типа отображаются добавленные и удаленные экземпляры объекта.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-204">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Представление "Сравнение"" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="bb4f0-206">Представление " **Сравнение** "</span><span class="sxs-lookup"><span data-stu-id="bb4f0-206">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="bb4f0-207">Представление "вложение"</span><span class="sxs-lookup"><span data-stu-id="bb4f0-207">Containment view</span></span>  

<span data-ttu-id="bb4f0-208">Представление " **вложение** " — это по сути представление "глаз с высоты птичьего полета" для структуры объектов приложения.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-208">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="bb4f0-209">Это позволяет просматривать замыкания функций внутри функции, чтобы отслеживать внутренние объекты виртуальной машины \ (VM \), которые вместе составляют объекты JavaScript, и понять, какая память используется приложением на очень низком уровне.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-209">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="bb4f0-210">Точки входа в Просмотр вложений</span><span class="sxs-lookup"><span data-stu-id="bb4f0-210">Containment view entry points</span></span> | <span data-ttu-id="bb4f0-211">Описание</span><span class="sxs-lookup"><span data-stu-id="bb4f0-211">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="bb4f0-212">Объекты DOMWindow</span><span class="sxs-lookup"><span data-stu-id="bb4f0-212">DOMWindow objects</span></span>** | <span data-ttu-id="bb4f0-213">Глобальные объекты для кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-213">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="bb4f0-214">Корни GC</span><span class="sxs-lookup"><span data-stu-id="bb4f0-214">GC roots</span></span>** | <span data-ttu-id="bb4f0-215">Фактические корни GC, используемые сборкой мусора ВМ.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-215">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="bb4f0-216">Корни GC состоят из встроенных карт объектов, таблиц символов, стеков потоков виртуальной машины, кэшей компиляций, областей обработки и глобальных дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-216">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="bb4f0-217">Собственные объекты</span><span class="sxs-lookup"><span data-stu-id="bb4f0-217">Native objects</span></span>** | <span data-ttu-id="bb4f0-218">Объекты браузера "отправили" на виртуальной машине JavaScript \ (JavaScript VM \), чтобы разрешить автоматизацию, например узлы DOM, правила CSS.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-218">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Представление "вложение"" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="bb4f0-220">Представление " **вложение** "</span><span class="sxs-lookup"><span data-stu-id="bb4f0-220">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="bb4f0-221">Всплывающая подсказка о замыканиях.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-221">A tip about closures.</span></span>  <span data-ttu-id="bb4f0-222">Назовите функции таким образом, чтобы можно было легко отличать между собой замыкания в снимке.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-222">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="bb4f0-223">Например, в этом примере не используются именованные функции.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-223">For example, this example does not use named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <span data-ttu-id="bb4f0-224">Во фрагменте followingcode используются именованные функции.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-224">The followingcode snippet uses named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="bb4f0-225">Попробуйте этот пример, чтобы [можно `eval` было][GlitchDevtoolsMemoryExample07] проанализировать влияние замыканий на память.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-225">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="bb4f0-226">Кроме того, вам может потребоваться подписаться на этот пример, в котором осуществляется запись [ресурсов кучи][GlitchDevtoolsMemoryExample08].</span><span class="sxs-lookup"><span data-stu-id="bb4f0-226">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="bb4f0-227">Поиск цветового кодирования</span><span class="sxs-lookup"><span data-stu-id="bb4f0-227">Look up color coding</span></span>  

<span data-ttu-id="bb4f0-228">Свойства и значения свойств объектов имеют различные типы и окрашены соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-228">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="bb4f0-229">Каждое свойство имеет один из четырех типов.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-229">Each property has one of four types.</span></span>  

| <span data-ttu-id="bb4f0-230">Тип свойства</span><span class="sxs-lookup"><span data-stu-id="bb4f0-230">Property Type</span></span> | <span data-ttu-id="bb4f0-231">Описание</span><span class="sxs-lookup"><span data-stu-id="bb4f0-231">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="bb4f0-232">a: свойство</span><span class="sxs-lookup"><span data-stu-id="bb4f0-232">a: property</span></span>** | <span data-ttu-id="bb4f0-233">Обычное свойство с именем, доступ к которому осуществляется с помощью `.` оператора \ (точка) или через `[` `]` \ (квадратные скобки \), например `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="bb4f0-233">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="bb4f0-234">0: элемент</span><span class="sxs-lookup"><span data-stu-id="bb4f0-234">0: element</span></span>** | <span data-ttu-id="bb4f0-235">Регулярное свойство с числовым индексом, доступ к которому осуществляется через `[` `]` представление \ (скобки).</span><span class="sxs-lookup"><span data-stu-id="bb4f0-235">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="bb4f0-236">a: VAR (контекст)</span><span class="sxs-lookup"><span data-stu-id="bb4f0-236">a: context var</span></span>** |  <span data-ttu-id="bb4f0-237">Переменная в контексте функции, доступная по имени переменной из замыкания функции.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-237">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="bb4f0-238">a: System Prop</span><span class="sxs-lookup"><span data-stu-id="bb4f0-238">a: system prop</span></span>** | <span data-ttu-id="bb4f0-239">Свойство, добавленное виртуальной машиной JavaScript, недоступно из кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-239">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="bb4f0-240">Объекты, помеченные как не `System` имеющие соответствующего типа JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-240">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="bb4f0-241">Каждый из них является частью реализации объектной системы виртуальной машины JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-241">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="bb4f0-242">V8 выделяет большинство внутренних объектов в той же куче, где находятся объекты JS пользователя.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-242">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="bb4f0-243">Итак, это только внутренние V8.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-243">So these are just V8 internals.</span></span>  

## <span data-ttu-id="bb4f0-244">Поиск конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="bb4f0-244">Find a specific object</span></span>  

<span data-ttu-id="bb4f0-245">Чтобы найти объект в собранной куче, вы можете найти его с помощью `Ctrl` + `F` и присвоить ему идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-245">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="bb4f0-246">Обнаружение утечек DOM</span><span class="sxs-lookup"><span data-stu-id="bb4f0-246">Uncover DOM leaks</span></span>  

<span data-ttu-id="bb4f0-247">Профилировщик кучи может отображать двунаправленные зависимости между собственными объектами браузера \ (узлы DOM, правила CSS \) и объекты JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-247">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="bb4f0-248">Это помогает выявить невидимые утечки, происходящие из-за плавающего отсоединенного поддерева DOM.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-248">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="bb4f0-249">Утечки DOM могут быть больше, чем вы думаете.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-249">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="bb4f0-250">Вот пример.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-250">Consider the following sample.</span></span>  <span data-ttu-id="bb4f0-251">Когда #tree GC?</span><span class="sxs-lookup"><span data-stu-id="bb4f0-251">When is the #tree GC?</span></span>  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

<span data-ttu-id="bb4f0-252">Функция `#leaf` хранит ссылку на подходящую родительскую структуру \ (ParentNode \) и рекурсивно `#tree` дополнить, так что только в том случае, если leafRef является nullified — это всего лишь дерево с `#tree` кандидатом на сборку мусора.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-252">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Поддерево DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="bb4f0-254">Поддерево DOM</span><span class="sxs-lookup"><span data-stu-id="bb4f0-254">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="bb4f0-255">Примеры: попробуйте этот пример [утечки узла DOM][GlitchDevtoolsMemoryExample06] , чтобы понять, где она может быть потеряна и как ее найти.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-255">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="bb4f0-256">Кроме того, вы можете просмотреть этот пример [утечек DOM больше, чем ожидалось][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="bb4f0-256">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="bb4f0-257">Для получения дополнительных сведений о утечках DOM и анализе памяти ознакомьтесь с разделом извлечение [и отладка утечек памяти с помощью Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] , Gonzalo Ruiz De Villa.</span><span class="sxs-lookup"><span data-stu-id="bb4f0-257">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <span data-ttu-id="bb4f0-258">Знакомство с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bb4f0-258">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Размеры объектов — терминология с памятью | Документы Microsoft"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Объекты, в которых хранятся терминология в дереве-память | Документы Microsoft"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html-Microsoft EDGE (Chromium) DevTools | Цепь"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "память | Закончен"  

> [!NOTE]
> <span data-ttu-id="bb4f0-268">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bb4f0-268">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bb4f0-269">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) и была написана с помощью [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="bb4f0-269">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bb4f0-271">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bb4f0-271">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

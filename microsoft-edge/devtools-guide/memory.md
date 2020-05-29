---
description: Использование панели «память» для
title: DevTools-Memory
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, память, куча, GC, сборка мусора, сохраненный размер, лидерские стороны
ms.custom: seodec18
ms.openlocfilehash: 416ba144f7e22bd50f5d2a3437bc21d9d31a9035
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571744"
---
# <span data-ttu-id="c0baa-104">Память</span><span class="sxs-lookup"><span data-stu-id="c0baa-104">Memory</span></span>

<span data-ttu-id="c0baa-105">С помощью панели **памяти** можно измерять использование системных ресурсов и сравнивать моментальные снимки кучи в разных состояниях выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="c0baa-105">Use the **Memory** panel to measure your use of system resources and compare heap snapshots at different states of code execution.</span></span> <span data-ttu-id="c0baa-106">С его помощью вы можете:</span><span class="sxs-lookup"><span data-stu-id="c0baa-106">With it, you can:</span></span>

- <span data-ttu-id="c0baa-107">[Диаграмма потребления памяти страницы в режиме реального времени](#memory-usage-timeline) и создание снимков кучи</span><span class="sxs-lookup"><span data-stu-id="c0baa-107">[Graph the memory consumption of your page in real time](#memory-usage-timeline) and take snapshots of the heap</span></span>
- <span data-ttu-id="c0baa-108">[Определение потенциальных проблем с памятью](#snapshot-summary) в коде, например удержанных объектов, не вложенных в DOM</span><span class="sxs-lookup"><span data-stu-id="c0baa-108">[Identify potential memory issues](#snapshot-summary) in your code, such as retained objects not attached to the DOM</span></span>
- <span data-ttu-id="c0baa-109">[Просмотр данных об использовании памяти](#snapshot-details) с помощью типа объекта, количества экземпляров, размера и ссылок, помогающих изолировать проблемы</span><span class="sxs-lookup"><span data-stu-id="c0baa-109">[Review memory usage data](#snapshot-details) by object type, instance count, size, and references to help isolate issues</span></span>
- <span data-ttu-id="c0baa-110">[Примените фильтры данных моментальных снимков](#filters) , чтобы уменьшить шум данных, не связанных с действиями</span><span class="sxs-lookup"><span data-stu-id="c0baa-110">[Apply snapshot data filters](#filters) to reduce the noise of non-actionable information</span></span>
- <span data-ttu-id="c0baa-111">[Определение объема памяти для определенного объекта](#object-references) и ссылок для его поддержания активности</span><span class="sxs-lookup"><span data-stu-id="c0baa-111">[Identify the memory cost of a specific object](#object-references) and the references keeping it alive</span></span>
- <span data-ttu-id="c0baa-112">[Сравнение кучи на разных этапах исследования](#snapshot-comparison) для отслеживания источника утечек памяти и других проблем</span><span class="sxs-lookup"><span data-stu-id="c0baa-112">[Diff the heap at different phases of your investigation](#snapshot-comparison) to track down the source of memory leaks and other problems</span></span>

![Панель DevTools памятью Microsoft Edge](./media/memory.png)


## <span data-ttu-id="c0baa-114">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="c0baa-114">Toolbar</span></span>

1. <span data-ttu-id="c0baa-115">**Запуск и остановка сеанса профилирования (Ctrl + E)**: Включение профилировщика позволяет отслеживать использование памяти и создавать снимки кучи.</span><span class="sxs-lookup"><span data-stu-id="c0baa-115">**Start/Stop profiling session (Ctrl+E)**: Turning on the profiler enables you to track memory usage and take snapshots of the heap.</span></span>
2. <span data-ttu-id="c0baa-116">**Импорт сеанса профилирования (Ctrl + O)**: Загрузка сохраненного сеанса диагностики памяти DevTools.</span><span class="sxs-lookup"><span data-stu-id="c0baa-116">**Import profiling session (Ctrl+O)**: Load a saved  DevTools memory diagnostic session.</span></span>
3. <span data-ttu-id="c0baa-117">**Экспорт сеанса профилирования (Ctrl + S)**: сохранение текущего диагностического сеанса на диске.</span><span class="sxs-lookup"><span data-stu-id="c0baa-117">**Export profiling session (Ctrl+S)**: Save the current diagnostic session to disk.</span></span>
4. <span data-ttu-id="c0baa-118">**Создание снимка кучи (Ctrl + Shift + T)**: запись текущих выделений памяти на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="c0baa-118">**Take heap snapshot (Ctrl+Shift+T)**: Record current memory allocations for a given point of time.</span></span>


## <span data-ttu-id="c0baa-119">Временная шкала использования памяти</span><span class="sxs-lookup"><span data-stu-id="c0baa-119">Memory usage timeline</span></span>

<span data-ttu-id="c0baa-120">Проблемы с памятью могут быть серьезным препятствием проблем с производительностью, что приводит к тому, что ваша страница становится все более недоступной и laggy с течением времени.</span><span class="sxs-lookup"><span data-stu-id="c0baa-120">Memory problems can be a major culprit of performance issues, causing your page to become increasingly unresponsive and laggy over time.</span></span>

<span data-ttu-id="c0baa-121">Первым шагом для анализа использования памяти на странице является [Запуск сеанса профилирования](#toolbar) для получения моментальных снимков до и после того, как вы воспроизведите этапы, вызывающие чрезмерное использование памяти или вероятную утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="c0baa-121">The first step to analyzing the memory usage of your page is to [start a profiling session](#toolbar) in order to take before/after snapshots of the heap as you repro the steps causing memory bloat or a suspected memory leak.</span></span>

<span data-ttu-id="c0baa-122">При запуске профилировщика памяти появится график обработки памяти, который позволяет наблюдать за общим частным рабочее набором (объем памяти, потребляемый страницей) с течением времени.</span><span class="sxs-lookup"><span data-stu-id="c0baa-122">When you start the memory profiler, you will see a process memory graph that allows you to observe the overall private working set (the amount of memory consumed by the page) over time.</span></span> <span data-ttu-id="c0baa-123">Граф памяти показывает, как можно просматривать память процесса вкладки, включая закрытые байты, машинную память и кучу JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0baa-123">The memory graph shows you a live view of the tab's process memory, which includes private bytes, native memory, and the JavaScript heap.</span></span> 

![Временная шкала использования памяти](./media/memory_timeline.png)

 <span data-ttu-id="c0baa-125">Диаграмма дает указание о тенденциях памяти для страницы, которая позволяет оценить, когда нужно [получить моментальный снимок кучи](#toolbar) для более позднего сравнения, например, если вы видите точки непредвиденного хранения памяти.</span><span class="sxs-lookup"><span data-stu-id="c0baa-125">The graph gives you an indication of the memory trend for the page which enables you to judge when it is appropriate to [take a heap snapshot](#toolbar) for later comparison, such as when you see periods of unexpected memory retention.</span></span>

### <span data-ttu-id="c0baa-126">Performance. Марка ()</span><span class="sxs-lookup"><span data-stu-id="c0baa-126">Performance.mark()</span></span>

<span data-ttu-id="c0baa-127">Вы можете добавить пользовательские **метки** на временную шкалу, чтобы определить события клавиш во время сеанса анализа, вызвав [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) метод из вашего кода или [**консоли**](./console.md)DevTools.</span><span class="sxs-lookup"><span data-stu-id="c0baa-127">You can add custom **User marks** to the timeline to help identify  key events during the course of your analysis session by calling the [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) method from within your code or the  DevTools [**Console**](./console.md).</span></span>

### <span data-ttu-id="c0baa-128">Console. takeheapSnapshot ()</span><span class="sxs-lookup"><span data-stu-id="c0baa-128">Console.takeheapSnapshot()</span></span>

<span data-ttu-id="c0baa-129">Иногда необходимо создавать снимки на очень конкретных моментах времени, например непосредственно перед большим изменением DOM.</span><span class="sxs-lookup"><span data-stu-id="c0baa-129">Sometimes you need to take snapshots at very specific points in time, such as immediately before a large mutation of the DOM.</span></span> <span data-ttu-id="c0baa-130">В этих случаях вы можете создавать моментальные снимки программными средствами с помощью [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) .</span><span class="sxs-lookup"><span data-stu-id="c0baa-130">In these cases,you can take snapshots programmatically with [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots).</span></span>

## <span data-ttu-id="c0baa-131">Сводка по снимкам</span><span class="sxs-lookup"><span data-stu-id="c0baa-131">Snapshot summary</span></span>

<span data-ttu-id="c0baa-132">Создание [снимка](#toolbar) формирует сводную плитку, указывающую размер кучи JavaScript на момент создания снимка, а также количество выделенных объектов и снимок экрана страницы.</span><span class="sxs-lookup"><span data-stu-id="c0baa-132">[Taking a snapshot](#toolbar) will generate a summary tile that indicates the size of the JavaScript heap at the time the snapshot was taken, along with the number of objects allocated and a screenshot of the page.</span></span> <span data-ttu-id="c0baa-133">Вы можете продолжать делать снимки в любое время, когда вы просматриваете сценарий пользователя, которому требуется выполнить анализ.</span><span class="sxs-lookup"><span data-stu-id="c0baa-133">You can continue to take snapshots at any time as you run through the user scenario requiring analysis.</span></span> <span data-ttu-id="c0baa-134">Снимки создают дополнительные плитки, каждая из которых указывает на разницу в памяти JavaScript из предыдущего снимка.</span><span class="sxs-lookup"><span data-stu-id="c0baa-134">The snapshots generate additional tiles, each of which indicates the difference in JavaScript memory from the previous snapshot.</span></span>

![Снимок кучи](./media/memory_snapshot.png)

<span data-ttu-id="c0baa-136">При щелчке значений в плитке "Сводка" будет переключена на область, отображающая [сведения о данных моментальных снимков](#snapshot-details).</span><span class="sxs-lookup"><span data-stu-id="c0baa-136">Clicking on the values in the summary tile will switch to the pane showing [details of the snapshot data](#snapshot-details).</span></span> <span data-ttu-id="c0baa-137">Потенциальные [проблемы с памятью обозначены](#snapshot-details) синим значком информационного ("i").</span><span class="sxs-lookup"><span data-stu-id="c0baa-137">Potential [memory issues are indicated](#snapshot-details) with a blue informational ("i") icon.</span></span>

## <span data-ttu-id="c0baa-138">Сведения о снимке</span><span class="sxs-lookup"><span data-stu-id="c0baa-138">Snapshot details</span></span>

<span data-ttu-id="c0baa-139">В области " *снимок* " отображаются объекты, созданные на странице, а также все ресурсы, выделенные платформой JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0baa-139">The data in the *Snapshot* pane shows the objects created by your page along with any memory allocated by JavaScript frameworks you may be consuming.</span></span>

![Таблица сведений о снимке](./media/memory_details.png)

<span data-ttu-id="c0baa-141">Три вкладки представляют различные представления данных:</span><span class="sxs-lookup"><span data-stu-id="c0baa-141">The three tabs represent different views of the data:</span></span>

#### <span data-ttu-id="c0baa-142">Типы</span><span class="sxs-lookup"><span data-stu-id="c0baa-142">Types</span></span>

<span data-ttu-id="c0baa-143">Показывает количество экземпляров и общий размер объектов в куче, сгруппированных по типам объектов.</span><span class="sxs-lookup"><span data-stu-id="c0baa-143">Shows the instance count and total size of objects on the heap, grouped by object type.</span></span> <span data-ttu-id="c0baa-144">По умолчанию они сортируются по количеству экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c0baa-144">By default, these are sorted by instance count.</span></span>

<span data-ttu-id="c0baa-145">Когда вы выберете объект в области " *типы* верхнего уровня", в нижней области в таблице " [ссылки на объекты](#object-references) " будет перечислены все объекты, которые указывают на этот объект.</span><span class="sxs-lookup"><span data-stu-id="c0baa-145">When you select an object in the upper *Types* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

#### <span data-ttu-id="c0baa-146">Корней</span><span class="sxs-lookup"><span data-stu-id="c0baa-146">Roots</span></span>

<span data-ttu-id="c0baa-147">Показывает иерархическое представление дочерних ссылок для описания того, как объекты находятся в корне глобального объекта, предотвращая их сбор сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="c0baa-147">Shows a hierarchical view of child references to describe how objects are rooted to the global object, thus preventing them from being garbage-collected.</span></span>

<span data-ttu-id="c0baa-148">По умолчанию дочерние узлы сортируются по столбцу сохраненного размера с наибольшим вверху.</span><span class="sxs-lookup"><span data-stu-id="c0baa-148">By default, the child nodes are sorted by the retained size column, with the largest at the top.</span></span>

#### <span data-ttu-id="c0baa-149">Лидеры</span><span class="sxs-lookup"><span data-stu-id="c0baa-149">Dominators</span></span>

<span data-ttu-id="c0baa-150">Показывает список объектов в куче, которые содержат исключительные ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="c0baa-150">Shows a list of objects on the heap that have exclusive references to other objects.</span></span> <span data-ttu-id="c0baa-151">Лидеры сортируются по сохраненному размеру, чтобы обозначить объекты, потребляющие наибольшее объем памяти, который может проще освобождать.</span><span class="sxs-lookup"><span data-stu-id="c0baa-151">Dominators are sorted by retained size to indicate the objects consuming the most memory that are potentially easiest to free.</span></span>

<span data-ttu-id="c0baa-152">Ниже показано, как интерпретировать столбцы в представлениях *типы, корни* и *лидерства* .</span><span class="sxs-lookup"><span data-stu-id="c0baa-152">Here's how to interpret the columns in the *Types, Roots* and *Dominators* views:</span></span>

<span data-ttu-id="c0baa-153">Столбец</span><span class="sxs-lookup"><span data-stu-id="c0baa-153">Column</span></span> | <span data-ttu-id="c0baa-154">Описание</span><span class="sxs-lookup"><span data-stu-id="c0baa-154">Description</span></span>
:------------ | :-------------
<span data-ttu-id="c0baa-155">Идентификатор (-ы)</span><span class="sxs-lookup"><span data-stu-id="c0baa-155">Identifier(s)</span></span> | <span data-ttu-id="c0baa-156">Имя, которое лучше определяет объект.</span><span class="sxs-lookup"><span data-stu-id="c0baa-156">Name that best identifies the object.</span></span> <span data-ttu-id="c0baa-157">Например, для HTML-элементов в сведениях о снимке отображается значение атрибута ID, если оно используется.</span><span class="sxs-lookup"><span data-stu-id="c0baa-157">For example, for HTML elements the snapshot details show the ID attribute value, if one is used.</span></span>
<span data-ttu-id="c0baa-158">Тип</span><span class="sxs-lookup"><span data-stu-id="c0baa-158">Type</span></span> | <span data-ttu-id="c0baa-159">Тип объекта (например, *HTMLDivElement*).</span><span class="sxs-lookup"><span data-stu-id="c0baa-159">Object type (for example, *HTMLDivElement*).</span></span>
<span data-ttu-id="c0baa-160">Size</span><span class="sxs-lookup"><span data-stu-id="c0baa-160">Size</span></span> | <span data-ttu-id="c0baa-161">Размер объекта, не включая размер объектов, на которые указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="c0baa-161">Object size, not including the size of any referenced objects.</span></span>
<span data-ttu-id="c0baa-162">Сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="c0baa-162">Retained size</span></span> | <span data-ttu-id="c0baa-163">Размер объекта и размер всех дочерних объектов, у которых нет других родителей.</span><span class="sxs-lookup"><span data-stu-id="c0baa-163">Object size plus the size of all child objects that have no other parents.</span></span> <span data-ttu-id="c0baa-164">Для практических целей это объем памяти, сохраненной объектом, поэтому при удалении объекта, для которого заданный объем памяти освобождается.</span><span class="sxs-lookup"><span data-stu-id="c0baa-164">For practical purposes, this is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>
<span data-ttu-id="c0baa-165">Количество</span><span class="sxs-lookup"><span data-stu-id="c0baa-165">Count</span></span> | <span data-ttu-id="c0baa-166">Количество экземпляров объекта.</span><span class="sxs-lookup"><span data-stu-id="c0baa-166">Number of object instances.</span></span> <span data-ttu-id="c0baa-167">Это значение отображается только в представлении типы.</span><span class="sxs-lookup"><span data-stu-id="c0baa-167">This value appears only in the Types view.</span></span>

<span data-ttu-id="c0baa-168">Когда вы выбираете объект *в верхней области* задач, таблица [ссылки на объекты](#object-references) в нижней области списка будет выделять все объекты, которые указывают на этот объект.</span><span class="sxs-lookup"><span data-stu-id="c0baa-168">When you select an object in the upper *Dominators* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

### <span data-ttu-id="c0baa-169">Фильтру</span><span class="sxs-lookup"><span data-stu-id="c0baa-169">Filters</span></span>

<span data-ttu-id="c0baa-170">Для дальнейшей настройки данных в таблице можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c0baa-170">You can further adjust data in the table with the following:</span></span>

![Фильтрация для встроенных и идентификаторов объектов](./media/memory_filter.png)

1. <span data-ttu-id="c0baa-172">**Фильтр идентификатора**: Фильтрация данных с помощью поиска определенного идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="c0baa-172">**Identifier filter**: Filter out data by searching for a particular object identifier</span></span>
2. <span data-ttu-id="c0baa-173">**Группировка по лидеру**: только объекты с *монопольными* ссылками на другие объекты отображаются в представлении верхнего уровня объектов (это представление по умолчанию на вкладке " *лидеры* ").</span><span class="sxs-lookup"><span data-stu-id="c0baa-173">**Group by dominator**: Only objects with *exclusive* references to other objects are shown in the top-level view of objects (this is the default view in the *Dominators* tab).</span></span>
3. <span data-ttu-id="c0baa-174">**Фильтр встроенных или идентификаторов**: по умолчанию [встроенные объекты JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) включены в список.</span><span class="sxs-lookup"><span data-stu-id="c0baa-174">**Built-ins / IDs filter**: By default, [JavaScript built-in objects](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) are included in the list.</span></span> <span data-ttu-id="c0baa-175">Список идентификаторов объектов может быть полезен, если существует несколько анонимных объектов, которые должны быть различны.</span><span class="sxs-lookup"><span data-stu-id="c0baa-175">Listing object IDs can be useful if there are multiple anonymous objects which need to be differentiated.</span></span>

<span data-ttu-id="c0baa-176">Каждый из представлений " *типы", "корни* " и " *лидеры* " имеет собственный фильтр, поэтому фильтр не сохраняется при переходе к другому представлению.</span><span class="sxs-lookup"><span data-stu-id="c0baa-176">The *Types, Roots* and *Dominators* views each has its own filter, so the filter isn't preserved when you switch to another view.</span></span>

### <span data-ttu-id="c0baa-177">Ссылки на объекты</span><span class="sxs-lookup"><span data-stu-id="c0baa-177">Object references</span></span>

<span data-ttu-id="c0baa-178">В представлении " [**типы**](#types) и [**лидеры**](#dominators) " в этой области содержится список **ссылок на объекты** , отображающий общие ссылки.</span><span class="sxs-lookup"><span data-stu-id="c0baa-178">In the [**Types**](#types) and [**Dominators**](#dominators) views, the lower pane contains an **Object references** list that displays shared references.</span></span> <span data-ttu-id="c0baa-179">Когда вы выбираете объект в верхней области, в этом списке отображаются все объекты, указывающие на этот объект, иными словами, объекты, которые не поддерживают выбранный объект.</span><span class="sxs-lookup"><span data-stu-id="c0baa-179">When you choose an object in the upper pane, this list displays all objects that point to that object--in other words, the objects that are keeping the selected object alive.</span></span>

<span data-ttu-id="c0baa-180">Циклические ссылки отображаются с помощью звездочки (\*) и информационных подсказок, и их невозможно развернуть.</span><span class="sxs-lookup"><span data-stu-id="c0baa-180">Circular references are shown with an asterisk (\*) and informational tooltip, and cannot be expanded.</span></span> <span data-ttu-id="c0baa-181">В противном случае они не позволят вам проанализировать дерево ссылок и идентифицировать объекты, которые сохраняют память.</span><span class="sxs-lookup"><span data-stu-id="c0baa-181">Otherwise, they would prevent you from walking up the reference tree and identifying objects that are retaining memory.</span></span>

<span data-ttu-id="c0baa-182">Чтобы быстро идентифицировать эквивалентные объекты, установите флажок фильтр [*идентификаторов объектов отображения*](#filters) , чтобы отобразить идентификаторы объектов рядом с именами объектов в столбце *идентификаторов* .</span><span class="sxs-lookup"><span data-stu-id="c0baa-182">To quickly identify equivalent objects, tick the [*Display object IDs*](#filters) filter option to display object IDs next to object names in the *Identifier(s)* column.</span></span> <span data-ttu-id="c0baa-183">Объекты с одинаковыми ИДЕНТИФИКАТОРами — это общие ссылки.</span><span class="sxs-lookup"><span data-stu-id="c0baa-183">Objects that have the same ID are shared references.</span></span>

### <span data-ttu-id="c0baa-184">Сравнение снимков</span><span class="sxs-lookup"><span data-stu-id="c0baa-184">Snapshot comparison</span></span>

<span data-ttu-id="c0baa-185">При нажатии на [вкладку "Сравнение снимков"](#snapshot-details) или ссылку "Сравнение" на [плитке сводки снимков](#snapshot-summary) будут показаны сведения о двух снимках.</span><span class="sxs-lookup"><span data-stu-id="c0baa-185">Clicking on a [snapshot comparison tab](#snapshot-details) or comparison link on the [snapshot summary tile](#snapshot-summary)  will show a diff of information between the two snapshots.</span></span> <span data-ttu-id="c0baa-186">На панели сравнения *лидеры, типы* и *корневые* представления предоставляют те же [*сведения о снимке*](#snapshot-details) , которые вы видите для одного снимка, и эти дополнительные значения:</span><span class="sxs-lookup"><span data-stu-id="c0baa-186">In the comparison pane, the *Dominators, Types* and *Roots* views provide the same [*snapshot details*](#snapshot-details) you would see for a single snapshots, with these additional values:</span></span>

<span data-ttu-id="c0baa-187">Столбец</span><span class="sxs-lookup"><span data-stu-id="c0baa-187">Column</span></span> | <span data-ttu-id="c0baa-188">Описание</span><span class="sxs-lookup"><span data-stu-id="c0baa-188">Description</span></span>
:------------ | :-------------
<span data-ttu-id="c0baa-189">Формат различий.</span><span class="sxs-lookup"><span data-stu-id="c0baa-189">Size diff.</span></span> | <span data-ttu-id="c0baa-190">Разница между размером объекта в текущем снимке и его размером в предыдущем снимке, не включая размер объектов, на которые указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="c0baa-190">Difference between the size of the object in the current snapshot and its size in the previous snapshot, not including the size of any referenced objects.</span></span>
<span data-ttu-id="c0baa-191">Сохраненный размер различий.</span><span class="sxs-lookup"><span data-stu-id="c0baa-191">Retained size diff.</span></span> | <span data-ttu-id="c0baa-192">Разница между сохраненным размером объекта в текущем снимке и его сохраненным размером в предыдущем снимке.</span><span class="sxs-lookup"><span data-stu-id="c0baa-192">Difference between the retained size of the object in the current snapshot and its retained size in the previous snapshot.</span></span> <span data-ttu-id="c0baa-193">Сохраненный размер включает в себя размер объекта и его дочерние объекты, у которых нет других родителей.</span><span class="sxs-lookup"><span data-stu-id="c0baa-193">The retained size includes the object size plus the size of all its child objects that have no other parents.</span></span> <span data-ttu-id="c0baa-194">Для практических целей сохраненный размер — это объем памяти, сохраненной объектом, поэтому если вы удалите объект, который освободит заданный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="c0baa-194">For practical purposes, the retained size is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>

<span data-ttu-id="c0baa-195">С помощью раскрывающегося списка **область** можно отфильтровать разностные данные между снимками.</span><span class="sxs-lookup"><span data-stu-id="c0baa-195">You can use the **Scope** dropdown to filter differential info between snapshots:</span></span>

![Фильтр областей для comparisions моментальных снимков](./media/memory_comparison_scope_filter.png)

- <strong><span data-ttu-id="c0baa-197">Объекты, оставленные на основе снимка # <number></strong> : показывает различие между объектами, добавленными в кучу, и удален из кучи базового снимка в предыдущий снимок.</span><span class="sxs-lookup"><span data-stu-id="c0baa-197">Objects left over from Snapshot #<number></strong>: Shows the diff between the objects added to the heap and removed from the heap from the baseline snapshot to the previous snapshot.</span></span> <span data-ttu-id="c0baa-198">Например, если в сводке по снимкам отображается <em> значение + 205/-195 </em> в счетчике объектов, в этом фильтре будут показаны десять объектов, которые были добавлены, но не удалены.</span><span class="sxs-lookup"><span data-stu-id="c0baa-198">For example, if the snapshot summary shows <em>+205 / -195</em> in the object count, this filter will show you the ten objects that were added but not removed.</span></span>

- <strong><span data-ttu-id="c0baa-199">Объекты, добавленные между снимками <number> и # <number></strong> : показывает все объекты, добавленные в кучу из предыдущего снимка.</span><span class="sxs-lookup"><span data-stu-id="c0baa-199">Objects added between Snapshot #<number> and #<number></strong>: Shows all objects added to the heap from the previous snapshot.</span></span>

- <strong><span data-ttu-id="c0baa-200">Все объекты в снимке # <number></strong> : показывает все объекты в куче (т. е. в <em> нефильтрованном </em> представлении).</span><span class="sxs-lookup"><span data-stu-id="c0baa-200">All objects in Snapshot #<number></strong>: Shows all objects on the heap (in other words, an <em>unfiltered</em> view).</span></span>

<span data-ttu-id="c0baa-201">По умолчанию фильтр " *Показать несовпадающие ссылки* " применяется к представлению сравнения для обозначения ссылок на объекты, которые не соответствуют текущему фильтру области.</span><span class="sxs-lookup"><span data-stu-id="c0baa-201">By default, the *Show non-matching references* filter is applied to the comparison view to indicate object references that don't match the current Scope filter.</span></span> <span data-ttu-id="c0baa-202">Вы можете отключить его из раскрывающегося меню:</span><span class="sxs-lookup"><span data-stu-id="c0baa-202">You can turn it off from the dropdown menu:</span></span>

![Фильтр несовпадающих ссылок по сравнению с моментальными снимками](./media/memory_comparison_matching_filter.png)


## <span data-ttu-id="c0baa-204">Горячие</span><span class="sxs-lookup"><span data-stu-id="c0baa-204">Shortcuts</span></span>

 <span data-ttu-id="c0baa-205">Действие</span><span class="sxs-lookup"><span data-stu-id="c0baa-205">Action</span></span> | <span data-ttu-id="c0baa-206">Появивше</span><span class="sxs-lookup"><span data-stu-id="c0baa-206">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="c0baa-207">Запуск и остановка сеанса профилирования</span><span class="sxs-lookup"><span data-stu-id="c0baa-207">Start / Stop profiling session</span></span>  | `Ctrl` + `E`
<span data-ttu-id="c0baa-208">Импорт сеанса профилирования</span><span class="sxs-lookup"><span data-stu-id="c0baa-208">Import profiling session</span></span> | `Ctrl` + `O`
<span data-ttu-id="c0baa-209">Экспорт сеанса профилирования</span><span class="sxs-lookup"><span data-stu-id="c0baa-209">Export profiling session</span></span> | `Ctrl` + `S`
<span data-ttu-id="c0baa-210">Создание снимка кучи</span><span class="sxs-lookup"><span data-stu-id="c0baa-210">Take heap snapshot</span></span> | `Ctrl` + `Shift` + `T`

## <span data-ttu-id="c0baa-211">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="c0baa-211">Known Issues</span></span>

### <span data-ttu-id="c0baa-212">Произошла ошибка при запуске сеанса профилирования</span><span class="sxs-lookup"><span data-stu-id="c0baa-212">An error occurred while starting the profiling session</span></span>

<span data-ttu-id="c0baa-213">Если отображается это сообщение об ошибке: **при запуске сеанса профилирования** в инструменте "память" выполните указанные ниже действия для решения этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="c0baa-213">If you see this error message: **An error occurred while starting the profiling session** in the Memory tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="c0baa-214">Нажмите клавишу `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="c0baa-214">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="c0baa-215">В диалоговом окне Выполнить введите **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="c0baa-215">In the Run dialog, enter **services.msc**.</span></span>
![Известные проблемы – 1](./media/known_issues_1.PNG)

3. <span data-ttu-id="c0baa-217">Найдите **стандартную службу сборщика центра диагностики Microsoft (R)** и щелкните ее правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="c0baa-217">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![Известные проблемы – 2](./media/known_issues_2.PNG)

4. <span data-ttu-id="c0baa-219">Перезапустите **стандартную службу сборщика центра диагностики Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="c0baa-219">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![Известные проблемы – 3](./media/known_issues_3.PNG)

5. <span data-ttu-id="c0baa-221">Закройте инструменты разработчика Microsoft EDGE и вкладку. Откройте новую вкладку, перейдите на нужную страницу и нажмите клавишу `F12` .</span><span class="sxs-lookup"><span data-stu-id="c0baa-221">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="c0baa-222">Теперь вы сможете начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="c0baa-222">You should now be able to begin profiling.</span></span> 
![Известные проблемы — 4](./media/known_issues_4-memory.PNG)

<span data-ttu-id="c0baa-224">Вы по-прежнему столкнулись с проблемами?</span><span class="sxs-lookup"><span data-stu-id="c0baa-224">Still running into problems?</span></span> <span data-ttu-id="c0baa-225">Пожалуйста, отправьте нам свой отзыв с помощью значка " **Отправить отзыв** "!</span><span class="sxs-lookup"><span data-stu-id="c0baa-225">Please send us your feedback using the **Send feedback** icon!</span></span> 

![Известные проблемы – 5](./media/known_issues_5.PNG)

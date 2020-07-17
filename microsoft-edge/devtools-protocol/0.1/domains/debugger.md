---
description: Ссылка на домен отладчика. Домен отладчика предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки останова, пошаговое выполнение, изменяя трассировку стека и т. д.
title: Debugger Domain-DevTools Protocol версии 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 1e76d17e5dfbe39ba61c7cb45a4e88b9fd223068
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882956"
---
# <span data-ttu-id="fb0a7-105">Debugger Domain-DevTools Protocol версии 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="fb0a7-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="fb0a7-106">Домен отладчика предоставляет возможности отладки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="fb0a7-107">Он позволяет устанавливать и удалять точки останова, пошаговое выполнение, изменяя трассировку стека и т. д.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="fb0a7-108">Методы</span><span class="sxs-lookup"><span data-stu-id="fb0a7-108">Methods</span></span>**](#methods) | <span data-ttu-id="fb0a7-109">[включить](#enable), [Отключить](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [steping](#stepout), [Pause](#pause), [Resume](#resume), [getScriptSource, setPauseOnExceptions](#getscriptsource) [, evaluateOnCallFrame](#setpauseonexceptions), [setVariableValue](#setvariablevalue) [setVariableValue](#evaluateoncallframe) [setBlackboxPatterns](#setblackboxpatterns) [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="fb0a7-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="fb0a7-110">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="fb0a7-110">Events</span></span>**](#events) | <span data-ttu-id="fb0a7-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [приостановлено](#paused), [возобновлено](#resumed)</span><span class="sxs-lookup"><span data-stu-id="fb0a7-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="fb0a7-112">Типы</span><span class="sxs-lookup"><span data-stu-id="fb0a7-112">Types</span></span>**](#types) | <span data-ttu-id="fb0a7-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [область](#scope)</span><span class="sxs-lookup"><span data-stu-id="fb0a7-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="fb0a7-114">Зависимости</span><span class="sxs-lookup"><span data-stu-id="fb0a7-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="fb0a7-115">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="fb0a7-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="fb0a7-116">Методы</span><span class="sxs-lookup"><span data-stu-id="fb0a7-116">Methods</span></span>

### <span data-ttu-id="fb0a7-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="fb0a7-117">enable</span></span>
<span data-ttu-id="fb0a7-118">Включает отладчик для заданной страницы.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-118">Enables debugger for the given page.</span></span> <span data-ttu-id="fb0a7-119">Клиенты не должны предполагать, что отладка включена, пока не будет получен результат этой команды.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>


---

### <span data-ttu-id="fb0a7-120">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="fb0a7-120">disable</span></span>
<span data-ttu-id="fb0a7-121">Отключает отладчик для данной страницы.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-121">Disables debugger for given page.</span></span>


---

### <span data-ttu-id="fb0a7-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="fb0a7-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="fb0a7-123">Возвращает возможные расположения для точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="fb0a7-124">scriptId в начальном и конечном диапазонах должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-125">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-126">start</span><span class="sxs-lookup"><span data-stu-id="fb0a7-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="fb0a7-127">Начало диапазона для поиска возможных местоположений точки останова в.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-128">завершить</span><span class="sxs-lookup"><span data-stu-id="fb0a7-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="fb0a7-129">Конец диапазона для поиска возможных местоположений точки останова в (исключая).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="fb0a7-130">Если не указано, конец сценариев используется как конец диапазона.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-131">Дает</span><span class="sxs-lookup"><span data-stu-id="fb0a7-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-132">ячейк</span><span class="sxs-lookup"><span data-stu-id="fb0a7-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="fb0a7-133">Список возможных местоположений точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="fb0a7-134">setBreakpointsActive</span></span>
<span data-ttu-id="fb0a7-135">Активирует и деактивирует все точки останова на странице.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-136">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-137">active</span><span class="sxs-lookup"><span data-stu-id="fb0a7-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fb0a7-138">Новое значение для точек останова в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="fb0a7-139">setBreakpointByUrl</span></span>
<span data-ttu-id="fb0a7-140">Задает точку останова JavaScript в указанном расположении с помощью URL-адреса или регулярного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="fb0a7-141">После того как вы выпустили эту команду, для всех существующих проанализированных сценариев будут заданы точки останова и они возвращаются в <code>locations</code> свойство.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="fb0a7-142">После синтаксического анализа сценария сопоставления будут <code>breakpointResolved</code> выданы последующие события.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="fb0a7-143">Эта логическая точка останова будет содержаться в повторной загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-144">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="fb0a7-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-146">Номер строки, в которой нужно установить точку останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-147">url</span><span class="sxs-lookup"><span data-stu-id="fb0a7-147">url</span></span> <br/> <i><span data-ttu-id="fb0a7-148">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-149">URL-адрес ресурсов, для которых нужно установить точку останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="fb0a7-150">urlRegex</span></span> <br/> <i><span data-ttu-id="fb0a7-151">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-152">Шаблон Regex для URL-адресов ресурсов, для которых нужно установить точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="fb0a7-153">Либо <code>url</code> <code>urlRegex</code> должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="fb0a7-154">columnNumber</span></span> <br/> <i><span data-ttu-id="fb0a7-155">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-156">Смещение в строке для задания точки останова в.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-157">постусловия</span><span class="sxs-lookup"><span data-stu-id="fb0a7-157">condition</span></span> <br/> <i><span data-ttu-id="fb0a7-158">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-159">Выражение, используемое в качестве условия для точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="fb0a7-160">Если указан, отладчик будет остановлен только в точке останова, если это выражение имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-161">Дает</span><span class="sxs-lookup"><span data-stu-id="fb0a7-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-162">breakpointId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="fb0a7-163">Идентификатор созданной точки останова для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-164">ячейк</span><span class="sxs-lookup"><span data-stu-id="fb0a7-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="fb0a7-165">Список местоположений, разрешенных этой точкой останова, на момент добавления.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-166">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="fb0a7-166">setBreakpoint</span></span>
<span data-ttu-id="fb0a7-167">Задает точку останова JavaScript в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-168">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-169">поиска</span><span class="sxs-lookup"><span data-stu-id="fb0a7-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="fb0a7-170">Расположение, в котором нужно установить точку останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-171">постусловия</span><span class="sxs-lookup"><span data-stu-id="fb0a7-171">condition</span></span> <br/> <i><span data-ttu-id="fb0a7-172">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-173">Выражение, используемое в качестве условия для точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="fb0a7-174">Если указан, отладчик будет остановлен только в точке останова, если это выражение имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-175">Дает</span><span class="sxs-lookup"><span data-stu-id="fb0a7-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-176">breakpointId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="fb0a7-177">Идентификатор созданной точки останова для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="fb0a7-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="fb0a7-179">Расположение, в которое разрешена точка останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="fb0a7-180">removeBreakpoint</span></span>
<span data-ttu-id="fb0a7-181">Удаляет точку останова JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-182">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-183">breakpointId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-184">stepOver</span><span class="sxs-lookup"><span data-stu-id="fb0a7-184">stepOver</span></span>
<span data-ttu-id="fb0a7-185">Пошаговые инструкции.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-185">Steps over the statement.</span></span>


---

### <span data-ttu-id="fb0a7-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="fb0a7-186">stepInto</span></span>
<span data-ttu-id="fb0a7-187">Пошаговые инструкции в вызов функции.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-187">Steps into the function call.</span></span>


---

### <span data-ttu-id="fb0a7-188">Пошаговое руководство</span><span class="sxs-lookup"><span data-stu-id="fb0a7-188">stepOut</span></span>
<span data-ttu-id="fb0a7-189">Пошаговые инструкции по вызову функции.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-189">Steps out of the function call.</span></span>


---

### <span data-ttu-id="fb0a7-190">pause</span><span class="sxs-lookup"><span data-stu-id="fb0a7-190">pause</span></span>
<span data-ttu-id="fb0a7-191">Останавливается на следующей инструкции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-191">Stops on the next JavaScript statement.</span></span>


---

### <span data-ttu-id="fb0a7-192">resume</span><span class="sxs-lookup"><span data-stu-id="fb0a7-192">resume</span></span>
<span data-ttu-id="fb0a7-193">Возобновляет выполнение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-193">Resumes JavaScript execution.</span></span>


---

### <span data-ttu-id="fb0a7-194">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="fb0a7-194">getScriptSource</span></span>
<span data-ttu-id="fb0a7-195">Возвращает источник для сценария с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-196">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-197">scriptId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="fb0a7-198">Идентификатор сценария, для которого требуется получить источник.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-199">Дает</span><span class="sxs-lookup"><span data-stu-id="fb0a7-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-200">scriptSource</span><span class="sxs-lookup"><span data-stu-id="fb0a7-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-201">Источник сценария.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="fb0a7-202">setPauseOnExceptions</span></span>
<span data-ttu-id="fb0a7-203">Определяет состояние Pause on Exceptions.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="fb0a7-204">Может быть настроено на остановку для всех исключений, неперехваченных исключений или исключений.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="fb0a7-205">Состояние начальной паузы в состоянии исключений <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="fb0a7-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-206">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-207">состояни</span><span class="sxs-lookup"><span data-stu-id="fb0a7-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="fb0a7-208">Разрешенные значения: нет, не перехвачено, все</span><span class="sxs-lookup"><span data-stu-id="fb0a7-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="fb0a7-209">Пауза в режиме исключений.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="fb0a7-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="fb0a7-211">Вычисляет выражение для данного кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-212">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="fb0a7-214">Идентификатор кадра звонка, который нужно вычислить.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-215">выражение</span><span class="sxs-lookup"><span data-stu-id="fb0a7-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-216">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-217">Дает</span><span class="sxs-lookup"><span data-stu-id="fb0a7-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-218">завершил</span><span class="sxs-lookup"><span data-stu-id="fb0a7-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="fb0a7-219">Обертка объекта для результата вычисления.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-220">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="fb0a7-220">setVariableValue</span></span>
<span data-ttu-id="fb0a7-221">Изменяет значение переменной в callframe.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="fb0a7-222">Области, основанные на объектах, не поддерживаются и должны изменяться вручную.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-223">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="fb0a7-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-225">число областей на основе 0, указанное в цепочке диапазонов.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="fb0a7-226">Разрешены только типы областей "локальный", "замыкание" и "Catch".</span><span class="sxs-lookup"><span data-stu-id="fb0a7-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="fb0a7-227">Другие области можно манипулировать вручную.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-228">variableName</span><span class="sxs-lookup"><span data-stu-id="fb0a7-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-229">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-230">newValue</span><span class="sxs-lookup"><span data-stu-id="fb0a7-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="fb0a7-231">Новое значение переменной.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="fb0a7-233">Идентификатор callframe, который содержит переменную.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="fb0a7-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="fb0a7-235">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-235">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-236">Замена предыдущих шаблонов BlackBox на прошедшие.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="fb0a7-237">Заставляет сервер пропускать пошаговое выполнение или приостановку в сценариях с URL-адресом, совпадающим с одним из шаблонов.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="fb0a7-238">Отладчик попытается покинуть сценарий blackboxed, выполнив несколько раз подряд, и, наконец, перейдет к элементу "шаг с выходом", если неудачно.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-239">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-240">структуру</span><span class="sxs-lookup"><span data-stu-id="fb0a7-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="fb0a7-241">Массив regexps, который будет использоваться для проверки URL-адреса сценария для состояния BlackBox.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="fb0a7-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="fb0a7-243">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-243">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-244">Microsoft: задает для указанного свойства отладчика указанное значение.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-245">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-247">Microsoft: заданный идентификатор свойства (например, msDebuggerPropertyId).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-248">newValue</span><span class="sxs-lookup"><span data-stu-id="fb0a7-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="fb0a7-249">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="fb0a7-249">Events</span></span>

### <span data-ttu-id="fb0a7-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="fb0a7-250">scriptParsed</span></span>
<span data-ttu-id="fb0a7-251">Возникает при синтаксическом анализе сценария.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-251">Fired when the script is parsed.</span></span> <span data-ttu-id="fb0a7-252">Это событие также срабатывает для всех известных и несобранных сценариев при включенном отладчике.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-253">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-254">scriptId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="fb0a7-255">Идентификатор синтаксического анализа сценария.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-256">url</span><span class="sxs-lookup"><span data-stu-id="fb0a7-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-257">URL-адрес или имя синтаксического анализа сценария (если есть).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-258">startLine</span><span class="sxs-lookup"><span data-stu-id="fb0a7-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-259">Смещение строки сценария в ресурсе с указанным URL-адресом (для тегов сценария).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-260">startColumn</span><span class="sxs-lookup"><span data-stu-id="fb0a7-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-261">Смещение столбца сценария в ресурсе с указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-262">endLine</span><span class="sxs-lookup"><span data-stu-id="fb0a7-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-263">Последняя строка сценария.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-264">endColumn</span><span class="sxs-lookup"><span data-stu-id="fb0a7-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-265">Длина последней строки сценария.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="fb0a7-267">Задает контекст создания сценария.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="fb0a7-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="fb0a7-269">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-270">URL-адрес карты источника, связанной со сценарием (если есть).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-271">Длина</span><span class="sxs-lookup"><span data-stu-id="fb0a7-271">length</span></span> <br/> <i><span data-ttu-id="fb0a7-272">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="fb0a7-273">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-273">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-274">Длина сценария.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-275">msParentId</span></span> <br/> <i><span data-ttu-id="fb0a7-276">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="fb0a7-277">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-277">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-278">Это идентификатор родительского документа.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="fb0a7-279">msMimeType</span></span> <br/> <i><span data-ttu-id="fb0a7-280">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="fb0a7-281">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-281">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-282">Это тип MIME.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="fb0a7-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="fb0a7-284">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="fb0a7-285">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-285">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-286">Это указывает на то, является ли этот динамический код.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="fb0a7-288">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="fb0a7-289">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-289">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-290">Это длинный идентификатор документа.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="fb0a7-291">breakpointResolved</span></span>
<span data-ttu-id="fb0a7-292">Срабатывает при разрешении точки останова для фактического сценария и местоположения.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-293">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-294">breakpointId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="fb0a7-295">Уникальный идентификатор точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-296">поиска</span><span class="sxs-lookup"><span data-stu-id="fb0a7-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="fb0a7-297">Место фактического местоположения точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-298">msLength</span><span class="sxs-lookup"><span data-stu-id="fb0a7-298">msLength</span></span> <br/> <i><span data-ttu-id="fb0a7-299">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="fb0a7-300">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-300">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-301">Microsoft: длина кода (например, число знаков) в месте точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-302">пауза</span><span class="sxs-lookup"><span data-stu-id="fb0a7-302">paused</span></span>
<span data-ttu-id="fb0a7-303">Возникает, когда отладчикы прерываются для точки останова или исключения.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-304">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb0a7-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="fb0a7-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="fb0a7-306">Стек вызовов, для которого остановлен отладчик.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-307">оправдан</span><span class="sxs-lookup"><span data-stu-id="fb0a7-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="fb0a7-308">Допустимые значения: точка останова, шаг, исключение, другое</span><span class="sxs-lookup"><span data-stu-id="fb0a7-308">Allowed values: breakpoint, step, exception, other</span></span></i></td>
            <td><span data-ttu-id="fb0a7-309">Причина приостановки.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-310">data</span><span class="sxs-lookup"><span data-stu-id="fb0a7-310">data</span></span> <br/> <i><span data-ttu-id="fb0a7-311">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="fb0a7-312">Объект, содержащий специфичные для разрыва дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="fb0a7-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="fb0a7-314">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="fb0a7-315">Идентификаторы точек останова</span><span class="sxs-lookup"><span data-stu-id="fb0a7-315">Hit breakpoints IDs</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="fb0a7-316">возобновляется</span><span class="sxs-lookup"><span data-stu-id="fb0a7-316">resumed</span></span>
<span data-ttu-id="fb0a7-317">Возникает, когда отладчик возобновляет выполнение.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-317">Fired when the debugger resumes execution.</span></span>


---

## <span data-ttu-id="fb0a7-318">Типы</span><span class="sxs-lookup"><span data-stu-id="fb0a7-318">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="fb0a7-319">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-319">BreakpointId</span></span> `string`

<span data-ttu-id="fb0a7-320">Идентификатор точки останова.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-320">Breakpoint identifier.</span></span>


---

### <a name="callframeid"></a> <span data-ttu-id="fb0a7-321">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-321">CallFrameId</span></span> `string`

<span data-ttu-id="fb0a7-322">Идентификатор кадра звонка.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-322">Call frame identifier.</span></span>


---

### <a name="location"></a> <span data-ttu-id="fb0a7-323">Расположение</span><span class="sxs-lookup"><span data-stu-id="fb0a7-323">Location</span></span> `object`

<span data-ttu-id="fb0a7-324">Расположение в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-324">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-325">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb0a7-325">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-326">scriptId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-326">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="fb0a7-327">Идентификатор сценария, указанный в <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="fb0a7-327">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-328">lineNumber</span><span class="sxs-lookup"><span data-stu-id="fb0a7-328">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-329">Номер строки в сценарии (от 0 до 1).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-329">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-330">columnNumber</span><span class="sxs-lookup"><span data-stu-id="fb0a7-330">columnNumber</span></span> <br/> <i><span data-ttu-id="fb0a7-331">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-331">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-332">Номер столбца в сценарии (от 0 до 1).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-332">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-333">msLength</span><span class="sxs-lookup"><span data-stu-id="fb0a7-333">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-334">Microsoft: длина кода (например, число символов) в этом кадре звонка.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-334">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> <span data-ttu-id="fb0a7-335">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="fb0a7-335">BreakLocation</span></span> `object`

<span data-ttu-id="fb0a7-336">Разрыв места в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-336">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-337">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb0a7-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-338">scriptId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-338">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="fb0a7-339">Идентификатор сценария, указанный в <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="fb0a7-339">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-340">lineNumber</span><span class="sxs-lookup"><span data-stu-id="fb0a7-340">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-341">Номер строки в сценарии (от 0 до 1).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-341">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-342">columnNumber</span><span class="sxs-lookup"><span data-stu-id="fb0a7-342">columnNumber</span></span> <br/> <i><span data-ttu-id="fb0a7-343">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-343">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-344">Номер столбца в сценарии (от 0 до 1).</span><span class="sxs-lookup"><span data-stu-id="fb0a7-344">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-345">msLength</span><span class="sxs-lookup"><span data-stu-id="fb0a7-345">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fb0a7-346">Microsoft: длина кода (например, число символов) в этом кадре звонка.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-346">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-347">Тип</span><span class="sxs-lookup"><span data-stu-id="fb0a7-347">type</span></span> <br/> <i><span data-ttu-id="fb0a7-348">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-348">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-349">Допустимые значения: debuggerStatement, Call, Return.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-349">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> <span data-ttu-id="fb0a7-350">CallFrame</span><span class="sxs-lookup"><span data-stu-id="fb0a7-350">CallFrame</span></span> `object`

<span data-ttu-id="fb0a7-351">Кадр звонка JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-351">JavaScript call frame.</span></span> <span data-ttu-id="fb0a7-352">Массив кадров звонка, вызываемый из стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-352">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-353">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb0a7-353">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-354">callFrameId</span><span class="sxs-lookup"><span data-stu-id="fb0a7-354">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="fb0a7-355">Идентификатор кадра звонка.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-355">Call frame identifier.</span></span> <span data-ttu-id="fb0a7-356">Этот идентификатор действителен только в том случае, если отладчик приостановлен.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-356">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-357">functionName</span><span class="sxs-lookup"><span data-stu-id="fb0a7-357">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-358">Имя функции JavaScript, вызываемой в этом кадре звонка.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-358">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-359">functionLocation</span><span class="sxs-lookup"><span data-stu-id="fb0a7-359">functionLocation</span></span> <br/> <i><span data-ttu-id="fb0a7-360">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-360">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="fb0a7-361">Проб.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-361">Experimental.</span></span> </b></span><span data-ttu-id="fb0a7-362">Расположение в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-362">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-363">поиска</span><span class="sxs-lookup"><span data-stu-id="fb0a7-363">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="fb0a7-364">Расположение в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-364">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-365">url</span><span class="sxs-lookup"><span data-stu-id="fb0a7-365">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fb0a7-366">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-366">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-367">scopeChain</span><span class="sxs-lookup"><span data-stu-id="fb0a7-367">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="fb0a7-368">Цепочка диапазонов для этого кадра звонка.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-368">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-369">этой</span><span class="sxs-lookup"><span data-stu-id="fb0a7-369">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="fb0a7-370">объект для этого кадра звонка.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-370">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-371">Возвращен</span><span class="sxs-lookup"><span data-stu-id="fb0a7-371">returnValue</span></span> <br/> <i><span data-ttu-id="fb0a7-372">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-372">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="fb0a7-373">Возвращаемое значение, если функция находится на точке возврата.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-373">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> <span data-ttu-id="fb0a7-374">Область применения</span><span class="sxs-lookup"><span data-stu-id="fb0a7-374">Scope</span></span> `object`

<span data-ttu-id="fb0a7-375">Описание области.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-375">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fb0a7-376">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb0a7-376">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fb0a7-377">Тип</span><span class="sxs-lookup"><span data-stu-id="fb0a7-377">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="fb0a7-378">Допустимые значения: Global, Local, with, замыкание, catch, Block, Script, eval, Module</span><span class="sxs-lookup"><span data-stu-id="fb0a7-378">Allowed values: global, local, with, closure, catch, block, script, eval, module</span></span></i></td>
            <td><span data-ttu-id="fb0a7-379">Тип области.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-379">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-380">объект</span><span class="sxs-lookup"><span data-stu-id="fb0a7-380">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="fb0a7-381">Объект, представляющий область.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-381">Object representing the scope.</span></span> <span data-ttu-id="fb0a7-382">Для <code>global</code> и <code>with</code> областей представляет фактический объект; для остальных областей это искусственный несохраняемый объект, перечисление переменных области в качестве свойств.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-382">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-383">name</span><span class="sxs-lookup"><span data-stu-id="fb0a7-383">name</span></span> <br/> <i><span data-ttu-id="fb0a7-384">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-384">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-385">startLocation</span><span class="sxs-lookup"><span data-stu-id="fb0a7-385">startLocation</span></span> <br/> <i><span data-ttu-id="fb0a7-386">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-386">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="fb0a7-387">Место в исходном коде, с которого начинается область</span><span class="sxs-lookup"><span data-stu-id="fb0a7-387">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fb0a7-388">endLocation</span><span class="sxs-lookup"><span data-stu-id="fb0a7-388">endLocation</span></span> <br/> <i><span data-ttu-id="fb0a7-389">необязательные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="fb0a7-390">Место в исходном коде, где заканчивается область</span><span class="sxs-lookup"><span data-stu-id="fb0a7-390">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="fb0a7-391">Зависимости</span><span class="sxs-lookup"><span data-stu-id="fb0a7-391">Dependencies</span></span>

[<span data-ttu-id="fb0a7-392">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="fb0a7-392">Runtime</span></span>](runtime.md)
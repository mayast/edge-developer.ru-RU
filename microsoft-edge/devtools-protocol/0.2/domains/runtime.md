---
description: Справочник по домену среды выполнения. Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов. Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не были явно освобождены.
title: Домен среды выполнения — протокол DevTools версии 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 710b3b3e0383f1f6feb7947e0468730d2e0b0e66
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882865"
---
# <span data-ttu-id="e9c4c-106">Домен среды выполнения — протокол DevTools версии 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e9c4c-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="e9c4c-107">Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="e9c4c-108">Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="e9c4c-109">Исходные объекты сохраняются в памяти, если они не были явно освобождены.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="e9c4c-110">Методы</span><span class="sxs-lookup"><span data-stu-id="e9c4c-110">Methods</span></span>**](#methods) | <span data-ttu-id="e9c4c-111">[Включение](#enable), [Отключение](#disable), [Оценка](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [Свойства](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="e9c4c-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="e9c4c-112">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="e9c4c-112">Events</span></span>**](#events) | <span data-ttu-id="e9c4c-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="e9c4c-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="e9c4c-114">Типы</span><span class="sxs-lookup"><span data-stu-id="e9c4c-114">Types</span></span>**](#types) | <span data-ttu-id="e9c4c-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription) [timestamp](#timestamp), [ExecutionContextDescription,](#exceptiondetails) [StackTrace](#stacktrace) [CallFrame](#callframe)</span><span class="sxs-lookup"><span data-stu-id="e9c4c-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="e9c4c-116">Методы</span><span class="sxs-lookup"><span data-stu-id="e9c4c-116">Methods</span></span>

### <span data-ttu-id="e9c4c-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="e9c4c-117">enable</span></span>
<span data-ttu-id="e9c4c-118">Позволяет создавать отчеты об ошибках <code>executionContextCreated</code> <code>executionContextDestroyed</code> и <code>executionContextsCleared</code> событиях.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="e9c4c-119">При включении отчетов <code>executionContextCreated</code> событие будет отправлено немедленно для каждого существующего контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="e9c4c-120">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="e9c4c-120">disable</span></span>
<span data-ttu-id="e9c4c-121">Отключает отчетность о <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> событиях.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="e9c4c-122">Проверьте</span><span class="sxs-lookup"><span data-stu-id="e9c4c-122">evaluate</span></span>
<span data-ttu-id="e9c4c-123">Вычисляет выражение для глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-125">выражение</span><span class="sxs-lookup"><span data-stu-id="e9c4c-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-126">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="e9c4c-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="e9c4c-128">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-129">Определяет, будет ли интерфейс API командной строки доступен во время оценки.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-130">objectGroup</span><span class="sxs-lookup"><span data-stu-id="e9c4c-130">objectGroup</span></span> <br/> <i><span data-ttu-id="e9c4c-131">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-132">Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-133">silent</span><span class="sxs-lookup"><span data-stu-id="e9c4c-133">silent</span></span> <br/> <i><span data-ttu-id="e9c4c-134">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-135">В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="e9c4c-136">Переопределение <code>setPauseOnException</code> состояния.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-137">contextId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-137">contextId</span></span> <br/> <i><span data-ttu-id="e9c4c-138">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e9c4c-139">Указывает, в каком контексте выполнения выполнить оценку.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="e9c4c-140">Если параметр опущен, то оценка будет выполнена в контексте страницы проверки.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="e9c4c-141">returnByValue</span></span> <br/> <i><span data-ttu-id="e9c4c-142">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-143">Может ли результат быть объектом JSON, который должен отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="e9c4c-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="e9c4c-145">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-146"><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-147">Дает</span><span class="sxs-lookup"><span data-stu-id="e9c4c-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-148">завершил</span><span class="sxs-lookup"><span data-stu-id="e9c4c-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e9c4c-149">Результат вычисления.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="e9c4c-150">callFunctionOn</span></span>
<span data-ttu-id="e9c4c-151">Вызывает функцию с заданным объявлением для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="e9c4c-152">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-153">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="e9c4c-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-155">Объявление вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-156">objectId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-156">objectId</span></span> <br/> <i><span data-ttu-id="e9c4c-157">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e9c4c-158">Идентификатор объекта, для которого вызывается функция.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="e9c4c-159">Следует указать значение objectId или executionContextId.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="e9c4c-160">objectId должен быть из функции Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="e9c4c-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-161">arguments</span><span class="sxs-lookup"><span data-stu-id="e9c4c-161">arguments</span></span> <br/> <i><span data-ttu-id="e9c4c-162">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="e9c4c-163">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-163">Call arguments.</span></span> <span data-ttu-id="e9c4c-164">Все аргументы вызова должны принадлежать тому же миру JavaScript, что и целевой объект.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-165">silent</span><span class="sxs-lookup"><span data-stu-id="e9c4c-165">silent</span></span> <br/> <i><span data-ttu-id="e9c4c-166">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-167">В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="e9c4c-168">Переопределение <code>setPauseOnException</code> состояния.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="e9c4c-169">returnByValue</span></span> <br/> <i><span data-ttu-id="e9c4c-170">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-171">Должен ли результат быть объектом JSON, который будет отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="e9c4c-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="e9c4c-173">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-174"><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-175">executionContextId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-175">executionContextId</span></span> <br/> <i><span data-ttu-id="e9c4c-176">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e9c4c-177">Задает контекст выполнения, для которого будет использоваться глобальный объект для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="e9c4c-178">Следует указать значение executionContextId или objectId.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-179">objectGroup</span><span class="sxs-lookup"><span data-stu-id="e9c4c-179">objectGroup</span></span> <br/> <i><span data-ttu-id="e9c4c-180">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-181">Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="e9c4c-182">Если objectGroup не указан, а objectId — objectGroup будет унаследован от Object.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-183">Дает</span><span class="sxs-lookup"><span data-stu-id="e9c4c-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-184">завершил</span><span class="sxs-lookup"><span data-stu-id="e9c4c-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e9c4c-185">Результат звонка.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="e9c4c-186">awaitPromise</span></span>
<span data-ttu-id="e9c4c-187">Добавьте обработчик в Promise с заданным идентификатором объекта Promise.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-188">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e9c4c-190">Идентификатор обещания.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="e9c4c-191">returnByValue</span></span> <br/> <i><span data-ttu-id="e9c4c-192">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-193">Может ли результат быть объектом JSON, который должен отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-194">Дает</span><span class="sxs-lookup"><span data-stu-id="e9c4c-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-195">завершил</span><span class="sxs-lookup"><span data-stu-id="e9c4c-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e9c4c-196">Результат обещания.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-196">Promise result.</span></span>  <span data-ttu-id="e9c4c-197">Будет содержать отклоненное значение, если обещание отклонено.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-198">Свойства.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-198">getProperties</span></span>
<span data-ttu-id="e9c4c-199">Возвращает свойства заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-199">Returns properties of a given object.</span></span> <span data-ttu-id="e9c4c-200">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-201">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-202">objectId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e9c4c-203">Идентификатор объекта, свойства которого нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="e9c4c-204">objectId должен быть из функции Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="e9c4c-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="e9c4c-205">ownProperties</span></span> <br/> <i><span data-ttu-id="e9c4c-206">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-207">Если значение равно true, возвращает свойства только для самого элемента, а не для цепочки прототипов.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="e9c4c-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="e9c4c-209">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="e9c4c-210">Проб.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-210">Experimental.</span></span> </b></span><span data-ttu-id="e9c4c-211">Если значение равно true, возвращает свойства метода доступа (только с методами Get и Set). внутренние свойства не возвращаются ни одному из них.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-212">Дает</span><span class="sxs-lookup"><span data-stu-id="e9c4c-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-213">завершил</span><span class="sxs-lookup"><span data-stu-id="e9c4c-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="e9c4c-214">Свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="e9c4c-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="e9c4c-216">Возвращает все переменные let, const и Class из глобальной области консоли.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-217">Дает</span><span class="sxs-lookup"><span data-stu-id="e9c4c-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-218">названия</span><span class="sxs-lookup"><span data-stu-id="e9c4c-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-219">releaseObject</span><span class="sxs-lookup"><span data-stu-id="e9c4c-219">releaseObject</span></span>
<span data-ttu-id="e9c4c-220">Освобождает удаленный объект с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-221">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-222">objectId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e9c4c-223">Идентификатор объекта для освобождения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="e9c4c-224">releaseObjectGroup</span></span>
<span data-ttu-id="e9c4c-225">Освобождает все удаленные объекты, которые принадлежат данной группе.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-226">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-227">objectGroup</span><span class="sxs-lookup"><span data-stu-id="e9c4c-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-228">Имя группы символьных объектов.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="e9c4c-229">discardConsoleEntries</span></span>
<span data-ttu-id="e9c4c-230">Отмена собранных исключений и вызовов API консоли.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="e9c4c-231">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="e9c4c-231">Events</span></span>

### <span data-ttu-id="e9c4c-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="e9c4c-232">executionContextCreated</span></span>
<span data-ttu-id="e9c4c-233">Выдается при создании нового контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-234">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-235">context</span><span class="sxs-lookup"><span data-stu-id="e9c4c-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="e9c4c-236">Вновь созданный контекст выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="e9c4c-237">executionContextDestroyed</span></span>
<span data-ttu-id="e9c4c-238">Выдается при удалении контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-239">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-240">executionContextId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e9c4c-241">Идентификатор разрушенного контекста</span><span class="sxs-lookup"><span data-stu-id="e9c4c-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="e9c4c-242">executionContextsCleared</span></span>
<span data-ttu-id="e9c4c-243">Выдается, когда все executionContexts были очищены в браузере</span><span class="sxs-lookup"><span data-stu-id="e9c4c-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="e9c4c-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="e9c4c-244">exceptionThrown</span></span>
<span data-ttu-id="e9c4c-245">Выдается, когда возникло исключение и оно не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-246">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-247">штамп</span><span class="sxs-lookup"><span data-stu-id="e9c4c-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="e9c4c-248">Метка времени исключения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="e9c4c-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e9c4c-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="e9c4c-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-251">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9c4c-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-252">Тип</span><span class="sxs-lookup"><span data-stu-id="e9c4c-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e9c4c-253">Допустимые значения: log, info, предупреждение, ошибка, отладка, тип, таблица, трассировка, dir, DirXML, Clear, выбор, подсчет, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span><span class="sxs-lookup"><span data-stu-id="e9c4c-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="e9c4c-254">Тип звонка.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-254">Type of the call.</span></span> <span data-ttu-id="e9c4c-255">Сюда входят журналы, сведения, предупреждение, ошибка, отладка, подсказка, таблица, трассировка, dir, DirXML, очистить, выбрать, счёт, countReset, timeEnd, исключение, метка времени, группа, сообщение, отметку и groupEnd.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-256">аргументы</span><span class="sxs-lookup"><span data-stu-id="e9c4c-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="e9c4c-257">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-258">executionContextId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e9c4c-259">Идентификатор контекста, в котором сделан вызов консоли</span><span class="sxs-lookup"><span data-stu-id="e9c4c-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-260">штамп</span><span class="sxs-lookup"><span data-stu-id="e9c4c-260">timestamp</span></span> <br/> <i><span data-ttu-id="e9c4c-261">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="e9c4c-262">Отметка времени вызова.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-263">Стек</span><span class="sxs-lookup"><span data-stu-id="e9c4c-263">stackTrace</span></span> <br/> <i><span data-ttu-id="e9c4c-264">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="e9c4c-265">Трассировка стека, записанная, если она доступна</span><span class="sxs-lookup"><span data-stu-id="e9c4c-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="e9c4c-266">Типы</span><span class="sxs-lookup"><span data-stu-id="e9c4c-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="e9c4c-267">ScriptId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-267">ScriptId</span></span> `string`

<span data-ttu-id="e9c4c-268">Уникальный идентификатор сценария.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="e9c4c-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="e9c4c-270">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="e9c4c-271">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="e9c4c-271">UnserializableValue</span></span> `string`

<span data-ttu-id="e9c4c-272">Примитивное значение, которое не может быть JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="e9c4c-273">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="e9c4c-273">Allowed Values</span></span>
<span data-ttu-id="e9c4c-274">Бесконечность, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="e9c4c-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="e9c4c-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e9c4c-275">RemoteObject</span></span> `object`

<span data-ttu-id="e9c4c-276">Зеркальный объект, который ссылается на исходный объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-277">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9c4c-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-278">Тип</span><span class="sxs-lookup"><span data-stu-id="e9c4c-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e9c4c-279">Допустимые значения: Object, Function, undefine, String, число, логический, символ</span><span class="sxs-lookup"><span data-stu-id="e9c4c-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="e9c4c-280">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-281">Подтип</span><span class="sxs-lookup"><span data-stu-id="e9c4c-281">subtype</span></span> <br/> <i><span data-ttu-id="e9c4c-282">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e9c4c-283">Допустимые значения: NULL, Error, Promise, Node</span><span class="sxs-lookup"><span data-stu-id="e9c4c-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="e9c4c-284">Подсказка подтипа объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-284">Object subtype hint.</span></span> <span data-ttu-id="e9c4c-285">Задается <code>object</code> только для значений типа.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-286">className</span><span class="sxs-lookup"><span data-stu-id="e9c4c-286">className</span></span> <br/> <i><span data-ttu-id="e9c4c-287">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-288">Имя класса объекта (конструктор).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-288">Object class (constructor) name.</span></span> <span data-ttu-id="e9c4c-289">Задается <code>object</code> только для значений типа.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-290">value</span><span class="sxs-lookup"><span data-stu-id="e9c4c-290">value</span></span> <br/> <i><span data-ttu-id="e9c4c-291">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="e9c4c-292">Значение удаленного объекта в случае примитивных значений или значений JSON (если оно было запрошено).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-293">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="e9c4c-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="e9c4c-294">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="e9c4c-295">Примитивное значение, которое не может быть JSON-stringified, не имеет</span><span class="sxs-lookup"><span data-stu-id="e9c4c-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="e9c4c-296">, но получает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-297">description</span><span class="sxs-lookup"><span data-stu-id="e9c4c-297">description</span></span> <br/> <i><span data-ttu-id="e9c4c-298">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-299">Строковое представление объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-300">objectId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-300">objectId</span></span> <br/> <i><span data-ttu-id="e9c4c-301">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e9c4c-302">Уникальный идентификатор объекта (для значений, не являющихся примитивами).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="e9c4c-304">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="e9c4c-305">Проб.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-305">Experimental.</span></span> </b></span><span data-ttu-id="e9c4c-306">Microsoft: соответствующий идентификатор свойства отладчика для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="e9c4c-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="e9c4c-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="e9c4c-308">Дескриптор свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-309">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9c4c-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-310">name</span><span class="sxs-lookup"><span data-stu-id="e9c4c-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-311">Описание свойства или символа.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-312">value</span><span class="sxs-lookup"><span data-stu-id="e9c4c-312">value</span></span> <br/> <i><span data-ttu-id="e9c4c-313">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e9c4c-314">Значение, связанное со свойством.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-315">доступных</span><span class="sxs-lookup"><span data-stu-id="e9c4c-315">writable</span></span> <br/> <i><span data-ttu-id="e9c4c-316">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-317">Значение true, если значение, связанное со свойством, может быть изменено (только дескрипторы данных).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-318">получить</span><span class="sxs-lookup"><span data-stu-id="e9c4c-318">get</span></span> <br/> <i><span data-ttu-id="e9c4c-319">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e9c4c-320">Функция, которая служит в качестве метода доступа к свойству или не <code>undefined</code> содержит дескрипторов методов доступа get ().</span><span class="sxs-lookup"><span data-stu-id="e9c4c-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-321">set</span><span class="sxs-lookup"><span data-stu-id="e9c4c-321">set</span></span> <br/> <i><span data-ttu-id="e9c4c-322">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e9c4c-323">Функция, которая используется в качестве Setter для свойства, или если отсутствует <code>undefined</code> Метод Setter (только дескрипторы методов доступа).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-324">настраиваемые</span><span class="sxs-lookup"><span data-stu-id="e9c4c-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-325">Значение true, если тип дескриптора свойства может изменяться, и если свойство может быть удалено из соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-326">Перечислим</span><span class="sxs-lookup"><span data-stu-id="e9c4c-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-327">Значение true, если это свойство появляется при перечислении свойств соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="e9c4c-328">wasThrown</span></span> <br/> <i><span data-ttu-id="e9c4c-329">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-330">Значение true, если результат был сгенерирован во время оценки.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="e9c4c-331">isOwn</span></span> <br/> <i><span data-ttu-id="e9c4c-332">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e9c4c-333">Значение true, если свойство принадлежит объекту.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="e9c4c-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="e9c4c-335">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="e9c4c-336">Проб.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-336">Experimental.</span></span> </b></span><span data-ttu-id="e9c4c-337">Microsoft: значение true, если свойство является возвращаемым значением.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-338">Символ</span><span class="sxs-lookup"><span data-stu-id="e9c4c-338">symbol</span></span> <br/> <i><span data-ttu-id="e9c4c-339">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e9c4c-340">Объект символа свойства, если свойство имеет `symbol` тип.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="e9c4c-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="e9c4c-341">CallArgument</span></span> `object`

<span data-ttu-id="e9c4c-342">Представляет аргумент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-342">Represents function call argument.</span></span> <span data-ttu-id="e9c4c-343">Идентификатор удаленного объекта <code>objectId</code> , примитивный <code>value</code> , несериализуемый примитивный или ни один из них (для неопределенного значения).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-344">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9c4c-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-345">value</span><span class="sxs-lookup"><span data-stu-id="e9c4c-345">value</span></span> <br/> <i><span data-ttu-id="e9c4c-346">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="e9c4c-347">Примитивное значение или сериализуемый объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-348">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="e9c4c-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="e9c4c-349">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="e9c4c-350">Примитивное значение, которое не может быть JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-351">objectId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-351">objectId</span></span> <br/> <i><span data-ttu-id="e9c4c-352">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e9c4c-353">Удаленный объектный обработчик.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="e9c4c-354">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="e9c4c-355">Идентификатор контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="e9c4c-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="e9c4c-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="e9c4c-357">Описание изолированного мира.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-358">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9c4c-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-359">id</span><span class="sxs-lookup"><span data-stu-id="e9c4c-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e9c4c-360">Уникальный идентификатор контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-360">Unique id of the execution context.</span></span> <span data-ttu-id="e9c4c-361">Его можно использовать, чтобы указать, в какой контекст выполнения следует выполнять оценку сценария.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-362">исходных</span><span class="sxs-lookup"><span data-stu-id="e9c4c-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-363">Источник контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-364">name</span><span class="sxs-lookup"><span data-stu-id="e9c4c-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-365">Понятное имя, описывающее данный контекст.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="e9c4c-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="e9c4c-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="e9c4c-367">Подробные сведения об исключении (или ошибке), выброшенных при компиляции или выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-368">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9c4c-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-369">exceptionId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e9c4c-370">Идентификатор исключения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-371">текст</span><span class="sxs-lookup"><span data-stu-id="e9c4c-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-372">Текст исключения, который должен использоваться вместе с объектом Exception, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-373">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e9c4c-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e9c4c-374">Номер строки в местоположении исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-375">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e9c4c-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e9c4c-376">Номер столбца в расположении исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-377">scriptId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-377">scriptId</span></span> <br/> <i><span data-ttu-id="e9c4c-378">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="e9c4c-379">Идентификатор сценария расположения исключения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-380">url</span><span class="sxs-lookup"><span data-stu-id="e9c4c-380">url</span></span> <br/> <i><span data-ttu-id="e9c4c-381">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-382">URL-адрес расположения исключения, которое будет использоваться, когда сценарий не был передан.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-383">Стек</span><span class="sxs-lookup"><span data-stu-id="e9c4c-383">stackTrace</span></span> <br/> <i><span data-ttu-id="e9c4c-384">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="e9c4c-385">Трассировка стека JavaScript (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-386">Ошибка</span><span class="sxs-lookup"><span data-stu-id="e9c4c-386">exception</span></span> <br/> <i><span data-ttu-id="e9c4c-387">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e9c4c-388">Объект Exception, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-389">executionContextId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-389">executionContextId</span></span> <br/> <i><span data-ttu-id="e9c4c-390">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e9c4c-391">Идентификатор контекста, в котором произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="e9c4c-392">Метка времени</span><span class="sxs-lookup"><span data-stu-id="e9c4c-392">Timestamp</span></span> `integer`

<span data-ttu-id="e9c4c-393">Количество миллисекунд, прошедшее с момента создания эпохи.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="e9c4c-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="e9c4c-394">CallFrame</span></span> `object`

<span data-ttu-id="e9c4c-395">Запись в стек для ошибок и утверждений во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-396">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9c4c-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-397">functionName</span><span class="sxs-lookup"><span data-stu-id="e9c4c-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-398">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-399">scriptId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="e9c4c-400">Идентификатор сценария JavaScript. Если отладчик не включен, ScriptId будет пустым.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-401">url</span><span class="sxs-lookup"><span data-stu-id="e9c4c-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-402">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-403">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e9c4c-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e9c4c-404">Номер строки сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-405">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e9c4c-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e9c4c-406">Номер столбца сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="e9c4c-407">Стек</span><span class="sxs-lookup"><span data-stu-id="e9c4c-407">StackTrace</span></span> `object`

<span data-ttu-id="e9c4c-408">Вызывайте кадры для утверждений и сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e9c4c-409">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9c4c-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e9c4c-410">description</span><span class="sxs-lookup"><span data-stu-id="e9c4c-410">description</span></span> <br/> <i><span data-ttu-id="e9c4c-411">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e9c4c-412">Метка строки для этой трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-412">String label of this stack trace.</span></span> <span data-ttu-id="e9c4c-413">Для асинхронных трассировок это может быть название функции, которая инициировала асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="e9c4c-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="e9c4c-415">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e9c4c-416">родитель</span><span class="sxs-lookup"><span data-stu-id="e9c4c-416">parent</span></span> <br/> <i><span data-ttu-id="e9c4c-417">необязательные</span><span class="sxs-lookup"><span data-stu-id="e9c4c-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="e9c4c-418">Асинхронная трассировка стека JavaScript, предшествующая данному стеку (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

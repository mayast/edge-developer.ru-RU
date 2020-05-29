---
description: Справочник по домену среды выполнения. Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов. Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не были явно освобождены.
title: Домен среды выполнения — протокол DevTools версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 504f944f7a8389450685b40cdd010b54c3a7ba4e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571663"
---
# <span data-ttu-id="273c1-106">Язык</span><span class="sxs-lookup"><span data-stu-id="273c1-106">Runtime</span></span>
<span data-ttu-id="273c1-107">Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="273c1-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="273c1-108">Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="273c1-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="273c1-109">Исходные объекты сохраняются в памяти, если они не были явно освобождены.</span><span class="sxs-lookup"><span data-stu-id="273c1-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="273c1-110">Методы</span><span class="sxs-lookup"><span data-stu-id="273c1-110">Methods</span></span>**](#methods) | <span data-ttu-id="273c1-111">[Включение](#enable), [Отключение](#disable), [Оценка](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [Свойства](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="273c1-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="273c1-112">События</span><span class="sxs-lookup"><span data-stu-id="273c1-112">Events</span></span>**](#events) | <span data-ttu-id="273c1-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="273c1-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="273c1-114">Типы</span><span class="sxs-lookup"><span data-stu-id="273c1-114">Types</span></span>**](#types) | <span data-ttu-id="273c1-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription) [timestamp](#timestamp), [ExecutionContextDescription,](#exceptiondetails) [StackTrace](#stacktrace) [CallFrame](#callframe)</span><span class="sxs-lookup"><span data-stu-id="273c1-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="273c1-116">Методы</span><span class="sxs-lookup"><span data-stu-id="273c1-116">Methods</span></span>

### <span data-ttu-id="273c1-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="273c1-117">enable</span></span>
<span data-ttu-id="273c1-118">Позволяет создавать отчеты об ошибках <code>executionContextCreated</code> <code>executionContextDestroyed</code> и <code>executionContextsCleared</code> событиях.</span><span class="sxs-lookup"><span data-stu-id="273c1-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="273c1-119">При включении отчетов <code>executionContextCreated</code> событие будет отправлено немедленно для каждого существующего контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="273c1-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="273c1-120">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="273c1-120">disable</span></span>
<span data-ttu-id="273c1-121">Отключает отчетность о <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> событиях.</span><span class="sxs-lookup"><span data-stu-id="273c1-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="273c1-122">Проверьте</span><span class="sxs-lookup"><span data-stu-id="273c1-122">evaluate</span></span>
<span data-ttu-id="273c1-123">Вычисляет выражение для глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-125">выражение</span><span class="sxs-lookup"><span data-stu-id="273c1-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-126">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="273c1-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="273c1-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="273c1-128">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-129">Определяет, будет ли интерфейс API командной строки доступен во время оценки.</span><span class="sxs-lookup"><span data-stu-id="273c1-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-130">objectGroup</span><span class="sxs-lookup"><span data-stu-id="273c1-130">objectGroup</span></span> <br/> <i><span data-ttu-id="273c1-131">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-132">Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="273c1-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-133">silent</span><span class="sxs-lookup"><span data-stu-id="273c1-133">silent</span></span> <br/> <i><span data-ttu-id="273c1-134">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-135">В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение.</span><span class="sxs-lookup"><span data-stu-id="273c1-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="273c1-136">Переопределение <code>setPauseOnException</code> состояния.</span><span class="sxs-lookup"><span data-stu-id="273c1-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-137">contextId</span><span class="sxs-lookup"><span data-stu-id="273c1-137">contextId</span></span> <br/> <i><span data-ttu-id="273c1-138">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="273c1-139">Указывает, в каком контексте выполнения выполнить оценку.</span><span class="sxs-lookup"><span data-stu-id="273c1-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="273c1-140">Если параметр опущен, то оценка будет выполнена в контексте страницы проверки.</span><span class="sxs-lookup"><span data-stu-id="273c1-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="273c1-141">returnByValue</span></span> <br/> <i><span data-ttu-id="273c1-142">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-143">Может ли результат быть объектом JSON, который должен отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="273c1-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="273c1-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="273c1-145">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-146"><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</span><span class="sxs-lookup"><span data-stu-id="273c1-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-147">Дает</span><span class="sxs-lookup"><span data-stu-id="273c1-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-148">завершил</span><span class="sxs-lookup"><span data-stu-id="273c1-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="273c1-149">Результат вычисления.</span><span class="sxs-lookup"><span data-stu-id="273c1-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="273c1-150">callFunctionOn</span></span>
<span data-ttu-id="273c1-151">Вызывает функцию с заданным объявлением для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="273c1-152">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-153">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="273c1-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-155">Объявление вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="273c1-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-156">objectId</span><span class="sxs-lookup"><span data-stu-id="273c1-156">objectId</span></span> <br/> <i><span data-ttu-id="273c1-157">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="273c1-158">Идентификатор объекта, для которого вызывается функция.</span><span class="sxs-lookup"><span data-stu-id="273c1-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="273c1-159">Следует указать значение objectId или executionContextId.</span><span class="sxs-lookup"><span data-stu-id="273c1-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="273c1-160">objectId должен быть из функции Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="273c1-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-161">arguments</span><span class="sxs-lookup"><span data-stu-id="273c1-161">arguments</span></span> <br/> <i><span data-ttu-id="273c1-162">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="273c1-163">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="273c1-163">Call arguments.</span></span> <span data-ttu-id="273c1-164">Все аргументы вызова должны принадлежать тому же миру JavaScript, что и целевой объект.</span><span class="sxs-lookup"><span data-stu-id="273c1-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-165">silent</span><span class="sxs-lookup"><span data-stu-id="273c1-165">silent</span></span> <br/> <i><span data-ttu-id="273c1-166">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-167">В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение.</span><span class="sxs-lookup"><span data-stu-id="273c1-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="273c1-168">Переопределение <code>setPauseOnException</code> состояния.</span><span class="sxs-lookup"><span data-stu-id="273c1-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="273c1-169">returnByValue</span></span> <br/> <i><span data-ttu-id="273c1-170">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-171">Должен ли результат быть объектом JSON, который будет отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="273c1-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="273c1-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="273c1-173">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-174"><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</span><span class="sxs-lookup"><span data-stu-id="273c1-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-175">executionContextId</span><span class="sxs-lookup"><span data-stu-id="273c1-175">executionContextId</span></span> <br/> <i><span data-ttu-id="273c1-176">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="273c1-177">Задает контекст выполнения, для которого будет использоваться глобальный объект для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="273c1-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="273c1-178">Следует указать значение executionContextId или objectId.</span><span class="sxs-lookup"><span data-stu-id="273c1-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-179">objectGroup</span><span class="sxs-lookup"><span data-stu-id="273c1-179">objectGroup</span></span> <br/> <i><span data-ttu-id="273c1-180">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-181">Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="273c1-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="273c1-182">Если objectGroup не указан, а objectId — objectGroup будет унаследован от Object.</span><span class="sxs-lookup"><span data-stu-id="273c1-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-183">Дает</span><span class="sxs-lookup"><span data-stu-id="273c1-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-184">завершил</span><span class="sxs-lookup"><span data-stu-id="273c1-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="273c1-185">Результат звонка.</span><span class="sxs-lookup"><span data-stu-id="273c1-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="273c1-186">awaitPromise</span></span>
<span data-ttu-id="273c1-187">Добавьте обработчик в Promise с заданным идентификатором объекта Promise.</span><span class="sxs-lookup"><span data-stu-id="273c1-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-188">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="273c1-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="273c1-190">Идентификатор обещания.</span><span class="sxs-lookup"><span data-stu-id="273c1-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="273c1-191">returnByValue</span></span> <br/> <i><span data-ttu-id="273c1-192">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-193">Может ли результат быть объектом JSON, который должен отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="273c1-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-194">Дает</span><span class="sxs-lookup"><span data-stu-id="273c1-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-195">завершил</span><span class="sxs-lookup"><span data-stu-id="273c1-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="273c1-196">Результат обещания.</span><span class="sxs-lookup"><span data-stu-id="273c1-196">Promise result.</span></span>  <span data-ttu-id="273c1-197">Будет содержать отклоненное значение, если обещание отклонено.</span><span class="sxs-lookup"><span data-stu-id="273c1-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-198">Свойства.</span><span class="sxs-lookup"><span data-stu-id="273c1-198">getProperties</span></span>
<span data-ttu-id="273c1-199">Возвращает свойства заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-199">Returns properties of a given object.</span></span> <span data-ttu-id="273c1-200">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-201">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-202">objectId</span><span class="sxs-lookup"><span data-stu-id="273c1-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="273c1-203">Идентификатор объекта, свойства которого нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="273c1-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="273c1-204">objectId должен быть из функции Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="273c1-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="273c1-205">ownProperties</span></span> <br/> <i><span data-ttu-id="273c1-206">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-207">Если значение равно true, возвращает свойства только для самого элемента, а не для цепочки прототипов.</span><span class="sxs-lookup"><span data-stu-id="273c1-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="273c1-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="273c1-209">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="273c1-210">Проб.</span><span class="sxs-lookup"><span data-stu-id="273c1-210">Experimental.</span></span> </b></span><span data-ttu-id="273c1-211">Если значение равно true, возвращает свойства метода доступа (только с методами Get и Set). внутренние свойства не возвращаются ни одному из них.</span><span class="sxs-lookup"><span data-stu-id="273c1-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-212">Дает</span><span class="sxs-lookup"><span data-stu-id="273c1-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-213">завершил</span><span class="sxs-lookup"><span data-stu-id="273c1-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="273c1-214">Свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="273c1-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="273c1-216">Возвращает все переменные let, const и Class из глобальной области консоли.</span><span class="sxs-lookup"><span data-stu-id="273c1-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-217">Дает</span><span class="sxs-lookup"><span data-stu-id="273c1-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-218">названия</span><span class="sxs-lookup"><span data-stu-id="273c1-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-219">releaseObject</span><span class="sxs-lookup"><span data-stu-id="273c1-219">releaseObject</span></span>
<span data-ttu-id="273c1-220">Освобождает удаленный объект с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="273c1-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-221">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-222">objectId</span><span class="sxs-lookup"><span data-stu-id="273c1-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="273c1-223">Идентификатор объекта для освобождения.</span><span class="sxs-lookup"><span data-stu-id="273c1-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="273c1-224">releaseObjectGroup</span></span>
<span data-ttu-id="273c1-225">Освобождает все удаленные объекты, которые принадлежат данной группе.</span><span class="sxs-lookup"><span data-stu-id="273c1-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-226">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-227">objectGroup</span><span class="sxs-lookup"><span data-stu-id="273c1-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-228">Имя группы символьных объектов.</span><span class="sxs-lookup"><span data-stu-id="273c1-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="273c1-229">discardConsoleEntries</span></span>
<span data-ttu-id="273c1-230">Отмена собранных исключений и вызовов API консоли.</span><span class="sxs-lookup"><span data-stu-id="273c1-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="273c1-231">События</span><span class="sxs-lookup"><span data-stu-id="273c1-231">Events</span></span>

### <span data-ttu-id="273c1-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="273c1-232">executionContextCreated</span></span>
<span data-ttu-id="273c1-233">Выдается при создании нового контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="273c1-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-234">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-235">context</span><span class="sxs-lookup"><span data-stu-id="273c1-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="273c1-236">Вновь созданный контекст выполнения.</span><span class="sxs-lookup"><span data-stu-id="273c1-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="273c1-237">executionContextDestroyed</span></span>
<span data-ttu-id="273c1-238">Выдается при удалении контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="273c1-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-239">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-240">executionContextId</span><span class="sxs-lookup"><span data-stu-id="273c1-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="273c1-241">Идентификатор разрушенного контекста</span><span class="sxs-lookup"><span data-stu-id="273c1-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="273c1-242">executionContextsCleared</span></span>
<span data-ttu-id="273c1-243">Выдается, когда все executionContexts были очищены в браузере</span><span class="sxs-lookup"><span data-stu-id="273c1-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="273c1-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="273c1-244">exceptionThrown</span></span>
<span data-ttu-id="273c1-245">Выдается, когда возникло исключение и оно не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="273c1-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-246">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-247">штамп</span><span class="sxs-lookup"><span data-stu-id="273c1-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="273c1-248">Метка времени исключения.</span><span class="sxs-lookup"><span data-stu-id="273c1-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="273c1-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="273c1-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="273c1-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-251">Параметры</span><span class="sxs-lookup"><span data-stu-id="273c1-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-252">Тип</span><span class="sxs-lookup"><span data-stu-id="273c1-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="273c1-253">Допустимые значения: log, info, предупреждение, ошибка, отладка, тип, таблица, трассировка, dir, DirXML, Clear, выбор, подсчет, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span><span class="sxs-lookup"><span data-stu-id="273c1-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="273c1-254">Тип звонка.</span><span class="sxs-lookup"><span data-stu-id="273c1-254">Type of the call.</span></span> <span data-ttu-id="273c1-255">Сюда входят журналы, сведения, предупреждение, ошибка, отладка, подсказка, таблица, трассировка, dir, DirXML, очистить, выбрать, счёт, countReset, timeEnd, исключение, метка времени, группа, сообщение, отметку и groupEnd.</span><span class="sxs-lookup"><span data-stu-id="273c1-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-256">аргументы</span><span class="sxs-lookup"><span data-stu-id="273c1-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="273c1-257">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="273c1-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-258">executionContextId</span><span class="sxs-lookup"><span data-stu-id="273c1-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="273c1-259">Идентификатор контекста, в котором сделан вызов консоли</span><span class="sxs-lookup"><span data-stu-id="273c1-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-260">штамп</span><span class="sxs-lookup"><span data-stu-id="273c1-260">timestamp</span></span> <br/> <i><span data-ttu-id="273c1-261">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="273c1-262">Отметка времени вызова.</span><span class="sxs-lookup"><span data-stu-id="273c1-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-263">Стек</span><span class="sxs-lookup"><span data-stu-id="273c1-263">stackTrace</span></span> <br/> <i><span data-ttu-id="273c1-264">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="273c1-265">Трассировка стека, записанная, если она доступна</span><span class="sxs-lookup"><span data-stu-id="273c1-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="273c1-266">Типы</span><span class="sxs-lookup"><span data-stu-id="273c1-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="273c1-267">ScriptId</span><span class="sxs-lookup"><span data-stu-id="273c1-267">ScriptId</span></span> `string`

<span data-ttu-id="273c1-268">Уникальный идентификатор сценария.</span><span class="sxs-lookup"><span data-stu-id="273c1-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="273c1-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="273c1-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="273c1-270">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="273c1-271">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="273c1-271">UnserializableValue</span></span> `string`

<span data-ttu-id="273c1-272">Примитивное значение, которое не может быть JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="273c1-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="273c1-273">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="273c1-273">Allowed Values</span></span>
<span data-ttu-id="273c1-274">Бесконечность, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="273c1-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="273c1-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="273c1-275">RemoteObject</span></span> `object`

<span data-ttu-id="273c1-276">Зеркальный объект, который ссылается на исходный объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="273c1-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-277">Свойства</span><span class="sxs-lookup"><span data-stu-id="273c1-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-278">Тип</span><span class="sxs-lookup"><span data-stu-id="273c1-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="273c1-279">Допустимые значения: Object, Function, undefine, String, число, логический, символ</span><span class="sxs-lookup"><span data-stu-id="273c1-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="273c1-280">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-281">Подтип</span><span class="sxs-lookup"><span data-stu-id="273c1-281">subtype</span></span> <br/> <i><span data-ttu-id="273c1-282">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="273c1-283">Допустимые значения: NULL, Error, Promise, Node</span><span class="sxs-lookup"><span data-stu-id="273c1-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="273c1-284">Подсказка подтипа объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-284">Object subtype hint.</span></span> <span data-ttu-id="273c1-285">Задается <code>object</code> только для значений типа.</span><span class="sxs-lookup"><span data-stu-id="273c1-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-286">className</span><span class="sxs-lookup"><span data-stu-id="273c1-286">className</span></span> <br/> <i><span data-ttu-id="273c1-287">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-288">Имя класса объекта (конструктор).</span><span class="sxs-lookup"><span data-stu-id="273c1-288">Object class (constructor) name.</span></span> <span data-ttu-id="273c1-289">Задается <code>object</code> только для значений типа.</span><span class="sxs-lookup"><span data-stu-id="273c1-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-290">value</span><span class="sxs-lookup"><span data-stu-id="273c1-290">value</span></span> <br/> <i><span data-ttu-id="273c1-291">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="273c1-292">Значение удаленного объекта в случае примитивных значений или значений JSON (если оно было запрошено).</span><span class="sxs-lookup"><span data-stu-id="273c1-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-293">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="273c1-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="273c1-294">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="273c1-295">Примитивное значение, которое не может быть JSON-stringified, не имеет</span><span class="sxs-lookup"><span data-stu-id="273c1-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="273c1-296">, но получает это свойство.</span><span class="sxs-lookup"><span data-stu-id="273c1-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-297">description</span><span class="sxs-lookup"><span data-stu-id="273c1-297">description</span></span> <br/> <i><span data-ttu-id="273c1-298">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-299">Строковое представление объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-300">objectId</span><span class="sxs-lookup"><span data-stu-id="273c1-300">objectId</span></span> <br/> <i><span data-ttu-id="273c1-301">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="273c1-302">Уникальный идентификатор объекта (для значений, не являющихся примитивами).</span><span class="sxs-lookup"><span data-stu-id="273c1-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="273c1-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="273c1-304">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="273c1-305">Проб.</span><span class="sxs-lookup"><span data-stu-id="273c1-305">Experimental.</span></span> </b></span><span data-ttu-id="273c1-306">Microsoft: соответствующий идентификатор свойства отладчика для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="273c1-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="273c1-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="273c1-308">Дескриптор свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-309">Свойства</span><span class="sxs-lookup"><span data-stu-id="273c1-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-310">name</span><span class="sxs-lookup"><span data-stu-id="273c1-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-311">Описание свойства или символа.</span><span class="sxs-lookup"><span data-stu-id="273c1-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-312">value</span><span class="sxs-lookup"><span data-stu-id="273c1-312">value</span></span> <br/> <i><span data-ttu-id="273c1-313">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="273c1-314">Значение, связанное со свойством.</span><span class="sxs-lookup"><span data-stu-id="273c1-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-315">доступных</span><span class="sxs-lookup"><span data-stu-id="273c1-315">writable</span></span> <br/> <i><span data-ttu-id="273c1-316">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-317">Значение true, если значение, связанное со свойством, может быть изменено (только дескрипторы данных).</span><span class="sxs-lookup"><span data-stu-id="273c1-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-318">получить</span><span class="sxs-lookup"><span data-stu-id="273c1-318">get</span></span> <br/> <i><span data-ttu-id="273c1-319">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="273c1-320">Функция, которая служит в качестве метода доступа к свойству или не <code>undefined</code> содержит дескрипторов методов доступа get ().</span><span class="sxs-lookup"><span data-stu-id="273c1-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-321">set</span><span class="sxs-lookup"><span data-stu-id="273c1-321">set</span></span> <br/> <i><span data-ttu-id="273c1-322">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="273c1-323">Функция, которая используется в качестве Setter для свойства, или если отсутствует <code>undefined</code> Метод Setter (только дескрипторы методов доступа).</span><span class="sxs-lookup"><span data-stu-id="273c1-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-324">настраиваемые</span><span class="sxs-lookup"><span data-stu-id="273c1-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-325">Значение true, если тип дескриптора свойства может изменяться, и если свойство может быть удалено из соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-326">Перечислим</span><span class="sxs-lookup"><span data-stu-id="273c1-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-327">Значение true, если это свойство появляется при перечислении свойств соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="273c1-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="273c1-328">wasThrown</span></span> <br/> <i><span data-ttu-id="273c1-329">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-330">Значение true, если результат был сгенерирован во время оценки.</span><span class="sxs-lookup"><span data-stu-id="273c1-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="273c1-331">isOwn</span></span> <br/> <i><span data-ttu-id="273c1-332">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="273c1-333">Значение true, если свойство принадлежит объекту.</span><span class="sxs-lookup"><span data-stu-id="273c1-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="273c1-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="273c1-335">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="273c1-336">Проб.</span><span class="sxs-lookup"><span data-stu-id="273c1-336">Experimental.</span></span> </b></span><span data-ttu-id="273c1-337">Microsoft: значение true, если свойство является возвращаемым значением.</span><span class="sxs-lookup"><span data-stu-id="273c1-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-338">Символ</span><span class="sxs-lookup"><span data-stu-id="273c1-338">symbol</span></span> <br/> <i><span data-ttu-id="273c1-339">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="273c1-340">Объект символа свойства, если свойство имеет `symbol` тип.</span><span class="sxs-lookup"><span data-stu-id="273c1-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="273c1-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="273c1-341">CallArgument</span></span> `object`

<span data-ttu-id="273c1-342">Представляет аргумент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="273c1-342">Represents function call argument.</span></span> <span data-ttu-id="273c1-343">Идентификатор удаленного объекта <code>objectId</code> , примитивный <code>value</code> , несериализуемый примитивный или ни один из них (для неопределенного значения).</span><span class="sxs-lookup"><span data-stu-id="273c1-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-344">Свойства</span><span class="sxs-lookup"><span data-stu-id="273c1-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-345">value</span><span class="sxs-lookup"><span data-stu-id="273c1-345">value</span></span> <br/> <i><span data-ttu-id="273c1-346">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="273c1-347">Примитивное значение или сериализуемый объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="273c1-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-348">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="273c1-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="273c1-349">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="273c1-350">Примитивное значение, которое не может быть JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="273c1-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-351">objectId</span><span class="sxs-lookup"><span data-stu-id="273c1-351">objectId</span></span> <br/> <i><span data-ttu-id="273c1-352">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="273c1-353">Удаленный объектный обработчик.</span><span class="sxs-lookup"><span data-stu-id="273c1-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="273c1-354">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="273c1-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="273c1-355">Идентификатор контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="273c1-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="273c1-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="273c1-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="273c1-357">Описание изолированного мира.</span><span class="sxs-lookup"><span data-stu-id="273c1-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-358">Свойства</span><span class="sxs-lookup"><span data-stu-id="273c1-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-359">id</span><span class="sxs-lookup"><span data-stu-id="273c1-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="273c1-360">Уникальный идентификатор контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="273c1-360">Unique id of the execution context.</span></span> <span data-ttu-id="273c1-361">Его можно использовать, чтобы указать, в какой контекст выполнения следует выполнять оценку сценария.</span><span class="sxs-lookup"><span data-stu-id="273c1-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-362">исходных</span><span class="sxs-lookup"><span data-stu-id="273c1-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-363">Источник контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="273c1-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-364">name</span><span class="sxs-lookup"><span data-stu-id="273c1-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-365">Понятное имя, описывающее данный контекст.</span><span class="sxs-lookup"><span data-stu-id="273c1-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="273c1-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="273c1-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="273c1-367">Подробные сведения об исключении (или ошибке), выброшенных при компиляции или выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="273c1-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-368">Свойства</span><span class="sxs-lookup"><span data-stu-id="273c1-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-369">exceptionId</span><span class="sxs-lookup"><span data-stu-id="273c1-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="273c1-370">Идентификатор исключения.</span><span class="sxs-lookup"><span data-stu-id="273c1-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-371">текст</span><span class="sxs-lookup"><span data-stu-id="273c1-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-372">Текст исключения, который должен использоваться вместе с объектом Exception, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="273c1-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-373">lineNumber</span><span class="sxs-lookup"><span data-stu-id="273c1-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="273c1-374">Номер строки в местоположении исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="273c1-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-375">columnNumber</span><span class="sxs-lookup"><span data-stu-id="273c1-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="273c1-376">Номер столбца в расположении исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="273c1-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-377">scriptId</span><span class="sxs-lookup"><span data-stu-id="273c1-377">scriptId</span></span> <br/> <i><span data-ttu-id="273c1-378">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="273c1-379">Идентификатор сценария расположения исключения.</span><span class="sxs-lookup"><span data-stu-id="273c1-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-380">url</span><span class="sxs-lookup"><span data-stu-id="273c1-380">url</span></span> <br/> <i><span data-ttu-id="273c1-381">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-382">URL-адрес расположения исключения, которое будет использоваться, когда сценарий не был передан.</span><span class="sxs-lookup"><span data-stu-id="273c1-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-383">Стек</span><span class="sxs-lookup"><span data-stu-id="273c1-383">stackTrace</span></span> <br/> <i><span data-ttu-id="273c1-384">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="273c1-385">Трассировка стека JavaScript (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="273c1-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-386">Ошибка</span><span class="sxs-lookup"><span data-stu-id="273c1-386">exception</span></span> <br/> <i><span data-ttu-id="273c1-387">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="273c1-388">Объект Exception, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="273c1-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-389">executionContextId</span><span class="sxs-lookup"><span data-stu-id="273c1-389">executionContextId</span></span> <br/> <i><span data-ttu-id="273c1-390">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="273c1-391">Идентификатор контекста, в котором произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="273c1-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="273c1-392">Метка времени</span><span class="sxs-lookup"><span data-stu-id="273c1-392">Timestamp</span></span> `integer`

<span data-ttu-id="273c1-393">Количество миллисекунд, прошедшее с момента создания эпохи.</span><span class="sxs-lookup"><span data-stu-id="273c1-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="273c1-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="273c1-394">CallFrame</span></span> `object`

<span data-ttu-id="273c1-395">Запись в стек для ошибок и утверждений во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="273c1-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-396">Свойства</span><span class="sxs-lookup"><span data-stu-id="273c1-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-397">functionName</span><span class="sxs-lookup"><span data-stu-id="273c1-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-398">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="273c1-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-399">scriptId</span><span class="sxs-lookup"><span data-stu-id="273c1-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="273c1-400">Идентификатор сценария JavaScript. Если отладчик не включен, ScriptId будет пустым.</span><span class="sxs-lookup"><span data-stu-id="273c1-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-401">url</span><span class="sxs-lookup"><span data-stu-id="273c1-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-402">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="273c1-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-403">lineNumber</span><span class="sxs-lookup"><span data-stu-id="273c1-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="273c1-404">Номер строки сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="273c1-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-405">columnNumber</span><span class="sxs-lookup"><span data-stu-id="273c1-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="273c1-406">Номер столбца сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="273c1-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="273c1-407">Стек</span><span class="sxs-lookup"><span data-stu-id="273c1-407">StackTrace</span></span> `object`

<span data-ttu-id="273c1-408">Вызывайте кадры для утверждений и сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="273c1-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="273c1-409">Свойства</span><span class="sxs-lookup"><span data-stu-id="273c1-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="273c1-410">description</span><span class="sxs-lookup"><span data-stu-id="273c1-410">description</span></span> <br/> <i><span data-ttu-id="273c1-411">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="273c1-412">Метка строки для этой трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="273c1-412">String label of this stack trace.</span></span> <span data-ttu-id="273c1-413">Для асинхронных трассировок это может быть название функции, которая инициировала асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="273c1-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="273c1-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="273c1-415">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="273c1-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="273c1-416">родитель</span><span class="sxs-lookup"><span data-stu-id="273c1-416">parent</span></span> <br/> <i><span data-ttu-id="273c1-417">необязательные</span><span class="sxs-lookup"><span data-stu-id="273c1-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="273c1-418">Асинхронная трассировка стека JavaScript, предшествующая данному стеку (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="273c1-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

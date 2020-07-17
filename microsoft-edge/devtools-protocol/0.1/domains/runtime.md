---
description: Справочник по домену среды выполнения. Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов. Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не были явно освобождены.
title: Домен среды выполнения — протокол DevTools версии 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 15d6cd254ddbe2337e3db850620dc3eb20a5ea67
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882935"
---
# <span data-ttu-id="128b4-106">Домен среды выполнения — протокол DevTools версии 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="128b4-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="128b4-107">Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="128b4-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="128b4-108">Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="128b4-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="128b4-109">Исходные объекты сохраняются в памяти, если они не были явно освобождены.</span><span class="sxs-lookup"><span data-stu-id="128b4-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="128b4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="128b4-110">Methods</span></span>**](#methods) | <span data-ttu-id="128b4-111">[Включение](#enable), [Отключение](#disable), [Оценка](#evaluate), [callFunctionOn](#callfunctionon), [Свойства](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="128b4-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |
| [**<span data-ttu-id="128b4-112">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="128b4-112">Events</span></span>**](#events) | <span data-ttu-id="128b4-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="128b4-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |
| [**<span data-ttu-id="128b4-114">Типы</span><span class="sxs-lookup"><span data-stu-id="128b4-114">Types</span></span>**](#types) | <span data-ttu-id="128b4-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Метка времени](#timestamp) [, CallFrame,](#callframe) [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="128b4-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="128b4-116">Методы</span><span class="sxs-lookup"><span data-stu-id="128b4-116">Methods</span></span>

### <span data-ttu-id="128b4-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="128b4-117">enable</span></span>
<span data-ttu-id="128b4-118">Включает создание отчетов о <code>executionContextsCleared</code> событии.</span><span class="sxs-lookup"><span data-stu-id="128b4-118">Enables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="128b4-119">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="128b4-119">disable</span></span>
<span data-ttu-id="128b4-120">Отключение отчета о <code>executionContextsCleared</code> событии.</span><span class="sxs-lookup"><span data-stu-id="128b4-120">Disables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="128b4-121">Проверьте</span><span class="sxs-lookup"><span data-stu-id="128b4-121">evaluate</span></span>
<span data-ttu-id="128b4-122">Вычисляет выражение для глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-122">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="128b4-123">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-124">выражение</span><span class="sxs-lookup"><span data-stu-id="128b4-124">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-125">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="128b4-125">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-126">silent</span><span class="sxs-lookup"><span data-stu-id="128b4-126">silent</span></span> <br/> <i><span data-ttu-id="128b4-127">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-127">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-128">В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение.</span><span class="sxs-lookup"><span data-stu-id="128b4-128">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="128b4-129">Переопределение <code>setPauseOnException</code> состояния.</span><span class="sxs-lookup"><span data-stu-id="128b4-129">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-130">contextId</span><span class="sxs-lookup"><span data-stu-id="128b4-130">contextId</span></span> <br/> <i><span data-ttu-id="128b4-131">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-131">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="128b4-132">Указывает, в каком контексте выполнения выполнить оценку.</span><span class="sxs-lookup"><span data-stu-id="128b4-132">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="128b4-133">Если параметр опущен, то оценка будет выполнена в контексте страницы проверки.</span><span class="sxs-lookup"><span data-stu-id="128b4-133">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-134">returnByValue</span><span class="sxs-lookup"><span data-stu-id="128b4-134">returnByValue</span></span> <br/> <i><span data-ttu-id="128b4-135">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-135">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-136">Может ли результат быть объектом JSON, который должен отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="128b4-136">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-137">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="128b4-137">awaitPromise</span></span> <br/> <i><span data-ttu-id="128b4-138">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-138">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-139"><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</span><span class="sxs-lookup"><span data-stu-id="128b4-139">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-140">Дает</span><span class="sxs-lookup"><span data-stu-id="128b4-140">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-141">завершил</span><span class="sxs-lookup"><span data-stu-id="128b4-141">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="128b4-142">Результат вычисления.</span><span class="sxs-lookup"><span data-stu-id="128b4-142">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="128b4-143">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="128b4-143">callFunctionOn</span></span>
<span data-ttu-id="128b4-144">Вызывает функцию с заданным объявлением для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-144">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="128b4-145">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-145">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-146">Параметры</span><span class="sxs-lookup"><span data-stu-id="128b4-146">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-147">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="128b4-147">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-148">Объявление вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="128b4-148">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-149">objectId</span><span class="sxs-lookup"><span data-stu-id="128b4-149">objectId</span></span> <br/> <i><span data-ttu-id="128b4-150">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-150">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="128b4-151">Идентификатор объекта, для которого вызывается функция.</span><span class="sxs-lookup"><span data-stu-id="128b4-151">Identifier of the object to call function on.</span></span> <span data-ttu-id="128b4-152">Следует указать значение objectId или executionContextId.</span><span class="sxs-lookup"><span data-stu-id="128b4-152">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="128b4-153">objectId должен быть из функции Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="128b4-153">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-154">arguments</span><span class="sxs-lookup"><span data-stu-id="128b4-154">arguments</span></span> <br/> <i><span data-ttu-id="128b4-155">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-155">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="128b4-156">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="128b4-156">Call arguments.</span></span> <span data-ttu-id="128b4-157">Все аргументы вызова должны принадлежать тому же миру JavaScript, что и целевой объект.</span><span class="sxs-lookup"><span data-stu-id="128b4-157">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-158">silent</span><span class="sxs-lookup"><span data-stu-id="128b4-158">silent</span></span> <br/> <i><span data-ttu-id="128b4-159">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-159">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-160">В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение.</span><span class="sxs-lookup"><span data-stu-id="128b4-160">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="128b4-161">Переопределение <code>setPauseOnException</code> состояния.</span><span class="sxs-lookup"><span data-stu-id="128b4-161">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-162">returnByValue</span><span class="sxs-lookup"><span data-stu-id="128b4-162">returnByValue</span></span> <br/> <i><span data-ttu-id="128b4-163">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-163">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-164">Должен ли результат быть объектом JSON, который будет отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="128b4-164">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-165">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="128b4-165">awaitPromise</span></span> <br/> <i><span data-ttu-id="128b4-166">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-167"><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</span><span class="sxs-lookup"><span data-stu-id="128b4-167">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-168">Дает</span><span class="sxs-lookup"><span data-stu-id="128b4-168">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-169">завершил</span><span class="sxs-lookup"><span data-stu-id="128b4-169">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="128b4-170">Результат звонка.</span><span class="sxs-lookup"><span data-stu-id="128b4-170">Call result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="128b4-171">Свойства.</span><span class="sxs-lookup"><span data-stu-id="128b4-171">getProperties</span></span>
<span data-ttu-id="128b4-172">Возвращает свойства заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-172">Returns properties of a given object.</span></span> <span data-ttu-id="128b4-173">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-173">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-174">Параметры</span><span class="sxs-lookup"><span data-stu-id="128b4-174">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-175">objectId</span><span class="sxs-lookup"><span data-stu-id="128b4-175">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="128b4-176">Идентификатор объекта, свойства которого нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="128b4-176">Identifier of the object to return properties for.</span></span>  <span data-ttu-id="128b4-177">objectId должен быть из функции Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="128b4-177">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-178">ownProperties</span><span class="sxs-lookup"><span data-stu-id="128b4-178">ownProperties</span></span> <br/> <i><span data-ttu-id="128b4-179">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-179">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-180">Если значение равно true, возвращает свойства только для самого элемента, а не для цепочки прототипов.</span><span class="sxs-lookup"><span data-stu-id="128b4-180">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-181">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="128b4-181">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="128b4-182">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-182">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="128b4-183">Проб.</span><span class="sxs-lookup"><span data-stu-id="128b4-183">Experimental.</span></span> </b></span><span data-ttu-id="128b4-184">Если значение равно true, возвращает свойства метода доступа (только с методами Get и Set). внутренние свойства не возвращаются ни одному из них.</span><span class="sxs-lookup"><span data-stu-id="128b4-184">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-185">Дает</span><span class="sxs-lookup"><span data-stu-id="128b4-185">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-186">завершил</span><span class="sxs-lookup"><span data-stu-id="128b4-186">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="128b4-187">Свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-187">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="128b4-188">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="128b4-188">Events</span></span>

### <span data-ttu-id="128b4-189">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="128b4-189">executionContextsCleared</span></span>
<span data-ttu-id="128b4-190">Выдается, когда все executionContexts были очищены в браузере</span><span class="sxs-lookup"><span data-stu-id="128b4-190">Issued when all executionContexts were cleared in browser</span></span>


---

### <span data-ttu-id="128b4-191">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="128b4-191">exceptionThrown</span></span>
<span data-ttu-id="128b4-192">Выдается, когда возникло исключение и оно не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="128b4-192">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-193">Параметры</span><span class="sxs-lookup"><span data-stu-id="128b4-193">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-194">штамп</span><span class="sxs-lookup"><span data-stu-id="128b4-194">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="128b4-195">Метка времени исключения.</span><span class="sxs-lookup"><span data-stu-id="128b4-195">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-196">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="128b4-196">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="128b4-197">Типы</span><span class="sxs-lookup"><span data-stu-id="128b4-197">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="128b4-198">ScriptId</span><span class="sxs-lookup"><span data-stu-id="128b4-198">ScriptId</span></span> `string`

<span data-ttu-id="128b4-199">Уникальный идентификатор сценария.</span><span class="sxs-lookup"><span data-stu-id="128b4-199">Unique script identifier.</span></span>


---

### <a name="remoteobjectid"></a> <span data-ttu-id="128b4-200">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="128b4-200">RemoteObjectId</span></span> `string`

<span data-ttu-id="128b4-201">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-201">Unique object identifier.</span></span>


---

### <a name="unserializablevalue"></a> <span data-ttu-id="128b4-202">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="128b4-202">UnserializableValue</span></span> `string`

<span data-ttu-id="128b4-203">Примитивное значение, которое не может быть JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="128b4-203">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="128b4-204">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="128b4-204">Allowed Values</span></span>
<span data-ttu-id="128b4-205">Бесконечность, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="128b4-205">Infinity, NaN, -Infinity, -0</span></span>

---

### <a name="remoteobject"></a> <span data-ttu-id="128b4-206">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="128b4-206">RemoteObject</span></span> `object`

<span data-ttu-id="128b4-207">Зеркальный объект, который ссылается на исходный объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="128b4-207">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-208">Свойства</span><span class="sxs-lookup"><span data-stu-id="128b4-208">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-209">Тип</span><span class="sxs-lookup"><span data-stu-id="128b4-209">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="128b4-210">Допустимые значения: Object, Function, undefine, String, число, логический, символ</span><span class="sxs-lookup"><span data-stu-id="128b4-210">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="128b4-211">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-211">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-212">Подтип</span><span class="sxs-lookup"><span data-stu-id="128b4-212">subtype</span></span> <br/> <i><span data-ttu-id="128b4-213">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-213">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="128b4-214">Допустимые значения: NULL, ошибка, обещание</span><span class="sxs-lookup"><span data-stu-id="128b4-214">Allowed values: null, error, promise</span></span></i></td>
            <td><span data-ttu-id="128b4-215">Подсказка подтипа объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-215">Object subtype hint.</span></span> <span data-ttu-id="128b4-216">Задается <code>object</code> только для значений типа.</span><span class="sxs-lookup"><span data-stu-id="128b4-216">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-217">className</span><span class="sxs-lookup"><span data-stu-id="128b4-217">className</span></span> <br/> <i><span data-ttu-id="128b4-218">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-218">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-219">Имя класса объекта (конструктор).</span><span class="sxs-lookup"><span data-stu-id="128b4-219">Object class (constructor) name.</span></span> <span data-ttu-id="128b4-220">Задается <code>object</code> только для значений типа.</span><span class="sxs-lookup"><span data-stu-id="128b4-220">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-221">value</span><span class="sxs-lookup"><span data-stu-id="128b4-221">value</span></span> <br/> <i><span data-ttu-id="128b4-222">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-222">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="128b4-223">Значение удаленного объекта в случае примитивных значений или значений JSON (если оно было запрошено).</span><span class="sxs-lookup"><span data-stu-id="128b4-223">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-224">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="128b4-224">unserializableValue</span></span> <br/> <i><span data-ttu-id="128b4-225">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-225">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="128b4-226">Примитивное значение, которое не может быть JSON-stringified, не имеет</span><span class="sxs-lookup"><span data-stu-id="128b4-226">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="128b4-227">, но получает это свойство.</span><span class="sxs-lookup"><span data-stu-id="128b4-227">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-228">description</span><span class="sxs-lookup"><span data-stu-id="128b4-228">description</span></span> <br/> <i><span data-ttu-id="128b4-229">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-229">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-230">Строковое представление объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-230">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-231">objectId</span><span class="sxs-lookup"><span data-stu-id="128b4-231">objectId</span></span> <br/> <i><span data-ttu-id="128b4-232">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-232">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="128b4-233">Уникальный идентификатор объекта (для значений, не являющихся примитивами).</span><span class="sxs-lookup"><span data-stu-id="128b4-233">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-234">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="128b4-234">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="128b4-235">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-235">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="128b4-236">Проб.</span><span class="sxs-lookup"><span data-stu-id="128b4-236">Experimental.</span></span> </b></span><span data-ttu-id="128b4-237">Microsoft: соответствующий идентификатор свойства отладчика для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-237">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="128b4-238">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="128b4-238">PropertyDescriptor</span></span> `object`

<span data-ttu-id="128b4-239">Дескриптор свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-239">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-240">Свойства</span><span class="sxs-lookup"><span data-stu-id="128b4-240">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-241">name</span><span class="sxs-lookup"><span data-stu-id="128b4-241">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-242">Описание свойства или символа.</span><span class="sxs-lookup"><span data-stu-id="128b4-242">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-243">value</span><span class="sxs-lookup"><span data-stu-id="128b4-243">value</span></span> <br/> <i><span data-ttu-id="128b4-244">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-244">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="128b4-245">Значение, связанное со свойством.</span><span class="sxs-lookup"><span data-stu-id="128b4-245">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-246">доступных</span><span class="sxs-lookup"><span data-stu-id="128b4-246">writable</span></span> <br/> <i><span data-ttu-id="128b4-247">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-247">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-248">Значение true, если значение, связанное со свойством, может быть изменено (только дескрипторы данных).</span><span class="sxs-lookup"><span data-stu-id="128b4-248">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-249">получить</span><span class="sxs-lookup"><span data-stu-id="128b4-249">get</span></span> <br/> <i><span data-ttu-id="128b4-250">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-250">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="128b4-251">Функция, которая служит в качестве метода доступа к свойству или не <code>undefined</code> содержит дескрипторов методов доступа get ().</span><span class="sxs-lookup"><span data-stu-id="128b4-251">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-252">set</span><span class="sxs-lookup"><span data-stu-id="128b4-252">set</span></span> <br/> <i><span data-ttu-id="128b4-253">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-253">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="128b4-254">Функция, которая используется в качестве Setter для свойства, или если отсутствует <code>undefined</code> Метод Setter (только дескрипторы методов доступа).</span><span class="sxs-lookup"><span data-stu-id="128b4-254">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-255">настраиваемые</span><span class="sxs-lookup"><span data-stu-id="128b4-255">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-256">Значение true, если тип дескриптора свойства может изменяться, и если свойство может быть удалено из соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-256">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-257">Перечислим</span><span class="sxs-lookup"><span data-stu-id="128b4-257">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-258">Значение true, если это свойство появляется при перечислении свойств соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="128b4-258">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-259">wasThrown</span><span class="sxs-lookup"><span data-stu-id="128b4-259">wasThrown</span></span> <br/> <i><span data-ttu-id="128b4-260">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-260">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-261">Значение true, если результат был сгенерирован во время оценки.</span><span class="sxs-lookup"><span data-stu-id="128b4-261">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-262">isOwn</span><span class="sxs-lookup"><span data-stu-id="128b4-262">isOwn</span></span> <br/> <i><span data-ttu-id="128b4-263">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-263">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="128b4-264">Значение true, если свойство принадлежит объекту.</span><span class="sxs-lookup"><span data-stu-id="128b4-264">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-265">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="128b4-265">msReturnValue</span></span> <br/> <i><span data-ttu-id="128b4-266">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-266">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="128b4-267">Проб.</span><span class="sxs-lookup"><span data-stu-id="128b4-267">Experimental.</span></span> </b></span><span data-ttu-id="128b4-268">Microsoft: значение true, если свойство является возвращаемым значением.</span><span class="sxs-lookup"><span data-stu-id="128b4-268">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-269">Символ</span><span class="sxs-lookup"><span data-stu-id="128b4-269">symbol</span></span> <br/> <i><span data-ttu-id="128b4-270">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-270">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="128b4-271">Объект символа свойства, если свойство имеет `symbol` тип.</span><span class="sxs-lookup"><span data-stu-id="128b4-271">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> <span data-ttu-id="128b4-272">CallArgument</span><span class="sxs-lookup"><span data-stu-id="128b4-272">CallArgument</span></span> `object`

<span data-ttu-id="128b4-273">Представляет аргумент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="128b4-273">Represents function call argument.</span></span> <span data-ttu-id="128b4-274">Идентификатор удаленного объекта <code>objectId</code> , примитивный <code>value</code> , несериализуемый примитивный или ни один из них (для неопределенного значения).</span><span class="sxs-lookup"><span data-stu-id="128b4-274">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-275">Свойства</span><span class="sxs-lookup"><span data-stu-id="128b4-275">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-276">value</span><span class="sxs-lookup"><span data-stu-id="128b4-276">value</span></span> <br/> <i><span data-ttu-id="128b4-277">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-277">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="128b4-278">Примитивное значение или сериализуемый объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="128b4-278">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-279">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="128b4-279">unserializableValue</span></span> <br/> <i><span data-ttu-id="128b4-280">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-280">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="128b4-281">Примитивное значение, которое не может быть JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="128b4-281">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-282">objectId</span><span class="sxs-lookup"><span data-stu-id="128b4-282">objectId</span></span> <br/> <i><span data-ttu-id="128b4-283">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-283">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="128b4-284">Удаленный объектный обработчик.</span><span class="sxs-lookup"><span data-stu-id="128b4-284">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> <span data-ttu-id="128b4-285">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="128b4-285">ExecutionContextId</span></span> `integer`

<span data-ttu-id="128b4-286">Идентификатор контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="128b4-286">Id of an execution context.</span></span>


---

### <a name="exceptiondetails"></a> <span data-ttu-id="128b4-287">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="128b4-287">ExceptionDetails</span></span> `object`

<span data-ttu-id="128b4-288">Подробные сведения об исключении (или ошибке), выброшенных при компиляции или выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="128b4-288">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-289">Свойства</span><span class="sxs-lookup"><span data-stu-id="128b4-289">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-290">exceptionId</span><span class="sxs-lookup"><span data-stu-id="128b4-290">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="128b4-291">Идентификатор исключения.</span><span class="sxs-lookup"><span data-stu-id="128b4-291">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-292">текст</span><span class="sxs-lookup"><span data-stu-id="128b4-292">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-293">Текст исключения, который должен использоваться вместе с объектом Exception, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="128b4-293">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-294">lineNumber</span><span class="sxs-lookup"><span data-stu-id="128b4-294">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="128b4-295">Номер строки в местоположении исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="128b4-295">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-296">columnNumber</span><span class="sxs-lookup"><span data-stu-id="128b4-296">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="128b4-297">Номер столбца в расположении исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="128b4-297">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-298">scriptId</span><span class="sxs-lookup"><span data-stu-id="128b4-298">scriptId</span></span> <br/> <i><span data-ttu-id="128b4-299">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-299">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="128b4-300">Идентификатор сценария расположения исключения.</span><span class="sxs-lookup"><span data-stu-id="128b4-300">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-301">url</span><span class="sxs-lookup"><span data-stu-id="128b4-301">url</span></span> <br/> <i><span data-ttu-id="128b4-302">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-302">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-303">URL-адрес расположения исключения, которое будет использоваться, когда сценарий не был передан.</span><span class="sxs-lookup"><span data-stu-id="128b4-303">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-304">Стек</span><span class="sxs-lookup"><span data-stu-id="128b4-304">stackTrace</span></span> <br/> <i><span data-ttu-id="128b4-305">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-305">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="128b4-306">Трассировка стека JavaScript (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="128b4-306">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-307">Ошибка</span><span class="sxs-lookup"><span data-stu-id="128b4-307">exception</span></span> <br/> <i><span data-ttu-id="128b4-308">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-308">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="128b4-309">Объект Exception, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="128b4-309">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-310">executionContextId</span><span class="sxs-lookup"><span data-stu-id="128b4-310">executionContextId</span></span> <br/> <i><span data-ttu-id="128b4-311">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-311">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="128b4-312">Идентификатор контекста, в котором произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="128b4-312">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> <span data-ttu-id="128b4-313">Метка времени</span><span class="sxs-lookup"><span data-stu-id="128b4-313">Timestamp</span></span> `integer`

<span data-ttu-id="128b4-314">Количество миллисекунд, прошедшее с момента создания эпохи.</span><span class="sxs-lookup"><span data-stu-id="128b4-314">Number of milliseconds since epoch.</span></span>


---

### <a name="callframe"></a> <span data-ttu-id="128b4-315">CallFrame</span><span class="sxs-lookup"><span data-stu-id="128b4-315">CallFrame</span></span> `object`

<span data-ttu-id="128b4-316">Запись в стек для ошибок и утверждений во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="128b4-316">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-317">Свойства</span><span class="sxs-lookup"><span data-stu-id="128b4-317">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-318">functionName</span><span class="sxs-lookup"><span data-stu-id="128b4-318">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-319">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="128b4-319">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-320">scriptId</span><span class="sxs-lookup"><span data-stu-id="128b4-320">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="128b4-321">Идентификатор сценария JavaScript.</span><span class="sxs-lookup"><span data-stu-id="128b4-321">JavaScript script id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-322">url</span><span class="sxs-lookup"><span data-stu-id="128b4-322">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-323">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="128b4-323">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-324">lineNumber</span><span class="sxs-lookup"><span data-stu-id="128b4-324">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="128b4-325">Номер строки сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="128b4-325">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-326">columnNumber</span><span class="sxs-lookup"><span data-stu-id="128b4-326">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="128b4-327">Номер столбца сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="128b4-327">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> <span data-ttu-id="128b4-328">Стек</span><span class="sxs-lookup"><span data-stu-id="128b4-328">StackTrace</span></span> `object`

<span data-ttu-id="128b4-329">Вызывайте кадры для утверждений и сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="128b4-329">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="128b4-330">Свойства</span><span class="sxs-lookup"><span data-stu-id="128b4-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="128b4-331">description</span><span class="sxs-lookup"><span data-stu-id="128b4-331">description</span></span> <br/> <i><span data-ttu-id="128b4-332">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-332">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="128b4-333">Метка строки для этой трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="128b4-333">String label of this stack trace.</span></span> <span data-ttu-id="128b4-334">Для асинхронных трассировок это может быть название функции, которая инициировала асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="128b4-334">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-335">callFrames</span><span class="sxs-lookup"><span data-stu-id="128b4-335">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="128b4-336">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="128b4-336">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="128b4-337">родитель</span><span class="sxs-lookup"><span data-stu-id="128b4-337">parent</span></span> <br/> <i><span data-ttu-id="128b4-338">необязательные</span><span class="sxs-lookup"><span data-stu-id="128b4-338">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="128b4-339">Асинхронная трассировка стека JavaScript, предшествующая данному стеку (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="128b4-339">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>

---

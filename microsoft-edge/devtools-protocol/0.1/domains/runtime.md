---
description: Справочник по домену среды выполнения. Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов. Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не были явно освобождены.
title: Домен среды выполнения — протокол DevTools версии 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 33bc98b272aaa8831e908207b97ea7d3d0842976
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571689"
---
# <span data-ttu-id="0db45-106">Язык</span><span class="sxs-lookup"><span data-stu-id="0db45-106">Runtime</span></span>
<span data-ttu-id="0db45-107">Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="0db45-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="0db45-108">Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="0db45-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="0db45-109">Исходные объекты сохраняются в памяти, если они не были явно освобождены.</span><span class="sxs-lookup"><span data-stu-id="0db45-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="0db45-110">Методы</span><span class="sxs-lookup"><span data-stu-id="0db45-110">Methods</span></span>**](#methods) | <span data-ttu-id="0db45-111">[Включение](#enable), [Отключение](#disable), [Оценка](#evaluate), [callFunctionOn](#callfunctionon), [Свойства](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="0db45-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |
| [**<span data-ttu-id="0db45-112">События</span><span class="sxs-lookup"><span data-stu-id="0db45-112">Events</span></span>**](#events) | <span data-ttu-id="0db45-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="0db45-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |
| [**<span data-ttu-id="0db45-114">Типы</span><span class="sxs-lookup"><span data-stu-id="0db45-114">Types</span></span>**](#types) | <span data-ttu-id="0db45-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Метка времени](#timestamp) [, CallFrame,](#callframe) [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="0db45-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="0db45-116">Методы</span><span class="sxs-lookup"><span data-stu-id="0db45-116">Methods</span></span>

### <span data-ttu-id="0db45-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="0db45-117">enable</span></span>
<span data-ttu-id="0db45-118">Включает создание отчетов о <code>executionContextsCleared</code> событии.</span><span class="sxs-lookup"><span data-stu-id="0db45-118">Enables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="0db45-119">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="0db45-119">disable</span></span>
<span data-ttu-id="0db45-120">Отключение отчета о <code>executionContextsCleared</code> событии.</span><span class="sxs-lookup"><span data-stu-id="0db45-120">Disables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="0db45-121">Проверьте</span><span class="sxs-lookup"><span data-stu-id="0db45-121">evaluate</span></span>
<span data-ttu-id="0db45-122">Вычисляет выражение для глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-122">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="0db45-123">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-124">выражение</span><span class="sxs-lookup"><span data-stu-id="0db45-124">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-125">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="0db45-125">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-126">silent</span><span class="sxs-lookup"><span data-stu-id="0db45-126">silent</span></span> <br/> <i><span data-ttu-id="0db45-127">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-127">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-128">В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение.</span><span class="sxs-lookup"><span data-stu-id="0db45-128">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="0db45-129">Переопределение <code>setPauseOnException</code> состояния.</span><span class="sxs-lookup"><span data-stu-id="0db45-129">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-130">contextId</span><span class="sxs-lookup"><span data-stu-id="0db45-130">contextId</span></span> <br/> <i><span data-ttu-id="0db45-131">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-131">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="0db45-132">Указывает, в каком контексте выполнения выполнить оценку.</span><span class="sxs-lookup"><span data-stu-id="0db45-132">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="0db45-133">Если параметр опущен, то оценка будет выполнена в контексте страницы проверки.</span><span class="sxs-lookup"><span data-stu-id="0db45-133">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-134">returnByValue</span><span class="sxs-lookup"><span data-stu-id="0db45-134">returnByValue</span></span> <br/> <i><span data-ttu-id="0db45-135">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-135">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-136">Может ли результат быть объектом JSON, который должен отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="0db45-136">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-137">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="0db45-137">awaitPromise</span></span> <br/> <i><span data-ttu-id="0db45-138">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-138">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-139"><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</span><span class="sxs-lookup"><span data-stu-id="0db45-139">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-140">Дает</span><span class="sxs-lookup"><span data-stu-id="0db45-140">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-141">завершил</span><span class="sxs-lookup"><span data-stu-id="0db45-141">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0db45-142">Результат вычисления.</span><span class="sxs-lookup"><span data-stu-id="0db45-142">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="0db45-143">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="0db45-143">callFunctionOn</span></span>
<span data-ttu-id="0db45-144">Вызывает функцию с заданным объявлением для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-144">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="0db45-145">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-145">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-146">Параметры</span><span class="sxs-lookup"><span data-stu-id="0db45-146">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-147">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="0db45-147">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-148">Объявление вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="0db45-148">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-149">objectId</span><span class="sxs-lookup"><span data-stu-id="0db45-149">objectId</span></span> <br/> <i><span data-ttu-id="0db45-150">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-150">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="0db45-151">Идентификатор объекта, для которого вызывается функция.</span><span class="sxs-lookup"><span data-stu-id="0db45-151">Identifier of the object to call function on.</span></span> <span data-ttu-id="0db45-152">Следует указать значение objectId или executionContextId.</span><span class="sxs-lookup"><span data-stu-id="0db45-152">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="0db45-153">objectId должен быть из функции Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="0db45-153">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-154">arguments</span><span class="sxs-lookup"><span data-stu-id="0db45-154">arguments</span></span> <br/> <i><span data-ttu-id="0db45-155">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-155">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="0db45-156">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="0db45-156">Call arguments.</span></span> <span data-ttu-id="0db45-157">Все аргументы вызова должны принадлежать тому же миру JavaScript, что и целевой объект.</span><span class="sxs-lookup"><span data-stu-id="0db45-157">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-158">silent</span><span class="sxs-lookup"><span data-stu-id="0db45-158">silent</span></span> <br/> <i><span data-ttu-id="0db45-159">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-159">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-160">В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение.</span><span class="sxs-lookup"><span data-stu-id="0db45-160">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="0db45-161">Переопределение <code>setPauseOnException</code> состояния.</span><span class="sxs-lookup"><span data-stu-id="0db45-161">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-162">returnByValue</span><span class="sxs-lookup"><span data-stu-id="0db45-162">returnByValue</span></span> <br/> <i><span data-ttu-id="0db45-163">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-163">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-164">Должен ли результат быть объектом JSON, который будет отправляться по значению.</span><span class="sxs-lookup"><span data-stu-id="0db45-164">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-165">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="0db45-165">awaitPromise</span></span> <br/> <i><span data-ttu-id="0db45-166">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-167"><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</span><span class="sxs-lookup"><span data-stu-id="0db45-167">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-168">Дает</span><span class="sxs-lookup"><span data-stu-id="0db45-168">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-169">завершил</span><span class="sxs-lookup"><span data-stu-id="0db45-169">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0db45-170">Результат звонка.</span><span class="sxs-lookup"><span data-stu-id="0db45-170">Call result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="0db45-171">Свойства.</span><span class="sxs-lookup"><span data-stu-id="0db45-171">getProperties</span></span>
<span data-ttu-id="0db45-172">Возвращает свойства заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-172">Returns properties of a given object.</span></span> <span data-ttu-id="0db45-173">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-173">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-174">Параметры</span><span class="sxs-lookup"><span data-stu-id="0db45-174">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-175">objectId</span><span class="sxs-lookup"><span data-stu-id="0db45-175">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="0db45-176">Идентификатор объекта, свойства которого нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="0db45-176">Identifier of the object to return properties for.</span></span>  <span data-ttu-id="0db45-177">objectId должен быть из функции Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="0db45-177">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-178">ownProperties</span><span class="sxs-lookup"><span data-stu-id="0db45-178">ownProperties</span></span> <br/> <i><span data-ttu-id="0db45-179">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-179">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-180">Если значение равно true, возвращает свойства только для самого элемента, а не для цепочки прототипов.</span><span class="sxs-lookup"><span data-stu-id="0db45-180">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-181">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="0db45-181">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="0db45-182">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-182">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="0db45-183">Проб.</span><span class="sxs-lookup"><span data-stu-id="0db45-183">Experimental.</span></span> </b></span><span data-ttu-id="0db45-184">Если значение равно true, возвращает свойства метода доступа (только с методами Get и Set). внутренние свойства не возвращаются ни одному из них.</span><span class="sxs-lookup"><span data-stu-id="0db45-184">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-185">Дает</span><span class="sxs-lookup"><span data-stu-id="0db45-185">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-186">завершил</span><span class="sxs-lookup"><span data-stu-id="0db45-186">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="0db45-187">Свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-187">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="0db45-188">События</span><span class="sxs-lookup"><span data-stu-id="0db45-188">Events</span></span>

### <span data-ttu-id="0db45-189">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="0db45-189">executionContextsCleared</span></span>
<span data-ttu-id="0db45-190">Выдается, когда все executionContexts были очищены в браузере</span><span class="sxs-lookup"><span data-stu-id="0db45-190">Issued when all executionContexts were cleared in browser</span></span>


---

### <span data-ttu-id="0db45-191">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="0db45-191">exceptionThrown</span></span>
<span data-ttu-id="0db45-192">Выдается, когда возникло исключение и оно не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="0db45-192">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-193">Параметры</span><span class="sxs-lookup"><span data-stu-id="0db45-193">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-194">штамп</span><span class="sxs-lookup"><span data-stu-id="0db45-194">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="0db45-195">Метка времени исключения.</span><span class="sxs-lookup"><span data-stu-id="0db45-195">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-196">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0db45-196">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="0db45-197">Типы</span><span class="sxs-lookup"><span data-stu-id="0db45-197">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="0db45-198">ScriptId</span><span class="sxs-lookup"><span data-stu-id="0db45-198">ScriptId</span></span> `string`

<span data-ttu-id="0db45-199">Уникальный идентификатор сценария.</span><span class="sxs-lookup"><span data-stu-id="0db45-199">Unique script identifier.</span></span>


---

### <a name="remoteobjectid"></a> <span data-ttu-id="0db45-200">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0db45-200">RemoteObjectId</span></span> `string`

<span data-ttu-id="0db45-201">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-201">Unique object identifier.</span></span>


---

### <a name="unserializablevalue"></a> <span data-ttu-id="0db45-202">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="0db45-202">UnserializableValue</span></span> `string`

<span data-ttu-id="0db45-203">Примитивное значение, которое не может быть JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="0db45-203">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="0db45-204">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="0db45-204">Allowed Values</span></span>
<span data-ttu-id="0db45-205">Бесконечность, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="0db45-205">Infinity, NaN, -Infinity, -0</span></span>

---

### <a name="remoteobject"></a> <span data-ttu-id="0db45-206">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0db45-206">RemoteObject</span></span> `object`

<span data-ttu-id="0db45-207">Зеркальный объект, который ссылается на исходный объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0db45-207">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-208">Свойства</span><span class="sxs-lookup"><span data-stu-id="0db45-208">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-209">Тип</span><span class="sxs-lookup"><span data-stu-id="0db45-209">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="0db45-210">Допустимые значения: Object, Function, undefine, String, число, логический, символ</span><span class="sxs-lookup"><span data-stu-id="0db45-210">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="0db45-211">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-211">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-212">Подтип</span><span class="sxs-lookup"><span data-stu-id="0db45-212">subtype</span></span> <br/> <i><span data-ttu-id="0db45-213">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-213">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="0db45-214">Допустимые значения: NULL, ошибка, обещание</span><span class="sxs-lookup"><span data-stu-id="0db45-214">Allowed values: null, error, promise</span></span></i></td>
            <td><span data-ttu-id="0db45-215">Подсказка подтипа объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-215">Object subtype hint.</span></span> <span data-ttu-id="0db45-216">Задается <code>object</code> только для значений типа.</span><span class="sxs-lookup"><span data-stu-id="0db45-216">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-217">className</span><span class="sxs-lookup"><span data-stu-id="0db45-217">className</span></span> <br/> <i><span data-ttu-id="0db45-218">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-218">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-219">Имя класса объекта (конструктор).</span><span class="sxs-lookup"><span data-stu-id="0db45-219">Object class (constructor) name.</span></span> <span data-ttu-id="0db45-220">Задается <code>object</code> только для значений типа.</span><span class="sxs-lookup"><span data-stu-id="0db45-220">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-221">value</span><span class="sxs-lookup"><span data-stu-id="0db45-221">value</span></span> <br/> <i><span data-ttu-id="0db45-222">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-222">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="0db45-223">Значение удаленного объекта в случае примитивных значений или значений JSON (если оно было запрошено).</span><span class="sxs-lookup"><span data-stu-id="0db45-223">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-224">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="0db45-224">unserializableValue</span></span> <br/> <i><span data-ttu-id="0db45-225">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-225">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="0db45-226">Примитивное значение, которое не может быть JSON-stringified, не имеет</span><span class="sxs-lookup"><span data-stu-id="0db45-226">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="0db45-227">, но получает это свойство.</span><span class="sxs-lookup"><span data-stu-id="0db45-227">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-228">description</span><span class="sxs-lookup"><span data-stu-id="0db45-228">description</span></span> <br/> <i><span data-ttu-id="0db45-229">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-229">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-230">Строковое представление объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-230">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-231">objectId</span><span class="sxs-lookup"><span data-stu-id="0db45-231">objectId</span></span> <br/> <i><span data-ttu-id="0db45-232">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-232">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="0db45-233">Уникальный идентификатор объекта (для значений, не являющихся примитивами).</span><span class="sxs-lookup"><span data-stu-id="0db45-233">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-234">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="0db45-234">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="0db45-235">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-235">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="0db45-236">Проб.</span><span class="sxs-lookup"><span data-stu-id="0db45-236">Experimental.</span></span> </b></span><span data-ttu-id="0db45-237">Microsoft: соответствующий идентификатор свойства отладчика для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-237">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="0db45-238">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="0db45-238">PropertyDescriptor</span></span> `object`

<span data-ttu-id="0db45-239">Дескриптор свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-239">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-240">Свойства</span><span class="sxs-lookup"><span data-stu-id="0db45-240">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-241">name</span><span class="sxs-lookup"><span data-stu-id="0db45-241">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-242">Описание свойства или символа.</span><span class="sxs-lookup"><span data-stu-id="0db45-242">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-243">value</span><span class="sxs-lookup"><span data-stu-id="0db45-243">value</span></span> <br/> <i><span data-ttu-id="0db45-244">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-244">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0db45-245">Значение, связанное со свойством.</span><span class="sxs-lookup"><span data-stu-id="0db45-245">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-246">доступных</span><span class="sxs-lookup"><span data-stu-id="0db45-246">writable</span></span> <br/> <i><span data-ttu-id="0db45-247">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-247">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-248">Значение true, если значение, связанное со свойством, может быть изменено (только дескрипторы данных).</span><span class="sxs-lookup"><span data-stu-id="0db45-248">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-249">получить</span><span class="sxs-lookup"><span data-stu-id="0db45-249">get</span></span> <br/> <i><span data-ttu-id="0db45-250">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-250">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0db45-251">Функция, которая служит в качестве метода доступа к свойству или не <code>undefined</code> содержит дескрипторов методов доступа get ().</span><span class="sxs-lookup"><span data-stu-id="0db45-251">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-252">set</span><span class="sxs-lookup"><span data-stu-id="0db45-252">set</span></span> <br/> <i><span data-ttu-id="0db45-253">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-253">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0db45-254">Функция, которая используется в качестве Setter для свойства, или если отсутствует <code>undefined</code> Метод Setter (только дескрипторы методов доступа).</span><span class="sxs-lookup"><span data-stu-id="0db45-254">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-255">настраиваемые</span><span class="sxs-lookup"><span data-stu-id="0db45-255">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-256">Значение true, если тип дескриптора свойства может изменяться, и если свойство может быть удалено из соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-256">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-257">Перечислим</span><span class="sxs-lookup"><span data-stu-id="0db45-257">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-258">Значение true, если это свойство появляется при перечислении свойств соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="0db45-258">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-259">wasThrown</span><span class="sxs-lookup"><span data-stu-id="0db45-259">wasThrown</span></span> <br/> <i><span data-ttu-id="0db45-260">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-260">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-261">Значение true, если результат был сгенерирован во время оценки.</span><span class="sxs-lookup"><span data-stu-id="0db45-261">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-262">isOwn</span><span class="sxs-lookup"><span data-stu-id="0db45-262">isOwn</span></span> <br/> <i><span data-ttu-id="0db45-263">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-263">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0db45-264">Значение true, если свойство принадлежит объекту.</span><span class="sxs-lookup"><span data-stu-id="0db45-264">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-265">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="0db45-265">msReturnValue</span></span> <br/> <i><span data-ttu-id="0db45-266">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-266">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="0db45-267">Проб.</span><span class="sxs-lookup"><span data-stu-id="0db45-267">Experimental.</span></span> </b></span><span data-ttu-id="0db45-268">Microsoft: значение true, если свойство является возвращаемым значением.</span><span class="sxs-lookup"><span data-stu-id="0db45-268">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-269">Символ</span><span class="sxs-lookup"><span data-stu-id="0db45-269">symbol</span></span> <br/> <i><span data-ttu-id="0db45-270">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-270">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0db45-271">Объект символа свойства, если свойство имеет `symbol` тип.</span><span class="sxs-lookup"><span data-stu-id="0db45-271">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> <span data-ttu-id="0db45-272">CallArgument</span><span class="sxs-lookup"><span data-stu-id="0db45-272">CallArgument</span></span> `object`

<span data-ttu-id="0db45-273">Представляет аргумент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="0db45-273">Represents function call argument.</span></span> <span data-ttu-id="0db45-274">Идентификатор удаленного объекта <code>objectId</code> , примитивный <code>value</code> , несериализуемый примитивный или ни один из них (для неопределенного значения).</span><span class="sxs-lookup"><span data-stu-id="0db45-274">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-275">Свойства</span><span class="sxs-lookup"><span data-stu-id="0db45-275">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-276">value</span><span class="sxs-lookup"><span data-stu-id="0db45-276">value</span></span> <br/> <i><span data-ttu-id="0db45-277">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-277">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="0db45-278">Примитивное значение или сериализуемый объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0db45-278">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-279">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="0db45-279">unserializableValue</span></span> <br/> <i><span data-ttu-id="0db45-280">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-280">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="0db45-281">Примитивное значение, которое не может быть JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="0db45-281">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-282">objectId</span><span class="sxs-lookup"><span data-stu-id="0db45-282">objectId</span></span> <br/> <i><span data-ttu-id="0db45-283">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-283">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="0db45-284">Удаленный объектный обработчик.</span><span class="sxs-lookup"><span data-stu-id="0db45-284">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> <span data-ttu-id="0db45-285">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0db45-285">ExecutionContextId</span></span> `integer`

<span data-ttu-id="0db45-286">Идентификатор контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="0db45-286">Id of an execution context.</span></span>


---

### <a name="exceptiondetails"></a> <span data-ttu-id="0db45-287">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0db45-287">ExceptionDetails</span></span> `object`

<span data-ttu-id="0db45-288">Подробные сведения об исключении (или ошибке), выброшенных при компиляции или выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="0db45-288">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-289">Свойства</span><span class="sxs-lookup"><span data-stu-id="0db45-289">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-290">exceptionId</span><span class="sxs-lookup"><span data-stu-id="0db45-290">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0db45-291">Идентификатор исключения.</span><span class="sxs-lookup"><span data-stu-id="0db45-291">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-292">текст</span><span class="sxs-lookup"><span data-stu-id="0db45-292">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-293">Текст исключения, который должен использоваться вместе с объектом Exception, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="0db45-293">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-294">lineNumber</span><span class="sxs-lookup"><span data-stu-id="0db45-294">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0db45-295">Номер строки в местоположении исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="0db45-295">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-296">columnNumber</span><span class="sxs-lookup"><span data-stu-id="0db45-296">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0db45-297">Номер столбца в расположении исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="0db45-297">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-298">scriptId</span><span class="sxs-lookup"><span data-stu-id="0db45-298">scriptId</span></span> <br/> <i><span data-ttu-id="0db45-299">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-299">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="0db45-300">Идентификатор сценария расположения исключения.</span><span class="sxs-lookup"><span data-stu-id="0db45-300">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-301">url</span><span class="sxs-lookup"><span data-stu-id="0db45-301">url</span></span> <br/> <i><span data-ttu-id="0db45-302">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-302">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-303">URL-адрес расположения исключения, которое будет использоваться, когда сценарий не был передан.</span><span class="sxs-lookup"><span data-stu-id="0db45-303">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-304">Стек</span><span class="sxs-lookup"><span data-stu-id="0db45-304">stackTrace</span></span> <br/> <i><span data-ttu-id="0db45-305">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-305">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="0db45-306">Трассировка стека JavaScript (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="0db45-306">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-307">Ошибка</span><span class="sxs-lookup"><span data-stu-id="0db45-307">exception</span></span> <br/> <i><span data-ttu-id="0db45-308">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-308">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0db45-309">Объект Exception, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="0db45-309">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-310">executionContextId</span><span class="sxs-lookup"><span data-stu-id="0db45-310">executionContextId</span></span> <br/> <i><span data-ttu-id="0db45-311">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-311">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="0db45-312">Идентификатор контекста, в котором произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="0db45-312">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> <span data-ttu-id="0db45-313">Метка времени</span><span class="sxs-lookup"><span data-stu-id="0db45-313">Timestamp</span></span> `integer`

<span data-ttu-id="0db45-314">Количество миллисекунд, прошедшее с момента создания эпохи.</span><span class="sxs-lookup"><span data-stu-id="0db45-314">Number of milliseconds since epoch.</span></span>


---

### <a name="callframe"></a> <span data-ttu-id="0db45-315">CallFrame</span><span class="sxs-lookup"><span data-stu-id="0db45-315">CallFrame</span></span> `object`

<span data-ttu-id="0db45-316">Запись в стек для ошибок и утверждений во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="0db45-316">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-317">Свойства</span><span class="sxs-lookup"><span data-stu-id="0db45-317">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-318">functionName</span><span class="sxs-lookup"><span data-stu-id="0db45-318">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-319">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0db45-319">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-320">scriptId</span><span class="sxs-lookup"><span data-stu-id="0db45-320">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="0db45-321">Идентификатор сценария JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0db45-321">JavaScript script id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-322">url</span><span class="sxs-lookup"><span data-stu-id="0db45-322">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-323">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="0db45-323">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-324">lineNumber</span><span class="sxs-lookup"><span data-stu-id="0db45-324">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0db45-325">Номер строки сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="0db45-325">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-326">columnNumber</span><span class="sxs-lookup"><span data-stu-id="0db45-326">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0db45-327">Номер столбца сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="0db45-327">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> <span data-ttu-id="0db45-328">Стек</span><span class="sxs-lookup"><span data-stu-id="0db45-328">StackTrace</span></span> `object`

<span data-ttu-id="0db45-329">Вызывайте кадры для утверждений и сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0db45-329">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0db45-330">Свойства</span><span class="sxs-lookup"><span data-stu-id="0db45-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0db45-331">description</span><span class="sxs-lookup"><span data-stu-id="0db45-331">description</span></span> <br/> <i><span data-ttu-id="0db45-332">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-332">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0db45-333">Метка строки для этой трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="0db45-333">String label of this stack trace.</span></span> <span data-ttu-id="0db45-334">Для асинхронных трассировок это может быть название функции, которая инициировала асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="0db45-334">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-335">callFrames</span><span class="sxs-lookup"><span data-stu-id="0db45-335">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="0db45-336">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0db45-336">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0db45-337">родитель</span><span class="sxs-lookup"><span data-stu-id="0db45-337">parent</span></span> <br/> <i><span data-ttu-id="0db45-338">необязательные</span><span class="sxs-lookup"><span data-stu-id="0db45-338">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="0db45-339">Асинхронная трассировка стека JavaScript, предшествующая данному стеку (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="0db45-339">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>

---

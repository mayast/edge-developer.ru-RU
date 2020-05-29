---
description: Код ошибки, возвращенный API размещения Chakra.
title: Перечисление JsErrorCode | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3d1a319872ac69b2acaf19997f3c38f9c04597b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572534"
---
# <span data-ttu-id="eae63-103">Перечисление JsErrorCode</span><span class="sxs-lookup"><span data-stu-id="eae63-103">JsErrorCode Enumeration</span></span>
<span data-ttu-id="eae63-104">Код ошибки, возвращенный API размещения Chakra.</span><span class="sxs-lookup"><span data-stu-id="eae63-104">An error code returned from a Chakra hosting API.</span></span>  
  
## <span data-ttu-id="eae63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eae63-105">Syntax</span></span>  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## <span data-ttu-id="eae63-106">Участников</span><span class="sxs-lookup"><span data-stu-id="eae63-106">Members</span></span>  
  
### <span data-ttu-id="eae63-107">Данные</span><span class="sxs-lookup"><span data-stu-id="eae63-107">Values</span></span>  
  
|<span data-ttu-id="eae63-108">Имя</span><span class="sxs-lookup"><span data-stu-id="eae63-108">Name</span></span>|<span data-ttu-id="eae63-109">Описание</span><span class="sxs-lookup"><span data-stu-id="eae63-109">Description</span></span>|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|<span data-ttu-id="eae63-110">Контекст нельзя перевести в состояние отладки, так как он уже находится в состоянии отладки.</span><span class="sxs-lookup"><span data-stu-id="eae63-110">The context cannot be put into a debug state because it is already in a debug state.</span></span>|  
|`JsErrorAlreadyProfilingContext`|<span data-ttu-id="eae63-111">Профилирование не может быть запущено, так как оно уже является профилированием.</span><span class="sxs-lookup"><span data-stu-id="eae63-111">The context cannot start profiling because it is already profiling.</span></span>|  
|`JsErrorArgumentNotObject`|<span data-ttu-id="eae63-112">API размещения, работающий с значениями объекта, вызывался с использованием значения, не являющегося объектом.</span><span class="sxs-lookup"><span data-stu-id="eae63-112">A hosting API that operates on object values was called with a non-object value.</span></span>|  
|`JsErrorBadSerializedScript`|<span data-ttu-id="eae63-113">Использован недопустимый сериализованный сценарий либо сериализованный сценарий был сериализован в другой версии обработчика Chakra.</span><span class="sxs-lookup"><span data-stu-id="eae63-113">A bad serialized script was used, or the serialized script was serialized by a different version of the Chakra engine.</span></span>|  
|`JsErrorCannotDisableExecution`|<span data-ttu-id="eae63-114">Среда выполнения не поддерживает ненадежное прерывание сценария.</span><span class="sxs-lookup"><span data-stu-id="eae63-114">Runtime does not support reliable script interruption.</span></span>|  
|`JsErrorCannotSerializeDebugScript`|<span data-ttu-id="eae63-115">Невозможно сериализовать сценарии в контекстах отладки.</span><span class="sxs-lookup"><span data-stu-id="eae63-115">Scripts cannot be serialized in debug contexts.</span></span>|  
|`JsErrorCategoryEngine`|<span data-ttu-id="eae63-116">Категория ошибок, связанных с ошибками, происходящими в самом ядре.</span><span class="sxs-lookup"><span data-stu-id="eae63-116">Category of errors that relates to errors occurring within the engine itself.</span></span>|  
|`JsErrorCategoryFatal`|<span data-ttu-id="eae63-117">Категория ошибок, которые являются неустранимыми и обозначают сбой обработчика.</span><span class="sxs-lookup"><span data-stu-id="eae63-117">Category of errors that are fatal and signify failure of the engine.</span></span>|  
|`JsErrorCategoryScript`|<span data-ttu-id="eae63-118">Категория ошибок, связанных с ошибками в сценарии.</span><span class="sxs-lookup"><span data-stu-id="eae63-118">Category of errors that relates to errors in a script.</span></span>|  
|`JsErrorCategoryUsage`|<span data-ttu-id="eae63-119">Категория ошибок, связанных с неправильным использованием самого API.</span><span class="sxs-lookup"><span data-stu-id="eae63-119">Category of errors that relates to incorrect usage of the API itself.</span></span>|  
|`JsErrorFatal`|<span data-ttu-id="eae63-120">Произошла неустранимая ошибка в обработчике.</span><span class="sxs-lookup"><span data-stu-id="eae63-120">A fatal error in the engine has occurred.</span></span>|  
|`JsErrorHeapEnumInProgress`|<span data-ttu-id="eae63-121">В данный момент выполняется перечисление кучи в контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="eae63-121">A heap enumeration is currently underway in the script context.</span></span>|  
|`JsErrorIdleNotEnabled`|<span data-ttu-id="eae63-122">Уведомление о недодействии, предопределенное, когда узел не сделал обработку на время бездействия.</span><span class="sxs-lookup"><span data-stu-id="eae63-122">Idle notification given when the host did not enable idle processing.</span></span>|  
|`JsErrorInDisabledState`|<span data-ttu-id="eae63-123">Среда выполнения находится в отключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="eae63-123">The runtime is in a disabled state.</span></span>|  
|`JsErrorInExceptionState`|<span data-ttu-id="eae63-124">Обработчик находится в состоянии исключения, и никакие API невозможно вызвать, пока не будет очищено исключение.</span><span class="sxs-lookup"><span data-stu-id="eae63-124">The engine is in an exception state and no APIs can be called until the exception is cleared.</span></span>|  
|`JsErrorInObjectBeforeCollectCallback`|<span data-ttu-id="eae63-125">Перед тем как приступить к сбору обратного вызова, операция не поддерживается в объекте.</span><span class="sxs-lookup"><span data-stu-id="eae63-125">The operation is not supported in an object before collect callback.</span></span><br /><br /> <span data-ttu-id="eae63-126">Это значение перечисления поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="eae63-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorInProfileCallback`|<span data-ttu-id="eae63-127">Контекст сценария входит в середину обратного вызова профиля.</span><span class="sxs-lookup"><span data-stu-id="eae63-127">A script context is in the middle of a profile callback.</span></span>|  
|`JsErrorInThreadServiceCallback`|<span data-ttu-id="eae63-128">Обратный вызов службы Threading в настоящее время выполняется.</span><span class="sxs-lookup"><span data-stu-id="eae63-128">A thread service callback is currently underway.</span></span>|  
|`JsErrorInvalidArgument`|<span data-ttu-id="eae63-129">Недопустимый аргумент для API размещения.</span><span class="sxs-lookup"><span data-stu-id="eae63-129">An argument to a hosting API was invalid.</span></span>|  
|`JsErrorNoCurrentContext`|<span data-ttu-id="eae63-130">Для API размещения требуется, чтобы контекст был текущим, но текущий контекст отсутствует.</span><span class="sxs-lookup"><span data-stu-id="eae63-130">The hosting API requires that a context be current, but there is no current context.</span></span>|  
|`JsErrorNotImplemented`|<span data-ttu-id="eae63-131">API размещения пока не реализован.</span><span class="sxs-lookup"><span data-stu-id="eae63-131">A hosting API is not yet implemented.</span></span>|  
|`JsErrorNullArgument`|<span data-ttu-id="eae63-132">Аргумент API размещения имеет значение NULL в контексте, где значение NULL не разрешено.</span><span class="sxs-lookup"><span data-stu-id="eae63-132">An argument to a hosting API was null in a context where null is not allowed.</span></span>|  
|`JsErrorObjectNotInspectable`|<span data-ttu-id="eae63-133">Не удается распаковать объект в `IInspectable` указатель.</span><span class="sxs-lookup"><span data-stu-id="eae63-133">Object cannot be unwrapped to `IInspectable` pointer.</span></span><br /><br /> <span data-ttu-id="eae63-134">Это значение перечисления поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="eae63-134">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorOutOfMemory`|<span data-ttu-id="eae63-135">Недостаточно памяти для работы модуля Chakra.</span><span class="sxs-lookup"><span data-stu-id="eae63-135">The Chakra engine has run out of memory.</span></span>|  
|`JsErrorPropertyNotSymbol`|<span data-ttu-id="eae63-136">API размещения, который работает с идентификаторами свойств символов, но был вызван с идентификатором свойства, не являющимся символом. Код ошибки возвращается в `JsGetSymbolFromPropertyId` том случае, если функция вызывается с идентификатором свойства, не являющимся символом.</span><span class="sxs-lookup"><span data-stu-id="eae63-136">A hosting API that operates on symbol property ids but was called with a non-symbol property id. The error code is returned by `JsGetSymbolFromPropertyId` if the function is called with non-symbol property id.</span></span><br /><br /> <span data-ttu-id="eae63-137">Это значение перечисления поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="eae63-137">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorPropertyNotString`|<span data-ttu-id="eae63-138">API размещения, работающий с идентификаторами строковых свойств, но вызванный идентификатором нестрокового свойства. Код ошибки возвращается функцией existing, `JsGetPropertyNamefromId` Если функция вызывается с идентификатором нестрокового свойства.</span><span class="sxs-lookup"><span data-stu-id="eae63-138">A hosting API that operates on string property ids but was called with a non-string property id. The error code is returned by existing `JsGetPropertyNamefromId` if the function is called with non-string property id.</span></span><br /><br /> <span data-ttu-id="eae63-139">Это значение перечисления поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="eae63-139">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorRuntimeInUse`|<span data-ttu-id="eae63-140">Среда выполнения, которая все еще используется, не может быть удалена.</span><span class="sxs-lookup"><span data-stu-id="eae63-140">A runtime that is still in use cannot be disposed.</span></span>|  
|`JsErrorScriptCompile`|<span data-ttu-id="eae63-141">Не удалось выполнить компиляцию JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eae63-141">JavaScript failed to compile.</span></span>|  
|`JsErrorScriptEvalDisabled`|<span data-ttu-id="eae63-142">Сценарий был завершен, так как он попытался использовать, `eval` `function` а функция eval была отключена.</span><span class="sxs-lookup"><span data-stu-id="eae63-142">A script was terminated because it tried to use `eval` or `function` and eval was disabled.</span></span>|  
|`JsErrorScriptException`|<span data-ttu-id="eae63-143">При выполнении сценария возникло исключение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eae63-143">A JavaScript exception occurred while running a script.</span></span>|  
|`JsErrorScriptTerminated`|<span data-ttu-id="eae63-144">Сценарий был завершен из-за запроса на приостановку выполнения.</span><span class="sxs-lookup"><span data-stu-id="eae63-144">A script was terminated due to a request to suspend a runtime.</span></span>|  
|`JsErrorWrongRuntime`|<span data-ttu-id="eae63-145">API размещения вызвал объект, созданный в другой среде выполнения JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eae63-145">A hosting API was called with object created on different JavaScript runtime.</span></span>|  
|`JsErrorWrongThread`|<span data-ttu-id="eae63-146">API размещения был вызван в неправильном потоке.</span><span class="sxs-lookup"><span data-stu-id="eae63-146">A hosting API was called on the wrong thread.</span></span>|  
|`JsNoError`|<span data-ttu-id="eae63-147">Код ошибки при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="eae63-147">Success error code.</span></span>|  
  
## <span data-ttu-id="eae63-148">Требования</span><span class="sxs-lookup"><span data-stu-id="eae63-148">Requirements</span></span>  
 <span data-ttu-id="eae63-149">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="eae63-149">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="eae63-150">См. также</span><span class="sxs-lookup"><span data-stu-id="eae63-150">See Also</span></span>  
 [<span data-ttu-id="eae63-151">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="eae63-151">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
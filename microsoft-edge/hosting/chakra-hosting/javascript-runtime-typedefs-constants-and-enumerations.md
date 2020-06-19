---
description: В среде выполнения JavaScript (JsRT) typedefs, константы и перечисления поддерживают добавление возможностей сценариев в классических и серверных приложений, работающих под управлением Windows.
title: Typedef, константы и перечисления в среде выполнения JavaScript
ms.date: 06/08/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 1aa107ed-e144-4947-b5bb-90284a537174
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 20c52c3a958f6ba14fbfbdcdad794747a9c34949
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752264"
---
# <span data-ttu-id="da7d2-103">Typedef, константы и перечисления в среде выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="da7d2-103">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="da7d2-104">В среде выполнения JavaScript (JsRT) typedefs, константы и перечисления поддерживают добавление возможностей сценариев в классических и серверных приложений, работающих под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="da7d2-104">JavaScript Runtime (JsRT) typedefs, constants, and enumerations support adding scripting capabilities to desktop and server-side applications running on Windows.</span></span>  

## <span data-ttu-id="da7d2-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="da7d2-105">In this section</span></span>  

<span data-ttu-id="da7d2-106">Следующие глобальные typedef поддерживают размещение JsRT:</span><span class="sxs-lookup"><span data-stu-id="da7d2-106">The following global typedefs support JsRT hosting:</span></span>  

*   [<span data-ttu-id="da7d2-107">JsBackgroundWorkItemCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-107">JsBackgroundWorkItemCallback Typedef</span></span>](./jsbackgroundworkitemcallback-typedef.md)  
*   [<span data-ttu-id="da7d2-108">JsBeforeCollectCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-108">JsBeforeCollectCallback Typedef</span></span>](./jsbeforecollectcallback-typedef.md)  
*   [<span data-ttu-id="da7d2-109">JsContextRef Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-109">JsContextRef Typedef</span></span>](./jscontextref-typedef.md)  
*   [<span data-ttu-id="da7d2-110">JsFinalizeCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-110">JsFinalizeCallback Typedef</span></span>](./jsfinalizecallback-typedef.md)  
*   [<span data-ttu-id="da7d2-111">JsMemoryAllocationCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-111">JsMemoryAllocationCallback Typedef</span></span>](./jsmemoryallocationcallback-typedef.md)  
*   [<span data-ttu-id="da7d2-112">JsNativeFunction Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-112">JsNativeFunction Typedef</span></span>](./jsnativefunction-typedef.md)  
*   [<span data-ttu-id="da7d2-113">JsObjectBeforeCollectCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-113">JsObjectBeforeCollectCallback Typedef</span></span>](./jsobjectbeforecollectcallback-typedef.md)  
*   [<span data-ttu-id="da7d2-114">JsProjectionCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-114">JsProjectionCallback Typedef</span></span>](./jsprojectioncallback-typedef.md)  
*   [<span data-ttu-id="da7d2-115">JsProjectionCallbackContext Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-115">JsProjectionCallbackContext Typedef</span></span>](./jsprojectioncallbackcontext-typedef.md)  
*   [<span data-ttu-id="da7d2-116">JsProjectionEnqueueCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-116">JsProjectionEnqueueCallback Typedef</span></span>](./jsprojectionenqueuecallback-typedef.md)  
*   [<span data-ttu-id="da7d2-117">JsPromiseContinuationCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-117">JsPromiseContinuationCallback Typedef</span></span>](./jspromisecontinuationcallback-typedef.md)  
*   [<span data-ttu-id="da7d2-118">JsPropertyIdRef Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-118">JsPropertyIdRef Typedef</span></span>](./jspropertyidref-typedef.md)  
*   [<span data-ttu-id="da7d2-119">JsRef Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-119">JsRef Typedef</span></span>](./jsref-typedef.md)  
*   [<span data-ttu-id="da7d2-120">JsRuntimeHandle Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-120">JsRuntimeHandle Typedef</span></span>](./jsruntimehandle-typedef.md)  
*   [<span data-ttu-id="da7d2-121">JsSerializedScriptLoadSourceCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-121">JsSerializedScriptLoadSourceCallback Typedef</span></span>](./jsserializedscriptloadsourcecallback-typedef.md)  
*   [<span data-ttu-id="da7d2-122">JsSerializedScriptUnloadCallback typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-122">JsSerializedScriptUnloadCallback typedef</span></span>](./jsserializedscriptunloadcallback-typedef.md)  
*   [<span data-ttu-id="da7d2-123">JsSourceContext Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-123">JsSourceContext Typedef</span></span>](./jssourcecontext-typedef.md)  
*   [<span data-ttu-id="da7d2-124">JsThreadServiceCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-124">JsThreadServiceCallback Typedef</span></span>](./jsthreadservicecallback-typedef.md)  
*   [<span data-ttu-id="da7d2-125">JsValueRef Typedef</span><span class="sxs-lookup"><span data-stu-id="da7d2-125">JsValueRef Typedef</span></span>](./jsvalueref-typedef.md)  

<span data-ttu-id="da7d2-126">Следующие константы поддерживают размещение JsRT:</span><span class="sxs-lookup"><span data-stu-id="da7d2-126">The following constants support JsRT hosting:</span></span>  

*   [<span data-ttu-id="da7d2-127">JS_INVALID_PROPERTYID Constant</span><span class="sxs-lookup"><span data-stu-id="da7d2-127">JS_INVALID_PROPERTYID Constant</span></span>](./js-invalid-propertyid-constant.md)  
*   [<span data-ttu-id="da7d2-128">JS_INVALID_REFERENCE Constant</span><span class="sxs-lookup"><span data-stu-id="da7d2-128">JS_INVALID_REFERENCE Constant</span></span>](./js-invalid-reference-constant.md)  
*   [<span data-ttu-id="da7d2-129">JS_INVALID_RUNTIME_HANDLE Constant</span><span class="sxs-lookup"><span data-stu-id="da7d2-129">JS_INVALID_RUNTIME_HANDLE Constant</span></span>](./js-invalid-runtime-handle-constant.md)  
*   [<span data-ttu-id="da7d2-130">JS_SOURCE_CONTEXT_NONE Constant</span><span class="sxs-lookup"><span data-stu-id="da7d2-130">JS_SOURCE_CONTEXT_NONE Constant</span></span>](./js-source-context-none-constant.md)  

<span data-ttu-id="da7d2-131">Перечисленные ниже перечисления поддерживают размещение JsRT:</span><span class="sxs-lookup"><span data-stu-id="da7d2-131">The following enumerations support JsRT hosting:</span></span>  

*   [<span data-ttu-id="da7d2-132">Перечисление JsErrorCode</span><span class="sxs-lookup"><span data-stu-id="da7d2-132">JsErrorCode Enumeration</span></span>](./jserrorcode-enumeration.md)  
*   [<span data-ttu-id="da7d2-133">Перечисление JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="da7d2-133">JsMemoryEventType Enumeration</span></span>](./jsmemoryeventtype-enumeration.md)  
*   [<span data-ttu-id="da7d2-134">Перечисление JsPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="da7d2-134">JsPropertyIdType Enumeration</span></span>](./jspropertyidtype-enumeration.md)  
*   [<span data-ttu-id="da7d2-135">Перечисление JsRuntimeAttributes</span><span class="sxs-lookup"><span data-stu-id="da7d2-135">JsRuntimeAttributes Enumeration</span></span>](./jsruntimeattributes-enumeration.md)  
*   [<span data-ttu-id="da7d2-136">Перечисление JsRuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="da7d2-136">JsRuntimeVersion Enumeration</span></span>](./jsruntimeversion-enumeration.md)  
*   [<span data-ttu-id="da7d2-137">Перечисление JsTypedArrayType</span><span class="sxs-lookup"><span data-stu-id="da7d2-137">JsTypedArrayType Enumeration</span></span>](./jstypedarraytype-enumeration.md)  
*   [<span data-ttu-id="da7d2-138">Перечисление JsValueType</span><span class="sxs-lookup"><span data-stu-id="da7d2-138">JsValueType Enumeration</span></span>](./jsvaluetype-enumeration.md)  

## <span data-ttu-id="da7d2-139">См. также</span><span class="sxs-lookup"><span data-stu-id="da7d2-139">See also</span></span>  

*   [<span data-ttu-id="da7d2-140">Размещение среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="da7d2-140">Hosting the JavaScript Runtime</span></span>](./hosting-the-javascript-runtime.md)  
*   [<span data-ttu-id="da7d2-141">Размещение среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="da7d2-141">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)  

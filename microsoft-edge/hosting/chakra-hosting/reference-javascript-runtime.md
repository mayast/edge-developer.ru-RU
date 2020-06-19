---
description: API среды выполнения JavaScript (JsRT) позволяют добавлять возможности сценариев для настольных и серверных приложений, работающих под управлением Windows.
title: Справочник (среда выполнения JavaScript)
ms.date: 06/08/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 0bfe50da-fd79-4e00-9458-bc667769b415
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 7166e6cd5d64060c2939d8404e1415dc34fce17b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752215"
---
# <span data-ttu-id="ad8b6-103">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ad8b6-103">Reference (JavaScript runtime)</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="ad8b6-104">API среды выполнения JavaScript (JsRT) позволяют добавлять возможности сценариев для настольных и серверных приложений, работающих под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="ad8b6-104">JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.</span></span>  

<span data-ttu-id="ad8b6-105">Если вы планируете внедрить [ChakraCore](https://github.com/Microsoft/ChakraCore) в свое приложение, обратитесь на [ChakraCore вики-сайт](https://aka.ms/corejsrtref) для ссылок на JSRT.</span><span class="sxs-lookup"><span data-stu-id="ad8b6-105">If you intend to embed [ChakraCore](https://github.com/Microsoft/ChakraCore) in your application, please refer to [ChakraCore Wiki](https://aka.ms/corejsrtref) for JSRT references instead.</span></span>  

## <span data-ttu-id="ad8b6-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="ad8b6-106">In this section</span></span>  

<span data-ttu-id="ad8b6-107">Определения typedef, константы и перечисления, поддерживающие размещение JsRT, описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="ad8b6-107">Typedefs, constants, and enumerations that support JsRT hosting are described here:</span></span>  
  
*   [<span data-ttu-id="ad8b6-108">Typedef, константы и перечисления в среде выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="ad8b6-108">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>](./javascript-runtime-typedefs-constants-and-enumerations.md)  

<span data-ttu-id="ad8b6-109">Следующие функции включают размещение JsRT:</span><span class="sxs-lookup"><span data-stu-id="ad8b6-109">The following functions enable JsRT hosting:</span></span>  

*   [<span data-ttu-id="ad8b6-110">Функция JsAddRef</span><span class="sxs-lookup"><span data-stu-id="ad8b6-110">JsAddRef Function</span></span>](./jsaddref-function.md)  
*   [<span data-ttu-id="ad8b6-111">Функция JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="ad8b6-111">JsBooleanToBool Function</span></span>](./jsbooleantobool-function.md)  
*   [<span data-ttu-id="ad8b6-112">Функция JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="ad8b6-112">JsBoolToBoolean Function</span></span>](./jsbooltoboolean-function.md)  
*   [<span data-ttu-id="ad8b6-113">Функция JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="ad8b6-113">JsCallFunction Function</span></span>](./jscallfunction-function.md)  
*   [<span data-ttu-id="ad8b6-114">Функция JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="ad8b6-114">JsCollectGarbage Function</span></span>](./jscollectgarbage-function.md)  
*   [<span data-ttu-id="ad8b6-115">Функция JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="ad8b6-115">JsConstructObject Function</span></span>](./jsconstructobject-function.md)  
*   [<span data-ttu-id="ad8b6-116">Функция JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="ad8b6-116">JsConvertValueToBoolean Function</span></span>](./jsconvertvaluetoboolean-function.md)  
*   [<span data-ttu-id="ad8b6-117">Функция JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="ad8b6-117">JsConvertValueToNumber Function</span></span>](./jsconvertvaluetonumber-function.md)  
*   [<span data-ttu-id="ad8b6-118">Функция JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="ad8b6-118">JsConvertValueToObject Function</span></span>](./jsconvertvaluetoobject-function.md)  
*   [<span data-ttu-id="ad8b6-119">Функция JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="ad8b6-119">JsConvertValueToString Function</span></span>](./jsconvertvaluetostring-function.md)  
*   [<span data-ttu-id="ad8b6-120">Функция JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="ad8b6-120">JsCreateArray Function</span></span>](./jscreatearray-function.md)  
*   [<span data-ttu-id="ad8b6-121">Функция JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="ad8b6-121">JsCreateArrayBuffer Function</span></span>](./jscreatearraybuffer-function.md)  
*   [<span data-ttu-id="ad8b6-122">Функция JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="ad8b6-122">JsCreateContext Function</span></span>](./jscreatecontext-function.md)  
*   [<span data-ttu-id="ad8b6-123">Функция JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="ad8b6-123">JsCreateDataView Function</span></span>](./jscreatedataview-function.md)  
*   [<span data-ttu-id="ad8b6-124">Функция JsCreateError</span><span class="sxs-lookup"><span data-stu-id="ad8b6-124">JsCreateError Function</span></span>](./jscreateerror-function.md)  
*   [<span data-ttu-id="ad8b6-125">Функция JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="ad8b6-125">JsCreateExternalArrayBuffer Function</span></span>](./jscreateexternalarraybuffer-function.md)  
*   [<span data-ttu-id="ad8b6-126">Функция JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="ad8b6-126">JsCreateExternalObject Function</span></span>](./jscreateexternalobject-function.md)  
*   [<span data-ttu-id="ad8b6-127">Функция JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="ad8b6-127">JsCreateFunction Function</span></span>](./jscreatefunction-function.md)  
*   [<span data-ttu-id="ad8b6-128">Функция JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="ad8b6-128">JsCreateNamedFunction Function</span></span>](./jscreatenamedfunction-function.md)  
*   [<span data-ttu-id="ad8b6-129">Функция JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="ad8b6-129">JsCreateObject Function</span></span>](./jscreateobject-function.md)  
*   [<span data-ttu-id="ad8b6-130">Функция JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="ad8b6-130">JsCreateRangeError Function</span></span>](./jscreaterangeerror-function.md)  
*   [<span data-ttu-id="ad8b6-131">Функция JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="ad8b6-131">JsCreateReferenceError Function</span></span>](./jscreatereferenceerror-function.md)  
*   [<span data-ttu-id="ad8b6-132">Функция JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="ad8b6-132">JsCreateRuntime Function</span></span>](./jscreateruntime-function.md)  
*   [<span data-ttu-id="ad8b6-133">Функция JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="ad8b6-133">JsCreateSymbol Function</span></span>](./jscreatesymbol-function.md)  
*   [<span data-ttu-id="ad8b6-134">Функция JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="ad8b6-134">JsCreateSyntaxError Function</span></span>](./jscreatesyntaxerror-function.md)  
*   [<span data-ttu-id="ad8b6-135">Функция JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="ad8b6-135">JsCreateTypeError Function</span></span>](./jscreatetypeerror-function.md)  
*   [<span data-ttu-id="ad8b6-136">Функция JsCreateTypedArray</span><span class="sxs-lookup"><span data-stu-id="ad8b6-136">JsCreateTypedArray Function</span></span>](./jscreatetypedarray-function.md)  
*   [<span data-ttu-id="ad8b6-137">Функция JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="ad8b6-137">JsCreateURIError Function</span></span>](./jscreateurierror-function.md)  
*   [<span data-ttu-id="ad8b6-138">Функция JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-138">JsDefineProperty Function</span></span>](./jsdefineproperty-function.md)  
*   [<span data-ttu-id="ad8b6-139">Функция JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-139">JsDeleteIndexedProperty Function</span></span>](./jsdeleteindexedproperty-function.md)  
*   [<span data-ttu-id="ad8b6-140">Функция JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-140">JsDeleteProperty Function</span></span>](./jsdeleteproperty-function.md)  
*   [<span data-ttu-id="ad8b6-141">Функция JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="ad8b6-141">JsDisableRuntimeExecution Function</span></span>](./jsdisableruntimeexecution-function.md)  
*   [<span data-ttu-id="ad8b6-142">Функция JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="ad8b6-142">JsDisposeRuntime Function</span></span>](./jsdisposeruntime-function.md)  
*   [<span data-ttu-id="ad8b6-143">Функция JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="ad8b6-143">JsDoubleToNumber Function</span></span>](./jsdoubletonumber-function.md)  
*   [<span data-ttu-id="ad8b6-144">Функция JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="ad8b6-144">JsEnableRuntimeExecution Function</span></span>](./jsenableruntimeexecution-function.md)  
*   [<span data-ttu-id="ad8b6-145">Функция JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="ad8b6-145">JsEnumerateHeap Function</span></span>](./jsenumerateheap-function.md)  
*   [<span data-ttu-id="ad8b6-146">Функция JsEquals</span><span class="sxs-lookup"><span data-stu-id="ad8b6-146">JsEquals Function</span></span>](./jsequals-function.md)  
*   [<span data-ttu-id="ad8b6-147">Функция JsGetAndClearException</span><span class="sxs-lookup"><span data-stu-id="ad8b6-147">JsGetAndClearException Function</span></span>](./jsgetandclearexception-function.md)  
*   [<span data-ttu-id="ad8b6-148">Функция JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="ad8b6-148">JsGetArrayBufferStorage Function</span></span>](./jsgetarraybufferstorage-function.md)  
*   [<span data-ttu-id="ad8b6-149">Функция JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="ad8b6-149">JsGetContextData Function</span></span>](./jsgetcontextdata-function.md)  
*   [<span data-ttu-id="ad8b6-150">Функция JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="ad8b6-150">JsGetContextOfObject Function</span></span>](./jsgetcontextofobject-function.md)  
*   [<span data-ttu-id="ad8b6-151">Функция JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="ad8b6-151">JsGetCurrentContext Function</span></span>](./jsgetcurrentcontext-function.md)  
*   [<span data-ttu-id="ad8b6-152">Функция JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="ad8b6-152">JsGetDataViewStorage Function</span></span>](./jsgetdataviewstorage-function.md)  
*   [<span data-ttu-id="ad8b6-153">Функция JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="ad8b6-153">JsGetExtensionAllowed Function</span></span>](./jsgetextensionallowed-function.md)  
*   [<span data-ttu-id="ad8b6-154">Функция JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="ad8b6-154">JsGetExternalData Function</span></span>](./jsgetexternaldata-function.md)  
*   [<span data-ttu-id="ad8b6-155">Функция JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="ad8b6-155">JsGetFalseValue Function</span></span>](./jsgetfalsevalue-function.md)  
*   [<span data-ttu-id="ad8b6-156">Функция JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="ad8b6-156">JsGetGlobalObject Function</span></span>](./jsgetglobalobject-function.md)  
*   [<span data-ttu-id="ad8b6-157">Функция JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="ad8b6-157">JsGetIndexedPropertiesExternalData Function</span></span>](./jsgetindexedpropertiesexternaldata-function.md)  
*   [<span data-ttu-id="ad8b6-158">Функция JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-158">JsGetIndexedProperty Function</span></span>](./jsgetindexedproperty-function.md)  
*   [<span data-ttu-id="ad8b6-159">Функция JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="ad8b6-159">JsGetNullValue Function</span></span>](./jsgetnullvalue-function.md)  
*   [<span data-ttu-id="ad8b6-160">Функция JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="ad8b6-160">JsGetOwnPropertyDescriptor Function</span></span>](./jsgetownpropertydescriptor-function.md)  
*   [<span data-ttu-id="ad8b6-161">Функция JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="ad8b6-161">JsGetOwnPropertyNames Function</span></span>](./jsgetownpropertynames-function.md)  
*   [<span data-ttu-id="ad8b6-162">Функция JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="ad8b6-162">JsGetOwnPropertySymbols Function</span></span>](./jsgetownpropertysymbols-function.md)  
*   [<span data-ttu-id="ad8b6-163">Функция JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-163">JsGetProperty Function</span></span>](./jsgetproperty-function.md)  
*   [<span data-ttu-id="ad8b6-164">Функция JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="ad8b6-164">JsGetPropertyIdFromName Function</span></span>](./jsgetpropertyidfromname-function.md)  
*   [<span data-ttu-id="ad8b6-165">Функция JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="ad8b6-165">JsGetPropertyIdFromSymbol Function</span></span>](./jsgetpropertyidfromsymbol-function.md)  
*   [<span data-ttu-id="ad8b6-166">Функция JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="ad8b6-166">JsGetPropertyIdType Function</span></span>](./jsgetpropertyidtype-function.md)  
*   [<span data-ttu-id="ad8b6-167">Функция JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="ad8b6-167">JsGetPropertyNameFromId Function</span></span>](./jsgetpropertynamefromid-function.md)  
*   [<span data-ttu-id="ad8b6-168">Функция JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="ad8b6-168">JsGetPrototype Function</span></span>](./jsgetprototype-function.md)  
*   [<span data-ttu-id="ad8b6-169">Функция JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="ad8b6-169">JsGetRuntime Function</span></span>](./jsgetruntime-function.md)  
*   [<span data-ttu-id="ad8b6-170">Функция JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="ad8b6-170">JsGetRuntimeMemoryLimit Function</span></span>](./jsgetruntimememorylimit-function.md)  
*   [<span data-ttu-id="ad8b6-171">Функция JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="ad8b6-171">JsGetRuntimeMemoryUsage Function</span></span>](./jsgetruntimememoryusage-function.md)  
*   [<span data-ttu-id="ad8b6-172">Функция JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="ad8b6-172">JsGetStringLength Function</span></span>](./jsgetstringlength-function.md)  
*   [<span data-ttu-id="ad8b6-173">Функция JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="ad8b6-173">JsGetSymbolFromPropertyId Function</span></span>](./jsgetsymbolfrompropertyid-function.md)  
*   [<span data-ttu-id="ad8b6-174">Функция JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="ad8b6-174">JsGetTrueValue Function</span></span>](./jsgettruevalue-function.md)  
*   [<span data-ttu-id="ad8b6-175">Функция JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="ad8b6-175">JsGetTypedArrayInfo Function</span></span>](./jsgettypedarrayinfo-function.md)  
*   [<span data-ttu-id="ad8b6-176">Функция JsGetTypedArrayStorage</span><span class="sxs-lookup"><span data-stu-id="ad8b6-176">JsGetTypedArrayStorage Function</span></span>](./jsgettypedarraystorage-function.md)  
*   [<span data-ttu-id="ad8b6-177">Функция JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="ad8b6-177">JsGetUndefinedValue Function</span></span>](./jsgetundefinedvalue-function.md)  
*   [<span data-ttu-id="ad8b6-178">Функция JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="ad8b6-178">JsGetValueType Function</span></span>](./jsgetvaluetype-function.md)  
*   [<span data-ttu-id="ad8b6-179">Функция JsHasException</span><span class="sxs-lookup"><span data-stu-id="ad8b6-179">JsHasException Function</span></span>](./jshasexception-function.md)  
*   [<span data-ttu-id="ad8b6-180">Функция JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="ad8b6-180">JsHasExternalData Function</span></span>](./jshasexternaldata-function.md)  
*   [<span data-ttu-id="ad8b6-181">Функция JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="ad8b6-181">JsHasIndexedPropertiesExternalData Function</span></span>](./jshasindexedpropertiesexternaldata-function.md)  
*   [<span data-ttu-id="ad8b6-182">Функция JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-182">JsHasIndexedProperty Function</span></span>](./jshasindexedproperty-function.md)  
*   [<span data-ttu-id="ad8b6-183">Функция JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-183">JsHasProperty Function</span></span>](./jshasproperty-function.md)  
*   [<span data-ttu-id="ad8b6-184">Функция JsIdle</span><span class="sxs-lookup"><span data-stu-id="ad8b6-184">JsIdle Function</span></span>](./jsidle-function.md)  
*   [<span data-ttu-id="ad8b6-185">Функция JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="ad8b6-185">JsInspectableToObject Function</span></span>](./jsinspectabletoobject-function.md)  
*   [<span data-ttu-id="ad8b6-186">Функция JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="ad8b6-186">JsInstanceOf Function</span></span>](./jsinstanceof-function.md)  
*   [<span data-ttu-id="ad8b6-187">Функция JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="ad8b6-187">JsIntToNumber Function</span></span>](./jsinttonumber-function.md)  
*   [<span data-ttu-id="ad8b6-188">Функция JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="ad8b6-188">JsIsEnumeratingHeap Function</span></span>](./jsisenumeratingheap-function.md)  
*   [<span data-ttu-id="ad8b6-189">Функция JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="ad8b6-189">JsIsRuntimeExecutionDisabled Function</span></span>](./jsisruntimeexecutiondisabled-function.md)  
*   [<span data-ttu-id="ad8b6-190">Функция JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="ad8b6-190">JsNumberToDouble Function</span></span>](./jsnumbertodouble-function.md)  
*   [<span data-ttu-id="ad8b6-191">Функция JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="ad8b6-191">JsNumberToInt Function</span></span>](./jsnumbertoint-function.md)  
*   [<span data-ttu-id="ad8b6-192">Функция JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="ad8b6-192">JsObjectToInspectable Function</span></span>](./jsobjecttoinspectable-function.md)  
*   [<span data-ttu-id="ad8b6-193">Функция JsParseScript</span><span class="sxs-lookup"><span data-stu-id="ad8b6-193">JsParseScript Function</span></span>](./jsparsescript-function.md)  
*   [<span data-ttu-id="ad8b6-194">Функция JsParseSerializedScript</span><span class="sxs-lookup"><span data-stu-id="ad8b6-194">JsParseSerializedScript Function</span></span>](./jsparseserializedscript-function.md)  
*   [<span data-ttu-id="ad8b6-195">Функция JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="ad8b6-195">JsParseSerializedScriptWithCallback Function</span></span>](./jsparseserializedscriptwithcallback-function.md)  
*   [<span data-ttu-id="ad8b6-196">Функция JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="ad8b6-196">JsPointerToString Function</span></span>](./jspointertostring-function.md)  
*   [<span data-ttu-id="ad8b6-197">Функция JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="ad8b6-197">JsPreventExtension Function</span></span>](./jspreventextension-function.md)  
*   [<span data-ttu-id="ad8b6-198">Функция JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="ad8b6-198">JsProjectWinRTNamespace Function</span></span>](./jsprojectwinrtnamespace-function.md)  
*   [<span data-ttu-id="ad8b6-199">Функция JsRelease</span><span class="sxs-lookup"><span data-stu-id="ad8b6-199">JsRelease Function</span></span>](./jsrelease-function.md)  
*   [<span data-ttu-id="ad8b6-200">Функция JsRunScript</span><span class="sxs-lookup"><span data-stu-id="ad8b6-200">JsRunScript Function</span></span>](./jsrunscript-function.md)  
*   [<span data-ttu-id="ad8b6-201">Функция JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="ad8b6-201">JsRunSerializedScript Function</span></span>](./jsrunserializedscript-function.md)  
*   [<span data-ttu-id="ad8b6-202">Функция JsRunSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="ad8b6-202">JsRunSerializedScriptWithCallback Function</span></span>](./jsrunserializedscriptwithcallback-function.md)  
*   [<span data-ttu-id="ad8b6-203">Функция JsSerializeScript</span><span class="sxs-lookup"><span data-stu-id="ad8b6-203">JsSerializeScript Function</span></span>](./jsserializescript-function.md)  
*   [<span data-ttu-id="ad8b6-204">Функция JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="ad8b6-204">JsSetContextData Function</span></span>](./jssetcontextdata-function.md)  
*   [<span data-ttu-id="ad8b6-205">Функция JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="ad8b6-205">JsSetCurrentContext Function</span></span>](./jssetcurrentcontext-function.md)  
*   [<span data-ttu-id="ad8b6-206">Функция JsSetException</span><span class="sxs-lookup"><span data-stu-id="ad8b6-206">JsSetException Function</span></span>](./jssetexception-function.md)  
*   [<span data-ttu-id="ad8b6-207">Функция JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="ad8b6-207">JsSetExternalData Function</span></span>](./jssetexternaldata-function.md)  
*   [<span data-ttu-id="ad8b6-208">Функция JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="ad8b6-208">JsSetIndexedPropertiesToExternalData Function</span></span>](./jssetindexedpropertiestoexternaldata-function.md)  
*   [<span data-ttu-id="ad8b6-209">Функция JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-209">JsSetIndexedProperty Function</span></span>](./jssetindexedproperty-function.md)  
*   [<span data-ttu-id="ad8b6-210">Функция JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="ad8b6-210">JsSetObjectBeforeCollectCallback Function</span></span>](./jssetobjectbeforecollectcallback-function.md)  
*   [<span data-ttu-id="ad8b6-211">Функция JsSetProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="ad8b6-211">JsSetProjectionEnqueueCallback Function</span></span>](./jssetprojectionenqueuecallback-function.md)  
*   [<span data-ttu-id="ad8b6-212">Функция JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="ad8b6-212">JsSetPromiseContinuationCallback Function</span></span>](./jssetpromisecontinuationcallback-function.md)  
*   [<span data-ttu-id="ad8b6-213">Функция JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="ad8b6-213">JsSetProperty Function</span></span>](./jssetproperty-function.md)  
*   [<span data-ttu-id="ad8b6-214">Функция JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="ad8b6-214">JsSetPrototype Function</span></span>](./jssetprototype-function.md)  
*   [<span data-ttu-id="ad8b6-215">Функция JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="ad8b6-215">JsSetRuntimeBeforeCollectCallback Function</span></span>](./jssetruntimebeforecollectcallback-function.md)  
*   [<span data-ttu-id="ad8b6-216">Функция JsSetRuntimeMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="ad8b6-216">JsSetRuntimeMemoryAllocationCallback Function</span></span>](./jssetruntimememoryallocationcallback-function.md)  
*   [<span data-ttu-id="ad8b6-217">Функция JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="ad8b6-217">JsSetRuntimeMemoryLimit Function</span></span>](./jssetruntimememorylimit-function.md)  
*   [<span data-ttu-id="ad8b6-218">Функция JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="ad8b6-218">JsStartDebugging Function</span></span>](./jsstartdebugging-function.md)  
*   [<span data-ttu-id="ad8b6-219">Функция JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="ad8b6-219">JsStartProfiling Function</span></span>](./jsstartprofiling-function.md)  
*   [<span data-ttu-id="ad8b6-220">Функция JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="ad8b6-220">JsStopProfiling Function</span></span>](./jsstopprofiling-function.md)  
*   [<span data-ttu-id="ad8b6-221">Функция JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="ad8b6-221">JsStrictEquals Function</span></span>](./jsstrictequals-function.md)  
*   [<span data-ttu-id="ad8b6-222">Функция JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="ad8b6-222">JsStringToPointer Function</span></span>](./jsstringtopointer-function.md)  
*   [<span data-ttu-id="ad8b6-223">Функция JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="ad8b6-223">JsValueToVariant Function</span></span>](./jsvaluetovariant-function.md)  
*   [<span data-ttu-id="ad8b6-224">Функция JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="ad8b6-224">JsVariantToValue Function</span></span>](./jsvarianttovalue-function.md)  

## <span data-ttu-id="ad8b6-225">См. также</span><span class="sxs-lookup"><span data-stu-id="ad8b6-225">See also</span></span>  

*   [<span data-ttu-id="ad8b6-226">Размещение среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="ad8b6-226">Hosting the JavaScript Runtime</span></span>](./hosting-the-javascript-runtime.md)  
*   [<span data-ttu-id="ad8b6-227">Размещение среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="ad8b6-227">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)  

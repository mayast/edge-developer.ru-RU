---
description: API среды выполнения JavaScript (JsRT) позволяют добавлять возможности сценариев для настольных и серверных приложений, работающих под управлением Windows.
title: Справочник (среда выполнения JavaScript) | Документы Microsoft
ms.custom: ''
ms.date: 01/15/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0bfe50da-fd79-4e00-9458-bc667769b415
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d1215d84daa31f2338b8c7e237625d0129026bea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571323"
---
# <span data-ttu-id="94430-103">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="94430-103">Reference (JavaScript Runtime)</span></span>
<span data-ttu-id="94430-104">API среды выполнения JavaScript (JsRT) позволяют добавлять возможности сценариев для настольных и серверных приложений, работающих под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="94430-104">JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.</span></span>  
  
 <span data-ttu-id="94430-105">Если вы планируете внедрить [ChakraCore](https://github.com/Microsoft/ChakraCore) в свое приложение, обратитесь на [ChakraCore вики-сайт](https://aka.ms/corejsrtref) для ссылок на JSRT.</span><span class="sxs-lookup"><span data-stu-id="94430-105">If you intend to embed [ChakraCore](https://github.com/Microsoft/ChakraCore) in your application, please refer to [ChakraCore Wiki](https://aka.ms/corejsrtref) for JSRT references instead.</span></span>  
  
## <span data-ttu-id="94430-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="94430-106">In This Section</span></span>  
 <span data-ttu-id="94430-107">Определения typedef, константы и перечисления, поддерживающие размещение JsRT, описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="94430-107">Typedefs, constants, and enumerations that support JsRT hosting are described here:</span></span>  
  
-   [<span data-ttu-id="94430-108">Typedef, константы и перечисления среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="94430-108">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>](../chakra-hosting/javascript-runtime-typedefs-constants-and-enumerations.md)  
  
 <span data-ttu-id="94430-109">Следующие функции включают размещение JsRT:</span><span class="sxs-lookup"><span data-stu-id="94430-109">The following functions enable JsRT hosting:</span></span>  
  
-   [<span data-ttu-id="94430-110">Функция JsAddRef</span><span class="sxs-lookup"><span data-stu-id="94430-110">JsAddRef Function</span></span>](../chakra-hosting/jsaddref-function.md)  
  
-   [<span data-ttu-id="94430-111">Функция JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="94430-111">JsBooleanToBool Function</span></span>](../chakra-hosting/jsbooleantobool-function.md)  
  
-   [<span data-ttu-id="94430-112">Функция JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="94430-112">JsBoolToBoolean Function</span></span>](../chakra-hosting/jsbooltoboolean-function.md)  
  
-   [<span data-ttu-id="94430-113">Функция JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="94430-113">JsCallFunction Function</span></span>](../chakra-hosting/jscallfunction-function.md)  
  
-   [<span data-ttu-id="94430-114">Функция JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="94430-114">JsCollectGarbage Function</span></span>](../chakra-hosting/jscollectgarbage-function.md)  
  
-   [<span data-ttu-id="94430-115">Функция JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="94430-115">JsConstructObject Function</span></span>](../chakra-hosting/jsconstructobject-function.md)  
  
-   [<span data-ttu-id="94430-116">Функция JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="94430-116">JsConvertValueToBoolean Function</span></span>](../chakra-hosting/jsconvertvaluetoboolean-function.md)  
  
-   [<span data-ttu-id="94430-117">Функция JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="94430-117">JsConvertValueToNumber Function</span></span>](../chakra-hosting/jsconvertvaluetonumber-function.md)  
  
-   [<span data-ttu-id="94430-118">Функция JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="94430-118">JsConvertValueToObject Function</span></span>](../chakra-hosting/jsconvertvaluetoobject-function.md)  
  
-   [<span data-ttu-id="94430-119">Функция JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="94430-119">JsConvertValueToString Function</span></span>](../chakra-hosting/jsconvertvaluetostring-function.md)  
  
-   [<span data-ttu-id="94430-120">Функция JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="94430-120">JsCreateArray Function</span></span>](../chakra-hosting/jscreatearray-function.md)  
  
-   [<span data-ttu-id="94430-121">Функция JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="94430-121">JsCreateArrayBuffer Function</span></span>](../chakra-hosting/jscreatearraybuffer-function.md)  
  
-   [<span data-ttu-id="94430-122">Функция JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="94430-122">JsCreateContext Function</span></span>](../chakra-hosting/jscreatecontext-function.md)  
  
-   [<span data-ttu-id="94430-123">Функция JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="94430-123">JsCreateDataView Function</span></span>](../chakra-hosting/jscreatedataview-function.md)  
  
-   [<span data-ttu-id="94430-124">Функция JsCreateError</span><span class="sxs-lookup"><span data-stu-id="94430-124">JsCreateError Function</span></span>](../chakra-hosting/jscreateerror-function.md)  
  
-   [<span data-ttu-id="94430-125">Функция JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="94430-125">JsCreateExternalArrayBuffer Function</span></span>](../chakra-hosting/jscreateexternalarraybuffer-function.md)  
  
-   [<span data-ttu-id="94430-126">Функция JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="94430-126">JsCreateExternalObject Function</span></span>](../chakra-hosting/jscreateexternalobject-function.md)  
  
-   [<span data-ttu-id="94430-127">Функция JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="94430-127">JsCreateFunction Function</span></span>](../chakra-hosting/jscreatefunction-function.md)  
  
-   [<span data-ttu-id="94430-128">Функция JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="94430-128">JsCreateNamedFunction Function</span></span>](../chakra-hosting/jscreatenamedfunction-function.md)  
  
-   [<span data-ttu-id="94430-129">Функция JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="94430-129">JsCreateObject Function</span></span>](../chakra-hosting/jscreateobject-function.md)  
  
-   [<span data-ttu-id="94430-130">Функция JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="94430-130">JsCreateRangeError Function</span></span>](../chakra-hosting/jscreaterangeerror-function.md)  
  
-   [<span data-ttu-id="94430-131">Функция JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="94430-131">JsCreateReferenceError Function</span></span>](../chakra-hosting/jscreatereferenceerror-function.md)  
  
-   [<span data-ttu-id="94430-132">Функция JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="94430-132">JsCreateRuntime Function</span></span>](../chakra-hosting/jscreateruntime-function.md)  
  
-   [<span data-ttu-id="94430-133">Функция JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="94430-133">JsCreateSymbol Function</span></span>](../chakra-hosting/jscreatesymbol-function.md)  
  
-   [<span data-ttu-id="94430-134">Функция JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="94430-134">JsCreateSyntaxError Function</span></span>](../chakra-hosting/jscreatesyntaxerror-function.md)  
  
-   [<span data-ttu-id="94430-135">Функция JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="94430-135">JsCreateTypeError Function</span></span>](../chakra-hosting/jscreatetypeerror-function.md)  
  
-   [<span data-ttu-id="94430-136">Функция JsCreateTypedArray</span><span class="sxs-lookup"><span data-stu-id="94430-136">JsCreateTypedArray Function</span></span>](../chakra-hosting/jscreatetypedarray-function.md)  
  
-   [<span data-ttu-id="94430-137">Функция JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="94430-137">JsCreateURIError Function</span></span>](../chakra-hosting/jscreateurierror-function.md)  
  
-   [<span data-ttu-id="94430-138">Функция JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="94430-138">JsDefineProperty Function</span></span>](../chakra-hosting/jsdefineproperty-function.md)  
  
-   [<span data-ttu-id="94430-139">Функция JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="94430-139">JsDeleteIndexedProperty Function</span></span>](../chakra-hosting/jsdeleteindexedproperty-function.md)  
  
-   [<span data-ttu-id="94430-140">Функция JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="94430-140">JsDeleteProperty Function</span></span>](../chakra-hosting/jsdeleteproperty-function.md)  
  
-   [<span data-ttu-id="94430-141">Функция JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="94430-141">JsDisableRuntimeExecution Function</span></span>](../chakra-hosting/jsdisableruntimeexecution-function.md)  
  
-   [<span data-ttu-id="94430-142">Функция JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="94430-142">JsDisposeRuntime Function</span></span>](../chakra-hosting/jsdisposeruntime-function.md)  
  
-   [<span data-ttu-id="94430-143">Функция JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="94430-143">JsDoubleToNumber Function</span></span>](../chakra-hosting/jsdoubletonumber-function.md)  
  
-   [<span data-ttu-id="94430-144">Функция JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="94430-144">JsEnableRuntimeExecution Function</span></span>](../chakra-hosting/jsenableruntimeexecution-function.md)  
  
-   [<span data-ttu-id="94430-145">Функция JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="94430-145">JsEnumerateHeap Function</span></span>](../chakra-hosting/jsenumerateheap-function.md)  
  
-   [<span data-ttu-id="94430-146">Функция JsEquals</span><span class="sxs-lookup"><span data-stu-id="94430-146">JsEquals Function</span></span>](../chakra-hosting/jsequals-function.md)  
  
-   [<span data-ttu-id="94430-147">Функция JsGetAndClearException</span><span class="sxs-lookup"><span data-stu-id="94430-147">JsGetAndClearException Function</span></span>](../chakra-hosting/jsgetandclearexception-function.md)  
  
-   [<span data-ttu-id="94430-148">Функция JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="94430-148">JsGetArrayBufferStorage Function</span></span>](../chakra-hosting/jsgetarraybufferstorage-function.md)  
  
-   [<span data-ttu-id="94430-149">Функция JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="94430-149">JsGetContextData Function</span></span>](../chakra-hosting/jsgetcontextdata-function.md)  
  
-   [<span data-ttu-id="94430-150">Функция JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="94430-150">JsGetContextOfObject Function</span></span>](../chakra-hosting/jsgetcontextofobject-function.md)  
  
-   [<span data-ttu-id="94430-151">Функция JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="94430-151">JsGetCurrentContext Function</span></span>](../chakra-hosting/jsgetcurrentcontext-function.md)  
  
-   [<span data-ttu-id="94430-152">Функция JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="94430-152">JsGetDataViewStorage Function</span></span>](../chakra-hosting/jsgetdataviewstorage-function.md)  
  
-   [<span data-ttu-id="94430-153">Функция JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="94430-153">JsGetExtensionAllowed Function</span></span>](../chakra-hosting/jsgetextensionallowed-function.md)  
  
-   [<span data-ttu-id="94430-154">Функция JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="94430-154">JsGetExternalData Function</span></span>](../chakra-hosting/jsgetexternaldata-function.md)  
  
-   [<span data-ttu-id="94430-155">Функция JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="94430-155">JsGetFalseValue Function</span></span>](../chakra-hosting/jsgetfalsevalue-function.md)  
  
-   [<span data-ttu-id="94430-156">Функция JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="94430-156">JsGetGlobalObject Function</span></span>](../chakra-hosting/jsgetglobalobject-function.md)  
  
-   [<span data-ttu-id="94430-157">Функция JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="94430-157">JsGetIndexedPropertiesExternalData Function</span></span>](../chakra-hosting/jsgetindexedpropertiesexternaldata-function.md)  
  
-   [<span data-ttu-id="94430-158">Функция JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="94430-158">JsGetIndexedProperty Function</span></span>](../chakra-hosting/jsgetindexedproperty-function.md)  
  
-   [<span data-ttu-id="94430-159">Функция JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="94430-159">JsGetNullValue Function</span></span>](../chakra-hosting/jsgetnullvalue-function.md)  
  
-   [<span data-ttu-id="94430-160">Функция JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="94430-160">JsGetOwnPropertyDescriptor Function</span></span>](../chakra-hosting/jsgetownpropertydescriptor-function.md)  
  
-   [<span data-ttu-id="94430-161">Функция JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="94430-161">JsGetOwnPropertyNames Function</span></span>](../chakra-hosting/jsgetownpropertynames-function.md)  
  
-   [<span data-ttu-id="94430-162">Функция JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="94430-162">JsGetOwnPropertySymbols Function</span></span>](../chakra-hosting/jsgetownpropertysymbols-function.md)  
  
-   [<span data-ttu-id="94430-163">Функция JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="94430-163">JsGetProperty Function</span></span>](../chakra-hosting/jsgetproperty-function.md)  
  
-   [<span data-ttu-id="94430-164">Функция JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="94430-164">JsGetPropertyIdFromName Function</span></span>](../chakra-hosting/jsgetpropertyidfromname-function.md)  
  
-   [<span data-ttu-id="94430-165">Функция JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="94430-165">JsGetPropertyIdFromSymbol Function</span></span>](../chakra-hosting/jsgetpropertyidfromsymbol-function.md)  
  
-   [<span data-ttu-id="94430-166">Функция JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="94430-166">JsGetPropertyIdType Function</span></span>](../chakra-hosting/jsgetpropertyidtype-function.md)  
  
-   [<span data-ttu-id="94430-167">Функция JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="94430-167">JsGetPropertyNameFromId Function</span></span>](../chakra-hosting/jsgetpropertynamefromid-function.md)  
  
-   [<span data-ttu-id="94430-168">Функция JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="94430-168">JsGetPrototype Function</span></span>](../chakra-hosting/jsgetprototype-function.md)  
  
-   [<span data-ttu-id="94430-169">Функция JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="94430-169">JsGetRuntime Function</span></span>](../chakra-hosting/jsgetruntime-function.md)  
  
-   [<span data-ttu-id="94430-170">Функция JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="94430-170">JsGetRuntimeMemoryLimit Function</span></span>](../chakra-hosting/jsgetruntimememorylimit-function.md)  
  
-   [<span data-ttu-id="94430-171">Функция JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="94430-171">JsGetRuntimeMemoryUsage Function</span></span>](../chakra-hosting/jsgetruntimememoryusage-function.md)  
  
-   [<span data-ttu-id="94430-172">Функция JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="94430-172">JsGetStringLength Function</span></span>](../chakra-hosting/jsgetstringlength-function.md)  
  
-   [<span data-ttu-id="94430-173">Функция JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="94430-173">JsGetSymbolFromPropertyId Function</span></span>](../chakra-hosting/jsgetsymbolfrompropertyid-function.md)  
  
-   [<span data-ttu-id="94430-174">Функция JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="94430-174">JsGetTrueValue Function</span></span>](../chakra-hosting/jsgettruevalue-function.md)  
  
-   [<span data-ttu-id="94430-175">Функция JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="94430-175">JsGetTypedArrayInfo Function</span></span>](../chakra-hosting/jsgettypedarrayinfo-function.md)  
  
-   [<span data-ttu-id="94430-176">Функция JsGetTypedArrayStorage</span><span class="sxs-lookup"><span data-stu-id="94430-176">JsGetTypedArrayStorage Function</span></span>](../chakra-hosting/jsgettypedarraystorage-function.md)  
  
-   [<span data-ttu-id="94430-177">Функция JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="94430-177">JsGetUndefinedValue Function</span></span>](../chakra-hosting/jsgetundefinedvalue-function.md)  
  
-   [<span data-ttu-id="94430-178">Функция JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="94430-178">JsGetValueType Function</span></span>](../chakra-hosting/jsgetvaluetype-function.md)  
  
-   [<span data-ttu-id="94430-179">Функция JsHasException</span><span class="sxs-lookup"><span data-stu-id="94430-179">JsHasException Function</span></span>](../chakra-hosting/jshasexception-function.md)  
  
-   [<span data-ttu-id="94430-180">Функция JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="94430-180">JsHasExternalData Function</span></span>](../chakra-hosting/jshasexternaldata-function.md)  
  
-   [<span data-ttu-id="94430-181">Функция JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="94430-181">JsHasIndexedPropertiesExternalData Function</span></span>](../chakra-hosting/jshasindexedpropertiesexternaldata-function.md)  
  
-   [<span data-ttu-id="94430-182">Функция JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="94430-182">JsHasIndexedProperty Function</span></span>](../chakra-hosting/jshasindexedproperty-function.md)  
  
-   [<span data-ttu-id="94430-183">Функция JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="94430-183">JsHasProperty Function</span></span>](../chakra-hosting/jshasproperty-function.md)  
  
-   [<span data-ttu-id="94430-184">Функция JsIdle</span><span class="sxs-lookup"><span data-stu-id="94430-184">JsIdle Function</span></span>](../chakra-hosting/jsidle-function.md)  
  
-   [<span data-ttu-id="94430-185">Функция JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="94430-185">JsInspectableToObject Function</span></span>](../chakra-hosting/jsinspectabletoobject-function.md)  
  
-   [<span data-ttu-id="94430-186">Функция JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="94430-186">JsInstanceOf Function</span></span>](../chakra-hosting/jsinstanceof-function.md)  
  
-   [<span data-ttu-id="94430-187">Функция JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="94430-187">JsIntToNumber Function</span></span>](../chakra-hosting/jsinttonumber-function.md)  
  
-   [<span data-ttu-id="94430-188">Функция JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="94430-188">JsIsEnumeratingHeap Function</span></span>](../chakra-hosting/jsisenumeratingheap-function.md)  
  
-   [<span data-ttu-id="94430-189">Функция JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="94430-189">JsIsRuntimeExecutionDisabled Function</span></span>](../chakra-hosting/jsisruntimeexecutiondisabled-function.md)  
  
-   [<span data-ttu-id="94430-190">Функция JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="94430-190">JsNumberToDouble Function</span></span>](../chakra-hosting/jsnumbertodouble-function.md)  
  
-   [<span data-ttu-id="94430-191">Функция JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="94430-191">JsNumberToInt Function</span></span>](../chakra-hosting/jsnumbertoint-function.md)  
  
-   [<span data-ttu-id="94430-192">Функция JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="94430-192">JsObjectToInspectable Function</span></span>](../chakra-hosting/jsobjecttoinspectable-function.md)  
  
-   [<span data-ttu-id="94430-193">Функция JsParseScript</span><span class="sxs-lookup"><span data-stu-id="94430-193">JsParseScript Function</span></span>](../chakra-hosting/jsparsescript-function.md)  
  
-   [<span data-ttu-id="94430-194">Функция JsParseSerializedScript</span><span class="sxs-lookup"><span data-stu-id="94430-194">JsParseSerializedScript Function</span></span>](../chakra-hosting/jsparseserializedscript-function.md)  
  
-   [<span data-ttu-id="94430-195">Функция JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="94430-195">JsParseSerializedScriptWithCallback Function</span></span>](../chakra-hosting/jsparseserializedscriptwithcallback-function.md)  
  
-   [<span data-ttu-id="94430-196">Функция JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="94430-196">JsPointerToString Function</span></span>](../chakra-hosting/jspointertostring-function.md)  
  
-   [<span data-ttu-id="94430-197">Функция JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="94430-197">JsPreventExtension Function</span></span>](../chakra-hosting/jspreventextension-function.md)  
  
-   [<span data-ttu-id="94430-198">Функция JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="94430-198">JsProjectWinRTNamespace Function</span></span>](../chakra-hosting/jsprojectwinrtnamespace-function.md)  
  
-   [<span data-ttu-id="94430-199">Функция JsRelease</span><span class="sxs-lookup"><span data-stu-id="94430-199">JsRelease Function</span></span>](../chakra-hosting/jsrelease-function.md)  
  
-   [<span data-ttu-id="94430-200">Функция JsRunScript</span><span class="sxs-lookup"><span data-stu-id="94430-200">JsRunScript Function</span></span>](../chakra-hosting/jsrunscript-function.md)  
  
-   [<span data-ttu-id="94430-201">Функция JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="94430-201">JsRunSerializedScript Function</span></span>](../chakra-hosting/jsrunserializedscript-function.md)  
  
-   [<span data-ttu-id="94430-202">Функция JsRunSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="94430-202">JsRunSerializedScriptWithCallback Function</span></span>](../chakra-hosting/jsrunserializedscriptwithcallback-function.md)  
  
-   [<span data-ttu-id="94430-203">Функция JsSerializeScript</span><span class="sxs-lookup"><span data-stu-id="94430-203">JsSerializeScript Function</span></span>](../chakra-hosting/jsserializescript-function.md)  
  
-   [<span data-ttu-id="94430-204">Функция JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="94430-204">JsSetContextData Function</span></span>](../chakra-hosting/jssetcontextdata-function.md)  
  
-   [<span data-ttu-id="94430-205">Функция JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="94430-205">JsSetCurrentContext Function</span></span>](../chakra-hosting/jssetcurrentcontext-function.md)  
  
-   [<span data-ttu-id="94430-206">Функция JsSetException</span><span class="sxs-lookup"><span data-stu-id="94430-206">JsSetException Function</span></span>](../chakra-hosting/jssetexception-function.md)  
  
-   [<span data-ttu-id="94430-207">Функция JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="94430-207">JsSetExternalData Function</span></span>](../chakra-hosting/jssetexternaldata-function.md)  
  
-   [<span data-ttu-id="94430-208">Функция JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="94430-208">JsSetIndexedPropertiesToExternalData Function</span></span>](../chakra-hosting/jssetindexedpropertiestoexternaldata-function.md)  
  
-   [<span data-ttu-id="94430-209">Функция JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="94430-209">JsSetIndexedProperty Function</span></span>](../chakra-hosting/jssetindexedproperty-function.md)  
  
-   [<span data-ttu-id="94430-210">Функция JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="94430-210">JsSetObjectBeforeCollectCallback Function</span></span>](../chakra-hosting/jssetobjectbeforecollectcallback-function.md)  
  
-   [<span data-ttu-id="94430-211">Функция JsSetProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="94430-211">JsSetProjectionEnqueueCallback Function</span></span>](../chakra-hosting/jssetprojectionenqueuecallback-function.md)  
  
-   [<span data-ttu-id="94430-212">Функция JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="94430-212">JsSetPromiseContinuationCallback Function</span></span>](../chakra-hosting/jssetpromisecontinuationcallback-function.md)  
  
-   [<span data-ttu-id="94430-213">Функция JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="94430-213">JsSetProperty Function</span></span>](../chakra-hosting/jssetproperty-function.md)  
  
-   [<span data-ttu-id="94430-214">Функция JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="94430-214">JsSetPrototype Function</span></span>](../chakra-hosting/jssetprototype-function.md)  
  
-   [<span data-ttu-id="94430-215">Функция JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="94430-215">JsSetRuntimeBeforeCollectCallback Function</span></span>](../chakra-hosting/jssetruntimebeforecollectcallback-function.md)  
  
-   [<span data-ttu-id="94430-216">Функция JsSetRuntimeMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="94430-216">JsSetRuntimeMemoryAllocationCallback Function</span></span>](../chakra-hosting/jssetruntimememoryallocationcallback-function.md)  
  
-   [<span data-ttu-id="94430-217">Функция JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="94430-217">JsSetRuntimeMemoryLimit Function</span></span>](../chakra-hosting/jssetruntimememorylimit-function.md)  
  
-   [<span data-ttu-id="94430-218">Функция JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="94430-218">JsStartDebugging Function</span></span>](../chakra-hosting/jsstartdebugging-function.md)  
  
-   [<span data-ttu-id="94430-219">Функция JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="94430-219">JsStartProfiling Function</span></span>](../chakra-hosting/jsstartprofiling-function.md)  
  
-   [<span data-ttu-id="94430-220">Функция JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="94430-220">JsStopProfiling Function</span></span>](../chakra-hosting/jsstopprofiling-function.md)  
  
-   [<span data-ttu-id="94430-221">Функция JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="94430-221">JsStrictEquals Function</span></span>](../chakra-hosting/jsstrictequals-function.md)  
  
-   [<span data-ttu-id="94430-222">Функция JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="94430-222">JsStringToPointer Function</span></span>](../chakra-hosting/jsstringtopointer-function.md)  
  
-   [<span data-ttu-id="94430-223">Функция JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="94430-223">JsValueToVariant Function</span></span>](../chakra-hosting/jsvaluetovariant-function.md)  
  
-   [<span data-ttu-id="94430-224">Функция JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="94430-224">JsVariantToValue Function</span></span>](../chakra-hosting/jsvarianttovalue-function.md)  
  
## <span data-ttu-id="94430-225">См. также</span><span class="sxs-lookup"><span data-stu-id="94430-225">See Also</span></span>  
 [<span data-ttu-id="94430-226">Размещение среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="94430-226">Hosting the JavaScript Runtime</span></span>](../chakra-hosting/hosting-the-javascript-runtime.md)   
 [<span data-ttu-id="94430-227">Размещение среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="94430-227">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)
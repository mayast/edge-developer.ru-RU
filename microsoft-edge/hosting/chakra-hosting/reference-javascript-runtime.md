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
# Справочник (среда выполнения JavaScript)  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

API среды выполнения JavaScript (JsRT) позволяют добавлять возможности сценариев для настольных и серверных приложений, работающих под управлением Windows.  

Если вы планируете внедрить [ChakraCore](https://github.com/Microsoft/ChakraCore) в свое приложение, обратитесь на [ChakraCore вики-сайт](https://aka.ms/corejsrtref) для ссылок на JSRT.  

## В этом разделе  

Определения typedef, константы и перечисления, поддерживающие размещение JsRT, описаны ниже.  
  
*   [Typedef, константы и перечисления в среде выполнения JavaScript](./javascript-runtime-typedefs-constants-and-enumerations.md)  

Следующие функции включают размещение JsRT:  

*   [Функция JsAddRef](./jsaddref-function.md)  
*   [Функция JsBooleanToBool](./jsbooleantobool-function.md)  
*   [Функция JsBoolToBoolean](./jsbooltoboolean-function.md)  
*   [Функция JsCallFunction](./jscallfunction-function.md)  
*   [Функция JsCollectGarbage](./jscollectgarbage-function.md)  
*   [Функция JsConstructObject](./jsconstructobject-function.md)  
*   [Функция JsConvertValueToBoolean](./jsconvertvaluetoboolean-function.md)  
*   [Функция JsConvertValueToNumber](./jsconvertvaluetonumber-function.md)  
*   [Функция JsConvertValueToObject](./jsconvertvaluetoobject-function.md)  
*   [Функция JsConvertValueToString](./jsconvertvaluetostring-function.md)  
*   [Функция JsCreateArray](./jscreatearray-function.md)  
*   [Функция JsCreateArrayBuffer](./jscreatearraybuffer-function.md)  
*   [Функция JsCreateContext](./jscreatecontext-function.md)  
*   [Функция JsCreateDataView](./jscreatedataview-function.md)  
*   [Функция JsCreateError](./jscreateerror-function.md)  
*   [Функция JsCreateExternalArrayBuffer](./jscreateexternalarraybuffer-function.md)  
*   [Функция JsCreateExternalObject](./jscreateexternalobject-function.md)  
*   [Функция JsCreateFunction](./jscreatefunction-function.md)  
*   [Функция JsCreateNamedFunction](./jscreatenamedfunction-function.md)  
*   [Функция JsCreateObject](./jscreateobject-function.md)  
*   [Функция JsCreateRangeError](./jscreaterangeerror-function.md)  
*   [Функция JsCreateReferenceError](./jscreatereferenceerror-function.md)  
*   [Функция JsCreateRuntime](./jscreateruntime-function.md)  
*   [Функция JsCreateSymbol](./jscreatesymbol-function.md)  
*   [Функция JsCreateSyntaxError](./jscreatesyntaxerror-function.md)  
*   [Функция JsCreateTypeError](./jscreatetypeerror-function.md)  
*   [Функция JsCreateTypedArray](./jscreatetypedarray-function.md)  
*   [Функция JsCreateURIError](./jscreateurierror-function.md)  
*   [Функция JsDefineProperty](./jsdefineproperty-function.md)  
*   [Функция JsDeleteIndexedProperty](./jsdeleteindexedproperty-function.md)  
*   [Функция JsDeleteProperty](./jsdeleteproperty-function.md)  
*   [Функция JsDisableRuntimeExecution](./jsdisableruntimeexecution-function.md)  
*   [Функция JsDisposeRuntime](./jsdisposeruntime-function.md)  
*   [Функция JsDoubleToNumber](./jsdoubletonumber-function.md)  
*   [Функция JsEnableRuntimeExecution](./jsenableruntimeexecution-function.md)  
*   [Функция JsEnumerateHeap](./jsenumerateheap-function.md)  
*   [Функция JsEquals](./jsequals-function.md)  
*   [Функция JsGetAndClearException](./jsgetandclearexception-function.md)  
*   [Функция JsGetArrayBufferStorage](./jsgetarraybufferstorage-function.md)  
*   [Функция JsGetContextData](./jsgetcontextdata-function.md)  
*   [Функция JsGetContextOfObject](./jsgetcontextofobject-function.md)  
*   [Функция JsGetCurrentContext](./jsgetcurrentcontext-function.md)  
*   [Функция JsGetDataViewStorage](./jsgetdataviewstorage-function.md)  
*   [Функция JsGetExtensionAllowed](./jsgetextensionallowed-function.md)  
*   [Функция JsGetExternalData](./jsgetexternaldata-function.md)  
*   [Функция JsGetFalseValue](./jsgetfalsevalue-function.md)  
*   [Функция JsGetGlobalObject](./jsgetglobalobject-function.md)  
*   [Функция JsGetIndexedPropertiesExternalData](./jsgetindexedpropertiesexternaldata-function.md)  
*   [Функция JsGetIndexedProperty](./jsgetindexedproperty-function.md)  
*   [Функция JsGetNullValue](./jsgetnullvalue-function.md)  
*   [Функция JsGetOwnPropertyDescriptor](./jsgetownpropertydescriptor-function.md)  
*   [Функция JsGetOwnPropertyNames](./jsgetownpropertynames-function.md)  
*   [Функция JsGetOwnPropertySymbols](./jsgetownpropertysymbols-function.md)  
*   [Функция JsGetProperty](./jsgetproperty-function.md)  
*   [Функция JsGetPropertyIdFromName](./jsgetpropertyidfromname-function.md)  
*   [Функция JsGetPropertyIdFromSymbol](./jsgetpropertyidfromsymbol-function.md)  
*   [Функция JsGetPropertyIdType](./jsgetpropertyidtype-function.md)  
*   [Функция JsGetPropertyNameFromId](./jsgetpropertynamefromid-function.md)  
*   [Функция JsGetPrototype](./jsgetprototype-function.md)  
*   [Функция JsGetRuntime](./jsgetruntime-function.md)  
*   [Функция JsGetRuntimeMemoryLimit](./jsgetruntimememorylimit-function.md)  
*   [Функция JsGetRuntimeMemoryUsage](./jsgetruntimememoryusage-function.md)  
*   [Функция JsGetStringLength](./jsgetstringlength-function.md)  
*   [Функция JsGetSymbolFromPropertyId](./jsgetsymbolfrompropertyid-function.md)  
*   [Функция JsGetTrueValue](./jsgettruevalue-function.md)  
*   [Функция JsGetTypedArrayInfo](./jsgettypedarrayinfo-function.md)  
*   [Функция JsGetTypedArrayStorage](./jsgettypedarraystorage-function.md)  
*   [Функция JsGetUndefinedValue](./jsgetundefinedvalue-function.md)  
*   [Функция JsGetValueType](./jsgetvaluetype-function.md)  
*   [Функция JsHasException](./jshasexception-function.md)  
*   [Функция JsHasExternalData](./jshasexternaldata-function.md)  
*   [Функция JsHasIndexedPropertiesExternalData](./jshasindexedpropertiesexternaldata-function.md)  
*   [Функция JsHasIndexedProperty](./jshasindexedproperty-function.md)  
*   [Функция JsHasProperty](./jshasproperty-function.md)  
*   [Функция JsIdle](./jsidle-function.md)  
*   [Функция JsInspectableToObject](./jsinspectabletoobject-function.md)  
*   [Функция JsInstanceOf](./jsinstanceof-function.md)  
*   [Функция JsIntToNumber](./jsinttonumber-function.md)  
*   [Функция JsIsEnumeratingHeap](./jsisenumeratingheap-function.md)  
*   [Функция JsIsRuntimeExecutionDisabled](./jsisruntimeexecutiondisabled-function.md)  
*   [Функция JsNumberToDouble](./jsnumbertodouble-function.md)  
*   [Функция JsNumberToInt](./jsnumbertoint-function.md)  
*   [Функция JsObjectToInspectable](./jsobjecttoinspectable-function.md)  
*   [Функция JsParseScript](./jsparsescript-function.md)  
*   [Функция JsParseSerializedScript](./jsparseserializedscript-function.md)  
*   [Функция JsParseSerializedScriptWithCallback](./jsparseserializedscriptwithcallback-function.md)  
*   [Функция JsPointerToString](./jspointertostring-function.md)  
*   [Функция JsPreventExtension](./jspreventextension-function.md)  
*   [Функция JsProjectWinRTNamespace](./jsprojectwinrtnamespace-function.md)  
*   [Функция JsRelease](./jsrelease-function.md)  
*   [Функция JsRunScript](./jsrunscript-function.md)  
*   [Функция JsRunSerializedScript](./jsrunserializedscript-function.md)  
*   [Функция JsRunSerializedScriptWithCallback](./jsrunserializedscriptwithcallback-function.md)  
*   [Функция JsSerializeScript](./jsserializescript-function.md)  
*   [Функция JsSetContextData](./jssetcontextdata-function.md)  
*   [Функция JsSetCurrentContext](./jssetcurrentcontext-function.md)  
*   [Функция JsSetException](./jssetexception-function.md)  
*   [Функция JsSetExternalData](./jssetexternaldata-function.md)  
*   [Функция JsSetIndexedPropertiesToExternalData](./jssetindexedpropertiestoexternaldata-function.md)  
*   [Функция JsSetIndexedProperty](./jssetindexedproperty-function.md)  
*   [Функция JsSetObjectBeforeCollectCallback](./jssetobjectbeforecollectcallback-function.md)  
*   [Функция JsSetProjectionEnqueueCallback](./jssetprojectionenqueuecallback-function.md)  
*   [Функция JsSetPromiseContinuationCallback](./jssetpromisecontinuationcallback-function.md)  
*   [Функция JsSetProperty](./jssetproperty-function.md)  
*   [Функция JsSetPrototype](./jssetprototype-function.md)  
*   [Функция JsSetRuntimeBeforeCollectCallback](./jssetruntimebeforecollectcallback-function.md)  
*   [Функция JsSetRuntimeMemoryAllocationCallback](./jssetruntimememoryallocationcallback-function.md)  
*   [Функция JsSetRuntimeMemoryLimit](./jssetruntimememorylimit-function.md)  
*   [Функция JsStartDebugging](./jsstartdebugging-function.md)  
*   [Функция JsStartProfiling](./jsstartprofiling-function.md)  
*   [Функция JsStopProfiling](./jsstopprofiling-function.md)  
*   [Функция JsStrictEquals](./jsstrictequals-function.md)  
*   [Функция JsStringToPointer](./jsstringtopointer-function.md)  
*   [Функция JsValueToVariant](./jsvaluetovariant-function.md)  
*   [Функция JsVariantToValue](./jsvarianttovalue-function.md)  

## См. также  

*   [Размещение среды выполнения JavaScript](./hosting-the-javascript-runtime.md)  
*   [Размещение среды выполнения JavaScript](../javascript-runtime-hosting.md)  

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
# Перечисление JsErrorCode
Код ошибки, возвращенный API размещения Chakra.  
  
## Синтаксис  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## Участников  
  
### Данные  
  
|Имя|Описание|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|Контекст нельзя перевести в состояние отладки, так как он уже находится в состоянии отладки.|  
|`JsErrorAlreadyProfilingContext`|Профилирование не может быть запущено, так как оно уже является профилированием.|  
|`JsErrorArgumentNotObject`|API размещения, работающий с значениями объекта, вызывался с использованием значения, не являющегося объектом.|  
|`JsErrorBadSerializedScript`|Использован недопустимый сериализованный сценарий либо сериализованный сценарий был сериализован в другой версии обработчика Chakra.|  
|`JsErrorCannotDisableExecution`|Среда выполнения не поддерживает ненадежное прерывание сценария.|  
|`JsErrorCannotSerializeDebugScript`|Невозможно сериализовать сценарии в контекстах отладки.|  
|`JsErrorCategoryEngine`|Категория ошибок, связанных с ошибками, происходящими в самом ядре.|  
|`JsErrorCategoryFatal`|Категория ошибок, которые являются неустранимыми и обозначают сбой обработчика.|  
|`JsErrorCategoryScript`|Категория ошибок, связанных с ошибками в сценарии.|  
|`JsErrorCategoryUsage`|Категория ошибок, связанных с неправильным использованием самого API.|  
|`JsErrorFatal`|Произошла неустранимая ошибка в обработчике.|  
|`JsErrorHeapEnumInProgress`|В данный момент выполняется перечисление кучи в контексте сценария.|  
|`JsErrorIdleNotEnabled`|Уведомление о недодействии, предопределенное, когда узел не сделал обработку на время бездействия.|  
|`JsErrorInDisabledState`|Среда выполнения находится в отключенном состоянии.|  
|`JsErrorInExceptionState`|Обработчик находится в состоянии исключения, и никакие API невозможно вызвать, пока не будет очищено исключение.|  
|`JsErrorInObjectBeforeCollectCallback`|Перед тем как приступить к сбору обратного вызова, операция не поддерживается в объекте.<br /><br /> Это значение перечисления поддерживается только в режиме Microsoft Edge.|  
|`JsErrorInProfileCallback`|Контекст сценария входит в середину обратного вызова профиля.|  
|`JsErrorInThreadServiceCallback`|Обратный вызов службы Threading в настоящее время выполняется.|  
|`JsErrorInvalidArgument`|Недопустимый аргумент для API размещения.|  
|`JsErrorNoCurrentContext`|Для API размещения требуется, чтобы контекст был текущим, но текущий контекст отсутствует.|  
|`JsErrorNotImplemented`|API размещения пока не реализован.|  
|`JsErrorNullArgument`|Аргумент API размещения имеет значение NULL в контексте, где значение NULL не разрешено.|  
|`JsErrorObjectNotInspectable`|Не удается распаковать объект в `IInspectable` указатель.<br /><br /> Это значение перечисления поддерживается только в режиме Microsoft Edge.|  
|`JsErrorOutOfMemory`|Недостаточно памяти для работы модуля Chakra.|  
|`JsErrorPropertyNotSymbol`|API размещения, который работает с идентификаторами свойств символов, но был вызван с идентификатором свойства, не являющимся символом. Код ошибки возвращается в `JsGetSymbolFromPropertyId` том случае, если функция вызывается с идентификатором свойства, не являющимся символом.<br /><br /> Это значение перечисления поддерживается только в режиме Microsoft Edge.|  
|`JsErrorPropertyNotString`|API размещения, работающий с идентификаторами строковых свойств, но вызванный идентификатором нестрокового свойства. Код ошибки возвращается функцией existing, `JsGetPropertyNamefromId` Если функция вызывается с идентификатором нестрокового свойства.<br /><br /> Это значение перечисления поддерживается только в режиме Microsoft Edge.|  
|`JsErrorRuntimeInUse`|Среда выполнения, которая все еще используется, не может быть удалена.|  
|`JsErrorScriptCompile`|Не удалось выполнить компиляцию JavaScript.|  
|`JsErrorScriptEvalDisabled`|Сценарий был завершен, так как он попытался использовать, `eval` `function` а функция eval была отключена.|  
|`JsErrorScriptException`|При выполнении сценария возникло исключение JavaScript.|  
|`JsErrorScriptTerminated`|Сценарий был завершен из-за запроса на приостановку выполнения.|  
|`JsErrorWrongRuntime`|API размещения вызвал объект, созданный в другой среде выполнения JavaScript.|  
|`JsErrorWrongThread`|API размещения был вызван в неправильном потоке.|  
|`JsNoError`|Код ошибки при успешном выполнении.|  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
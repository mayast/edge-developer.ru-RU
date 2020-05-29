---
description: Возвращает исключение, которое привело к тому, что среда выполнения текущего контекста находится в состоянии исключения, и сбрасывает состояние исключения для этой среды выполнения.
title: Функция JsGetAndClearException | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: eb70b4b66b4bb270d9f26487708720efddc2effa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572532"
---
# <span data-ttu-id="283dc-103">Функция JsGetAndClearException</span><span class="sxs-lookup"><span data-stu-id="283dc-103">JsGetAndClearException Function</span></span>
<span data-ttu-id="283dc-104">Возвращает исключение, которое привело к тому, что среда выполнения текущего контекста находится в состоянии исключения, и сбрасывает состояние исключения для этой среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="283dc-104">Returns the exception that caused the runtime of the current context to be in the exception state and resets the exception state for that runtime.</span></span>  
  
## <span data-ttu-id="283dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="283dc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### <span data-ttu-id="283dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="283dc-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="283dc-107">Исключение для среды выполнения текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="283dc-107">The exception for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="283dc-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="283dc-108">Return Value</span></span>  
 <span data-ttu-id="283dc-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="283dc-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="283dc-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="283dc-110">Remarks</span></span>  
 <span data-ttu-id="283dc-111">Если среда выполнения текущего контекста не находится в состоянии исключения, этот API будет возвращен `JsErrorInvalidArgument` .</span><span class="sxs-lookup"><span data-stu-id="283dc-111">If the runtime of the current context is not in an exception state, this API will return `JsErrorInvalidArgument`.</span></span> <span data-ttu-id="283dc-112">Если среда выполнения отключена, будет возвращено исключение, указывающее на то, что сценарий был завершен, но не будет очищать это исключение (исключение будет очищено, если среда выполнения повторно включена с помощью `JsEnableRuntimeExecution` ).</span><span class="sxs-lookup"><span data-stu-id="283dc-112">If the runtime is disabled, this will return an exception indicating that the script was terminated, but it will not clear the exception (the exception will be cleared if the runtime is re-enabled using `JsEnableRuntimeExecution`).</span></span>  
  
 <span data-ttu-id="283dc-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="283dc-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="283dc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="283dc-114">Requirements</span></span>  
 <span data-ttu-id="283dc-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="283dc-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="283dc-116">См. также</span><span class="sxs-lookup"><span data-stu-id="283dc-116">See Also</span></span>  
 [<span data-ttu-id="283dc-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="283dc-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
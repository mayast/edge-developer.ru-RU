---
description: Определяет, находится ли среда выполнения текущего контекста в состоянии исключения.
title: Функция JsHasException | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572498"
---
# <span data-ttu-id="628de-103">Функция JsHasException</span><span class="sxs-lookup"><span data-stu-id="628de-103">JsHasException Function</span></span>
<span data-ttu-id="628de-104">Определяет, находится ли среда выполнения текущего контекста в состоянии исключения.</span><span class="sxs-lookup"><span data-stu-id="628de-104">Determines whether the runtime of the current context is in an exception state.</span></span>  
  
## <span data-ttu-id="628de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="628de-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### <span data-ttu-id="628de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="628de-106">Parameters</span></span>  
 `hasException`  
 <span data-ttu-id="628de-107">Указывает, находится ли среда выполнения текущего контекста в состоянии исключения.</span><span class="sxs-lookup"><span data-stu-id="628de-107">Whether the runtime of the current context is in the exception state.</span></span>  
  
## <span data-ttu-id="628de-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="628de-108">Return Value</span></span>  
 <span data-ttu-id="628de-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="628de-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="628de-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="628de-110">Remarks</span></span>  
 <span data-ttu-id="628de-111">Если вызов в среду выполнения приводит к возникновению исключения (как в результате выполнения сценария, так и из-за ошибки преобразования), среда выполнения помещается в состояние Exception.</span><span class="sxs-lookup"><span data-stu-id="628de-111">If a call into the runtime results in an exception (either as the result of running a script or due to something like a conversion failure), the runtime is placed into an "exception state."</span></span> <span data-ttu-id="628de-112">Все звонки в любой контекст, созданный средой выполнения (за исключением API исключений), будут завершаться сбоем `JsErrorInExceptionState` до тех пор, пока не будет очищено исключение.</span><span class="sxs-lookup"><span data-stu-id="628de-112">All calls into any context created by the runtime (except for the exception APIs) will fail with `JsErrorInExceptionState` until the exception is cleared.</span></span>  
  
 <span data-ttu-id="628de-113">Если среда выполнения текущего контекста находится в состоянии исключения, когда обратный вызов возвращает обработчик, обработчик автоматически создаст исключение.</span><span class="sxs-lookup"><span data-stu-id="628de-113">If the runtime of the current context is in the exception state when a callback returns into the engine, the engine will automatically rethrow the exception.</span></span>  
  
 <span data-ttu-id="628de-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="628de-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="628de-115">Требования</span><span class="sxs-lookup"><span data-stu-id="628de-115">Requirements</span></span>  
 <span data-ttu-id="628de-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="628de-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="628de-117">См. также</span><span class="sxs-lookup"><span data-stu-id="628de-117">See Also</span></span>  
 [<span data-ttu-id="628de-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="628de-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
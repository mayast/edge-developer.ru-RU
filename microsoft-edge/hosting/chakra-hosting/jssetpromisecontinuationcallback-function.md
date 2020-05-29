---
description: Задает функцию обратного вызова для продолжения Promise, которая вызывается контекстом, когда задача должна быть поставлена в очередь для будущего выполнения.
title: Функция JsSetPromiseContinuationCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9438bf05d879b0c2014c0a4d49d374d26eff3fb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572437"
---
# <span data-ttu-id="af0b7-103">Функция JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="af0b7-103">JsSetPromiseContinuationCallback Function</span></span>
<span data-ttu-id="af0b7-104">Задает функцию обратного вызова для продолжения Promise, которая вызывается контекстом, когда задача должна быть поставлена в очередь для будущего выполнения.</span><span class="sxs-lookup"><span data-stu-id="af0b7-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="af0b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af0b7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="af0b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af0b7-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="af0b7-107">Задается функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="af0b7-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="af0b7-108">Указанное пользователем состояние, которое будет передано обратно обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="af0b7-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="af0b7-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="af0b7-109">Return Value</span></span>  
 <span data-ttu-id="af0b7-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="af0b7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="af0b7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af0b7-111">Remarks</span></span>  
 <span data-ttu-id="af0b7-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="af0b7-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="af0b7-113">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="af0b7-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="af0b7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="af0b7-114">Requirements</span></span>  
 <span data-ttu-id="af0b7-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="af0b7-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="af0b7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="af0b7-116">See Also</span></span>  
 [<span data-ttu-id="af0b7-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="af0b7-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Обратный вызов для продолжения обещания.
title: JsPromiseContinuationCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571338"
---
# <span data-ttu-id="817c7-103">JsPromiseContinuationCallback typedef</span><span class="sxs-lookup"><span data-stu-id="817c7-103">JsPromiseContinuationCallback Typedef</span></span>
<span data-ttu-id="817c7-104">Обратный вызов для продолжения обещания.</span><span class="sxs-lookup"><span data-stu-id="817c7-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="817c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="817c7-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="817c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="817c7-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="817c7-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="817c7-107">Remarks</span></span>  
 <span data-ttu-id="817c7-108">Основное приложение может указать обратный вызов для продолжения Promise `JsSetPromiseContinuationCallback` .</span><span class="sxs-lookup"><span data-stu-id="817c7-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="817c7-109">Если сценарий создает задачу, которая должна выполняться позже, для нее будет вызван обратный вызов для продолжения по обещанию, а задача должна быть помещена в очередь FIFO, чтобы выполняться при завершении выполнения текущего сценария.</span><span class="sxs-lookup"><span data-stu-id="817c7-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="817c7-110">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="817c7-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="817c7-111">Требования</span><span class="sxs-lookup"><span data-stu-id="817c7-111">Requirements</span></span>  
 <span data-ttu-id="817c7-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="817c7-112">jsrt.h</span></span>  
  
## <span data-ttu-id="817c7-113">См. также</span><span class="sxs-lookup"><span data-stu-id="817c7-113">See Also</span></span>  
 [<span data-ttu-id="817c7-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="817c7-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
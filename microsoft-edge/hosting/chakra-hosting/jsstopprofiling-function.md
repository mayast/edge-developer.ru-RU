---
description: Прекращение профилирования в текущем контексте.
title: Функция JsStopProfiling | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9d021c7c9849d20283a39d6ecffc89c5b2ea0db0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572336"
---
# <span data-ttu-id="55fae-103">Функция JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="55fae-103">JsStopProfiling Function</span></span>
<span data-ttu-id="55fae-104">Прекращение профилирования в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="55fae-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="55fae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55fae-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="55fae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55fae-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="55fae-107">Причина остановки профилирования для передачи обратного вызова профилировщика.</span><span class="sxs-lookup"><span data-stu-id="55fae-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="55fae-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="55fae-108">Return Value</span></span>  
 <span data-ttu-id="55fae-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="55fae-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="55fae-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55fae-110">Remarks</span></span>  
 <span data-ttu-id="55fae-111">Не будет возвращать ошибку, если профилирование не началось.</span><span class="sxs-lookup"><span data-stu-id="55fae-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="55fae-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="55fae-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="55fae-113">Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.</span><span class="sxs-lookup"><span data-stu-id="55fae-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="55fae-114">Требования</span><span class="sxs-lookup"><span data-stu-id="55fae-114">Requirements</span></span>  
 <span data-ttu-id="55fae-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="55fae-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="55fae-116">См. также</span><span class="sxs-lookup"><span data-stu-id="55fae-116">See Also</span></span>  
 [<span data-ttu-id="55fae-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="55fae-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
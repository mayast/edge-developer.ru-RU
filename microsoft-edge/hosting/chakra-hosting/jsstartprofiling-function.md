---
description: Запускает профилирование в текущем контексте.
title: Функция JsStartProfiling | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartProfiling
helpviewer_keywords:
- JsStartProfiling function
ms.assetid: 638da395-42dd-4fc5-b581-819e647e887d
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 891c39305e08d214a8f06b680c7022683a9d6fe4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572337"
---
# <span data-ttu-id="85cf7-103">Функция JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="85cf7-103">JsStartProfiling Function</span></span>
<span data-ttu-id="85cf7-104">Запускает профилирование в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="85cf7-104">Starts profiling in the current context.</span></span>  
  
## <span data-ttu-id="85cf7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85cf7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStartProfiling(  
   _In_ IActiveScriptProfilerCallback *callback,  
   _In_ PROFILER_EVENT_MASK eventMask,  
   _In_ unsigned long context  
);  
```  
  
#### <span data-ttu-id="85cf7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85cf7-106">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="85cf7-107">Используемый обратный вызов для профилирования.</span><span class="sxs-lookup"><span data-stu-id="85cf7-107">The profiling callback to use.</span></span>  
  
 `eventMask`  
 <span data-ttu-id="85cf7-108">События профилирования для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="85cf7-108">The profiling events to callback with.</span></span>  
  
 `context`  
 <span data-ttu-id="85cf7-109">Контекст, передаваемый обратному вызову профилирования.</span><span class="sxs-lookup"><span data-stu-id="85cf7-109">A context to pass to the profiling callback.</span></span>  
  
## <span data-ttu-id="85cf7-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="85cf7-110">Return Value</span></span>  
 <span data-ttu-id="85cf7-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="85cf7-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="85cf7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85cf7-112">Remarks</span></span>  
 <span data-ttu-id="85cf7-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="85cf7-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="85cf7-114">Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.</span><span class="sxs-lookup"><span data-stu-id="85cf7-114">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="85cf7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="85cf7-115">Requirements</span></span>  
 <span data-ttu-id="85cf7-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="85cf7-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="85cf7-117">См. также</span><span class="sxs-lookup"><span data-stu-id="85cf7-117">See Also</span></span>  
 [<span data-ttu-id="85cf7-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="85cf7-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
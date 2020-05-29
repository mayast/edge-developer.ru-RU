---
description: Вызывает функцию.
title: Функция JsCallFunction | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f242ccef71d8a2b361dbe2d1a299728f5551f5d3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571463"
---
# <span data-ttu-id="4c2ec-103">Функция JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="4c2ec-103">JsCallFunction Function</span></span>
<span data-ttu-id="4c2ec-104">Вызывает функцию.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="4c2ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c2ec-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="4c2ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c2ec-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="4c2ec-107">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="4c2ec-108">Аргументы для вызова.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="4c2ec-109">Число аргументов, передаваемых функции.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="4c2ec-110">Значение, возвращаемое при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="4c2ec-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="4c2ec-111">Return Value</span></span>  
 <span data-ttu-id="4c2ec-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4c2ec-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c2ec-113">Remarks</span></span>  
 <span data-ttu-id="4c2ec-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4c2ec-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4c2ec-115">Requirements</span></span>  
 <span data-ttu-id="4c2ec-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4c2ec-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4c2ec-117">См. также</span><span class="sxs-lookup"><span data-stu-id="4c2ec-117">See Also</span></span>  
 [<span data-ttu-id="4c2ec-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4c2ec-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Сравните два значения JavaScript для строгого равенства.
title: Функция JsStrictEquals | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b7f2b7a66c32428100f0c0d0f9db6150559ed7a2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572434"
---
# <span data-ttu-id="43bec-103">Функция JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="43bec-103">JsStrictEquals Function</span></span>
<span data-ttu-id="43bec-104">Сравните два значения JavaScript для строгого равенства.</span><span class="sxs-lookup"><span data-stu-id="43bec-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="43bec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43bec-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="43bec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43bec-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="43bec-107">Первый сравниваемый объект.</span><span class="sxs-lookup"><span data-stu-id="43bec-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="43bec-108">Второй сравниваемый объект.</span><span class="sxs-lookup"><span data-stu-id="43bec-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="43bec-109">Являются ли значения строго эквивалентными.</span><span class="sxs-lookup"><span data-stu-id="43bec-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="43bec-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="43bec-110">Return Value</span></span>  
 <span data-ttu-id="43bec-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="43bec-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="43bec-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43bec-112">Remarks</span></span>  
 <span data-ttu-id="43bec-113">Эта функция эквивалентна `===` оператору в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="43bec-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="43bec-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="43bec-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="43bec-115">Требования</span><span class="sxs-lookup"><span data-stu-id="43bec-115">Requirements</span></span>  
 <span data-ttu-id="43bec-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="43bec-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="43bec-117">См. также</span><span class="sxs-lookup"><span data-stu-id="43bec-117">See Also</span></span>  
 [<span data-ttu-id="43bec-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="43bec-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
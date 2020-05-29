---
description: Возвращает значение `true` в текущем контексте сценария.
title: Функция JsGetTrueValue | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 620ed775947db9d7156d61df1cfdf974a46baec2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571370"
---
# <span data-ttu-id="90ba2-103">Функция JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="90ba2-103">JsGetTrueValue Function</span></span>
<span data-ttu-id="90ba2-104">Возвращает значение `true` в текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="90ba2-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="90ba2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90ba2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="90ba2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90ba2-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="90ba2-107">`true`Значение.</span><span class="sxs-lookup"><span data-stu-id="90ba2-107">The `true` value.</span></span>  
  
## <span data-ttu-id="90ba2-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="90ba2-108">Return Value</span></span>  
 <span data-ttu-id="90ba2-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="90ba2-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="90ba2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90ba2-110">Remarks</span></span>  
 <span data-ttu-id="90ba2-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="90ba2-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="90ba2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="90ba2-112">Requirements</span></span>  
 <span data-ttu-id="90ba2-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="90ba2-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="90ba2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="90ba2-114">See Also</span></span>  
 [<span data-ttu-id="90ba2-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="90ba2-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
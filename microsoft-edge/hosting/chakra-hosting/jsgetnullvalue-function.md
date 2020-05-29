---
description: Возвращает значение `null` в текущем контексте сценария.
title: Функция JsGetNullValue | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84164aa9ce5d522b0933d928d85b26c652be066f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572523"
---
# <span data-ttu-id="914be-103">Функция JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="914be-103">JsGetNullValue Function</span></span>
<span data-ttu-id="914be-104">Возвращает значение `null` в текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="914be-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="914be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="914be-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="914be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="914be-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="914be-107">`null`Значение.</span><span class="sxs-lookup"><span data-stu-id="914be-107">The `null` value.</span></span>  
  
## <span data-ttu-id="914be-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="914be-108">Return Value</span></span>  
 <span data-ttu-id="914be-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="914be-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="914be-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="914be-110">Remarks</span></span>  
 <span data-ttu-id="914be-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="914be-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="914be-112">Требования</span><span class="sxs-lookup"><span data-stu-id="914be-112">Requirements</span></span>  
 <span data-ttu-id="914be-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="914be-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="914be-114">См. также</span><span class="sxs-lookup"><span data-stu-id="914be-114">See Also</span></span>  
 [<span data-ttu-id="914be-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="914be-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
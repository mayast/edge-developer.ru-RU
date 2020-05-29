---
description: Возвращает значение `false` в текущем контексте сценария.
title: Функция JsGetFalseValue | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 52e54ad7eb34877c3cb83b06f5aba70edf285bca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571390"
---
# <span data-ttu-id="a25d9-103">Функция JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="a25d9-103">JsGetFalseValue Function</span></span>
<span data-ttu-id="a25d9-104">Возвращает значение `false` в текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="a25d9-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="a25d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a25d9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="a25d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a25d9-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="a25d9-107">`false`Значение.</span><span class="sxs-lookup"><span data-stu-id="a25d9-107">The `false` value.</span></span>  
  
## <span data-ttu-id="a25d9-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a25d9-108">Return Value</span></span>  
 <span data-ttu-id="a25d9-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a25d9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a25d9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a25d9-110">Remarks</span></span>  
 <span data-ttu-id="a25d9-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="a25d9-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a25d9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a25d9-112">Requirements</span></span>  
 <span data-ttu-id="a25d9-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a25d9-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a25d9-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a25d9-114">See Also</span></span>  
 [<span data-ttu-id="a25d9-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a25d9-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Преобразует значение в Boolean с помощью стандартной семантики JavaScript.
title: Функция JsConvertValueToBoolean | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 861871a030d5a47621ccaf40b6cd332f42a06583
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571453"
---
# <span data-ttu-id="0bcb2-103">Функция JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="0bcb2-103">JsConvertValueToBoolean Function</span></span>
<span data-ttu-id="0bcb2-104">Преобразует значение в Boolean с помощью стандартной семантики JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0bcb2-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="0bcb2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bcb2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="0bcb2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bcb2-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="0bcb2-107">Преобразуемое значение.</span><span class="sxs-lookup"><span data-stu-id="0bcb2-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="0bcb2-108">Преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="0bcb2-108">The converted value.</span></span>  
  
## <span data-ttu-id="0bcb2-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="0bcb2-109">Return Value</span></span>  
 <span data-ttu-id="0bcb2-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0bcb2-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0bcb2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bcb2-111">Remarks</span></span>  
 <span data-ttu-id="0bcb2-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="0bcb2-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0bcb2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0bcb2-113">Requirements</span></span>  
 <span data-ttu-id="0bcb2-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0bcb2-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0bcb2-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0bcb2-115">See Also</span></span>  
 [<span data-ttu-id="0bcb2-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0bcb2-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
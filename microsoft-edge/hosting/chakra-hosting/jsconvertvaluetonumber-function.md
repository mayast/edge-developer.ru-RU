---
description: Преобразует значение в число с помощью стандартной семантики JavaScript.
title: Функция JsConvertValueToNumber | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3b3f450a58aaf1c434e1d34cd51577e3a5a9ee31
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571451"
---
# <span data-ttu-id="4420d-103">Функция JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="4420d-103">JsConvertValueToNumber Function</span></span>
<span data-ttu-id="4420d-104">Преобразует значение в число с помощью стандартной семантики JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4420d-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="4420d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4420d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="4420d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4420d-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="4420d-107">Преобразуемое значение.</span><span class="sxs-lookup"><span data-stu-id="4420d-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="4420d-108">Преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="4420d-108">The converted value.</span></span>  
  
## <span data-ttu-id="4420d-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="4420d-109">Return Value</span></span>  
 <span data-ttu-id="4420d-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4420d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4420d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4420d-111">Remarks</span></span>  
 <span data-ttu-id="4420d-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="4420d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4420d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4420d-113">Requirements</span></span>  
 <span data-ttu-id="4420d-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4420d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4420d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4420d-115">See Also</span></span>  
 [<span data-ttu-id="4420d-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4420d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
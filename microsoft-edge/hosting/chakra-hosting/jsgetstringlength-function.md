---
description: Возвращает длину строкового значения.
title: Функция JsGetStringLength | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6b562b2dc58341523910db41fb8b748453b2a836
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571376"
---
# <span data-ttu-id="e8ce4-103">Функция JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="e8ce4-103">JsGetStringLength Function</span></span>
<span data-ttu-id="e8ce4-104">Возвращает длину строкового значения.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="e8ce4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8ce4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="e8ce4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8ce4-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="e8ce4-107">Строковое значение, для которого требуется получить длину.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="e8ce4-108">Длина строки.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-108">The length of the string.</span></span>  
  
## <span data-ttu-id="e8ce4-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e8ce4-109">Return Value</span></span>  
 <span data-ttu-id="e8ce4-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e8ce4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8ce4-111">Remarks</span></span>  
 <span data-ttu-id="e8ce4-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e8ce4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e8ce4-113">Requirements</span></span>  
 <span data-ttu-id="e8ce4-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e8ce4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e8ce4-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e8ce4-115">See Also</span></span>  
 [<span data-ttu-id="e8ce4-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e8ce4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
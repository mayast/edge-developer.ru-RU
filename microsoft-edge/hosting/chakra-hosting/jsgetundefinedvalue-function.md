---
description: Возвращает значение `undefined` в текущем контексте сценария.
title: Функция JsGetUndefinedValue | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5edd536a29f5003591de476cb5d21ddb64f48c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572504"
---
# <span data-ttu-id="ae251-103">Функция JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="ae251-103">JsGetUndefinedValue Function</span></span>
<span data-ttu-id="ae251-104">Возвращает значение `undefined` в текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="ae251-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="ae251-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae251-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="ae251-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae251-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="ae251-107">`undefined`Значение.</span><span class="sxs-lookup"><span data-stu-id="ae251-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="ae251-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ae251-108">Return Value</span></span>  
 <span data-ttu-id="ae251-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ae251-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ae251-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae251-110">Remarks</span></span>  
 <span data-ttu-id="ae251-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="ae251-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ae251-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ae251-112">Requirements</span></span>  
 <span data-ttu-id="ae251-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ae251-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ae251-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ae251-114">See Also</span></span>  
 [<span data-ttu-id="ae251-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ae251-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
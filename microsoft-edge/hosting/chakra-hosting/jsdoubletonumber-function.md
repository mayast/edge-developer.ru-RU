---
description: Создает числовое значение на основе двойного значения.
title: Функция JsDoubleToNumber | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c33adbe217f27f77e348fc56e87c4587c6a6ec4c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572539"
---
# <span data-ttu-id="9e101-103">Функция JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="9e101-103">JsDoubleToNumber Function</span></span>
<span data-ttu-id="9e101-104">Создает числовое значение из `double` значения.</span><span class="sxs-lookup"><span data-stu-id="9e101-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="9e101-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e101-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="9e101-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e101-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="9e101-107">`double`Преобразование в числовое значение.</span><span class="sxs-lookup"><span data-stu-id="9e101-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="9e101-108">Новое числовое значение.</span><span class="sxs-lookup"><span data-stu-id="9e101-108">The new number value.</span></span>  
  
## <span data-ttu-id="9e101-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="9e101-109">Return Value</span></span>  
 <span data-ttu-id="9e101-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9e101-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9e101-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e101-111">Remarks</span></span>  
 <span data-ttu-id="9e101-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="9e101-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9e101-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9e101-113">Requirements</span></span>  
 <span data-ttu-id="9e101-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9e101-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9e101-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9e101-115">See Also</span></span>  
 [<span data-ttu-id="9e101-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9e101-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
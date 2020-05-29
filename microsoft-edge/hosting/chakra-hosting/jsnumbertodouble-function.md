---
description: Возвращает `double` значение числового значения.
title: Функция JsNumberToDouble | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fc99e02aa0376bb100b4e1302c29532a57bd539f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571350"
---
# <span data-ttu-id="935aa-103">Функция JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="935aa-103">JsNumberToDouble Function</span></span>
<span data-ttu-id="935aa-104">Возвращает `double` значение числового значения.</span><span class="sxs-lookup"><span data-stu-id="935aa-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="935aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="935aa-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="935aa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="935aa-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="935aa-107">Числовое значение, которое нужно преобразовать в `double` значение.</span><span class="sxs-lookup"><span data-stu-id="935aa-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="935aa-108">`double`Значение.</span><span class="sxs-lookup"><span data-stu-id="935aa-108">The `double` value.</span></span>  
  
## <span data-ttu-id="935aa-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="935aa-109">Return Value</span></span>  
 <span data-ttu-id="935aa-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="935aa-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="935aa-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="935aa-111">Remarks</span></span>  
 <span data-ttu-id="935aa-112">Эта функция возвращает значение числового значения.</span><span class="sxs-lookup"><span data-stu-id="935aa-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="935aa-113">`JsErrorInvalidArgument`Если тип значения не является числом, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="935aa-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="935aa-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="935aa-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="935aa-115">Требования</span><span class="sxs-lookup"><span data-stu-id="935aa-115">Requirements</span></span>  
 <span data-ttu-id="935aa-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="935aa-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="935aa-117">См. также</span><span class="sxs-lookup"><span data-stu-id="935aa-117">See Also</span></span>  
 [<span data-ttu-id="935aa-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="935aa-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
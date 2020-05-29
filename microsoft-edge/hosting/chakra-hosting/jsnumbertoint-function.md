---
description: Возвращает `int` значение числового значения.
title: Функция JsNumberToInt | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572490"
---
# <span data-ttu-id="411c6-103">Функция JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="411c6-103">JsNumberToInt Function</span></span>
<span data-ttu-id="411c6-104">Возвращает `int` значение числового значения.</span><span class="sxs-lookup"><span data-stu-id="411c6-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="411c6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="411c6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="411c6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="411c6-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="411c6-107">Числовое значение, которое нужно преобразовать в `int` значение.</span><span class="sxs-lookup"><span data-stu-id="411c6-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="411c6-108">`int`Значение.</span><span class="sxs-lookup"><span data-stu-id="411c6-108">The `int` value.</span></span>  
  
## <span data-ttu-id="411c6-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="411c6-109">Return Value</span></span>  
  
## <span data-ttu-id="411c6-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="411c6-110">Remarks</span></span>  
 <span data-ttu-id="411c6-111">Эта функция извлекает значение числового значения и преобразует его в `int` значение.</span><span class="sxs-lookup"><span data-stu-id="411c6-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="411c6-112">`JsErrorInvalidArgument`Если тип значения не является числом, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="411c6-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="411c6-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="411c6-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="411c6-114">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="411c6-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="411c6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="411c6-115">Requirements</span></span>  
 <span data-ttu-id="411c6-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="411c6-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="411c6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="411c6-117">See Also</span></span>  
 [<span data-ttu-id="411c6-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="411c6-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Возвращает идентификатор свойства, связанного с символом.
title: Функция JsGetPropertyIdFromSymbol | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0d11dbaf25b85e2bcd85a0cf2bac1b499fd4fa3e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572514"
---
# <span data-ttu-id="f5f6b-103">Функция JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="f5f6b-103">JsGetPropertyIdFromSymbol Function</span></span>
<span data-ttu-id="f5f6b-104">Возвращает идентификатор свойства, связанного с символом.</span><span class="sxs-lookup"><span data-stu-id="f5f6b-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="f5f6b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5f6b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="f5f6b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5f6b-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="f5f6b-107">Символ, идентификатор свойства которого извлекается.</span><span class="sxs-lookup"><span data-stu-id="f5f6b-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="f5f6b-108">Идентификатор свойства для заданного символа.</span><span class="sxs-lookup"><span data-stu-id="f5f6b-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="f5f6b-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f5f6b-109">Return Value</span></span>  
 <span data-ttu-id="f5f6b-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f5f6b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f5f6b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5f6b-111">Remarks</span></span>  
 <span data-ttu-id="f5f6b-112">Идентификаторы свойств зависят от контекста и не могут использоваться в разных контекстах.</span><span class="sxs-lookup"><span data-stu-id="f5f6b-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="f5f6b-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="f5f6b-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f5f6b-114">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f5f6b-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="f5f6b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f5f6b-115">Requirements</span></span>  
 <span data-ttu-id="f5f6b-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f5f6b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f5f6b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f5f6b-117">See Also</span></span>  
 [<span data-ttu-id="f5f6b-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f5f6b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
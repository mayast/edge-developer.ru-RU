---
description: Возвращает символ, связанный с ИДЕНТИФИКАТОРом свойства.
title: Функция JsGetSymbolFromPropertyId | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6902384772f29f80751660ce2d4a295d2ea620ab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571372"
---
# <span data-ttu-id="32ca1-103">Функция JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="32ca1-103">JsGetSymbolFromPropertyId Function</span></span>
<span data-ttu-id="32ca1-104">Возвращает символ, связанный с ИДЕНТИФИКАТОРом свойства.</span><span class="sxs-lookup"><span data-stu-id="32ca1-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="32ca1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32ca1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="32ca1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32ca1-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="32ca1-107">Идентификатор свойства, для которого нужно получить символ.</span><span class="sxs-lookup"><span data-stu-id="32ca1-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="32ca1-108">Символ, связанный с ИДЕНТИФИКАТОРом свойства.</span><span class="sxs-lookup"><span data-stu-id="32ca1-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="32ca1-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="32ca1-109">Return Value</span></span>  
 <span data-ttu-id="32ca1-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="32ca1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="32ca1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32ca1-111">Remarks</span></span>  
 <span data-ttu-id="32ca1-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="32ca1-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="32ca1-113">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="32ca1-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="32ca1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="32ca1-114">Requirements</span></span>  
 <span data-ttu-id="32ca1-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="32ca1-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="32ca1-116">См. также</span><span class="sxs-lookup"><span data-stu-id="32ca1-116">See Also</span></span>  
 [<span data-ttu-id="32ca1-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="32ca1-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
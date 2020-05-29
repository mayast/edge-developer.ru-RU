---
description: Возвращает тип свойства.
title: Функция JsGetPropertyIdType | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a43cfc2efd69cc14813ad88850afbf602d477d71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572512"
---
# <span data-ttu-id="879e9-103">Функция JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="879e9-103">JsGetPropertyIdType Function</span></span>
<span data-ttu-id="879e9-104">Возвращает тип свойства.</span><span class="sxs-lookup"><span data-stu-id="879e9-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="879e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="879e9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="879e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="879e9-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="879e9-107">Идентификатор свойства, для которого нужно получить тип.</span><span class="sxs-lookup"><span data-stu-id="879e9-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="879e9-108">Значение `JsPropertyIdType` заданного идентификатора свойства.</span><span class="sxs-lookup"><span data-stu-id="879e9-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="879e9-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="879e9-109">Return Value</span></span>  
 <span data-ttu-id="879e9-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="879e9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="879e9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="879e9-111">Remarks</span></span>  
 <span data-ttu-id="879e9-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="879e9-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="879e9-113">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="879e9-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="879e9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="879e9-114">Requirements</span></span>  
 <span data-ttu-id="879e9-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="879e9-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="879e9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="879e9-116">See Also</span></span>  
 [<span data-ttu-id="879e9-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="879e9-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
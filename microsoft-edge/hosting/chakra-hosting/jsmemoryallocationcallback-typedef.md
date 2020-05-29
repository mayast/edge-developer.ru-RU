---
description: Пользователь реализовал подпрограмму обратного вызова для событий выделения памяти.
title: JsMemoryAllocationCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571356"
---
# <span data-ttu-id="fb6ee-103">JsMemoryAllocationCallback typedef</span><span class="sxs-lookup"><span data-stu-id="fb6ee-103">JsMemoryAllocationCallback Typedef</span></span>
<span data-ttu-id="fb6ee-104">Пользователь реализовал подпрограмму обратного вызова для событий выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="fb6ee-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="fb6ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb6ee-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="fb6ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb6ee-106">Parameters</span></span>  
 <span data-ttu-id="fb6ee-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="fb6ee-107">callbackState</span></span>  
 <span data-ttu-id="fb6ee-108">Состояние, передаваемое в JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="fb6ee-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="fb6ee-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="fb6ee-109">allocationEvent</span></span>  
 <span data-ttu-id="fb6ee-110">Тип события выделения типа.</span><span class="sxs-lookup"><span data-stu-id="fb6ee-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="fb6ee-111">allocationSize</span><span class="sxs-lookup"><span data-stu-id="fb6ee-111">allocationSize</span></span>  
 <span data-ttu-id="fb6ee-112">Размер выделения.</span><span class="sxs-lookup"><span data-stu-id="fb6ee-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="fb6ee-113">Значение свойства/возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb6ee-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="fb6ee-114">Для события JsMemoryAllocate возвращаемое значение true позволяет среде выполнения продолжить выделение.</span><span class="sxs-lookup"><span data-stu-id="fb6ee-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="fb6ee-115">Если возвращено значение false, запрос на выделение отклоняется.</span><span class="sxs-lookup"><span data-stu-id="fb6ee-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="fb6ee-116">Возвращаемое значение игнорируется для других событий выделения.</span><span class="sxs-lookup"><span data-stu-id="fb6ee-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="fb6ee-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb6ee-117">Remarks</span></span>  
 <span data-ttu-id="fb6ee-118">Для регистрации этого обратного вызова используйте JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="fb6ee-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="fb6ee-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fb6ee-119">Requirements</span></span>  
 <span data-ttu-id="fb6ee-120">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fb6ee-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fb6ee-121">См. также</span><span class="sxs-lookup"><span data-stu-id="fb6ee-121">See Also</span></span>  
 [<span data-ttu-id="fb6ee-122">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fb6ee-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
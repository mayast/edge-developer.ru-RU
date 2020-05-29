---
description: Делает объект нерасширяемым.
title: Функция JsPreventExtension | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: baa001b2fd26133ef3a20c88213ac6aaf34a2e0d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572476"
---
# <span data-ttu-id="891c8-103">Функция JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="891c8-103">JsPreventExtension Function</span></span>
<span data-ttu-id="891c8-104">Делает объект нерасширяемым.</span><span class="sxs-lookup"><span data-stu-id="891c8-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="891c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="891c8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="891c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="891c8-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="891c8-107">Объект, который нужно сделать нерасширяемым.</span><span class="sxs-lookup"><span data-stu-id="891c8-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="891c8-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="891c8-108">Return Value</span></span>  
 <span data-ttu-id="891c8-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="891c8-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="891c8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="891c8-110">Remarks</span></span>  
 <span data-ttu-id="891c8-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="891c8-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="891c8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="891c8-112">Requirements</span></span>  
 <span data-ttu-id="891c8-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="891c8-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="891c8-114">См. также</span><span class="sxs-lookup"><span data-stu-id="891c8-114">See Also</span></span>  
 [<span data-ttu-id="891c8-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="891c8-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
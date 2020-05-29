---
description: Возвращает значение, указывающее, перечислена ли куча текущего контекста.
title: Функция JsIsEnumeratingHeap | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 79f263547ef5812d905103d09ede7499d56c5dfb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571360"
---
# <span data-ttu-id="1fab7-103">Функция JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="1fab7-103">JsIsEnumeratingHeap Function</span></span>
<span data-ttu-id="1fab7-104">Возвращает значение, указывающее, перечислена ли куча текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="1fab7-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="1fab7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fab7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="1fab7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1fab7-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="1fab7-107">Указывает, производится ли перечисление кучи.</span><span class="sxs-lookup"><span data-stu-id="1fab7-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="1fab7-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="1fab7-108">Return Value</span></span>  
 <span data-ttu-id="1fab7-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1fab7-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1fab7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fab7-110">Remarks</span></span>  
 <span data-ttu-id="1fab7-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="1fab7-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="1fab7-112">Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.</span><span class="sxs-lookup"><span data-stu-id="1fab7-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="1fab7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1fab7-113">Requirements</span></span>  
 <span data-ttu-id="1fab7-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1fab7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1fab7-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1fab7-115">See Also</span></span>  
 [<span data-ttu-id="1fab7-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1fab7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
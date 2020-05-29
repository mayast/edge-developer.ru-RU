---
description: Инициализирует переданный метод `VARIANT` как проекцию значения JavaScript.
title: Функция JsValueToVariant | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571329"
---
# <span data-ttu-id="f6407-103">Функция JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="f6407-103">JsValueToVariant Function</span></span>
<span data-ttu-id="f6407-104">Инициализирует переданный метод `VARIANT` как проекцию значения JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f6407-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="f6407-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6407-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="f6407-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6407-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="f6407-107">Значение JavaScript для проекта как `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="f6407-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="f6407-108">Указатель на `VARIANT` структуру, которая будет инициализирована как проекция.</span><span class="sxs-lookup"><span data-stu-id="f6407-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="f6407-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f6407-109">Return Value</span></span>  
  
## <span data-ttu-id="f6407-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6407-110">Remarks</span></span>  
 <span data-ttu-id="f6407-111">Проекция `VARIANT` может использоваться клиентами автоматизации com для вызова проецируемого объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f6407-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="f6407-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="f6407-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f6407-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f6407-113">Requirements</span></span>  
 <span data-ttu-id="f6407-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f6407-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f6407-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f6407-115">See Also</span></span>  
 [<span data-ttu-id="f6407-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f6407-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
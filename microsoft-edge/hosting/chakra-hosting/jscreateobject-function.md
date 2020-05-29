---
description: Создание нового объекта.
title: Функция JsCreateObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9ed988aae0921978819d379562d4a966e4a082a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571428"
---
# <span data-ttu-id="4ce0f-103">Функция JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="4ce0f-103">JsCreateObject Function</span></span>
<span data-ttu-id="4ce0f-104">Создание нового объекта.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-104">Creates a new object.</span></span>
  
## <span data-ttu-id="4ce0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ce0f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="4ce0f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ce0f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="4ce0f-107">Новый объект.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-107">The new object.</span></span>  
  
## <span data-ttu-id="4ce0f-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="4ce0f-108">Return Value</span></span>  
 <span data-ttu-id="4ce0f-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4ce0f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ce0f-110">Remarks</span></span>  
 <span data-ttu-id="4ce0f-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4ce0f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4ce0f-112">Requirements</span></span>  
 <span data-ttu-id="4ce0f-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4ce0f-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4ce0f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="4ce0f-114">See Also</span></span>  
 [<span data-ttu-id="4ce0f-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4ce0f-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
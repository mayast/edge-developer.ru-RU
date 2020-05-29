---
description: Возвращает прототип объекта.
title: Функция JsGetPrototype | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 12708634fea9e8f9fd1205514845b1cb9760ee9e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571383"
---
# <span data-ttu-id="5924d-103">Функция JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="5924d-103">JsGetPrototype Function</span></span>
<span data-ttu-id="5924d-104">Возвращает прототип объекта.</span><span class="sxs-lookup"><span data-stu-id="5924d-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="5924d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5924d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="5924d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5924d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="5924d-107">Объект, для которого нужно вернуть прототип.</span><span class="sxs-lookup"><span data-stu-id="5924d-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="5924d-108">Прототип объекта.</span><span class="sxs-lookup"><span data-stu-id="5924d-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="5924d-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="5924d-109">Return Value</span></span>  
 <span data-ttu-id="5924d-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5924d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5924d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5924d-111">Remarks</span></span>  
 <span data-ttu-id="5924d-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="5924d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5924d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5924d-113">Requirements</span></span>  
 <span data-ttu-id="5924d-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5924d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5924d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5924d-115">See Also</span></span>  
 [<span data-ttu-id="5924d-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5924d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Помещает свойство объекта.
title: Функция JsSetProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2aba03a73f35284f79355a7d93161d9a9518012c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572435"
---
# <span data-ttu-id="e47f5-103">Функция JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="e47f5-103">JsSetProperty Function</span></span>
<span data-ttu-id="e47f5-104">Помещает свойство объекта.</span><span class="sxs-lookup"><span data-stu-id="e47f5-104">Puts an object's property.</span></span>  
  
## <span data-ttu-id="e47f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e47f5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### <span data-ttu-id="e47f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e47f5-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e47f5-107">Объект, содержащий свойство.</span><span class="sxs-lookup"><span data-stu-id="e47f5-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="e47f5-108">Идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="e47f5-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="e47f5-109">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="e47f5-109">The new value of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="e47f5-110">Набор свойств должен соответствовать правилам строгого режима.</span><span class="sxs-lookup"><span data-stu-id="e47f5-110">The property set should follow strict mode rules.</span></span>  
  
## <span data-ttu-id="e47f5-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e47f5-111">Return Value</span></span>  
 <span data-ttu-id="e47f5-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e47f5-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e47f5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e47f5-113">Remarks</span></span>  
 <span data-ttu-id="e47f5-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="e47f5-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e47f5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e47f5-115">Requirements</span></span>  
 <span data-ttu-id="e47f5-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e47f5-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e47f5-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e47f5-117">See Also</span></span>  
 [<span data-ttu-id="e47f5-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e47f5-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
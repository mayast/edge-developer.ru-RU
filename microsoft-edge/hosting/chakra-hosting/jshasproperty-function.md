---
description: Определяет, имеет ли объект свойство.
title: Функция JsHasProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c6cc195ae02c28500f0a018256d24278ad4b47d8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572494"
---
# <span data-ttu-id="a9721-103">Функция JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="a9721-103">JsHasProperty Function</span></span>
<span data-ttu-id="a9721-104">Определяет, имеет ли объект свойство.</span><span class="sxs-lookup"><span data-stu-id="a9721-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="a9721-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9721-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="a9721-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9721-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="a9721-107">Объект, который может содержать свойство.</span><span class="sxs-lookup"><span data-stu-id="a9721-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="a9721-108">Идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="a9721-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="a9721-109">Имеет ли свойство объект (или прототип).</span><span class="sxs-lookup"><span data-stu-id="a9721-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="a9721-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a9721-110">Return Value</span></span>  
 <span data-ttu-id="a9721-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a9721-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a9721-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9721-112">Remarks</span></span>  
 <span data-ttu-id="a9721-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="a9721-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a9721-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a9721-114">Requirements</span></span>  
 <span data-ttu-id="a9721-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a9721-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a9721-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a9721-116">See Also</span></span>  
 [<span data-ttu-id="a9721-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a9721-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
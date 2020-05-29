---
description: Тип JavaScript JsValueRef.
title: Перечисление JsValueType | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c42231525b55b49f0931a2ace33b373e0d4ae441
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571328"
---
# <span data-ttu-id="27c53-103">Перечисление JsValueType</span><span class="sxs-lookup"><span data-stu-id="27c53-103">JsValueType Enumeration</span></span>
<span data-ttu-id="27c53-104">Тип JavaScript JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="27c53-104">The JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="27c53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27c53-105">Syntax</span></span>  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## <span data-ttu-id="27c53-106">Участников</span><span class="sxs-lookup"><span data-stu-id="27c53-106">Members</span></span>  
  
### <span data-ttu-id="27c53-107">Данные</span><span class="sxs-lookup"><span data-stu-id="27c53-107">Values</span></span>  
  
|<span data-ttu-id="27c53-108">Имя</span><span class="sxs-lookup"><span data-stu-id="27c53-108">Name</span></span>|<span data-ttu-id="27c53-109">Описание</span><span class="sxs-lookup"><span data-stu-id="27c53-109">Description</span></span>|  
|----------|-----------------|  
|`JsUndefined`|<span data-ttu-id="27c53-110">Значением является `undefined` значение.</span><span class="sxs-lookup"><span data-stu-id="27c53-110">The value is the `undefined` value.</span></span>|  
|`JsNull`|<span data-ttu-id="27c53-111">Значением является `null` значение.</span><span class="sxs-lookup"><span data-stu-id="27c53-111">The value is the `null` value.</span></span>|  
|`JsNumber`|<span data-ttu-id="27c53-112">Значение является значением номера JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-112">The value is a JavaScript number value.</span></span>|  
|`JsString`|<span data-ttu-id="27c53-113">Значение — это строковое значение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-113">The value is a JavaScript string value.</span></span>|  
|`JsBoolean`|<span data-ttu-id="27c53-114">Значение является логическим значением JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-114">The value is a JavaScript Boolean value.</span></span>|  
|`JsObject`|<span data-ttu-id="27c53-115">Значение является значением объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-115">The value is a JavaScript object value.</span></span>|  
|`JsFunction`|<span data-ttu-id="27c53-116">Значением является значение объекта функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-116">The value is a JavaScript function object value.</span></span>|  
|`JsError`|<span data-ttu-id="27c53-117">Значением является значение объекта ошибки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-117">The value is a JavaScript error object value.</span></span>|  
|`JsArray`|<span data-ttu-id="27c53-118">Значение является значением объекта-массива JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-118">The value is a JavaScript array object value.</span></span>|  
|`JsSymbol`|<span data-ttu-id="27c53-119">Значение является значением символа JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-119">The value is a JavaScript symbol value.</span></span><br /><br /> <span data-ttu-id="27c53-120">Это значение перечисления поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="27c53-120">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsArrayBuffer`|<span data-ttu-id="27c53-121">Значение является `ArrayBuffer` значением объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-121">The value is a JavaScript `ArrayBuffer` object value.</span></span><br /><br /> <span data-ttu-id="27c53-122">Это значение перечисления поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="27c53-122">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsTypedArray`|<span data-ttu-id="27c53-123">Значение является значением объекта типизированного массива JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-123">The value is a JavaScript typed array object value.</span></span><br /><br /> <span data-ttu-id="27c53-124">Это значение перечисления поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="27c53-124">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsDataView`|<span data-ttu-id="27c53-125">Значение является `DataView` значением объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="27c53-125">The value is a JavaScript `DataView` object value.</span></span><br /><br /> <span data-ttu-id="27c53-126">Это значение перечисления поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="27c53-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
  
## <span data-ttu-id="27c53-127">Требования</span><span class="sxs-lookup"><span data-stu-id="27c53-127">Requirements</span></span>  
 <span data-ttu-id="27c53-128">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="27c53-128">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="27c53-129">См. также</span><span class="sxs-lookup"><span data-stu-id="27c53-129">See Also</span></span>  
 [<span data-ttu-id="27c53-130">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="27c53-130">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
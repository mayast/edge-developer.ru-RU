---
description: Проверяет, имеет ли объект значение по указанному индексу.
title: Функция JsHasIndexedProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85d9fa12c44bd1d961ec2a7ba494484873635586
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572495"
---
# <span data-ttu-id="a9818-103">Функция JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="a9818-103">JsHasIndexedProperty Function</span></span>
<span data-ttu-id="a9818-104">Проверяет, имеет ли объект значение по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="a9818-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="a9818-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9818-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="a9818-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9818-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="a9818-107">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="a9818-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="a9818-108">Индекс для проверки.</span><span class="sxs-lookup"><span data-stu-id="a9818-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="a9818-109">Имеет ли объект значение по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="a9818-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="a9818-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a9818-110">Return Value</span></span>  
 <span data-ttu-id="a9818-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a9818-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a9818-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9818-112">Remarks</span></span>  
 <span data-ttu-id="a9818-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="a9818-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a9818-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a9818-114">Requirements</span></span>  
 <span data-ttu-id="a9818-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a9818-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a9818-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a9818-116">See Also</span></span>  
 [<span data-ttu-id="a9818-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a9818-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
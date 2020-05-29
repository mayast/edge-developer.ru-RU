---
description: Получает идентификатор свойства, связанный с именем.
title: Функция JsGetPropertyIdFromName | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e1954b86937056523a30c15dbf350ac02fd63dde
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572513"
---
# <span data-ttu-id="8d6a3-103">Функция JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="8d6a3-103">JsGetPropertyIdFromName Function</span></span>
<span data-ttu-id="8d6a3-104">Получает идентификатор свойства, связанный с именем.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-104">Gets the property ID associated with the name.</span></span>  
  
## <span data-ttu-id="8d6a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d6a3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="8d6a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d6a3-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="8d6a3-107">Имя идентификатора свойства для получения или создания.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-107">The name of the property ID to get or create.</span></span> <span data-ttu-id="8d6a3-108">Имя может состоять только из цифр.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-108">The name may consist of only digits.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="8d6a3-109">Идентификатор свойства в этой среде выполнения для заданного имени.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-109">The property ID in this runtime for the given name.</span></span>  
  
## <span data-ttu-id="8d6a3-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="8d6a3-110">Return Value</span></span>  
 <span data-ttu-id="8d6a3-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8d6a3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d6a3-112">Remarks</span></span>  
 <span data-ttu-id="8d6a3-113">Идентификаторы свойств зависят от контекста и не могут использоваться в разных контекстах.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-113">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="8d6a3-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8d6a3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8d6a3-115">Requirements</span></span>  
 <span data-ttu-id="8d6a3-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8d6a3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8d6a3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8d6a3-117">See Also</span></span>  
 [<span data-ttu-id="8d6a3-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8d6a3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
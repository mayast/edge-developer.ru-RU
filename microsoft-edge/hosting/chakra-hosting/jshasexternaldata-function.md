---
description: Определяет, является ли объект внешним объектом.
title: Функция JsHasExternalData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0ca86df09264eb82dac2e928874ca15edd2c8c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572501"
---
# <span data-ttu-id="83789-103">Функция JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="83789-103">JsHasExternalData Function</span></span>
<span data-ttu-id="83789-104">Определяет, является ли объект внешним объектом.</span><span class="sxs-lookup"><span data-stu-id="83789-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="83789-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83789-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="83789-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83789-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="83789-107">Объект.</span><span class="sxs-lookup"><span data-stu-id="83789-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="83789-108">Является ли объект внешним объектом.</span><span class="sxs-lookup"><span data-stu-id="83789-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="83789-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="83789-109">Return Value</span></span>  
 <span data-ttu-id="83789-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="83789-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="83789-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83789-111">Remarks</span></span>  
 <span data-ttu-id="83789-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="83789-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="83789-113">Требования</span><span class="sxs-lookup"><span data-stu-id="83789-113">Requirements</span></span>  
 <span data-ttu-id="83789-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="83789-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="83789-115">См. также</span><span class="sxs-lookup"><span data-stu-id="83789-115">See Also</span></span>  
 [<span data-ttu-id="83789-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="83789-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
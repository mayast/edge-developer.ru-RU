---
description: Возвращает свойство объекта.
title: Функция JsGetProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ea0e5a3bad9363800d2b4a3a18ab932ecc384486
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572515"
---
# <span data-ttu-id="cd937-103">Функция JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="cd937-103">JsGetProperty Function</span></span>
<span data-ttu-id="cd937-104">Возвращает свойство объекта.</span><span class="sxs-lookup"><span data-stu-id="cd937-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="cd937-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd937-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="cd937-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd937-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="cd937-107">Объект, содержащий свойство.</span><span class="sxs-lookup"><span data-stu-id="cd937-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="cd937-108">Идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="cd937-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="cd937-109">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="cd937-109">The value of the property.</span></span>  
  
## <span data-ttu-id="cd937-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="cd937-110">Return Value</span></span>  
 <span data-ttu-id="cd937-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cd937-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cd937-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd937-112">Remarks</span></span>  
 <span data-ttu-id="cd937-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="cd937-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cd937-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cd937-114">Requirements</span></span>  
 <span data-ttu-id="cd937-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cd937-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cd937-116">См. также</span><span class="sxs-lookup"><span data-stu-id="cd937-116">See Also</span></span>  
 [<span data-ttu-id="cd937-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cd937-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
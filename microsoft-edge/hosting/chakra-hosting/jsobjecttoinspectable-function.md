---
description: Распаковывает объект JavaScript в `IInspectable` указатель.
title: Функция JsObjectToInspectable | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7127e1cf1372020e0df00b81ed172739379426f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572489"
---
# <span data-ttu-id="ef5db-103">Функция JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="ef5db-103">JsObjectToInspectable Function</span></span>
<span data-ttu-id="ef5db-104">Распаковывает объект JavaScript в `IInspectable` указатель.</span><span class="sxs-lookup"><span data-stu-id="ef5db-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="ef5db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef5db-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="ef5db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef5db-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="ef5db-107">Значение JavaScript, на которое должно быть запланировано проецирование `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="ef5db-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="ef5db-108">`IInspectable`Значение объекта.</span><span class="sxs-lookup"><span data-stu-id="ef5db-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="ef5db-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ef5db-109">Return Value</span></span>  
 <span data-ttu-id="ef5db-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ef5db-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ef5db-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef5db-111">Remarks</span></span>  
 <span data-ttu-id="ef5db-112">Узлы ответственны за принудительное использование правил COM Threading.</span><span class="sxs-lookup"><span data-stu-id="ef5db-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="ef5db-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="ef5db-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="ef5db-114">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="ef5db-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="ef5db-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ef5db-115">Requirements</span></span>  
 <span data-ttu-id="ef5db-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ef5db-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ef5db-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ef5db-117">See Also</span></span>  
 [<span data-ttu-id="ef5db-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ef5db-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
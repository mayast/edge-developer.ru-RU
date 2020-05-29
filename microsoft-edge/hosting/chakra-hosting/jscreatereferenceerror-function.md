---
description: Создает новый объект ошибки ReferenceError JavaScript.
title: Функция JsCreateReferenceError | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 958af7111a233077aa7a2c2391b26666f55c634b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571425"
---
# <span data-ttu-id="ba589-103">Функция JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="ba589-103">JsCreateReferenceError Function</span></span>
<span data-ttu-id="ba589-104">Создает новый объект ошибки ReferenceError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba589-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="ba589-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba589-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="ba589-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba589-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="ba589-107">Сообщение для объекта Error.</span><span class="sxs-lookup"><span data-stu-id="ba589-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="ba589-108">Новый объект Error.</span><span class="sxs-lookup"><span data-stu-id="ba589-108">The new error object.</span></span>  
  
## <span data-ttu-id="ba589-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ba589-109">Return Value</span></span>  
 <span data-ttu-id="ba589-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ba589-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ba589-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba589-111">Remarks</span></span>  
 <span data-ttu-id="ba589-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="ba589-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ba589-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ba589-113">Requirements</span></span>  
 <span data-ttu-id="ba589-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ba589-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ba589-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ba589-115">See Also</span></span>  
 [<span data-ttu-id="ba589-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ba589-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Создает новый объект ошибки TypeError JavaScript.
title: Функция JsCreateTypeError | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 302bf75af3668dfdd0b40336e940e3eef3a74bce
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571413"
---
# <span data-ttu-id="5c55d-103">Функция JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="5c55d-103">JsCreateTypeError Function</span></span>
<span data-ttu-id="5c55d-104">Создает новый объект ошибки TypeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5c55d-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="5c55d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c55d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="5c55d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c55d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="5c55d-107">Сообщение для объекта Error.</span><span class="sxs-lookup"><span data-stu-id="5c55d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="5c55d-108">Новый объект Error.</span><span class="sxs-lookup"><span data-stu-id="5c55d-108">The new error object.</span></span>  
  
## <span data-ttu-id="5c55d-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="5c55d-109">Return Value</span></span>  
 <span data-ttu-id="5c55d-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5c55d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5c55d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c55d-111">Remarks</span></span>  
 <span data-ttu-id="5c55d-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="5c55d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5c55d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5c55d-113">Requirements</span></span>  
 <span data-ttu-id="5c55d-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5c55d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5c55d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5c55d-115">See Also</span></span>  
 [<span data-ttu-id="5c55d-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5c55d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
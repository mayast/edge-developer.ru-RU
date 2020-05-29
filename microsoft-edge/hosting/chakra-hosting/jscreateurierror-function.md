---
description: Создает новый объект ошибки URIError JavaScript.
title: Функция JsCreateURIError | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5188827cd0b89b1dd6b54af005f6e118c4ae4c94
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571412"
---
# <span data-ttu-id="50c87-103">Функция JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="50c87-103">JsCreateURIError Function</span></span>
<span data-ttu-id="50c87-104">Создает новый объект ошибки URIError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="50c87-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="50c87-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50c87-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="50c87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50c87-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="50c87-107">Сообщение для объекта Error.</span><span class="sxs-lookup"><span data-stu-id="50c87-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="50c87-108">Новый объект Error.</span><span class="sxs-lookup"><span data-stu-id="50c87-108">The new error object.</span></span>  
  
## <span data-ttu-id="50c87-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="50c87-109">Return Value</span></span>  
 <span data-ttu-id="50c87-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="50c87-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="50c87-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50c87-111">Remarks</span></span>  
 <span data-ttu-id="50c87-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="50c87-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="50c87-113">Требования</span><span class="sxs-lookup"><span data-stu-id="50c87-113">Requirements</span></span>  
 <span data-ttu-id="50c87-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="50c87-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="50c87-115">См. также</span><span class="sxs-lookup"><span data-stu-id="50c87-115">See Also</span></span>  
 [<span data-ttu-id="50c87-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="50c87-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
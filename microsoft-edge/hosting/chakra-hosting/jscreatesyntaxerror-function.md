---
description: Создает новый объект ошибки SyntaxError JavaScript.
title: Функция JsCreateSyntaxError | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 8f7459e8300df56aa8ccfaa78ef97ce2b6ec6fa0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571416"
---
# <span data-ttu-id="37b30-103">Функция JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="37b30-103">JsCreateSyntaxError Function</span></span>
<span data-ttu-id="37b30-104">Создает новый объект ошибки SyntaxError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="37b30-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="37b30-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37b30-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="37b30-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37b30-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="37b30-107">Сообщение для объекта Error.</span><span class="sxs-lookup"><span data-stu-id="37b30-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="37b30-108">Новый объект Error.</span><span class="sxs-lookup"><span data-stu-id="37b30-108">The new error object.</span></span>  
  
## <span data-ttu-id="37b30-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="37b30-109">Return Value</span></span>  
 <span data-ttu-id="37b30-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="37b30-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="37b30-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37b30-111">Remarks</span></span>  
 <span data-ttu-id="37b30-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="37b30-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="37b30-113">Требования</span><span class="sxs-lookup"><span data-stu-id="37b30-113">Requirements</span></span>  
 <span data-ttu-id="37b30-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="37b30-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="37b30-115">См. также</span><span class="sxs-lookup"><span data-stu-id="37b30-115">See Also</span></span>  
 [<span data-ttu-id="37b30-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="37b30-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
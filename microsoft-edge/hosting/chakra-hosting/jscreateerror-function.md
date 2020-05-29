---
description: Создает новый объект ошибки JavaScript.
title: Функция JsCreateError | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 33d70e3f077b085ccb4ab541d3246d777ea68978
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571438"
---
# <span data-ttu-id="d23cf-103">Функция JsCreateError</span><span class="sxs-lookup"><span data-stu-id="d23cf-103">JsCreateError Function</span></span>
<span data-ttu-id="d23cf-104">Создает новый объект ошибки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d23cf-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="d23cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d23cf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="d23cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d23cf-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="d23cf-107">Сообщение для объекта Error.</span><span class="sxs-lookup"><span data-stu-id="d23cf-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="d23cf-108">Новый объект Error.</span><span class="sxs-lookup"><span data-stu-id="d23cf-108">The new error object.</span></span>  
  
## <span data-ttu-id="d23cf-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="d23cf-109">Return Value</span></span>  
 <span data-ttu-id="d23cf-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d23cf-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d23cf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d23cf-111">Remarks</span></span>  
 <span data-ttu-id="d23cf-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="d23cf-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d23cf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d23cf-113">Requirements</span></span>  
 <span data-ttu-id="d23cf-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d23cf-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d23cf-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d23cf-115">See Also</span></span>  
 [<span data-ttu-id="d23cf-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d23cf-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
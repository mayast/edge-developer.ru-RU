---
description: Создает новый объект ошибки RangeError JavaScript.
title: Функция JsCreateRangeError | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3759f1c04a2eb13488f756ae2c135373d9db1f74
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571427"
---
# <span data-ttu-id="adc73-103">Функция JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="adc73-103">JsCreateRangeError Function</span></span>
<span data-ttu-id="adc73-104">Создает новый объект ошибки RangeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="adc73-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="adc73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adc73-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="adc73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="adc73-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="adc73-107">Сообщение для объекта Error.</span><span class="sxs-lookup"><span data-stu-id="adc73-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="adc73-108">Новый объект Error.</span><span class="sxs-lookup"><span data-stu-id="adc73-108">The new error object.</span></span>  
  
## <span data-ttu-id="adc73-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="adc73-109">Return Value</span></span>  
 <span data-ttu-id="adc73-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="adc73-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="adc73-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adc73-111">Remarks</span></span>  
 <span data-ttu-id="adc73-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="adc73-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="adc73-113">Требования</span><span class="sxs-lookup"><span data-stu-id="adc73-113">Requirements</span></span>  
 <span data-ttu-id="adc73-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="adc73-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="adc73-115">См. также</span><span class="sxs-lookup"><span data-stu-id="adc73-115">See Also</span></span>  
 [<span data-ttu-id="adc73-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="adc73-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
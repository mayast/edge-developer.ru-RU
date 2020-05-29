---
description: Извлекает `bool` значение логического значения.
title: Функция JsBooleanToBool | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 55b0ef1278cbc73652fc8427e004cab002d76e5b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571468"
---
# <span data-ttu-id="9b78d-103">Функция JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="9b78d-103">JsBooleanToBool Function</span></span>
<span data-ttu-id="9b78d-104">Извлекает `bool` значение логического значения.</span><span class="sxs-lookup"><span data-stu-id="9b78d-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="9b78d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b78d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="9b78d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b78d-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="9b78d-107">Преобразуемое значение.</span><span class="sxs-lookup"><span data-stu-id="9b78d-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="9b78d-108">Преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="9b78d-108">The converted value.</span></span>  
  
## <span data-ttu-id="9b78d-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="9b78d-109">Return Value</span></span>  
 <span data-ttu-id="9b78d-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9b78d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9b78d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b78d-111">Remarks</span></span>  
 <span data-ttu-id="9b78d-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="9b78d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9b78d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9b78d-113">Requirements</span></span>  
 <span data-ttu-id="9b78d-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9b78d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9b78d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9b78d-115">See Also</span></span>  
 [<span data-ttu-id="9b78d-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9b78d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
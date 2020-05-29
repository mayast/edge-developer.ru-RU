---
description: Создает числовое значение из `int` значения.
title: Функция JsIntToNumber | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8f51638292346ec3058f9537d72b8fd21bebc6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571364"
---
# <span data-ttu-id="377ff-103">Функция JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="377ff-103">JsIntToNumber Function</span></span>
<span data-ttu-id="377ff-104">Создает числовое значение из `int` значения.</span><span class="sxs-lookup"><span data-stu-id="377ff-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="377ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="377ff-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="377ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="377ff-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="377ff-107">`int`Преобразование в числовое значение.</span><span class="sxs-lookup"><span data-stu-id="377ff-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="377ff-108">Новое числовое значение.</span><span class="sxs-lookup"><span data-stu-id="377ff-108">The new number value.</span></span>  
  
## <span data-ttu-id="377ff-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="377ff-109">Return Value</span></span>  
 <span data-ttu-id="377ff-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="377ff-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="377ff-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="377ff-111">Remarks</span></span>  
 <span data-ttu-id="377ff-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="377ff-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="377ff-113">Требования</span><span class="sxs-lookup"><span data-stu-id="377ff-113">Requirements</span></span>  
 <span data-ttu-id="377ff-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="377ff-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="377ff-115">См. также</span><span class="sxs-lookup"><span data-stu-id="377ff-115">See Also</span></span>  
 [<span data-ttu-id="377ff-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="377ff-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
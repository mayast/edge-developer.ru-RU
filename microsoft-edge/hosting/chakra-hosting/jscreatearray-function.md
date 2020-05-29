---
description: Создает объект-массив JavaScript.
title: Функция JsCreateArray | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fb6a65df1484eb308224a42bb5a65443855c6215
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571446"
---
# <span data-ttu-id="b521f-103">Функция JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="b521f-103">JsCreateArray Function</span></span>
<span data-ttu-id="b521f-104">Создает объект-массив JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b521f-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="b521f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b521f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="b521f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b521f-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="b521f-107">Начальная длина массива.</span><span class="sxs-lookup"><span data-stu-id="b521f-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="b521f-108">Новый объект массива.</span><span class="sxs-lookup"><span data-stu-id="b521f-108">The new array object.</span></span>  
  
## <span data-ttu-id="b521f-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b521f-109">Return Value</span></span>  
 <span data-ttu-id="b521f-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b521f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b521f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b521f-111">Remarks</span></span>  
 <span data-ttu-id="b521f-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="b521f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b521f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b521f-113">Requirements</span></span>  
 <span data-ttu-id="b521f-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b521f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b521f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b521f-115">See Also</span></span>  
 [<span data-ttu-id="b521f-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b521f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Получает текущий контекст скрипта в потоке.
title: Функция JsGetCurrentContext | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 78f04674aab8783c43f22516903669e0f9b7543b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571396"
---
# <span data-ttu-id="54fd9-103">Функция JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="54fd9-103">JsGetCurrentContext Function</span></span>
<span data-ttu-id="54fd9-104">Получает текущий контекст скрипта в потоке.</span><span class="sxs-lookup"><span data-stu-id="54fd9-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="54fd9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54fd9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="54fd9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54fd9-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="54fd9-107">Контекст текущего скрипта в потоке, значение null, если контекст текущего скрипта отсутствует.</span><span class="sxs-lookup"><span data-stu-id="54fd9-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="54fd9-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="54fd9-108">Return Value</span></span>  
 <span data-ttu-id="54fd9-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="54fd9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="54fd9-110">Требования</span><span class="sxs-lookup"><span data-stu-id="54fd9-110">Requirements</span></span>  
 <span data-ttu-id="54fd9-111">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="54fd9-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="54fd9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="54fd9-112">See Also</span></span>  
 [<span data-ttu-id="54fd9-113">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="54fd9-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
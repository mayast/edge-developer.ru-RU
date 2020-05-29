---
description: Создает новую функцию JavaScript.
title: Функция JsCreateFunction | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 22585afcb379c281eda621c3b233ccf4bc278ad1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571432"
---
# <span data-ttu-id="9a262-103">Функция JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="9a262-103">JsCreateFunction Function</span></span>
<span data-ttu-id="9a262-104">Создает новую функцию JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9a262-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="9a262-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a262-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="9a262-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a262-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="9a262-107">Метод, который нужно вызвать при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="9a262-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="9a262-108">Определяемое пользователем состояние, которое будет передано обратно обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="9a262-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="9a262-109">Новый объект Function.</span><span class="sxs-lookup"><span data-stu-id="9a262-109">The new function object.</span></span>  
  
## <span data-ttu-id="9a262-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="9a262-110">Return Value</span></span>  
 <span data-ttu-id="9a262-111">Результат звонка (если таковой имеется).</span><span class="sxs-lookup"><span data-stu-id="9a262-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="9a262-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a262-112">Remarks</span></span>  
 <span data-ttu-id="9a262-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="9a262-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9a262-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9a262-114">Requirements</span></span>  
 <span data-ttu-id="9a262-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9a262-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9a262-116">См. также</span><span class="sxs-lookup"><span data-stu-id="9a262-116">See Also</span></span>  
 [<span data-ttu-id="9a262-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9a262-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
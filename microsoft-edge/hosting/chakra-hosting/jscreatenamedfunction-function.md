---
description: Создает новую функцию JavaScript с именем.
title: Функция JsCreateNamedFunction | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d963fe196b8e56394e22501ed3898a0d887a3d3b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571430"
---
# <span data-ttu-id="f8e01-103">Функция JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="f8e01-103">JsCreateNamedFunction Function</span></span>
<span data-ttu-id="f8e01-104">Создает новую функцию JavaScript с именем.</span><span class="sxs-lookup"><span data-stu-id="f8e01-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="f8e01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8e01-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="f8e01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8e01-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="f8e01-107">Имя функции, которая будет использоваться в целях диагностики и stringification.</span><span class="sxs-lookup"><span data-stu-id="f8e01-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="f8e01-108">Метод, который нужно вызвать при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="f8e01-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="f8e01-109">Указанное пользователем состояние, которое будет передано обратно обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="f8e01-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="f8e01-110">Новый объект Function.</span><span class="sxs-lookup"><span data-stu-id="f8e01-110">The new function object.</span></span>  
  
## <span data-ttu-id="f8e01-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f8e01-111">Return Value</span></span>  
  
## <span data-ttu-id="f8e01-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8e01-112">Remarks</span></span>  
 <span data-ttu-id="f8e01-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="f8e01-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f8e01-114">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f8e01-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="f8e01-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f8e01-115">Requirements</span></span>  
 <span data-ttu-id="f8e01-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f8e01-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f8e01-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f8e01-117">See Also</span></span>  
 [<span data-ttu-id="f8e01-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f8e01-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
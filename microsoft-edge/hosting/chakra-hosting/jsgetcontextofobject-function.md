---
description: Возвращает контекст скрипта, которому принадлежит объект.
title: Функция JsGetContextOfObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4f1b996954e877d9c98ac0caf06f255af629a386
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571400"
---
# <span data-ttu-id="875a5-103">Функция JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="875a5-103">JsGetContextOfObject Function</span></span>
<span data-ttu-id="875a5-104">Возвращает контекст скрипта, которому принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="875a5-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="875a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="875a5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="875a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="875a5-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="875a5-107">Объект, из которого нужно получить контекст.</span><span class="sxs-lookup"><span data-stu-id="875a5-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="875a5-108">Контекст, которому принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="875a5-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="875a5-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="875a5-109">Return Value</span></span>  
 <span data-ttu-id="875a5-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="875a5-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="875a5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="875a5-111">Remarks</span></span>  
 <span data-ttu-id="875a5-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="875a5-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="875a5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="875a5-113">Requirements</span></span>  
 <span data-ttu-id="875a5-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="875a5-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="875a5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="875a5-115">See Also</span></span>  
 [<span data-ttu-id="875a5-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="875a5-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
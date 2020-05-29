---
description: Задает прототип объекта.
title: Функция JsSetPrototype | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 625269c5f9f459a5c7eecb6cfc31cb85fc24214b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572355"
---
# <span data-ttu-id="c5fca-103">Функция JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="c5fca-103">JsSetPrototype Function</span></span>
<span data-ttu-id="c5fca-104">Задает прототип объекта.</span><span class="sxs-lookup"><span data-stu-id="c5fca-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="c5fca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5fca-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="c5fca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5fca-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="c5fca-107">Объект, прототип которого нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c5fca-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="c5fca-108">Новый прототип объекта.</span><span class="sxs-lookup"><span data-stu-id="c5fca-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="c5fca-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="c5fca-109">Return Value</span></span>  
 <span data-ttu-id="c5fca-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c5fca-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c5fca-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5fca-111">Remarks</span></span>  
 <span data-ttu-id="c5fca-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="c5fca-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c5fca-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c5fca-113">Requirements</span></span>  
 <span data-ttu-id="c5fca-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c5fca-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c5fca-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c5fca-115">See Also</span></span>  
 [<span data-ttu-id="c5fca-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c5fca-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
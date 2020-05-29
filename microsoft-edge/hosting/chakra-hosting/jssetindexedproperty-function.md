---
description: Установка значения по указанному индексу объекта.
title: Функция JsSetIndexedProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 893849c42d9cbf0de160846d3397fcd5d7c77b7b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572442"
---
# <span data-ttu-id="62528-103">Функция JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="62528-103">JsSetIndexedProperty Function</span></span>
<span data-ttu-id="62528-104">Установка значения по указанному индексу объекта.</span><span class="sxs-lookup"><span data-stu-id="62528-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="62528-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62528-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="62528-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62528-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="62528-107">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="62528-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="62528-108">Устанавливаемый индекс.</span><span class="sxs-lookup"><span data-stu-id="62528-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="62528-109">Значение, которое нужно установить.</span><span class="sxs-lookup"><span data-stu-id="62528-109">The value to set.</span></span>  
  
## <span data-ttu-id="62528-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="62528-110">Return Value</span></span>  
 <span data-ttu-id="62528-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="62528-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="62528-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62528-112">Remarks</span></span>  
 <span data-ttu-id="62528-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="62528-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="62528-114">Требования</span><span class="sxs-lookup"><span data-stu-id="62528-114">Requirements</span></span>  
 <span data-ttu-id="62528-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="62528-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="62528-116">См. также</span><span class="sxs-lookup"><span data-stu-id="62528-116">See Also</span></span>  
 [<span data-ttu-id="62528-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="62528-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
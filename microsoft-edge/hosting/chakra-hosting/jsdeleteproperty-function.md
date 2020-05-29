---
description: Удаляет свойство объекта.
title: Функция JsDeleteProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c5539238324d59126b45f19fa9a6f8facc0f2ee3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571408"
---
# <span data-ttu-id="b8b87-103">Функция JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="b8b87-103">JsDeleteProperty Function</span></span>
<span data-ttu-id="b8b87-104">Удаляет свойство объекта.</span><span class="sxs-lookup"><span data-stu-id="b8b87-104">Deletes an object's property.</span></span>  
  
## <span data-ttu-id="b8b87-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8b87-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="b8b87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8b87-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b8b87-107">Объект, содержащий свойство.</span><span class="sxs-lookup"><span data-stu-id="b8b87-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="b8b87-108">Идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="b8b87-108">The ID of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="b8b87-109">Набор свойств должен соответствовать правилам строгого режима.</span><span class="sxs-lookup"><span data-stu-id="b8b87-109">The property set should follow strict mode rules.</span></span>  
  
 `result`  
 <span data-ttu-id="b8b87-110">Удалено ли свойство.</span><span class="sxs-lookup"><span data-stu-id="b8b87-110">Whether the property was deleted.</span></span>  
  
## <span data-ttu-id="b8b87-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b8b87-111">Return Value</span></span>  
 <span data-ttu-id="b8b87-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b8b87-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b8b87-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8b87-113">Remarks</span></span>  
 <span data-ttu-id="b8b87-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="b8b87-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b8b87-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b8b87-115">Requirements</span></span>  
 <span data-ttu-id="b8b87-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b8b87-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b8b87-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b8b87-117">See Also</span></span>  
 [<span data-ttu-id="b8b87-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b8b87-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
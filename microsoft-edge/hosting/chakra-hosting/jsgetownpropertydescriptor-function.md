---
description: Получает дескриптор свойства для собственного свойства объекта.
title: Функция JsGetOwnPropertyDescriptor | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6f500aec8b892cb2ad437bd7159ab14165a8bfb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572524"
---
# <span data-ttu-id="c469c-103">Функция JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="c469c-103">JsGetOwnPropertyDescriptor Function</span></span>
<span data-ttu-id="c469c-104">Получает дескриптор свойства для собственного свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="c469c-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="c469c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c469c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="c469c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c469c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="c469c-107">Объект со свойством.</span><span class="sxs-lookup"><span data-stu-id="c469c-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="c469c-108">Идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="c469c-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="c469c-109">Дескриптор свойства.</span><span class="sxs-lookup"><span data-stu-id="c469c-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="c469c-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="c469c-110">Return Value</span></span>  
 <span data-ttu-id="c469c-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c469c-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c469c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c469c-112">Remarks</span></span>  
 <span data-ttu-id="c469c-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="c469c-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c469c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c469c-114">Requirements</span></span>  
 <span data-ttu-id="c469c-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c469c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c469c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="c469c-116">See Also</span></span>  
 [<span data-ttu-id="c469c-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c469c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
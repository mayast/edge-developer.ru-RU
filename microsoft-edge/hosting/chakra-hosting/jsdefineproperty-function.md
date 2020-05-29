---
description: Определяет собственное свойство нового объекта из дескриптора свойств.
title: Функция JsDefineProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c9641b4d00540670b44d1718a6aa2aca3b02de
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571410"
---
# <span data-ttu-id="b9f89-103">Функция JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="b9f89-103">JsDefineProperty Function</span></span>
<span data-ttu-id="b9f89-104">Определяет собственное свойство нового объекта из дескриптора свойств.</span><span class="sxs-lookup"><span data-stu-id="b9f89-104">Defines a new object's own property from a property descriptor.</span></span>  
  
## <span data-ttu-id="b9f89-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9f89-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="b9f89-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9f89-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b9f89-107">Объект со свойством.</span><span class="sxs-lookup"><span data-stu-id="b9f89-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="b9f89-108">Идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="b9f89-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="b9f89-109">Дескриптор свойства.</span><span class="sxs-lookup"><span data-stu-id="b9f89-109">The property descriptor.</span></span>  
  
 `result`  
 <span data-ttu-id="b9f89-110">Определено ли свойство.</span><span class="sxs-lookup"><span data-stu-id="b9f89-110">Whether the property was defined.</span></span>  
  
## <span data-ttu-id="b9f89-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b9f89-111">Return Value</span></span>  
 <span data-ttu-id="b9f89-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b9f89-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b9f89-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9f89-113">Remarks</span></span>  
 <span data-ttu-id="b9f89-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="b9f89-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b9f89-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b9f89-115">Requirements</span></span>  
 <span data-ttu-id="b9f89-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b9f89-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b9f89-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b9f89-117">See Also</span></span>  
 [<span data-ttu-id="b9f89-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b9f89-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Возвращает значение, указывающее, является ли объект расширяемым.
title: Функция JsGetExtensionAllowed | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3baa6449294f7b055251d861a32095deb1bdfe9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571392"
---
# <span data-ttu-id="99bcc-103">Функция JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="99bcc-103">JsGetExtensionAllowed Function</span></span>
<span data-ttu-id="99bcc-104">Возвращает значение, указывающее, является ли объект расширяемым.</span><span class="sxs-lookup"><span data-stu-id="99bcc-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="99bcc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99bcc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="99bcc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99bcc-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="99bcc-107">Проверяемый объект.</span><span class="sxs-lookup"><span data-stu-id="99bcc-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="99bcc-108">Является ли объект расширяемым.</span><span class="sxs-lookup"><span data-stu-id="99bcc-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="99bcc-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="99bcc-109">Return Value</span></span>  
 <span data-ttu-id="99bcc-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="99bcc-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="99bcc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99bcc-111">Remarks</span></span>  
 <span data-ttu-id="99bcc-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="99bcc-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="99bcc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="99bcc-113">Requirements</span></span>  
 <span data-ttu-id="99bcc-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="99bcc-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="99bcc-115">См. также</span><span class="sxs-lookup"><span data-stu-id="99bcc-115">See Also</span></span>  
 [<span data-ttu-id="99bcc-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="99bcc-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Создает новый объект, в котором хранятся некоторые внешние данные.
title: Функция JsCreateExternalObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9a68f4befea7dc7c3369bcade475e29d53342730
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571433"
---
# <span data-ttu-id="dff01-103">Функция JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="dff01-103">JsCreateExternalObject Function</span></span>
<span data-ttu-id="dff01-104">Создает новый объект, в котором хранятся некоторые внешние данные.</span><span class="sxs-lookup"><span data-stu-id="dff01-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="dff01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dff01-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="dff01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dff01-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="dff01-107">Внешние данные, которые будет представлять объект.</span><span class="sxs-lookup"><span data-stu-id="dff01-107">External data that the object will represent.</span></span> <span data-ttu-id="dff01-108">Может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="dff01-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="dff01-109">Обратный вызов для завершения работы объекта.</span><span class="sxs-lookup"><span data-stu-id="dff01-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="dff01-110">Может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="dff01-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="dff01-111">Новый объект.</span><span class="sxs-lookup"><span data-stu-id="dff01-111">The new object.</span></span>  
  
## <span data-ttu-id="dff01-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="dff01-112">Return Value</span></span>  
 <span data-ttu-id="dff01-113">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dff01-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dff01-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dff01-114">Remarks</span></span>  
 <span data-ttu-id="dff01-115">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="dff01-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dff01-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dff01-116">Requirements</span></span>  
 <span data-ttu-id="dff01-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dff01-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dff01-118">См. также</span><span class="sxs-lookup"><span data-stu-id="dff01-118">See Also</span></span>  
 [<span data-ttu-id="dff01-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dff01-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
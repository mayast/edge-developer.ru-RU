---
description: Выполняет `instanceof` проверку оператора JavaScript.
title: Функция JsInstanceOf | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3a7e2397abe5dcb25346e583a0fdab301b8b45f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571365"
---
# <span data-ttu-id="cb13c-103">Функция JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="cb13c-103">JsInstanceOf Function</span></span>
<span data-ttu-id="cb13c-104">Выполняет `instanceof` проверку оператора JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cb13c-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="cb13c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb13c-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="cb13c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb13c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="cb13c-107">Проверяемый объект.</span><span class="sxs-lookup"><span data-stu-id="cb13c-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="cb13c-108">Функция конструктора для проверки.</span><span class="sxs-lookup"><span data-stu-id="cb13c-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="cb13c-109">Значение, определяющее, имеет ли instanceof конструктор Object.</span><span class="sxs-lookup"><span data-stu-id="cb13c-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="cb13c-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="cb13c-110">Return Value</span></span>  
 <span data-ttu-id="cb13c-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cb13c-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cb13c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb13c-112">Remarks</span></span>  
 <span data-ttu-id="cb13c-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="cb13c-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cb13c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cb13c-114">Requirements</span></span>  
 <span data-ttu-id="cb13c-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cb13c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cb13c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="cb13c-116">See Also</span></span>  
 [<span data-ttu-id="cb13c-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cb13c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
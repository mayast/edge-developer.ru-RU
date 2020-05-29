---
description: Задает в качестве среды выполнения текущего контекста состояние исключения.
title: Функция JsSetException | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572449"
---
# <span data-ttu-id="1ebf8-103">Функция JsSetException</span><span class="sxs-lookup"><span data-stu-id="1ebf8-103">JsSetException Function</span></span>
<span data-ttu-id="1ebf8-104">Задает в качестве среды выполнения текущего контекста состояние исключения.</span><span class="sxs-lookup"><span data-stu-id="1ebf8-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="1ebf8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ebf8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="1ebf8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ebf8-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="1ebf8-107">Исключение JavaScript, которое необходимо установить для среды выполнения текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="1ebf8-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="1ebf8-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="1ebf8-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="1ebf8-109">Если обработчик установил состояние исключения, в противном случае — код ошибки.</span><span class="sxs-lookup"><span data-stu-id="1ebf8-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1ebf8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ebf8-110">Remarks</span></span>  
 <span data-ttu-id="1ebf8-111">Если среда выполнения текущего контекста уже находится в состоянии исключения, этот API будет возвращен `JsErrorInExceptionState` .</span><span class="sxs-lookup"><span data-stu-id="1ebf8-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="1ebf8-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="1ebf8-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1ebf8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1ebf8-113">Requirements</span></span>  
 <span data-ttu-id="1ebf8-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1ebf8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1ebf8-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1ebf8-115">See Also</span></span>  
 [<span data-ttu-id="1ebf8-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1ebf8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
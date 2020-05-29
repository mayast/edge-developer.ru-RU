---
description: 'Задает функцию обратного вызова, вызываемую средой выполнения перед сборкой мусора. '
title: Функция JsSetRuntimeBeforeCollectCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 31aefd28698c14a6fe17421a990a7c8b120876bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572343"
---
# <span data-ttu-id="dcbbe-103">Функция JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="dcbbe-103">JsSetRuntimeBeforeCollectCallback Function</span></span>
<span data-ttu-id="dcbbe-104">Задает функцию обратного вызова, вызываемую средой выполнения перед сборкой мусора.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-104">Sets a callback function that is called by the runtime before garbage collection.</span></span>  
  
## <span data-ttu-id="dcbbe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcbbe-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="dcbbe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcbbe-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="dcbbe-107">Среда выполнения, для которой регистрируется обратный вызов выделения.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="dcbbe-108">Указанное пользователем состояние, которое будет передано обратно обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-108">User provided state that will be passed back to the callback.</span></span>  
  
 `beforeCollectCallback`  
 <span data-ttu-id="dcbbe-109">Задается функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-109">The callback function being set.</span></span>  
  
## <span data-ttu-id="dcbbe-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="dcbbe-110">Return Value</span></span>  
 <span data-ttu-id="dcbbe-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dcbbe-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcbbe-112">Remarks</span></span>  
 <span data-ttu-id="dcbbe-113">Обратный вызов вызывается в текущем потоке выполнения среды выполнения, поэтому выполнение блокируется до тех пор, пока не завершится обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-113">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="dcbbe-114">Обратный вызов может использоваться узлами для подготовки к сбору мусора.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-114">The callback can be used by hosts to prepare for garbage collection.</span></span> <span data-ttu-id="dcbbe-115">Например, освобождая ненужные ссылки на объекты Chakra.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-115">For example, by releasing unnecessary references on Chakra objects.</span></span>  
  
## <span data-ttu-id="dcbbe-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dcbbe-116">Requirements</span></span>  
 <span data-ttu-id="dcbbe-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dcbbe-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dcbbe-118">См. также</span><span class="sxs-lookup"><span data-stu-id="dcbbe-118">See Also</span></span>  
 [<span data-ttu-id="dcbbe-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dcbbe-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
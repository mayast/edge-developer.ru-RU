---
description: Задает функцию обратного вызова, вызываемую средой выполнения перед сборкой мусора объекта.
title: Функция JsSetObjectBeforeCollectCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 77a59c6ace96809c0b232c96aa9639555e7badcd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572440"
---
# <span data-ttu-id="02370-103">Функция JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="02370-103">JsSetObjectBeforeCollectCallback Function</span></span>
<span data-ttu-id="02370-104">Задает функцию обратного вызова, вызываемую средой выполнения перед сборкой мусора объекта.</span><span class="sxs-lookup"><span data-stu-id="02370-104">Sets a callback function that is called by the runtime before garbage collection of an object.</span></span>  
  
## <span data-ttu-id="02370-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02370-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="02370-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="02370-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="02370-107">Объект, для которого регистрируется обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="02370-107">The object for which to register the callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="02370-108">Определяемое пользователем состояние, которое будет передано обратно обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="02370-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `objectBeforeCollectCallback`  
 <span data-ttu-id="02370-109">Задается функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="02370-109">The callback function being set.</span></span> <span data-ttu-id="02370-110">Используйте значение null, чтобы удалить ранее зарегистрированный обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="02370-110">Use null to clear previously registered callback.</span></span>  
  
## <span data-ttu-id="02370-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="02370-111">Return Value</span></span>  
 <span data-ttu-id="02370-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="02370-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="02370-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02370-113">Remarks</span></span>  
 <span data-ttu-id="02370-114">Обратный вызов вызывается в текущем потоке выполнения среды выполнения, поэтому выполнение блокируется до тех пор, пока не завершится обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="02370-114">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="02370-115">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="02370-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="02370-116">Требования</span><span class="sxs-lookup"><span data-stu-id="02370-116">Requirements</span></span>  
 <span data-ttu-id="02370-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="02370-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="02370-118">См. также</span><span class="sxs-lookup"><span data-stu-id="02370-118">See Also</span></span>  
 [<span data-ttu-id="02370-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="02370-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
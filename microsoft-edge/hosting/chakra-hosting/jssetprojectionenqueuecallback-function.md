---
description: Задает метод обратного вызова, который должен использоваться для того, чтобы вызвать завершение проекции для потока вызывающих абонентов.
title: Функция JsSetProjectionEnqueueCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 02da0238360b0dc6fff9bb86c9f5ab04d1ba7112
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572436"
---
# <span data-ttu-id="d136d-103">Функция JsSetProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="d136d-103">JsSetProjectionEnqueueCallback Function</span></span>
<span data-ttu-id="d136d-104">Задает метод обратного вызова, который должен использоваться для того, чтобы вызвать завершение проекции для потока вызывающих абонентов.</span><span class="sxs-lookup"><span data-stu-id="d136d-104">Sets the callback to be used in order to invoke a projection completion back to the callers required thread.</span></span>  
  
## <span data-ttu-id="d136d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d136d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### <span data-ttu-id="d136d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d136d-106">Parameters</span></span>  
 `projectionEnqueueContext`  
 <span data-ttu-id="d136d-107">Обратный вызов, который будет вызываться каждый раз, когда завершение проекции выполняется в фоновом потоке.</span><span class="sxs-lookup"><span data-stu-id="d136d-107">The callback that will be invoked any time a projection completion occurs on a background thread.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="d136d-108">Контекст приложения, представленный в `projectionEnqueueContext` .</span><span class="sxs-lookup"><span data-stu-id="d136d-108">The application context provided to `projectionEnqueueContext`.</span></span>  
  
## <span data-ttu-id="d136d-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="d136d-109">Return Value</span></span>  
 <span data-ttu-id="d136d-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d136d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d136d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d136d-111">Remarks</span></span>  
 <span data-ttu-id="d136d-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="d136d-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d136d-113">Вызов должен выполняться из другого апартамента COM или из другого потока в том же MTA.</span><span class="sxs-lookup"><span data-stu-id="d136d-113">The call should be coming from a different COM apartment or from a different thread in the same MTA.</span></span>  
  
 <span data-ttu-id="d136d-114">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d136d-114">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="d136d-115">Для этого API в настоящее время не поддерживается PInvoke.</span><span class="sxs-lookup"><span data-stu-id="d136d-115">PInvoke is not currently supported for this API.</span></span>  
  
## <span data-ttu-id="d136d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d136d-116">Requirements</span></span>  
 <span data-ttu-id="d136d-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d136d-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d136d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d136d-118">See Also</span></span>  
 [<span data-ttu-id="d136d-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d136d-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
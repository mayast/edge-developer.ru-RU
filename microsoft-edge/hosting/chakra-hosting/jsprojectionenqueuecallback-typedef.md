---
description: Обратный вызов приложения, вызываемый функцией JsRT, когда интерфейс API проекции завершается в потоке, отличном от исходного.
title: JsProjectionEnqueueCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571344"
---
# <span data-ttu-id="1119b-103">JsProjectionEnqueueCallback typedef</span><span class="sxs-lookup"><span data-stu-id="1119b-103">JsProjectionEnqueueCallback Typedef</span></span>
<span data-ttu-id="1119b-104">Обратный вызов приложения, вызываемый функцией JsRT, когда интерфейс API проекции завершается в потоке, отличном от исходного.</span><span class="sxs-lookup"><span data-stu-id="1119b-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="1119b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1119b-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="1119b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1119b-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="1119b-107">Обратный вызов, вызываемый в исходном потоке.</span><span class="sxs-lookup"><span data-stu-id="1119b-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="1119b-108">Контекст приложения.</span><span class="sxs-lookup"><span data-stu-id="1119b-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="1119b-109">Контекст JsRT, который необходимо передать `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="1119b-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="1119b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1119b-110">Remarks</span></span>  
 <span data-ttu-id="1119b-111">Требуется вызов JsSetProjectionEnqueueCallback для получения обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="1119b-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="1119b-112">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="1119b-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="1119b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1119b-113">Requirements</span></span>  
 <span data-ttu-id="1119b-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1119b-114">jsrt.h</span></span>  
  
## <span data-ttu-id="1119b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1119b-115">See Also</span></span>  
 [<span data-ttu-id="1119b-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1119b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
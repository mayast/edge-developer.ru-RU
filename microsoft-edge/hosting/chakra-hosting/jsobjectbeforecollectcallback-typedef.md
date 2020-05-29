---
description: Обратный вызов, вызываемый перед сбором объекта.
title: JsObjectBeforeCollectCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 27bbd1aed72cc751397ac4e6734f107612653b66
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571348"
---
# <span data-ttu-id="227b9-103">JsObjectBeforeCollectCallback typedef</span><span class="sxs-lookup"><span data-stu-id="227b9-103">JsObjectBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="227b9-104">Обратный вызов, вызываемый перед сбором объекта.</span><span class="sxs-lookup"><span data-stu-id="227b9-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="227b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="227b9-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="227b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="227b9-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="227b9-107">Объект, который нужно собрать.</span><span class="sxs-lookup"><span data-stu-id="227b9-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="227b9-108">Состояние, в которое передается `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="227b9-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="227b9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="227b9-109">Remarks</span></span>  
 <span data-ttu-id="227b9-110">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="227b9-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="227b9-111">Требования</span><span class="sxs-lookup"><span data-stu-id="227b9-111">Requirements</span></span>  
 <span data-ttu-id="227b9-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="227b9-112">jsrt.h</span></span>  
  
## <span data-ttu-id="227b9-113">См. также</span><span class="sxs-lookup"><span data-stu-id="227b9-113">See Also</span></span>  
 [<span data-ttu-id="227b9-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="227b9-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
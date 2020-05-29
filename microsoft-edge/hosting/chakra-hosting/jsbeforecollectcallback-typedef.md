---
description: Обратный вызов, вызванный перед коллекцией.
title: JsBeforeCollectCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 17f279c2d2ffcc8d02819994dddebfc22baa4cab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571467"
---
# <span data-ttu-id="c6224-103">JsBeforeCollectCallback typedef</span><span class="sxs-lookup"><span data-stu-id="c6224-103">JsBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="c6224-104">Обратный вызов, вызванный перед коллекцией.</span><span class="sxs-lookup"><span data-stu-id="c6224-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="c6224-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6224-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="c6224-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6224-106">Parameters</span></span>  
 <span data-ttu-id="c6224-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="c6224-107">callbackState</span></span>  
 <span data-ttu-id="c6224-108">Состояние, передаваемое в JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="c6224-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="c6224-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6224-109">Remarks</span></span>  
 <span data-ttu-id="c6224-110">Для регистрации этого обратного вызова используйте JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="c6224-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="c6224-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c6224-111">Requirements</span></span>  
 <span data-ttu-id="c6224-112">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c6224-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c6224-113">См. также</span><span class="sxs-lookup"><span data-stu-id="c6224-113">See Also</span></span>  
 [<span data-ttu-id="c6224-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c6224-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
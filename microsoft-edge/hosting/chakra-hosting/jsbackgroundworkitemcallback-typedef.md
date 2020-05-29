---
description: Обратный вызов фонового рабочего элемента.
title: JsBackgroundWorkItemCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571470"
---
# <span data-ttu-id="8f2c3-103">JsBackgroundWorkItemCallback typedef</span><span class="sxs-lookup"><span data-stu-id="8f2c3-103">JsBackgroundWorkItemCallback Typedef</span></span>
<span data-ttu-id="8f2c3-104">Обратный вызов фонового рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="8f2c3-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="8f2c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f2c3-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="8f2c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f2c3-106">Parameters</span></span>  
 <span data-ttu-id="8f2c3-107">callbackData</span><span class="sxs-lookup"><span data-stu-id="8f2c3-107">callbackData</span></span>  
 <span data-ttu-id="8f2c3-108">Аргумент данных, передаваемый службе потока.</span><span class="sxs-lookup"><span data-stu-id="8f2c3-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="8f2c3-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f2c3-109">Remarks</span></span>  
 <span data-ttu-id="8f2c3-110">Это значение передается службе потока узла (если она предоставлена), чтобы разрешить ведущему приложению вызвать обратный вызов рабочего элемента в фоновом потоке выбора.</span><span class="sxs-lookup"><span data-stu-id="8f2c3-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="8f2c3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="8f2c3-111">Requirements</span></span>  
 <span data-ttu-id="8f2c3-112">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8f2c3-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8f2c3-113">См. также</span><span class="sxs-lookup"><span data-stu-id="8f2c3-113">See Also</span></span>  
 [<span data-ttu-id="8f2c3-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8f2c3-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
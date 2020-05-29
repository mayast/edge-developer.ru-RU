---
description: Задает внутренние данные JsrtContext.
title: Функция JsSetContextData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 00521bafdaf6125dd15746de8a1d403eaf03b4a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572452"
---
# <span data-ttu-id="ec2d1-103">Функция JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="ec2d1-103">JsSetContextData Function</span></span>
<span data-ttu-id="ec2d1-104">Задает внутренние данные JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="ec2d1-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="ec2d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec2d1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="ec2d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec2d1-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="ec2d1-107">Контекст, для которого необходимо установить данные.</span><span class="sxs-lookup"><span data-stu-id="ec2d1-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="ec2d1-108">Указатель на данные, которые нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="ec2d1-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="ec2d1-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ec2d1-109">Return Value</span></span>  
 <span data-ttu-id="ec2d1-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ec2d1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ec2d1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec2d1-111">Remarks</span></span>  
 <span data-ttu-id="ec2d1-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="ec2d1-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ec2d1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ec2d1-113">Requirements</span></span>  
 <span data-ttu-id="ec2d1-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ec2d1-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ec2d1-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ec2d1-115">See Also</span></span>  
 [<span data-ttu-id="ec2d1-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ec2d1-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
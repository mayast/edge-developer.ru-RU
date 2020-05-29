---
description: Обратный вызов службы Threading.
title: JsThreadServiceCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571336"
---
# <span data-ttu-id="582ae-103">JsThreadServiceCallback typedef</span><span class="sxs-lookup"><span data-stu-id="582ae-103">JsThreadServiceCallback Typedef</span></span>
<span data-ttu-id="582ae-104">Обратный вызов службы Threading.</span><span class="sxs-lookup"><span data-stu-id="582ae-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="582ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="582ae-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="582ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="582ae-106">Parameters</span></span>  
 <span data-ttu-id="582ae-107">предусмотрен</span><span class="sxs-lookup"><span data-stu-id="582ae-107">callback</span></span>  
 <span data-ttu-id="582ae-108">Обратный вызов для элемента фоновой задачи.</span><span class="sxs-lookup"><span data-stu-id="582ae-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="582ae-109">callbackData</span><span class="sxs-lookup"><span data-stu-id="582ae-109">callbackData</span></span>  
 <span data-ttu-id="582ae-110">Аргумент данных, передаваемый обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="582ae-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="582ae-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="582ae-111">Remarks</span></span>  
 <span data-ttu-id="582ae-112">Ведущее приложение может указать службу фонового потока при вызове JsCreateRuntime.</span><span class="sxs-lookup"><span data-stu-id="582ae-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="582ae-113">Если задано, фоновые рабочие элементы будут переданы узлу с помощью этого обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="582ae-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="582ae-114">Предполагается, что основное приложение либо сразу же начинает выполнение фонового рабочего элемента, и возвращает значение true, и среда выполнения будет обрабатывать рабочий элемент in-Thread.</span><span class="sxs-lookup"><span data-stu-id="582ae-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="582ae-115">Требования</span><span class="sxs-lookup"><span data-stu-id="582ae-115">Requirements</span></span>  
 <span data-ttu-id="582ae-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="582ae-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="582ae-117">См. также</span><span class="sxs-lookup"><span data-stu-id="582ae-117">See Also</span></span>  
 [<span data-ttu-id="582ae-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="582ae-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
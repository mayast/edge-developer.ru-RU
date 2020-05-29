---
description: Выполняет сериализованный сценарий.
title: Функция JsRunSerializedScript | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1e2fb7fdc5df52fde3b7cc59cf9173d658782a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572470"
---
# <span data-ttu-id="f5f1e-103">Функция JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="f5f1e-103">JsRunSerializedScript Function</span></span>
<span data-ttu-id="f5f1e-104">Выполняет сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-104">Runs a serialized script.</span></span>  
  
## <span data-ttu-id="f5f1e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5f1e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="f5f1e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5f1e-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="f5f1e-107">Исходный код сериализованного сценария.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-107">The source code of the serialized script.</span></span>  
  
 `buffer`  
 <span data-ttu-id="f5f1e-108">Сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="f5f1e-109">Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="f5f1e-110">Расположение, из которого получен сценарий.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="f5f1e-111">Результат выполнения сценария, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-111">The result of running the script, if any.</span></span> <span data-ttu-id="f5f1e-112">Этот параметр может быть равен null.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-112">This parameter can be null.</span></span>  
  
## <span data-ttu-id="f5f1e-113">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f5f1e-113">Return Value</span></span>  
 <span data-ttu-id="f5f1e-114">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f5f1e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5f1e-115">Remarks</span></span>  
 <span data-ttu-id="f5f1e-116">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f5f1e-117">Буфер не сохраняется в памяти обработчиком сценариев, поэтому ваш код должен поддерживать его, пока он может использоваться для выполнения сценариев.</span><span class="sxs-lookup"><span data-stu-id="f5f1e-117">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="f5f1e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f5f1e-118">Requirements</span></span>  
 <span data-ttu-id="f5f1e-119">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f5f1e-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f5f1e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f5f1e-120">See Also</span></span>  
 [<span data-ttu-id="f5f1e-121">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f5f1e-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
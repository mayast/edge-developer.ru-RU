---
description: Выполняет сериализованный сценарий. Обеспечивает возможность отложенной загрузки источника сценария только в том случае, если он необходим.
title: Функция JsRunSerializedScriptWithCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84a74d3c1aa68469dfe2fe42fdee685faa4c358c
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752222"
---
# <span data-ttu-id="c441b-104">Функция JsRunSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="c441b-104">JsRunSerializedScriptWithCallback Function</span></span>
<span data-ttu-id="c441b-105">Выполняет сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="c441b-105">Runs a serialized script.</span></span> <span data-ttu-id="c441b-106">Обеспечивает возможность отложенной загрузки источника сценария только в том случае, если он необходим.</span><span class="sxs-lookup"><span data-stu-id="c441b-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="c441b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c441b-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="c441b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c441b-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="c441b-109">Функция обратного вызова, вызываемая при необходимости загрузки исходного кода сценария.</span><span class="sxs-lookup"><span data-stu-id="c441b-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="c441b-110">Функция обратного вызова вызывается, когда сериализованный сценарий и исходный код больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="c441b-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="c441b-111">Сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="c441b-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="c441b-112">Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.</span><span class="sxs-lookup"><span data-stu-id="c441b-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="c441b-113">Этот контекст будет передан в scriptLoadCallback и scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="c441b-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="c441b-114">Расположение, из которого получен сценарий.</span><span class="sxs-lookup"><span data-stu-id="c441b-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="c441b-115">Результат выполнения сценария, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="c441b-115">The result of running the script, if any.</span></span> <span data-ttu-id="c441b-116">Этот параметр может быть равен null.</span><span class="sxs-lookup"><span data-stu-id="c441b-116">This parameter can be null.</span></span>  
  
## <span data-ttu-id="c441b-117">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="c441b-117">Return Value</span></span>  
 <span data-ttu-id="c441b-118">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c441b-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c441b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c441b-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c441b-120">Этот API пока не доступен для приложений Магазина.</span><span class="sxs-lookup"><span data-stu-id="c441b-120">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="c441b-121">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="c441b-121">Requires an active script context.</span></span>  
  
 <span data-ttu-id="c441b-122">Среда выполнения будет храниться в буфере до тех пор, пока все экземпляры функций, созданных из буфера, не будут собраны сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="c441b-122">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="c441b-123">Затем он вызывает scriptUnloadCallback для информирования вызывающего абонента о том, что он безопасно в целях освобождения.</span><span class="sxs-lookup"><span data-stu-id="c441b-123">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="c441b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c441b-124">Requirements</span></span>  
 <span data-ttu-id="c441b-125">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c441b-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c441b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c441b-126">See Also</span></span>  
 [<span data-ttu-id="c441b-127">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c441b-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
---
description: Анализирует сериализованный сценарий и возвращает функцию, которая представляет сценарий. Обеспечивает возможность отложенной загрузки источника сценария только в том случае, если он необходим.
title: Функция JsParseSerializedScriptWithCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0315fa82201671fc0ef0c950ef05a14a26be114e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752243"
---
# <span data-ttu-id="4bede-104">Функция JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="4bede-104">JsParseSerializedScriptWithCallback Function</span></span>
<span data-ttu-id="4bede-105">Анализирует сериализованный сценарий и возвращает функцию, которая представляет сценарий.</span><span class="sxs-lookup"><span data-stu-id="4bede-105">Parses a serialized script and returns a function representing the script.</span></span> <span data-ttu-id="4bede-106">Обеспечивает возможность отложенной загрузки источника сценария только в том случае, если он необходим.</span><span class="sxs-lookup"><span data-stu-id="4bede-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="4bede-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bede-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### <span data-ttu-id="4bede-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bede-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="4bede-109">Функция обратного вызова, вызываемая при необходимости загрузки исходного кода сценария.</span><span class="sxs-lookup"><span data-stu-id="4bede-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="4bede-110">Функция обратного вызова вызывается, когда сериализованный сценарий и исходный код больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="4bede-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="4bede-111">Сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="4bede-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="4bede-112">Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.</span><span class="sxs-lookup"><span data-stu-id="4bede-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="4bede-113">Этот контекст будет передан в scriptLoadCallback и scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="4bede-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="4bede-114">Расположение, из которого получен сценарий.</span><span class="sxs-lookup"><span data-stu-id="4bede-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="4bede-115">Функция, представляющая код сценария.</span><span class="sxs-lookup"><span data-stu-id="4bede-115">A function representing the script code.</span></span>  
  
## <span data-ttu-id="4bede-116">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="4bede-116">Return Value</span></span>  
 <span data-ttu-id="4bede-117">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4bede-117">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4bede-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bede-118">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4bede-119">Этот API пока не доступен для приложений Магазина.</span><span class="sxs-lookup"><span data-stu-id="4bede-119">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="4bede-120">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="4bede-120">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4bede-121">Среда выполнения будет храниться в буфере до тех пор, пока все экземпляры функций, созданных из буфера, не будут собраны сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="4bede-121">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="4bede-122">Затем он вызывает scriptUnloadCallback для информирования вызывающего абонента о том, что он безопасно в целях освобождения.</span><span class="sxs-lookup"><span data-stu-id="4bede-122">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="4bede-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4bede-123">Requirements</span></span>  
 <span data-ttu-id="4bede-124">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4bede-124">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4bede-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4bede-125">See Also</span></span>  
 [<span data-ttu-id="4bede-126">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4bede-126">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
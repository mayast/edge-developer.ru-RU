---
description: Вызывается средой выполнения для загрузки исходного кода сериализованного сценария. Вызывающий объект должен поддерживать буфер сценария, пока не будет `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 571314145cc19513f04174a9a1c93822a5795b29
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752201"
---
# <span data-ttu-id="a1a4f-104">JsSerializedScriptLoadSourceCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="a1a4f-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>
<span data-ttu-id="a1a4f-105">Вызывается средой выполнения для загрузки исходного кода сериализованного сценария.</span><span class="sxs-lookup"><span data-stu-id="a1a4f-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="a1a4f-106">Вызывающий объект должен поддерживать буфер сценария, пока не будет `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="a1a4f-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="a1a4f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1a4f-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="a1a4f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1a4f-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="a1a4f-109">Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="a1a4f-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="a1a4f-110">Возвращаемый сценарий.</span><span class="sxs-lookup"><span data-stu-id="a1a4f-110">The script returned.</span></span>  
  
## <span data-ttu-id="a1a4f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1a4f-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="a1a4f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a1a4f-112">Requirements</span></span>  
 <span data-ttu-id="a1a4f-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a1a4f-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a1a4f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a1a4f-114">See Also</span></span>  
 [<span data-ttu-id="a1a4f-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a1a4f-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
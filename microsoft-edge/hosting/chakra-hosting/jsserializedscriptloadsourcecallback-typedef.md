---
description: Вызывается средой выполнения для загрузки исходного кода сериализованного сценария. Вызывающий объект должен поддерживать буфер сценария, пока не будет `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1264bdc77da10cadb44a570ae37e7f3cd9ce6b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572456"
---
# <span data-ttu-id="8fe31-104">JsSerializedScriptLoadSourceCallback typedef</span><span class="sxs-lookup"><span data-stu-id="8fe31-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>
<span data-ttu-id="8fe31-105">Вызывается средой выполнения для загрузки исходного кода сериализованного сценария.</span><span class="sxs-lookup"><span data-stu-id="8fe31-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="8fe31-106">Вызывающий объект должен поддерживать буфер сценария, пока не будет `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="8fe31-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="8fe31-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fe31-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="8fe31-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fe31-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="8fe31-109">Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="8fe31-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="8fe31-110">Возвращаемый сценарий.</span><span class="sxs-lookup"><span data-stu-id="8fe31-110">The script returned.</span></span>  
  
## <span data-ttu-id="8fe31-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fe31-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="8fe31-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8fe31-112">Requirements</span></span>  
 <span data-ttu-id="8fe31-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8fe31-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8fe31-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8fe31-114">See Also</span></span>  
 [<span data-ttu-id="8fe31-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8fe31-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
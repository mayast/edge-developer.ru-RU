---
description: Вызывается средой выполнения, когда она завершает работу со всеми ресурсами, относящимися к выполнению сценария. Вызывающий объект должен освобождать источник, если в настоящее время загружено, байтовый код и контекст.
title: JsSerializedScriptUnloadCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572455"
---
# <span data-ttu-id="492a3-104">JsSerializedScriptUnloadCallback typedef</span><span class="sxs-lookup"><span data-stu-id="492a3-104">JsSerializedScriptUnloadCallback typedef</span></span>
<span data-ttu-id="492a3-105">Вызывается средой выполнения, когда она завершает работу со всеми ресурсами, относящимися к выполнению сценария.</span><span class="sxs-lookup"><span data-stu-id="492a3-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="492a3-106">Вызывающий объект должен освобождать источник, если в настоящее время загружено, байтовый код и контекст.</span><span class="sxs-lookup"><span data-stu-id="492a3-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="492a3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="492a3-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="492a3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="492a3-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="492a3-109">Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="492a3-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="492a3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="492a3-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="492a3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="492a3-111">Requirements</span></span>  
 <span data-ttu-id="492a3-112">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="492a3-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="492a3-113">См. также</span><span class="sxs-lookup"><span data-stu-id="492a3-113">See Also</span></span>  
 [<span data-ttu-id="492a3-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="492a3-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
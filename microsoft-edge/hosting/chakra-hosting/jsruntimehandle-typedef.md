---
description: Дескриптор среды выполнения Chakra.
title: JsRuntimeHandle typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572457"
---
# <span data-ttu-id="69deb-103">JsRuntimeHandle typedef</span><span class="sxs-lookup"><span data-stu-id="69deb-103">JsRuntimeHandle Typedef</span></span>
<span data-ttu-id="69deb-104">Дескриптор среды выполнения Chakra.</span><span class="sxs-lookup"><span data-stu-id="69deb-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="69deb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69deb-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="69deb-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69deb-106">Remarks</span></span>  
 <span data-ttu-id="69deb-107">У каждой среды выполнения Chakra есть собственный независимый обработчик выполнения, JIT-компилятор и куча, собранные сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="69deb-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="69deb-108">Таким образом, все среды выполнения полностью изолированы от других сред выполнения.</span><span class="sxs-lookup"><span data-stu-id="69deb-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="69deb-109">Среды выполнения можно использовать в любом потоке, но в любой момент можно вызвать среду выполнения только из одного потока.</span><span class="sxs-lookup"><span data-stu-id="69deb-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="69deb-110">JsRuntimeHandle, в отличие от других ссылок на объекты в API размещения Chakra, не собирается сборщиком мусора, так как он содержит саму кучу, в которой собрано мусора.</span><span class="sxs-lookup"><span data-stu-id="69deb-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="69deb-111">Среда выполнения продолжает существовать до тех пор, пока JsDisposeRuntime не будет вызван.</span><span class="sxs-lookup"><span data-stu-id="69deb-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="69deb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="69deb-112">Requirements</span></span>  
 <span data-ttu-id="69deb-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="69deb-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="69deb-114">См. также</span><span class="sxs-lookup"><span data-stu-id="69deb-114">See Also</span></span>  
 [<span data-ttu-id="69deb-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="69deb-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
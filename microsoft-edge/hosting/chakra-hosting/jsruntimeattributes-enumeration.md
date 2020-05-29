---
description: 'Атрибуты среды выполнения. '
title: Перечисление JsRuntimeAttributes | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9b8f6788f1de4988e3936701cfc742a564c92cfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572459"
---
# <span data-ttu-id="b1d5d-103">Перечисление JsRuntimeAttributes</span><span class="sxs-lookup"><span data-stu-id="b1d5d-103">JsRuntimeAttributes Enumeration</span></span>
<span data-ttu-id="b1d5d-104">Атрибуты среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-104">Attributes of a runtime.</span></span>  
  
## <span data-ttu-id="b1d5d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1d5d-105">Syntax</span></span>  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## <span data-ttu-id="b1d5d-106">Участников</span><span class="sxs-lookup"><span data-stu-id="b1d5d-106">Members</span></span>  
  
### <span data-ttu-id="b1d5d-107">Данные</span><span class="sxs-lookup"><span data-stu-id="b1d5d-107">Values</span></span>  
  
|<span data-ttu-id="b1d5d-108">Имя</span><span class="sxs-lookup"><span data-stu-id="b1d5d-108">Name</span></span>|<span data-ttu-id="b1d5d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b1d5d-109">Description</span></span>|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|<span data-ttu-id="b1d5d-110">Среда выполнения должна поддерживать надежное прерывание сценария.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-110">The runtime should support reliable script interruption.</span></span> <span data-ttu-id="b1d5d-111">Это позволяет увеличить количество мест, в которых среда выполнения будет проверять запрос на прерывание сценария с учетом затрат на небольшое количество производительности во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-111">This increases the number of places where the runtime will check for a script interrupt request at the cost of a small amount of runtime performance.</span></span>|  
|`JsRuntimeAttributeDisableBackgroundWork`|<span data-ttu-id="b1d5d-112">Среда выполнения не будет выполнять какие-либо действия (такие как сборка мусора) в фоновых потоках.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-112">The runtime will not do any work (such as garbage collection) on background threads.</span></span>|  
|`JsRuntimeAttributeDisableEval`|<span data-ttu-id="b1d5d-113">Использование `eval` или `function` конструктор вызывает исключение.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-113">Using `eval` or `function` constructor will throw an exception.</span></span>|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|<span data-ttu-id="b1d5d-114">Среда выполнения не будет создавать машинный код.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-114">Runtime will not generate native code.</span></span>|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|<span data-ttu-id="b1d5d-115">В среде выполнения будут включены все экспериментальные функции.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-115">Runtime will enable all experimental features.</span></span>|  
|`JsRuntimeAttributeEnableIdleProcessing`|<span data-ttu-id="b1d5d-116">Ведущее приложение будет вызываться `JsIdle` , поэтому Включите обработку бездействия.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-116">Host will call `JsIdle`, so enable idle processing.</span></span> <span data-ttu-id="b1d5d-117">В противном случае среда выполнения будет несколько более агрессивно управлять памятью.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-117">Otherwise, the runtime will manage memory slightly more aggressively.</span></span>|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|<span data-ttu-id="b1d5d-118">Вызов `JsSetException` также выдает исключение в отладчик сценариев (если есть), давая отладчику шанс на прерывание на исключении.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-118">Calling `JsSetException` will also dispatch the exception to the script debugger (if any) giving the debugger a chance to break on the exception.</span></span>|  
|`JsRuntimeAttributeNone`|<span data-ttu-id="b1d5d-119">Никаких специальных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b1d5d-119">No special attributes.</span></span>|  
  
## <span data-ttu-id="b1d5d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b1d5d-120">Requirements</span></span>  
 <span data-ttu-id="b1d5d-121">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b1d5d-121">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b1d5d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b1d5d-122">See Also</span></span>  
 [<span data-ttu-id="b1d5d-123">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b1d5d-123">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
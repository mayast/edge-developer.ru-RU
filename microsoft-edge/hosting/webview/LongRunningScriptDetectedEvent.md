---
description: ''
title: Объект LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752154"
---
# <span data-ttu-id="3232d-103">Объект LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="3232d-103">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="3232d-104">Представлена информация для [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="3232d-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>  

## <span data-ttu-id="3232d-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="3232d-105">Properties</span></span>  

### <span data-ttu-id="3232d-106">executionTime</span><span class="sxs-lookup"><span data-stu-id="3232d-106">executionTime</span></span>  

<span data-ttu-id="3232d-107">Возвращает количество миллисекунд, в течение которых элемент [WebView](../webview.md) выполнял долго выполняемый сценарий.</span><span class="sxs-lookup"><span data-stu-id="3232d-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <span data-ttu-id="3232d-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3232d-108">Property value</span></span>  

<span data-ttu-id="3232d-109">Тип: **длинный**</span><span class="sxs-lookup"><span data-stu-id="3232d-109">Type: **long**</span></span>  

### <span data-ttu-id="3232d-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="3232d-110">stopPageScriptExecution</span></span>  

<span data-ttu-id="3232d-111">Останавливает выполнение долго выполняющегося сценария в элементе [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="3232d-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <span data-ttu-id="3232d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3232d-112">Property value</span></span>  

<span data-ttu-id="3232d-113">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="3232d-113">Type: **Boolean**</span></span>  

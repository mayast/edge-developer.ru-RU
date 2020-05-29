---
description: ''
title: Объект LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571310"
---
# <span data-ttu-id="c76a7-103">Объект LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="c76a7-103">LongRunningScriptDetectedEvent object</span></span>

<span data-ttu-id="c76a7-104">Представлена информация для [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="c76a7-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>

## <span data-ttu-id="c76a7-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="c76a7-105">Properties</span></span>

### <span data-ttu-id="c76a7-106">executionTime</span><span class="sxs-lookup"><span data-stu-id="c76a7-106">executionTime</span></span>

<span data-ttu-id="c76a7-107">Возвращает количество миллисекунд, в течение которых элемент [WebView](../webview.md) выполнял долго выполняемый сценарий.</span><span class="sxs-lookup"><span data-stu-id="c76a7-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### <span data-ttu-id="c76a7-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c76a7-108">Property value</span></span>
<span data-ttu-id="c76a7-109">Тип: **длинный**</span><span class="sxs-lookup"><span data-stu-id="c76a7-109">Type: **long**</span></span>

### <span data-ttu-id="c76a7-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="c76a7-110">stopPageScriptExecution</span></span>
<span data-ttu-id="c76a7-111">Останавливает выполнение долго выполняющегося сценария в элементе [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="c76a7-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### <span data-ttu-id="c76a7-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c76a7-112">Property value</span></span>
<span data-ttu-id="c76a7-113">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="c76a7-113">Type: **Boolean**</span></span>
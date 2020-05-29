---
description: Определяет свойства, которые включают и отключают функции WebView
title: Объект MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571301"
---
# <span data-ttu-id="1f118-104">Объект MSWebViewSettings</span><span class="sxs-lookup"><span data-stu-id="1f118-104">MSWebViewSettings object</span></span>

<span data-ttu-id="1f118-105">Определяет свойства, которые включают и отключают функции [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="1f118-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>

## <span data-ttu-id="1f118-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f118-106">Properties</span></span>

### <span data-ttu-id="1f118-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="1f118-107">isIndexedDBEnabled</span></span>

<span data-ttu-id="1f118-108">Возвращает или задает значение, указывающее, разрешено ли использование IndexedDB в [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="1f118-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### <span data-ttu-id="1f118-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1f118-109">Property value</span></span>
<span data-ttu-id="1f118-110">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="1f118-110">Type: **boolean**</span></span>

<span data-ttu-id="1f118-111">**Значение true** , если IndexedDB можно использовать в **WebView**; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f118-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span> 

### <span data-ttu-id="1f118-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1f118-112">isJavaScriptEnabled</span></span>

<span data-ttu-id="1f118-113">Возвращает или задает значение, указывающее, разрешено ли использование JavaScript в [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="1f118-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### <span data-ttu-id="1f118-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1f118-114">Property value</span></span>
<span data-ttu-id="1f118-115">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="1f118-115">Type: **boolean**</span></span>

<span data-ttu-id="1f118-116">**Значение истина** JavaScript разрешен в [WebView](../webview.md); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f118-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 

### <span data-ttu-id="1f118-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="1f118-117">isScriptNotifyAllowed</span></span>

<span data-ttu-id="1f118-118">Возвращает или задает значение, указывающее, разрешено ли использование [ScriptNotifyEvent](ScriptNotifyEvent.md) в [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="1f118-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### <span data-ttu-id="1f118-119">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1f118-119">Property value</span></span>
<span data-ttu-id="1f118-120">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="1f118-120">Type: **boolean**</span></span>

<span data-ttu-id="1f118-121">**Значение true** [ScriptNotifyEvent](ScriptNotifyEvent.md) разрешено в [WebView](../webview.md); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f118-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 

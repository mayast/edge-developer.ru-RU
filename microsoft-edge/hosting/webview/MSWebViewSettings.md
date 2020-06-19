---
description: Определяет свойства, которые включают и отключают функции WebView
title: Объект MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752180"
---
# <span data-ttu-id="f2638-104">Объект MSWebViewSettings</span><span class="sxs-lookup"><span data-stu-id="f2638-104">MSWebViewSettings object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="f2638-105">Определяет свойства, которые включают и отключают функции [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="f2638-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>  

## <span data-ttu-id="f2638-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2638-106">Properties</span></span>  

### <span data-ttu-id="f2638-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="f2638-107">isIndexedDBEnabled</span></span>  

<span data-ttu-id="f2638-108">Возвращает или задает значение, указывающее, разрешено ли использование IndexedDB в [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="f2638-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### <span data-ttu-id="f2638-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2638-109">Property value</span></span>  

<span data-ttu-id="f2638-110">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="f2638-110">Type: **boolean**</span></span>  

<span data-ttu-id="f2638-111">**Значение true** , если IndexedDB можно использовать в **WebView**; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f2638-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span>  

### <span data-ttu-id="f2638-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f2638-112">isJavaScriptEnabled</span></span>  

<span data-ttu-id="f2638-113">Возвращает или задает значение, указывающее, разрешено ли использование JavaScript в [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="f2638-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### <span data-ttu-id="f2638-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2638-114">Property value</span></span>  

<span data-ttu-id="f2638-115">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="f2638-115">Type: **boolean**</span></span>  

<span data-ttu-id="f2638-116">**Значение истина** JavaScript разрешен в [WebView](../webview.md); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f2638-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  

### <span data-ttu-id="f2638-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="f2638-117">isScriptNotifyAllowed</span></span>  

<span data-ttu-id="f2638-118">Возвращает или задает значение, указывающее, разрешено ли использование [ScriptNotifyEvent](ScriptNotifyEvent.md) в [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="f2638-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### <span data-ttu-id="f2638-119">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2638-119">Property value</span></span>  

<span data-ttu-id="f2638-120">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="f2638-120">Type: **boolean**</span></span>  

<span data-ttu-id="f2638-121">**Значение true** [ScriptNotifyEvent](ScriptNotifyEvent.md) разрешено в [WebView](../webview.md); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f2638-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  

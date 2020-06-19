---
description: Событие, которое возникает при выполнении HTTP-запроса.
title: Объект WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751984"
---
# <span data-ttu-id="7d5a0-104">Объект WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="7d5a0-104">WebResourceRequestedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="7d5a0-105">Событие, которое возникает при выполнении HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="7d5a0-105">An event that is fired when an HTTP request is made.</span></span>  

## <span data-ttu-id="7d5a0-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d5a0-106">Properties</span></span>  

### <span data-ttu-id="7d5a0-107">аргументы</span><span class="sxs-lookup"><span data-stu-id="7d5a0-107">args</span></span>  

<span data-ttu-id="7d5a0-108">Сведения о запросе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d5a0-108">Information about the resource request.</span></span>  <span data-ttu-id="7d5a0-109">Это элемент [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="7d5a0-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>  

<span data-ttu-id="7d5a0-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7d5a0-110">This property is read-only.</span></span>  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### <span data-ttu-id="7d5a0-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7d5a0-111">Property value</span></span>  

<span data-ttu-id="7d5a0-112">Type (тип): **ANY**</span><span class="sxs-lookup"><span data-stu-id="7d5a0-112">Type: **any**</span></span>  

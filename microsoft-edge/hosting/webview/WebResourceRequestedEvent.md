---
description: Событие, которое возникает при выполнении HTTP-запроса.
title: Объект WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570823"
---
# <span data-ttu-id="6c06f-104">Объект WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="6c06f-104">WebResourceRequestedEvent object</span></span>

<span data-ttu-id="6c06f-105">Событие, которое возникает при выполнении HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="6c06f-105">An event that is fired when an HTTP request is made.</span></span>

## <span data-ttu-id="6c06f-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="6c06f-106">Properties</span></span>

### <span data-ttu-id="6c06f-107">аргументы</span><span class="sxs-lookup"><span data-stu-id="6c06f-107">args</span></span>

<span data-ttu-id="6c06f-108">Сведения о запросе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c06f-108">Information about the resource request.</span></span> <span data-ttu-id="6c06f-109">Это элемент [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="6c06f-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>

<span data-ttu-id="6c06f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6c06f-110">This property is read-only.</span></span>

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### <span data-ttu-id="6c06f-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6c06f-111">Property value</span></span>
<span data-ttu-id="6c06f-112">Type (тип): **ANY**</span><span class="sxs-lookup"><span data-stu-id="6c06f-112">Type: **any**</span></span>


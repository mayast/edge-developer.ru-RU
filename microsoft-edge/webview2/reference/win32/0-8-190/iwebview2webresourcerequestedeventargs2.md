---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 7f710b4da71a4a4e61869f06e5d2a4a95a2d0891
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885711"
---
# <span data-ttu-id="3a23d-104">0.8.355-Interface IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="3a23d-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="3a23d-105">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="3a23d-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="3a23d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3a23d-106">Summary</span></span>

 <span data-ttu-id="3a23d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="3a23d-107">Members</span></span>                        | <span data-ttu-id="3a23d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="3a23d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3a23d-109">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="3a23d-109">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="3a23d-110">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a23d-110">The web resource request contexts.</span></span>

## <span data-ttu-id="3a23d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="3a23d-111">Members</span></span>

#### <span data-ttu-id="3a23d-112">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="3a23d-112">get_ResourceContext</span></span> 

<span data-ttu-id="3a23d-113">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a23d-113">The web resource request contexts.</span></span>

> <span data-ttu-id="3a23d-114">общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* контекст)</span><span class="sxs-lookup"><span data-stu-id="3a23d-114">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>


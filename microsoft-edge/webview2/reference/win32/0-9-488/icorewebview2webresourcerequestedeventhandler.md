---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 4f2bb4e5077fea7583f7d9f9886923ea1867e1ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883684"
---
# <span data-ttu-id="986c6-104">0.9.515-Interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="986c6-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="986c6-105">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="986c6-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="986c6-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="986c6-106">Summary</span></span>

 <span data-ttu-id="986c6-107">Участников</span><span class="sxs-lookup"><span data-stu-id="986c6-107">Members</span></span>                        | <span data-ttu-id="986c6-108">Описания</span><span class="sxs-lookup"><span data-stu-id="986c6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="986c6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="986c6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="986c6-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="986c6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="986c6-111">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="986c6-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="986c6-112">Участников</span><span class="sxs-lookup"><span data-stu-id="986c6-112">Members</span></span>

#### <span data-ttu-id="986c6-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="986c6-113">Invoke</span></span> 

<span data-ttu-id="986c6-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="986c6-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="986c6-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="986c6-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


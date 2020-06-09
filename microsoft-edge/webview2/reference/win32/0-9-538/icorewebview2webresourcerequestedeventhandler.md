---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 64f29f8c771a14d569fd45f7359614795bbc0386
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699275"
---
# <span data-ttu-id="6992a-104">интерфейс ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6992a-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="6992a-105">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="6992a-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="6992a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6992a-106">Summary</span></span>

 <span data-ttu-id="6992a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="6992a-107">Members</span></span>                        | <span data-ttu-id="6992a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="6992a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6992a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6992a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6992a-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="6992a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6992a-111">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="6992a-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="6992a-112">Участников</span><span class="sxs-lookup"><span data-stu-id="6992a-112">Members</span></span>

#### <span data-ttu-id="6992a-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="6992a-113">Invoke</span></span> 

<span data-ttu-id="6992a-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="6992a-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6992a-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="6992a-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d35e21fde7788b1df5b201f8690196ecd0d82a34
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884094"
---
# <span data-ttu-id="5e1ae-104">0.9.430-Interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5e1ae-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="5e1ae-105">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="5e1ae-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5e1ae-106">Summary</span></span>

 <span data-ttu-id="5e1ae-107">Участников</span><span class="sxs-lookup"><span data-stu-id="5e1ae-107">Members</span></span>                        | <span data-ttu-id="5e1ae-108">Описания</span><span class="sxs-lookup"><span data-stu-id="5e1ae-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5e1ae-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5e1ae-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5e1ae-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="5e1ae-111">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="5e1ae-112">Участников</span><span class="sxs-lookup"><span data-stu-id="5e1ae-112">Members</span></span>

#### <span data-ttu-id="5e1ae-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="5e1ae-113">Invoke</span></span> 

<span data-ttu-id="5e1ae-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5e1ae-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="5e1ae-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 70ecc1898f9a72656f12b912d103116c381d4218
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885676"
---
# <span data-ttu-id="be171-104">0.8.355-Interface IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="be171-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="be171-105">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="be171-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="be171-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="be171-106">Summary</span></span>

 <span data-ttu-id="be171-107">Участников</span><span class="sxs-lookup"><span data-stu-id="be171-107">Members</span></span>                        | <span data-ttu-id="be171-108">Описания</span><span class="sxs-lookup"><span data-stu-id="be171-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be171-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="be171-109">Invoke</span></span>](#invoke) | <span data-ttu-id="be171-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="be171-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="be171-111">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="be171-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="be171-112">Участников</span><span class="sxs-lookup"><span data-stu-id="be171-112">Members</span></span>

#### <span data-ttu-id="be171-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="be171-113">Invoke</span></span> 

<span data-ttu-id="be171-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="be171-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="be171-115">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="be171-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


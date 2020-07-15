---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: c0980f26ef06497cded81e2f9c7c00162af18d9b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878094"
---
# <span data-ttu-id="b9282-104">0.8.355-Interface IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b9282-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b9282-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="b9282-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="b9282-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="b9282-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="b9282-107">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="b9282-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="b9282-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b9282-108">Summary</span></span>

 <span data-ttu-id="b9282-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b9282-109">Members</span></span>                        | <span data-ttu-id="b9282-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b9282-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b9282-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="b9282-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b9282-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b9282-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b9282-113">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="b9282-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="b9282-114">Участников</span><span class="sxs-lookup"><span data-stu-id="b9282-114">Members</span></span>

#### <span data-ttu-id="b9282-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="b9282-115">Invoke</span></span> 

<span data-ttu-id="b9282-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b9282-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b9282-117">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b9282-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


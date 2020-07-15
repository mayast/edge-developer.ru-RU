---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 9cd221ac1b528b0be52201daa0c15217534944a6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879228"
---
# <span data-ttu-id="d03ee-104">интерфейс ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d03ee-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="d03ee-105">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="d03ee-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="d03ee-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d03ee-106">Summary</span></span>

 <span data-ttu-id="d03ee-107">Участников</span><span class="sxs-lookup"><span data-stu-id="d03ee-107">Members</span></span>                        | <span data-ttu-id="d03ee-108">Описания</span><span class="sxs-lookup"><span data-stu-id="d03ee-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d03ee-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d03ee-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d03ee-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d03ee-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d03ee-111">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="d03ee-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="d03ee-112">Участников</span><span class="sxs-lookup"><span data-stu-id="d03ee-112">Members</span></span>

#### <span data-ttu-id="d03ee-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="d03ee-113">Invoke</span></span> 

<span data-ttu-id="d03ee-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d03ee-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d03ee-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d03ee-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


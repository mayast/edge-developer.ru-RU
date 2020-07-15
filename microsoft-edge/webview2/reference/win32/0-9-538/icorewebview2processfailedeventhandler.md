---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ProcessFailedEventHandler
ms.openlocfilehash: 5ae5a64bfbcd0692d7c284974e960f9ed6249e50
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877401"
---
# <span data-ttu-id="e39bd-104">интерфейс ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e39bd-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="e39bd-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="e39bd-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="e39bd-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e39bd-106">Summary</span></span>

 <span data-ttu-id="e39bd-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e39bd-107">Members</span></span>                        | <span data-ttu-id="e39bd-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e39bd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e39bd-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e39bd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e39bd-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e39bd-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e39bd-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e39bd-111">Members</span></span>

#### <span data-ttu-id="e39bd-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e39bd-112">Invoke</span></span> 

<span data-ttu-id="e39bd-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e39bd-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e39bd-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e39bd-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


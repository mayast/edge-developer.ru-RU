---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 5221a08f8da8e0b51bb873a2e312e4012c868528
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012534"
---
# <span data-ttu-id="c9fcb-104">интерфейс ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="c9fcb-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="c9fcb-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="c9fcb-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c9fcb-106">Summary</span></span>

 <span data-ttu-id="c9fcb-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c9fcb-107">Members</span></span>                        | <span data-ttu-id="c9fcb-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c9fcb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c9fcb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c9fcb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c9fcb-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c9fcb-111">Участников</span><span class="sxs-lookup"><span data-stu-id="c9fcb-111">Members</span></span>

#### <span data-ttu-id="c9fcb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c9fcb-112">Invoke</span></span> 

<span data-ttu-id="c9fcb-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c9fcb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c9fcb-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c9fcb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


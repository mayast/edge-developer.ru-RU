---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 82a5e73b8b928897e5c0af1610631c9e7d636337
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879746"
---
# <span data-ttu-id="f502f-104">интерфейс ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="f502f-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="f502f-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="f502f-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="f502f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f502f-106">Summary</span></span>

 <span data-ttu-id="f502f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f502f-107">Members</span></span>                        | <span data-ttu-id="f502f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f502f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f502f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f502f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f502f-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f502f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f502f-111">Участников</span><span class="sxs-lookup"><span data-stu-id="f502f-111">Members</span></span>

#### <span data-ttu-id="f502f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f502f-112">Invoke</span></span> 

<span data-ttu-id="f502f-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f502f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f502f-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f502f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


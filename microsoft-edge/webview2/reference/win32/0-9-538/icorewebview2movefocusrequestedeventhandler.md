---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: b0e7f3f005b90c5656eeeac09716130544b0ee20
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879837"
---
# <span data-ttu-id="db4c4-104">интерфейс ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="db4c4-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="db4c4-105">Вызывающий объект реализует этот метод для получения события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="db4c4-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="db4c4-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="db4c4-106">Summary</span></span>

 <span data-ttu-id="db4c4-107">Участников</span><span class="sxs-lookup"><span data-stu-id="db4c4-107">Members</span></span>                        | <span data-ttu-id="db4c4-108">Описания</span><span class="sxs-lookup"><span data-stu-id="db4c4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="db4c4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="db4c4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="db4c4-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="db4c4-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="db4c4-111">Участников</span><span class="sxs-lookup"><span data-stu-id="db4c4-111">Members</span></span>

#### <span data-ttu-id="db4c4-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="db4c4-112">Invoke</span></span> 

<span data-ttu-id="db4c4-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="db4c4-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="db4c4-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="db4c4-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


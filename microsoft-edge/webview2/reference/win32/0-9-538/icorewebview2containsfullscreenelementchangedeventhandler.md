---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ContainsFullScreenElementChangedEventHandler
ms.openlocfilehash: 0f0efc8cc5315c35bef4c0ad122be37f26444f8d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877429"
---
# <span data-ttu-id="c4c66-104">интерфейс ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c4c66-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c4c66-105">Вызывающий объект реализует этот метод для получения событий ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="c4c66-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="c4c66-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c4c66-106">Summary</span></span>

 <span data-ttu-id="c4c66-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c4c66-107">Members</span></span>                        | <span data-ttu-id="c4c66-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c4c66-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4c66-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4c66-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c4c66-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c4c66-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c4c66-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="c4c66-111">There are no event args for this event.</span></span>

## <span data-ttu-id="c4c66-112">Участников</span><span class="sxs-lookup"><span data-stu-id="c4c66-112">Members</span></span>

#### <span data-ttu-id="c4c66-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4c66-113">Invoke</span></span> 

<span data-ttu-id="c4c66-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c4c66-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c4c66-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c4c66-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c4c66-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="c4c66-116">There are no event args and the args parameter will be null.</span></span>


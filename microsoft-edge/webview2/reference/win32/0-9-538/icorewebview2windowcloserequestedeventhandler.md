---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: fcfdb3b28f4f1d1e1d1159e6664cb898613d0601
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879963"
---
# <span data-ttu-id="ef0d6-104">интерфейс ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef0d6-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="ef0d6-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="ef0d6-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="ef0d6-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ef0d6-106">Summary</span></span>

 <span data-ttu-id="ef0d6-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ef0d6-107">Members</span></span>                        | <span data-ttu-id="ef0d6-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ef0d6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef0d6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ef0d6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ef0d6-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ef0d6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ef0d6-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ef0d6-111">Members</span></span>

#### <span data-ttu-id="ef0d6-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ef0d6-112">Invoke</span></span> 

<span data-ttu-id="ef0d6-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ef0d6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ef0d6-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ef0d6-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ef0d6-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="ef0d6-115">There are no event args and the args parameter will be null.</span></span>


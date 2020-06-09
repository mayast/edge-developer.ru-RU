---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c154b80e29476666bc0b2121b3eba63009946b36
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699185"
---
# <span data-ttu-id="c894d-104">интерфейс ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c894d-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="c894d-105">Вызывающий объект реализует этот интерфейс, чтобы получать события DevToolsProtocolEventReceived из WebView.</span><span class="sxs-lookup"><span data-stu-id="c894d-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="c894d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c894d-106">Summary</span></span>

 <span data-ttu-id="c894d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c894d-107">Members</span></span>                        | <span data-ttu-id="c894d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c894d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c894d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c894d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c894d-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c894d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c894d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="c894d-111">Members</span></span>

#### <span data-ttu-id="c894d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c894d-112">Invoke</span></span> 

<span data-ttu-id="c894d-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c894d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c894d-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c894d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


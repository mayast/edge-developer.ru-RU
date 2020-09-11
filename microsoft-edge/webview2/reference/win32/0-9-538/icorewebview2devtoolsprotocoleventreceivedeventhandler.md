---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 163ab3f16b6d835fc64aef4ea0fdff2883084faa
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010268"
---
# <span data-ttu-id="e62ad-104">0.9.579-Interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e62ad-104">0.9.579 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="e62ad-105">Вызывающий объект реализует этот интерфейс, чтобы получать события DevToolsProtocolEventReceived из WebView.</span><span class="sxs-lookup"><span data-stu-id="e62ad-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="e62ad-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e62ad-106">Summary</span></span>

 <span data-ttu-id="e62ad-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e62ad-107">Members</span></span>                        | <span data-ttu-id="e62ad-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e62ad-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e62ad-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e62ad-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e62ad-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e62ad-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e62ad-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e62ad-111">Members</span></span>

#### <span data-ttu-id="e62ad-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e62ad-112">Invoke</span></span> 

<span data-ttu-id="e62ad-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e62ad-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e62ad-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e62ad-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


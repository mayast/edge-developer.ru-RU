---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 4b280a16c18c84641f91efd39407f93db968f69d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012566"
---
# <span data-ttu-id="b0483-104">интерфейс ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b0483-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="b0483-105">Вызывающий объект реализует этот интерфейс, чтобы получать события DevToolsProtocolEventReceived из WebView.</span><span class="sxs-lookup"><span data-stu-id="b0483-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="b0483-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b0483-106">Summary</span></span>

 <span data-ttu-id="b0483-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b0483-107">Members</span></span>                        | <span data-ttu-id="b0483-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b0483-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b0483-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b0483-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b0483-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b0483-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b0483-111">Участников</span><span class="sxs-lookup"><span data-stu-id="b0483-111">Members</span></span>

#### <span data-ttu-id="b0483-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b0483-112">Invoke</span></span> 

<span data-ttu-id="b0483-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b0483-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b0483-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b0483-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


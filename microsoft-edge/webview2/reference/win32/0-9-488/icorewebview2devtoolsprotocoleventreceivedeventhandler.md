---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1e59d8d830c3357fafd4f8315388ee5fff93a3d2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880810"
---
# <span data-ttu-id="dc2f3-104">0.9.515-Interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="dc2f3-104">0.9.515 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="dc2f3-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="dc2f3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="dc2f3-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="dc2f3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="dc2f3-107">Вызывающий объект реализует этот интерфейс, чтобы получать события DevToolsProtocolEventReceived из WebView.</span><span class="sxs-lookup"><span data-stu-id="dc2f3-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="dc2f3-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="dc2f3-108">Summary</span></span>

 <span data-ttu-id="dc2f3-109">Участников</span><span class="sxs-lookup"><span data-stu-id="dc2f3-109">Members</span></span>                        | <span data-ttu-id="dc2f3-110">Описания</span><span class="sxs-lookup"><span data-stu-id="dc2f3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc2f3-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="dc2f3-111">Invoke</span></span>](#invoke) | <span data-ttu-id="dc2f3-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="dc2f3-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="dc2f3-113">Участников</span><span class="sxs-lookup"><span data-stu-id="dc2f3-113">Members</span></span>

#### <span data-ttu-id="dc2f3-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="dc2f3-114">Invoke</span></span> 

<span data-ttu-id="dc2f3-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="dc2f3-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="dc2f3-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="dc2f3-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


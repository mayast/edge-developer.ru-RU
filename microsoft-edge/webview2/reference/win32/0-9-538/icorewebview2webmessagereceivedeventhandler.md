---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebMessageReceivedEventHandler
ms.openlocfilehash: 77af4fc8c3e05e46883e6d2428d9fa9015815f8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010378"
---
# <span data-ttu-id="838bd-104">0.9.579-Interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="838bd-104">0.9.579 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="838bd-105">Вызывающий объект реализует этот интерфейс для получения события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="838bd-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="838bd-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="838bd-106">Summary</span></span>

 <span data-ttu-id="838bd-107">Участников</span><span class="sxs-lookup"><span data-stu-id="838bd-107">Members</span></span>                        | <span data-ttu-id="838bd-108">Описания</span><span class="sxs-lookup"><span data-stu-id="838bd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="838bd-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="838bd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="838bd-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="838bd-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="838bd-111">Участников</span><span class="sxs-lookup"><span data-stu-id="838bd-111">Members</span></span>

#### <span data-ttu-id="838bd-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="838bd-112">Invoke</span></span> 

<span data-ttu-id="838bd-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="838bd-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="838bd-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="838bd-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>


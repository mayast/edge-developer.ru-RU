---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebMessageReceivedEventHandler
ms.openlocfilehash: 3d88ffc5e7821ef3163c357738019ecb914ea758
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012561"
---
# <span data-ttu-id="1c0f8-104">интерфейс ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1c0f8-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="1c0f8-105">Вызывающий объект реализует этот интерфейс для получения события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="1c0f8-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1c0f8-106">Summary</span></span>

 <span data-ttu-id="1c0f8-107">Участников</span><span class="sxs-lookup"><span data-stu-id="1c0f8-107">Members</span></span>                        | <span data-ttu-id="1c0f8-108">Описания</span><span class="sxs-lookup"><span data-stu-id="1c0f8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1c0f8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1c0f8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1c0f8-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="1c0f8-111">Участников</span><span class="sxs-lookup"><span data-stu-id="1c0f8-111">Members</span></span>

#### <span data-ttu-id="1c0f8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="1c0f8-112">Invoke</span></span> 

<span data-ttu-id="1c0f8-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1c0f8-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="1c0f8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>


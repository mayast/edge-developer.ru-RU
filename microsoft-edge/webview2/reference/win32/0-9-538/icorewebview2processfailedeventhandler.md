---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ProcessFailedEventHandler
ms.openlocfilehash: d65c6ae63f5c79540587f99e3ff42c4ebb3e409e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010833"
---
# <span data-ttu-id="dc258-104">0.9.579-Interface ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="dc258-104">0.9.579 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="dc258-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="dc258-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="dc258-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="dc258-106">Summary</span></span>

 <span data-ttu-id="dc258-107">Участников</span><span class="sxs-lookup"><span data-stu-id="dc258-107">Members</span></span>                        | <span data-ttu-id="dc258-108">Описания</span><span class="sxs-lookup"><span data-stu-id="dc258-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc258-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="dc258-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dc258-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="dc258-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="dc258-111">Участников</span><span class="sxs-lookup"><span data-stu-id="dc258-111">Members</span></span>

#### <span data-ttu-id="dc258-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="dc258-112">Invoke</span></span> 

<span data-ttu-id="dc258-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="dc258-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="dc258-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="dc258-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


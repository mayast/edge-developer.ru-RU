---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 7cadbfddca9c05c8649b79503de3ce4f3695ea4c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011274"
---
# <span data-ttu-id="52e4d-104">0.9.579-Interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="52e4d-104">0.9.579 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="52e4d-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="52e4d-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="52e4d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="52e4d-106">Summary</span></span>

 <span data-ttu-id="52e4d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="52e4d-107">Members</span></span>                        | <span data-ttu-id="52e4d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="52e4d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52e4d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="52e4d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="52e4d-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="52e4d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="52e4d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="52e4d-111">Members</span></span>

#### <span data-ttu-id="52e4d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="52e4d-112">Invoke</span></span> 

<span data-ttu-id="52e4d-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="52e4d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="52e4d-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="52e4d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


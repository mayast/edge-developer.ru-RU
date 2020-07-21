---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: aa59efbb0b47977b41236950c47a01d6d95ee123
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886294"
---
# <span data-ttu-id="11bf7-104">0.9.515-Interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="11bf7-104">0.9.515 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="11bf7-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="11bf7-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="11bf7-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="11bf7-106">Summary</span></span>

 <span data-ttu-id="11bf7-107">Участников</span><span class="sxs-lookup"><span data-stu-id="11bf7-107">Members</span></span>                        | <span data-ttu-id="11bf7-108">Описания</span><span class="sxs-lookup"><span data-stu-id="11bf7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="11bf7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="11bf7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="11bf7-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="11bf7-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="11bf7-111">Участников</span><span class="sxs-lookup"><span data-stu-id="11bf7-111">Members</span></span>

#### <span data-ttu-id="11bf7-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="11bf7-112">Invoke</span></span> 

<span data-ttu-id="11bf7-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="11bf7-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="11bf7-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="11bf7-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


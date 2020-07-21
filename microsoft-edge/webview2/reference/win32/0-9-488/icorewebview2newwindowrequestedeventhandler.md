---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2623dad17d8e8b34348bdb21a38e900c28eaeebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885445"
---
# <span data-ttu-id="33735-104">0.9.515-Interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="33735-104">0.9.515 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="33735-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="33735-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="33735-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="33735-106">Summary</span></span>

 <span data-ttu-id="33735-107">Участников</span><span class="sxs-lookup"><span data-stu-id="33735-107">Members</span></span>                        | <span data-ttu-id="33735-108">Описания</span><span class="sxs-lookup"><span data-stu-id="33735-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="33735-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="33735-109">Invoke</span></span>](#invoke) | <span data-ttu-id="33735-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="33735-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="33735-111">Участников</span><span class="sxs-lookup"><span data-stu-id="33735-111">Members</span></span>

#### <span data-ttu-id="33735-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="33735-112">Invoke</span></span> 

<span data-ttu-id="33735-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="33735-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="33735-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="33735-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


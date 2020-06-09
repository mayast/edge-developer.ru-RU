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
ms.openlocfilehash: a39eeadaf1243d57223f3739dce836b1db998998
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699124"
---
# <span data-ttu-id="65db5-104">интерфейс ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="65db5-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="65db5-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="65db5-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="65db5-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="65db5-106">Summary</span></span>

 <span data-ttu-id="65db5-107">Участников</span><span class="sxs-lookup"><span data-stu-id="65db5-107">Members</span></span>                        | <span data-ttu-id="65db5-108">Описания</span><span class="sxs-lookup"><span data-stu-id="65db5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65db5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="65db5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="65db5-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="65db5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="65db5-111">Участников</span><span class="sxs-lookup"><span data-stu-id="65db5-111">Members</span></span>

#### <span data-ttu-id="65db5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="65db5-112">Invoke</span></span> 

<span data-ttu-id="65db5-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="65db5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="65db5-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="65db5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


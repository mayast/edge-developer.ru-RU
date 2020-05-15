---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a8cd4dd948aa00aca7c2ef7d8c0c744b30db37e3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654869"
---
# <span data-ttu-id="84009-104">интерфейс ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="84009-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="84009-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="84009-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="84009-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="84009-106">Summary</span></span>

 <span data-ttu-id="84009-107">Участников</span><span class="sxs-lookup"><span data-stu-id="84009-107">Members</span></span>                        | <span data-ttu-id="84009-108">Описания</span><span class="sxs-lookup"><span data-stu-id="84009-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="84009-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="84009-109">Invoke</span></span>](#invoke) | <span data-ttu-id="84009-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="84009-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="84009-111">Участников</span><span class="sxs-lookup"><span data-stu-id="84009-111">Members</span></span>

#### <span data-ttu-id="84009-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="84009-112">Invoke</span></span> 

<span data-ttu-id="84009-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="84009-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="84009-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="84009-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


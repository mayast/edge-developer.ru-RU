---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 30c39bf10c874c17787c235ebb1589de1c9449ff
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885557"
---
# <span data-ttu-id="027b2-104">0.9.515-Interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="027b2-104">0.9.515 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="027b2-105">Вызывающий объект реализует этот интерфейс для получения события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="027b2-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="027b2-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="027b2-106">Summary</span></span>

 <span data-ttu-id="027b2-107">Участников</span><span class="sxs-lookup"><span data-stu-id="027b2-107">Members</span></span>                        | <span data-ttu-id="027b2-108">Описания</span><span class="sxs-lookup"><span data-stu-id="027b2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="027b2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="027b2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="027b2-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="027b2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="027b2-111">Участников</span><span class="sxs-lookup"><span data-stu-id="027b2-111">Members</span></span>

#### <span data-ttu-id="027b2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="027b2-112">Invoke</span></span> 

<span data-ttu-id="027b2-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="027b2-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="027b2-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="027b2-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


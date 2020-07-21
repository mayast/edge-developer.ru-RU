---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 41687dcb162d8d56e773b9050898e9f22bd034ab
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883884"
---
# <span data-ttu-id="79321-104">0.9.515-Interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="79321-104">0.9.515 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="79321-105">Вызывающий объект реализует этот метод для получения событий ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="79321-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="79321-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="79321-106">Summary</span></span>

 <span data-ttu-id="79321-107">Участников</span><span class="sxs-lookup"><span data-stu-id="79321-107">Members</span></span>                        | <span data-ttu-id="79321-108">Описания</span><span class="sxs-lookup"><span data-stu-id="79321-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="79321-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="79321-109">Invoke</span></span>](#invoke) | <span data-ttu-id="79321-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="79321-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="79321-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="79321-111">There are no event args for this event.</span></span>

## <span data-ttu-id="79321-112">Участников</span><span class="sxs-lookup"><span data-stu-id="79321-112">Members</span></span>

#### <span data-ttu-id="79321-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="79321-113">Invoke</span></span> 

<span data-ttu-id="79321-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="79321-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="79321-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="79321-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="79321-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="79321-116">There are no event args and the args parameter will be null.</span></span>


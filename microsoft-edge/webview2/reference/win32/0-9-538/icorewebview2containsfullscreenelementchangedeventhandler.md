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
ms.openlocfilehash: 8c717bb57a5dc984d6cb2bbbbac79cf91d64fe2f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699200"
---
# <span data-ttu-id="e6a53-104">интерфейс ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e6a53-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e6a53-105">Вызывающий объект реализует этот метод для получения событий ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="e6a53-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="e6a53-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e6a53-106">Summary</span></span>

 <span data-ttu-id="e6a53-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e6a53-107">Members</span></span>                        | <span data-ttu-id="e6a53-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e6a53-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e6a53-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e6a53-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e6a53-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e6a53-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e6a53-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="e6a53-111">There are no event args for this event.</span></span>

## <span data-ttu-id="e6a53-112">Участников</span><span class="sxs-lookup"><span data-stu-id="e6a53-112">Members</span></span>

#### <span data-ttu-id="e6a53-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="e6a53-113">Invoke</span></span> 

<span data-ttu-id="e6a53-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e6a53-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e6a53-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e6a53-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="e6a53-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="e6a53-116">There are no event args and the args parameter will be null.</span></span>


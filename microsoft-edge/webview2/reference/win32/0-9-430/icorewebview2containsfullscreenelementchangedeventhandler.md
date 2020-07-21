---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8afab2e15381c99f5f677b13e539e4b6a9279b63
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884325"
---
# <span data-ttu-id="1959a-104">0.9.430-Interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1959a-104">0.9.430 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1959a-105">Вызывающий объект реализует этот метод для получения событий ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="1959a-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="1959a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1959a-106">Summary</span></span>

 <span data-ttu-id="1959a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="1959a-107">Members</span></span>                        | <span data-ttu-id="1959a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="1959a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1959a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1959a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1959a-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1959a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1959a-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1959a-111">There are no event args for this event.</span></span>

## <span data-ttu-id="1959a-112">Участников</span><span class="sxs-lookup"><span data-stu-id="1959a-112">Members</span></span>

#### <span data-ttu-id="1959a-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="1959a-113">Invoke</span></span> 

<span data-ttu-id="1959a-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1959a-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1959a-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1959a-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="1959a-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="1959a-116">There are no event args and the args parameter will be null.</span></span>


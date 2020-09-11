---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ContainsFullScreenElementChangedEventHandler
ms.openlocfilehash: e1c51ee30a7b61d5a5638adb4130b1add3bddb23
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010560"
---
# <span data-ttu-id="7f6bc-104">0.9.579-Interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7f6bc-104">0.9.579 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="7f6bc-105">Вызывающий объект реализует этот метод для получения событий ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="7f6bc-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7f6bc-106">Summary</span></span>

 <span data-ttu-id="7f6bc-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7f6bc-107">Members</span></span>                        | <span data-ttu-id="7f6bc-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7f6bc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f6bc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7f6bc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7f6bc-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7f6bc-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-111">There are no event args for this event.</span></span>

## <span data-ttu-id="7f6bc-112">Участников</span><span class="sxs-lookup"><span data-stu-id="7f6bc-112">Members</span></span>

#### <span data-ttu-id="7f6bc-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="7f6bc-113">Invoke</span></span> 

<span data-ttu-id="7f6bc-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7f6bc-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="7f6bc-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="7f6bc-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-116">There are no event args and the args parameter will be null.</span></span>


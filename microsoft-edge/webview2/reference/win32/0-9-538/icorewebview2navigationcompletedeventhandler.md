---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 7e61f54882d653a28ec31a97c59758eeff300b26
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011267"
---
# <span data-ttu-id="411ca-104">0.9.579-Interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="411ca-104">0.9.579 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="411ca-105">Вызывающий объект реализует этот интерфейс для получения события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="411ca-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="411ca-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="411ca-106">Summary</span></span>

 <span data-ttu-id="411ca-107">Участников</span><span class="sxs-lookup"><span data-stu-id="411ca-107">Members</span></span>                        | <span data-ttu-id="411ca-108">Описания</span><span class="sxs-lookup"><span data-stu-id="411ca-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="411ca-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="411ca-109">Invoke</span></span>](#invoke) | <span data-ttu-id="411ca-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="411ca-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="411ca-111">Участников</span><span class="sxs-lookup"><span data-stu-id="411ca-111">Members</span></span>

#### <span data-ttu-id="411ca-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="411ca-112">Invoke</span></span> 

<span data-ttu-id="411ca-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="411ca-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="411ca-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="411ca-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


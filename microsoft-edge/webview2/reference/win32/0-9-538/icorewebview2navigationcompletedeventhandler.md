---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 24651585298998eaa42b2be242785de1bf4d6f84
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879795"
---
# <span data-ttu-id="591ab-104">интерфейс ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="591ab-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="591ab-105">Вызывающий объект реализует этот интерфейс для получения события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="591ab-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="591ab-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="591ab-106">Summary</span></span>

 <span data-ttu-id="591ab-107">Участников</span><span class="sxs-lookup"><span data-stu-id="591ab-107">Members</span></span>                        | <span data-ttu-id="591ab-108">Описания</span><span class="sxs-lookup"><span data-stu-id="591ab-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="591ab-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="591ab-109">Invoke</span></span>](#invoke) | <span data-ttu-id="591ab-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="591ab-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="591ab-111">Участников</span><span class="sxs-lookup"><span data-stu-id="591ab-111">Members</span></span>

#### <span data-ttu-id="591ab-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="591ab-112">Invoke</span></span> 

<span data-ttu-id="591ab-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="591ab-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="591ab-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="591ab-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


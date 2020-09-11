---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2SourceChangedEventHandler
ms.openlocfilehash: 2c174d498843b7cc1d680d58eb36b5f53d652ad3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012523"
---
# <span data-ttu-id="1f0e5-104">интерфейс ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1f0e5-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1f0e5-105">Вызывающий объект реализует этот интерфейс для получения события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="1f0e5-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="1f0e5-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1f0e5-106">Summary</span></span>

 <span data-ttu-id="1f0e5-107">Участников</span><span class="sxs-lookup"><span data-stu-id="1f0e5-107">Members</span></span>                        | <span data-ttu-id="1f0e5-108">Описания</span><span class="sxs-lookup"><span data-stu-id="1f0e5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1f0e5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1f0e5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1f0e5-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1f0e5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="1f0e5-111">Участников</span><span class="sxs-lookup"><span data-stu-id="1f0e5-111">Members</span></span>

#### <span data-ttu-id="1f0e5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="1f0e5-112">Invoke</span></span> 

<span data-ttu-id="1f0e5-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1f0e5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1f0e5-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="1f0e5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


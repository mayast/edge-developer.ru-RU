---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2SourceChangedEventHandler
ms.openlocfilehash: b856211b8a4b4088acc741d4d5626b49340124d1
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879333"
---
# <span data-ttu-id="fe51b-104">интерфейс ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fe51b-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="fe51b-105">Вызывающий объект реализует этот интерфейс для получения события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="fe51b-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="fe51b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fe51b-106">Summary</span></span>

 <span data-ttu-id="fe51b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="fe51b-107">Members</span></span>                        | <span data-ttu-id="fe51b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="fe51b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fe51b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fe51b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fe51b-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fe51b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fe51b-111">Участников</span><span class="sxs-lookup"><span data-stu-id="fe51b-111">Members</span></span>

#### <span data-ttu-id="fe51b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="fe51b-112">Invoke</span></span> 

<span data-ttu-id="fe51b-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fe51b-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fe51b-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fe51b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: fb6e3cfabae0116ac746d6e8e5cc03efa0f1c1b6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877449"
---
# <span data-ttu-id="17531-104">интерфейс ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="17531-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="17531-105">Вызывающий объект реализует этот интерфейс для получения события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="17531-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="17531-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="17531-106">Summary</span></span>

 <span data-ttu-id="17531-107">Участников</span><span class="sxs-lookup"><span data-stu-id="17531-107">Members</span></span>                        | <span data-ttu-id="17531-108">Описания</span><span class="sxs-lookup"><span data-stu-id="17531-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17531-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="17531-109">Invoke</span></span>](#invoke) | <span data-ttu-id="17531-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="17531-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="17531-111">Участников</span><span class="sxs-lookup"><span data-stu-id="17531-111">Members</span></span>

#### <span data-ttu-id="17531-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="17531-112">Invoke</span></span> 

<span data-ttu-id="17531-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="17531-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="17531-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="17531-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: cf9d04c14f39a9ba1686d5cc9b002041313b645d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879914"
---
# <span data-ttu-id="e1f4f-104">интерфейс ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e1f4f-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e1f4f-105">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="e1f4f-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="e1f4f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e1f4f-106">Summary</span></span>

 <span data-ttu-id="e1f4f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e1f4f-107">Members</span></span>                        | <span data-ttu-id="e1f4f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e1f4f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1f4f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1f4f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e1f4f-110">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="e1f4f-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="e1f4f-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e1f4f-111">Members</span></span>

#### <span data-ttu-id="e1f4f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1f4f-112">Invoke</span></span> 

<span data-ttu-id="e1f4f-113">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="e1f4f-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="e1f4f-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e1f4f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


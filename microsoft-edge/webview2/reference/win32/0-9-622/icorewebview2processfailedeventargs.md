---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 0f4ce5d4922b7a721ce2652fadfa5169a52cb458
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012527"
---
# <span data-ttu-id="c1520-104">интерфейс ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c1520-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="c1520-105">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="c1520-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="c1520-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c1520-106">Summary</span></span>

 <span data-ttu-id="c1520-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c1520-107">Members</span></span>                        | <span data-ttu-id="c1520-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c1520-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c1520-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="c1520-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="c1520-110">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="c1520-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="c1520-111">Участников</span><span class="sxs-lookup"><span data-stu-id="c1520-111">Members</span></span>

#### <span data-ttu-id="c1520-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="c1520-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="c1520-113">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="c1520-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="c1520-114">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="c1520-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


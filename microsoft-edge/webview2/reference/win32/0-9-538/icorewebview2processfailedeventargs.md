---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 70fb6f75594284560cb0d64663fbda47cc7404d6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879347"
---
# <span data-ttu-id="cbe1b-104">интерфейс ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cbe1b-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="cbe1b-105">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="cbe1b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="cbe1b-106">Summary</span></span>

 <span data-ttu-id="cbe1b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="cbe1b-107">Members</span></span>                        | <span data-ttu-id="cbe1b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="cbe1b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cbe1b-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="cbe1b-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="cbe1b-110">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="cbe1b-111">Участников</span><span class="sxs-lookup"><span data-stu-id="cbe1b-111">Members</span></span>

#### <span data-ttu-id="cbe1b-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="cbe1b-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="cbe1b-113">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="cbe1b-114">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="cbe1b-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


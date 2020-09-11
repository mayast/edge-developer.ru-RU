---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: af27c39b2ed9ba197ab1c567bcf18a43c3dee932
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010021"
---
# <span data-ttu-id="95cbf-104">0.9.579-Interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="95cbf-104">0.9.579 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="95cbf-105">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="95cbf-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="95cbf-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="95cbf-106">Summary</span></span>

 <span data-ttu-id="95cbf-107">Участников</span><span class="sxs-lookup"><span data-stu-id="95cbf-107">Members</span></span>                        | <span data-ttu-id="95cbf-108">Описания</span><span class="sxs-lookup"><span data-stu-id="95cbf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95cbf-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="95cbf-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="95cbf-110">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="95cbf-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="95cbf-111">Участников</span><span class="sxs-lookup"><span data-stu-id="95cbf-111">Members</span></span>

#### <span data-ttu-id="95cbf-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="95cbf-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="95cbf-113">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="95cbf-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="95cbf-114">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="95cbf-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


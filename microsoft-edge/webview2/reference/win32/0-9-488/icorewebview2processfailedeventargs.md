---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2dc5c437acadb06b5f8b12ae0dc54aec12412355
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883793"
---
# <span data-ttu-id="64a77-104">0.9.515-Interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="64a77-104">0.9.515 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="64a77-105">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="64a77-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="64a77-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="64a77-106">Summary</span></span>

 <span data-ttu-id="64a77-107">Участников</span><span class="sxs-lookup"><span data-stu-id="64a77-107">Members</span></span>                        | <span data-ttu-id="64a77-108">Описания</span><span class="sxs-lookup"><span data-stu-id="64a77-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64a77-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="64a77-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="64a77-110">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="64a77-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="64a77-111">Участников</span><span class="sxs-lookup"><span data-stu-id="64a77-111">Members</span></span>

#### <span data-ttu-id="64a77-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="64a77-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="64a77-113">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="64a77-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="64a77-114">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="64a77-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


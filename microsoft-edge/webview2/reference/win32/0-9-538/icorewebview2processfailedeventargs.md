---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c01d98ca997a0b4e288ecaa8ede609c93fc84ea1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699155"
---
# <span data-ttu-id="67405-104">интерфейс ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="67405-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="67405-105">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="67405-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="67405-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="67405-106">Summary</span></span>

 <span data-ttu-id="67405-107">Участников</span><span class="sxs-lookup"><span data-stu-id="67405-107">Members</span></span>                        | <span data-ttu-id="67405-108">Описания</span><span class="sxs-lookup"><span data-stu-id="67405-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67405-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="67405-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="67405-110">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="67405-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="67405-111">Участников</span><span class="sxs-lookup"><span data-stu-id="67405-111">Members</span></span>

#### <span data-ttu-id="67405-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="67405-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="67405-113">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="67405-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="67405-114">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="67405-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


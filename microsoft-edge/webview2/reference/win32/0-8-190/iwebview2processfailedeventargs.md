---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 697a49bfe68f83085f6c961ee2cdd5ab21f3b59b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885823"
---
# <span data-ttu-id="d04b5-104">0.8.355-Interface IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d04b5-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="d04b5-105">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d04b5-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="d04b5-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d04b5-106">Summary</span></span>

 <span data-ttu-id="d04b5-107">Участников</span><span class="sxs-lookup"><span data-stu-id="d04b5-107">Members</span></span>                        | <span data-ttu-id="d04b5-108">Описания</span><span class="sxs-lookup"><span data-stu-id="d04b5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d04b5-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d04b5-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="d04b5-110">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="d04b5-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="d04b5-111">Участников</span><span class="sxs-lookup"><span data-stu-id="d04b5-111">Members</span></span>

#### <span data-ttu-id="d04b5-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d04b5-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="d04b5-113">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="d04b5-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="d04b5-114">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="d04b5-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


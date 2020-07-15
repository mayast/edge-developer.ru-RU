---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ac3b1fc5ceb31cbf2d67649b91f3bfbf2c8ecbe3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880369"
---
# <span data-ttu-id="ab566-104">0.9.515-Interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ab566-104">0.9.515 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="ab566-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="ab566-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ab566-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="ab566-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="ab566-107">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="ab566-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="ab566-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ab566-108">Summary</span></span>

 <span data-ttu-id="ab566-109">Участников</span><span class="sxs-lookup"><span data-stu-id="ab566-109">Members</span></span>                        | <span data-ttu-id="ab566-110">Описания</span><span class="sxs-lookup"><span data-stu-id="ab566-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ab566-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="ab566-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="ab566-112">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="ab566-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="ab566-113">Участников</span><span class="sxs-lookup"><span data-stu-id="ab566-113">Members</span></span>

#### <span data-ttu-id="ab566-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="ab566-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="ab566-115">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="ab566-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="ab566-116">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="ab566-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


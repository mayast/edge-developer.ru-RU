---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 4183f3a1c60bd9e2bdcff5227426db1f07c313cf
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697520"
---
# <span data-ttu-id="4562b-104">интерфейс ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4562b-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="4562b-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="4562b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4562b-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="4562b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="4562b-107">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="4562b-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="4562b-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4562b-108">Summary</span></span>

 <span data-ttu-id="4562b-109">Участников</span><span class="sxs-lookup"><span data-stu-id="4562b-109">Members</span></span>                        | <span data-ttu-id="4562b-110">Описания</span><span class="sxs-lookup"><span data-stu-id="4562b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4562b-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="4562b-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="4562b-112">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="4562b-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="4562b-113">Участников</span><span class="sxs-lookup"><span data-stu-id="4562b-113">Members</span></span>

#### <span data-ttu-id="4562b-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="4562b-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="4562b-115">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="4562b-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="4562b-116">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="4562b-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


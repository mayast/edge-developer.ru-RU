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
ms.openlocfilehash: 0efc1656b8204b9775002db49e0e4a5734682cc4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654631"
---
# <span data-ttu-id="d2272-104">интерфейс ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d2272-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="d2272-105">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d2272-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="d2272-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d2272-106">Summary</span></span>

 <span data-ttu-id="d2272-107">Участников</span><span class="sxs-lookup"><span data-stu-id="d2272-107">Members</span></span>                        | <span data-ttu-id="d2272-108">Описания</span><span class="sxs-lookup"><span data-stu-id="d2272-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d2272-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d2272-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="d2272-110">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="d2272-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="d2272-111">Участников</span><span class="sxs-lookup"><span data-stu-id="d2272-111">Members</span></span>

#### <span data-ttu-id="d2272-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d2272-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="d2272-113">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="d2272-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="d2272-114">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="d2272-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


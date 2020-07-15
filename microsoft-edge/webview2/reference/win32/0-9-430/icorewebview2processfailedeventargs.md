---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f4238f0d75f39727260296703e84740ca77b30d4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877739"
---
# <span data-ttu-id="96dc0-104">0.9.430-Interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="96dc0-104">0.9.430 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="96dc0-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="96dc0-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="96dc0-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="96dc0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="96dc0-107">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="96dc0-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="96dc0-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="96dc0-108">Summary</span></span>

 <span data-ttu-id="96dc0-109">Участников</span><span class="sxs-lookup"><span data-stu-id="96dc0-109">Members</span></span>                        | <span data-ttu-id="96dc0-110">Описания</span><span class="sxs-lookup"><span data-stu-id="96dc0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="96dc0-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="96dc0-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="96dc0-112">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="96dc0-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="96dc0-113">Участников</span><span class="sxs-lookup"><span data-stu-id="96dc0-113">Members</span></span>

#### <span data-ttu-id="96dc0-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="96dc0-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="96dc0-115">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="96dc0-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="96dc0-116">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="96dc0-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


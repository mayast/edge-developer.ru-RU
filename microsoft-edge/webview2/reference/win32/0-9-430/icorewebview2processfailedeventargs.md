---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8fba2759ce0e264dcde515ee1191ec819f26eef9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654838"
---
# <span data-ttu-id="28456-104">интерфейс ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="28456-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="28456-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="28456-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="28456-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="28456-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="28456-107">Аргументы события для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="28456-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="28456-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="28456-108">Summary</span></span>

 <span data-ttu-id="28456-109">Участников</span><span class="sxs-lookup"><span data-stu-id="28456-109">Members</span></span>                        | <span data-ttu-id="28456-110">Описания</span><span class="sxs-lookup"><span data-stu-id="28456-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="28456-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="28456-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="28456-112">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="28456-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="28456-113">Участников</span><span class="sxs-lookup"><span data-stu-id="28456-113">Members</span></span>

#### <span data-ttu-id="28456-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="28456-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="28456-115">Произошел сбой процесса.</span><span class="sxs-lookup"><span data-stu-id="28456-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="28456-116">общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="28456-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


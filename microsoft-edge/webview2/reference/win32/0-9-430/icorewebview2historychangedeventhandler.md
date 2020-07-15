---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6afd1983b90b4412fd3011dc35f192809a9583b7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881020"
---
# <span data-ttu-id="55496-104">0.9.430-Interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="55496-104">0.9.430 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="55496-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="55496-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="55496-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="55496-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="55496-107">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="55496-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="55496-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="55496-108">Summary</span></span>

 <span data-ttu-id="55496-109">Участников</span><span class="sxs-lookup"><span data-stu-id="55496-109">Members</span></span>                        | <span data-ttu-id="55496-110">Описания</span><span class="sxs-lookup"><span data-stu-id="55496-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="55496-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="55496-111">Invoke</span></span>](#invoke) | <span data-ttu-id="55496-112">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="55496-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="55496-113">Участников</span><span class="sxs-lookup"><span data-stu-id="55496-113">Members</span></span>

#### <span data-ttu-id="55496-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="55496-114">Invoke</span></span> 

<span data-ttu-id="55496-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="55496-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="55496-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="55496-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>


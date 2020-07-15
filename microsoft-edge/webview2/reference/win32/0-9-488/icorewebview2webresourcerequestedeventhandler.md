---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 715af5cbf2bbaf8301e39dce1516019102b61ab1
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877331"
---
# <span data-ttu-id="7d4a5-104">0.9.515-Interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7d4a5-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7d4a5-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7d4a5-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="7d4a5-107">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="7d4a5-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7d4a5-108">Summary</span></span>

 <span data-ttu-id="7d4a5-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7d4a5-109">Members</span></span>                        | <span data-ttu-id="7d4a5-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7d4a5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7d4a5-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="7d4a5-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7d4a5-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7d4a5-113">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="7d4a5-114">Участников</span><span class="sxs-lookup"><span data-stu-id="7d4a5-114">Members</span></span>

#### <span data-ttu-id="7d4a5-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="7d4a5-115">Invoke</span></span> 

<span data-ttu-id="7d4a5-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7d4a5-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7d4a5-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


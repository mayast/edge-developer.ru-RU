---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 602c00258e9ff3362269ebe90de8306ecbd7503e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654675"
---
# <span data-ttu-id="622cb-104">интерфейс IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="622cb-104">interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="622cb-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="622cb-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="622cb-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="622cb-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="622cb-107">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="622cb-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="622cb-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="622cb-108">Summary</span></span>

 <span data-ttu-id="622cb-109">Участников</span><span class="sxs-lookup"><span data-stu-id="622cb-109">Members</span></span>                        | <span data-ttu-id="622cb-110">Описания</span><span class="sxs-lookup"><span data-stu-id="622cb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="622cb-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="622cb-111">Invoke</span></span>](#invoke) | <span data-ttu-id="622cb-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="622cb-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="622cb-113">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="622cb-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="622cb-114">Участников</span><span class="sxs-lookup"><span data-stu-id="622cb-114">Members</span></span>

#### <span data-ttu-id="622cb-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="622cb-115">Invoke</span></span> 

<span data-ttu-id="622cb-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="622cb-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="622cb-117">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="622cb-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


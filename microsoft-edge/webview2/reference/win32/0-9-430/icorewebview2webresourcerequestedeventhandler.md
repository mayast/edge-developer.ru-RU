---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d2b1aa9bbfc15aa44023a43425bb2fc939165cae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880159"
---
# <span data-ttu-id="99b43-104">0.9.430-Interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="99b43-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="99b43-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="99b43-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="99b43-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="99b43-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="99b43-107">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="99b43-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="99b43-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="99b43-108">Summary</span></span>

 <span data-ttu-id="99b43-109">Участников</span><span class="sxs-lookup"><span data-stu-id="99b43-109">Members</span></span>                        | <span data-ttu-id="99b43-110">Описания</span><span class="sxs-lookup"><span data-stu-id="99b43-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99b43-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="99b43-111">Invoke</span></span>](#invoke) | <span data-ttu-id="99b43-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="99b43-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="99b43-113">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="99b43-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="99b43-114">Участников</span><span class="sxs-lookup"><span data-stu-id="99b43-114">Members</span></span>

#### <span data-ttu-id="99b43-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="99b43-115">Invoke</span></span> 

<span data-ttu-id="99b43-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="99b43-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="99b43-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="99b43-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


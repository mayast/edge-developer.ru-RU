---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c4f76c468cc5001c9eae347247dd5ffb8a60594f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654974"
---
# <span data-ttu-id="8cc20-104">интерфейс ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8cc20-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8cc20-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="8cc20-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8cc20-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="8cc20-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="8cc20-107">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="8cc20-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="8cc20-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8cc20-108">Summary</span></span>

 <span data-ttu-id="8cc20-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8cc20-109">Members</span></span>                        | <span data-ttu-id="8cc20-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8cc20-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8cc20-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="8cc20-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8cc20-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8cc20-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="8cc20-113">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="8cc20-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="8cc20-114">Участников</span><span class="sxs-lookup"><span data-stu-id="8cc20-114">Members</span></span>

#### <span data-ttu-id="8cc20-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="8cc20-115">Invoke</span></span> 

<span data-ttu-id="8cc20-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8cc20-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8cc20-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8cc20-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


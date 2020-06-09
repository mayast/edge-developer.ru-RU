---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 622a7e93912a3380cc0d7dabae9293734cd3fcfa
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697940"
---
# <span data-ttu-id="dd7b6-104">интерфейс ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="dd7b6-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="dd7b6-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="dd7b6-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="dd7b6-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="dd7b6-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="dd7b6-107">Активируется, когда HTTP-запрос выполняется в WebView.</span><span class="sxs-lookup"><span data-stu-id="dd7b6-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="dd7b6-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="dd7b6-108">Summary</span></span>

 <span data-ttu-id="dd7b6-109">Участников</span><span class="sxs-lookup"><span data-stu-id="dd7b6-109">Members</span></span>                        | <span data-ttu-id="dd7b6-110">Описания</span><span class="sxs-lookup"><span data-stu-id="dd7b6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dd7b6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="dd7b6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="dd7b6-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="dd7b6-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="dd7b6-113">Ведущее приложение может переопределить запросы, заголовки ответов и содержимое ответа.</span><span class="sxs-lookup"><span data-stu-id="dd7b6-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="dd7b6-114">Участников</span><span class="sxs-lookup"><span data-stu-id="dd7b6-114">Members</span></span>

#### <span data-ttu-id="dd7b6-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="dd7b6-115">Invoke</span></span> 

<span data-ttu-id="dd7b6-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="dd7b6-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="dd7b6-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="dd7b6-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


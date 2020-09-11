---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6c97e0591d55570f4076f6a5c4f2eebc2cc7c5ad
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012418"
---
# <span data-ttu-id="b5270-104">интерфейс ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b5270-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b5270-105">Обработчик завершения для асинхронного метода PopulateResponseContent.</span><span class="sxs-lookup"><span data-stu-id="b5270-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="b5270-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b5270-106">Summary</span></span>

 <span data-ttu-id="b5270-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b5270-107">Members</span></span>                        | <span data-ttu-id="b5270-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b5270-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b5270-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b5270-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b5270-110">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b5270-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="b5270-111">Он вызывается, когда доступен поток содержимого для ответа на событие WebResourceResponseReceieved.</span><span class="sxs-lookup"><span data-stu-id="b5270-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="b5270-112">Участников</span><span class="sxs-lookup"><span data-stu-id="b5270-112">Members</span></span>

#### <span data-ttu-id="b5270-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="b5270-113">Invoke</span></span> 

<span data-ttu-id="b5270-114">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b5270-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b5270-115">общедоступный [вызов](#invoke)HRESULT (код ошибки HRESULT)</span><span class="sxs-lookup"><span data-stu-id="b5270-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>


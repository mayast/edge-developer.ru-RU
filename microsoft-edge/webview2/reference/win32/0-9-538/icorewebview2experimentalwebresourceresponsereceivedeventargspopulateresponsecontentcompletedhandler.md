---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: c021cfa866e55bfdf30185eeaf6015db1b523271
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886570"
---
# <span data-ttu-id="173be-104">интерфейс ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="173be-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="173be-105">Обработчик завершения для асинхронного метода PopulateResponseContent.</span><span class="sxs-lookup"><span data-stu-id="173be-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="173be-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="173be-106">Summary</span></span>

 <span data-ttu-id="173be-107">Участников</span><span class="sxs-lookup"><span data-stu-id="173be-107">Members</span></span>                        | <span data-ttu-id="173be-108">Описания</span><span class="sxs-lookup"><span data-stu-id="173be-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="173be-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="173be-109">Invoke</span></span>](#invoke) | <span data-ttu-id="173be-110">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="173be-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="173be-111">Он вызывается, когда доступен поток содержимого для ответа на событие WebResourceResponseReceieved.</span><span class="sxs-lookup"><span data-stu-id="173be-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="173be-112">Участников</span><span class="sxs-lookup"><span data-stu-id="173be-112">Members</span></span>

#### <span data-ttu-id="173be-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="173be-113">Invoke</span></span> 

<span data-ttu-id="173be-114">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="173be-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="173be-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="173be-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6a854eb9ca73f45e366edfa144c273f780bcee94
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011414"
---
# <span data-ttu-id="aaa95-104">0.9.579-Interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="aaa95-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="aaa95-105">Обработчик завершения для асинхронного метода PopulateResponseContent.</span><span class="sxs-lookup"><span data-stu-id="aaa95-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="aaa95-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="aaa95-106">Summary</span></span>

 <span data-ttu-id="aaa95-107">Участников</span><span class="sxs-lookup"><span data-stu-id="aaa95-107">Members</span></span>                        | <span data-ttu-id="aaa95-108">Описания</span><span class="sxs-lookup"><span data-stu-id="aaa95-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aaa95-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="aaa95-109">Invoke</span></span>](#invoke) | <span data-ttu-id="aaa95-110">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="aaa95-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="aaa95-111">Он вызывается, когда доступен поток содержимого для ответа на событие WebResourceResponseReceieved.</span><span class="sxs-lookup"><span data-stu-id="aaa95-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="aaa95-112">Участников</span><span class="sxs-lookup"><span data-stu-id="aaa95-112">Members</span></span>

#### <span data-ttu-id="aaa95-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="aaa95-113">Invoke</span></span> 

<span data-ttu-id="aaa95-114">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="aaa95-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="aaa95-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="aaa95-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


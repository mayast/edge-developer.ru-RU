---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 013a7076648b93bf259d28422f418365d988a586
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877442"
---
# <span data-ttu-id="cf739-104">интерфейс ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="cf739-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="cf739-105">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="cf739-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="cf739-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="cf739-106">Summary</span></span>

 <span data-ttu-id="cf739-107">Участников</span><span class="sxs-lookup"><span data-stu-id="cf739-107">Members</span></span>                        | <span data-ttu-id="cf739-108">Описания</span><span class="sxs-lookup"><span data-stu-id="cf739-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf739-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="cf739-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cf739-110">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="cf739-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="cf739-111">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="cf739-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="cf739-112">Участников</span><span class="sxs-lookup"><span data-stu-id="cf739-112">Members</span></span>

#### <span data-ttu-id="cf739-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="cf739-113">Invoke</span></span> 

<span data-ttu-id="cf739-114">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="cf739-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="cf739-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="cf739-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


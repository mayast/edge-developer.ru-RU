---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 321aff5097783391e4596c22dbd5cb906e45dace
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881160"
---
# <span data-ttu-id="6202d-104">0.9.430-Interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6202d-104">0.9.430 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="6202d-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6202d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6202d-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="6202d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6202d-107">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="6202d-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="6202d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6202d-108">Summary</span></span>

 <span data-ttu-id="6202d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="6202d-109">Members</span></span>                        | <span data-ttu-id="6202d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="6202d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6202d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="6202d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="6202d-112">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="6202d-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="6202d-113">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="6202d-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="6202d-114">Участников</span><span class="sxs-lookup"><span data-stu-id="6202d-114">Members</span></span>

#### <span data-ttu-id="6202d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="6202d-115">Invoke</span></span> 

<span data-ttu-id="6202d-116">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="6202d-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6202d-117">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="6202d-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


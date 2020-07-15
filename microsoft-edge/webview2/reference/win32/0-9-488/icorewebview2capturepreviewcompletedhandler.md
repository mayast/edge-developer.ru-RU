---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 5b560cc0cd91c3445b539dbc6e317d6e6fe0c2d5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880915"
---
# <span data-ttu-id="404ae-104">0.9.515-Interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="404ae-104">0.9.515 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="404ae-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="404ae-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="404ae-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="404ae-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="404ae-107">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="404ae-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="404ae-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="404ae-108">Summary</span></span>

 <span data-ttu-id="404ae-109">Участников</span><span class="sxs-lookup"><span data-stu-id="404ae-109">Members</span></span>                        | <span data-ttu-id="404ae-110">Описания</span><span class="sxs-lookup"><span data-stu-id="404ae-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="404ae-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="404ae-111">Invoke</span></span>](#invoke) | <span data-ttu-id="404ae-112">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="404ae-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="404ae-113">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="404ae-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="404ae-114">Участников</span><span class="sxs-lookup"><span data-stu-id="404ae-114">Members</span></span>

#### <span data-ttu-id="404ae-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="404ae-115">Invoke</span></span> 

<span data-ttu-id="404ae-116">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="404ae-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="404ae-117">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="404ae-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


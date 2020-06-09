---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 290d82666e5b9c5062132e1eb7515e39e2deb978
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699202"
---
# <span data-ttu-id="08976-104">интерфейс ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="08976-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="08976-105">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="08976-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="08976-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="08976-106">Summary</span></span>

 <span data-ttu-id="08976-107">Участников</span><span class="sxs-lookup"><span data-stu-id="08976-107">Members</span></span>                        | <span data-ttu-id="08976-108">Описания</span><span class="sxs-lookup"><span data-stu-id="08976-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="08976-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="08976-109">Invoke</span></span>](#invoke) | <span data-ttu-id="08976-110">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="08976-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="08976-111">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="08976-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="08976-112">Участников</span><span class="sxs-lookup"><span data-stu-id="08976-112">Members</span></span>

#### <span data-ttu-id="08976-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="08976-113">Invoke</span></span> 

<span data-ttu-id="08976-114">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="08976-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="08976-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="08976-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


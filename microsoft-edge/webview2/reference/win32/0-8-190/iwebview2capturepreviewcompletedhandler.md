---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 991c09167ba3fe382c74d6244c76ffae25d628a6
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886194"
---
# <span data-ttu-id="26fb5-104">0.8.355-Interface IWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="26fb5-104">0.8.355 - interface IWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="26fb5-105">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="26fb5-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="26fb5-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="26fb5-106">Summary</span></span>

 <span data-ttu-id="26fb5-107">Участников</span><span class="sxs-lookup"><span data-stu-id="26fb5-107">Members</span></span>                        | <span data-ttu-id="26fb5-108">Описания</span><span class="sxs-lookup"><span data-stu-id="26fb5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="26fb5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="26fb5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="26fb5-110">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="26fb5-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="26fb5-111">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="26fb5-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="26fb5-112">Участников</span><span class="sxs-lookup"><span data-stu-id="26fb5-112">Members</span></span>

#### <span data-ttu-id="26fb5-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="26fb5-113">Invoke</span></span> 

<span data-ttu-id="26fb5-114">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="26fb5-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="26fb5-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="26fb5-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


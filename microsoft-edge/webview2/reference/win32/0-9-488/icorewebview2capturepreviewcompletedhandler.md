---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6aaac0d062d0e97d3ec0c87bec243c5cf682ad6f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697051"
---
# <span data-ttu-id="19f73-104">интерфейс ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="19f73-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="19f73-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="19f73-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="19f73-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="19f73-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="19f73-107">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="19f73-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="19f73-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="19f73-108">Summary</span></span>

 <span data-ttu-id="19f73-109">Участников</span><span class="sxs-lookup"><span data-stu-id="19f73-109">Members</span></span>                        | <span data-ttu-id="19f73-110">Описания</span><span class="sxs-lookup"><span data-stu-id="19f73-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="19f73-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="19f73-111">Invoke</span></span>](#invoke) | <span data-ttu-id="19f73-112">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="19f73-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="19f73-113">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="19f73-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="19f73-114">Участников</span><span class="sxs-lookup"><span data-stu-id="19f73-114">Members</span></span>

#### <span data-ttu-id="19f73-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="19f73-115">Invoke</span></span> 

<span data-ttu-id="19f73-116">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="19f73-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="19f73-117">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="19f73-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


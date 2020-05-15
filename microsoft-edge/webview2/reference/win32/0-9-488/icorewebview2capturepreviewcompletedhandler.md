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
ms.openlocfilehash: 793dbde462e25ae0bfe0dc0bc475cc49e7237fb2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654914"
---
# <span data-ttu-id="72201-104">интерфейс ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="72201-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="72201-105">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="72201-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="72201-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="72201-106">Summary</span></span>

 <span data-ttu-id="72201-107">Участников</span><span class="sxs-lookup"><span data-stu-id="72201-107">Members</span></span>                        | <span data-ttu-id="72201-108">Описания</span><span class="sxs-lookup"><span data-stu-id="72201-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="72201-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="72201-109">Invoke</span></span>](#invoke) | <span data-ttu-id="72201-110">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="72201-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="72201-111">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="72201-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="72201-112">Участников</span><span class="sxs-lookup"><span data-stu-id="72201-112">Members</span></span>

#### <span data-ttu-id="72201-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="72201-113">Invoke</span></span> 

<span data-ttu-id="72201-114">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="72201-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="72201-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="72201-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


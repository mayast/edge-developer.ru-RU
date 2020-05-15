---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 06f7f664acb5f169215b603841d935730532b62b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654793"
---
# <span data-ttu-id="a6110-104">интерфейс ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a6110-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a6110-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="a6110-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a6110-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="a6110-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a6110-107">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="a6110-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="a6110-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a6110-108">Summary</span></span>

 <span data-ttu-id="a6110-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a6110-109">Members</span></span>                        | <span data-ttu-id="a6110-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a6110-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a6110-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a6110-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a6110-112">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a6110-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="a6110-113">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="a6110-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="a6110-114">Участников</span><span class="sxs-lookup"><span data-stu-id="a6110-114">Members</span></span>

#### <span data-ttu-id="a6110-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="a6110-115">Invoke</span></span> 

<span data-ttu-id="a6110-116">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a6110-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a6110-117">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="a6110-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


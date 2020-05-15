---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 0cdb6dc17549022bac6ada366f5f54dd5b9b7e12
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654957"
---
# <span data-ttu-id="9ea54-104">интерфейс IWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="9ea54-104">interface IWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="9ea54-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="9ea54-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="9ea54-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="9ea54-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9ea54-107">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="9ea54-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="9ea54-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9ea54-108">Summary</span></span>

 <span data-ttu-id="9ea54-109">Участников</span><span class="sxs-lookup"><span data-stu-id="9ea54-109">Members</span></span>                        | <span data-ttu-id="9ea54-110">Описания</span><span class="sxs-lookup"><span data-stu-id="9ea54-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ea54-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="9ea54-111">Invoke</span></span>](#invoke) | <span data-ttu-id="9ea54-112">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="9ea54-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="9ea54-113">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="9ea54-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="9ea54-114">Участников</span><span class="sxs-lookup"><span data-stu-id="9ea54-114">Members</span></span>

#### <span data-ttu-id="9ea54-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="9ea54-115">Invoke</span></span> 

<span data-ttu-id="9ea54-116">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="9ea54-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9ea54-117">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="9ea54-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


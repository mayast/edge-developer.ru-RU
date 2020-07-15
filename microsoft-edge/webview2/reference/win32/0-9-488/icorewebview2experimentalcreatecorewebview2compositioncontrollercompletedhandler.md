---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9aa9a18701621ca78b74b12340ef5132953fbd2b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880670"
---
# <span data-ttu-id="a260f-104">0.9.515-Interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a260f-104">0.9.515 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a260f-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="a260f-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a260f-106">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="a260f-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="a260f-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a260f-107">Summary</span></span>

 <span data-ttu-id="a260f-108">Участников</span><span class="sxs-lookup"><span data-stu-id="a260f-108">Members</span></span>                        | <span data-ttu-id="a260f-109">Описания</span><span class="sxs-lookup"><span data-stu-id="a260f-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a260f-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="a260f-110">Invoke</span></span>](#invoke) | <span data-ttu-id="a260f-111">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a260f-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a260f-112">Участников</span><span class="sxs-lookup"><span data-stu-id="a260f-112">Members</span></span>

#### <span data-ttu-id="a260f-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="a260f-113">Invoke</span></span> 

<span data-ttu-id="a260f-114">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a260f-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a260f-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span><span class="sxs-lookup"><span data-stu-id="a260f-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


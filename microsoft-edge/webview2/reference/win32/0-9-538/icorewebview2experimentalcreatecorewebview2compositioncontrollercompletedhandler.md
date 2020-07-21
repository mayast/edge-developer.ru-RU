---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: ab811f717c90ce77293c74a0e54bd3a66c896e72
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885270"
---
# <span data-ttu-id="88656-104">интерфейс ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="88656-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="88656-105">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="88656-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="88656-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="88656-106">Summary</span></span>

 <span data-ttu-id="88656-107">Участников</span><span class="sxs-lookup"><span data-stu-id="88656-107">Members</span></span>                        | <span data-ttu-id="88656-108">Описания</span><span class="sxs-lookup"><span data-stu-id="88656-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="88656-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="88656-109">Invoke</span></span>](#invoke) | <span data-ttu-id="88656-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="88656-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="88656-111">Участников</span><span class="sxs-lookup"><span data-stu-id="88656-111">Members</span></span>

#### <span data-ttu-id="88656-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="88656-112">Invoke</span></span> 

<span data-ttu-id="88656-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="88656-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="88656-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span><span class="sxs-lookup"><span data-stu-id="88656-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


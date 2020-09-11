---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: 8fc3efa6bf1ba9a9e721dcba67e8350ded38cc62
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011141"
---
# <span data-ttu-id="ddc93-104">0.9.579-Interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ddc93-104">0.9.579 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ddc93-105">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="ddc93-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="ddc93-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ddc93-106">Summary</span></span>

 <span data-ttu-id="ddc93-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ddc93-107">Members</span></span>                        | <span data-ttu-id="ddc93-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ddc93-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ddc93-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ddc93-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ddc93-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ddc93-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ddc93-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ddc93-111">Members</span></span>

#### <span data-ttu-id="ddc93-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ddc93-112">Invoke</span></span> 

<span data-ttu-id="ddc93-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ddc93-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ddc93-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span><span class="sxs-lookup"><span data-stu-id="ddc93-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 91c4e7885526def5de6fd1910a4a6f06c6a6953a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654712"
---
# <span data-ttu-id="1d1ca-104">интерфейс ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1d1ca-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="1d1ca-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="1d1ca-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="1d1ca-106">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="1d1ca-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="1d1ca-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1d1ca-107">Summary</span></span>

 <span data-ttu-id="1d1ca-108">Участников</span><span class="sxs-lookup"><span data-stu-id="1d1ca-108">Members</span></span>                        | <span data-ttu-id="1d1ca-109">Описания</span><span class="sxs-lookup"><span data-stu-id="1d1ca-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1d1ca-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="1d1ca-110">Invoke</span></span>](#invoke) | <span data-ttu-id="1d1ca-111">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="1d1ca-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="1d1ca-112">Участников</span><span class="sxs-lookup"><span data-stu-id="1d1ca-112">Members</span></span>

#### <span data-ttu-id="1d1ca-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="1d1ca-113">Invoke</span></span> 

<span data-ttu-id="1d1ca-114">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="1d1ca-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="1d1ca-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span><span class="sxs-lookup"><span data-stu-id="1d1ca-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


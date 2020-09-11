---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 845c3a3f0241fb66032ecf818c484b6110258327
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012572"
---
# <span data-ttu-id="e0c9d-104">интерфейс ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e0c9d-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e0c9d-105">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="e0c9d-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="e0c9d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e0c9d-106">Summary</span></span>

 <span data-ttu-id="e0c9d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e0c9d-107">Members</span></span>                        | <span data-ttu-id="e0c9d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e0c9d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e0c9d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e0c9d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e0c9d-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="e0c9d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e0c9d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e0c9d-111">Members</span></span>

#### <span data-ttu-id="e0c9d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e0c9d-112">Invoke</span></span> 

<span data-ttu-id="e0c9d-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="e0c9d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e0c9d-114">общедоступный [вызов](#invoke)HRESULT (errorCode, код HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="e0c9d-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


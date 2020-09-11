---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 3ecafb8181b04032bf121a93af3771cfcad8fa91
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011169"
---
# <span data-ttu-id="bf70a-104">0.9.579-Interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="bf70a-104">0.9.579 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="bf70a-105">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="bf70a-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="bf70a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="bf70a-106">Summary</span></span>

 <span data-ttu-id="bf70a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="bf70a-107">Members</span></span>                        | <span data-ttu-id="bf70a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="bf70a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bf70a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="bf70a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bf70a-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="bf70a-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="bf70a-111">Участников</span><span class="sxs-lookup"><span data-stu-id="bf70a-111">Members</span></span>

#### <span data-ttu-id="bf70a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="bf70a-112">Invoke</span></span> 

<span data-ttu-id="bf70a-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="bf70a-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="bf70a-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="bf70a-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


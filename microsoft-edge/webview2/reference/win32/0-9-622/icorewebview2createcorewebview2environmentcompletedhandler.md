---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
ms.openlocfilehash: 3f6b6b9a2d4df2a450b4589c351c3ea98f7cc28f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012571"
---
# <span data-ttu-id="a767e-104">интерфейс ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a767e-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a767e-105">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="a767e-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="a767e-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a767e-106">Summary</span></span>

 <span data-ttu-id="a767e-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a767e-107">Members</span></span>                        | <span data-ttu-id="a767e-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a767e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a767e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a767e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a767e-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a767e-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a767e-111">Участников</span><span class="sxs-lookup"><span data-stu-id="a767e-111">Members</span></span>

#### <span data-ttu-id="a767e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a767e-112">Invoke</span></span> 

<span data-ttu-id="a767e-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a767e-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a767e-114">общедоступный [вызов](#invoke)HRESULT (errorCode, код HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* createdEnvironment)</span><span class="sxs-lookup"><span data-stu-id="a767e-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2Environment](icorewebview2environment.md) \* createdEnvironment)</span></span>


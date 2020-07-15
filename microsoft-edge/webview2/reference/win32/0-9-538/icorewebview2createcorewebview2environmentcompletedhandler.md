---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
ms.openlocfilehash: c41da3c6f88c06d0642d00f38a8181acb079a009
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877408"
---
# <span data-ttu-id="ffdbf-104">интерфейс ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ffdbf-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ffdbf-105">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="ffdbf-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ffdbf-106">Summary</span></span>

 <span data-ttu-id="ffdbf-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ffdbf-107">Members</span></span>                        | <span data-ttu-id="ffdbf-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ffdbf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ffdbf-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ffdbf-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ffdbf-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ffdbf-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ffdbf-111">Members</span></span>

#### <span data-ttu-id="ffdbf-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ffdbf-112">Invoke</span></span> 

<span data-ttu-id="ffdbf-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ffdbf-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="ffdbf-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: fe81be15531cedae7a01355cbb6b6b27b52f15cc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878633"
---
# <span data-ttu-id="71ff4-104">0.8.355-Interface IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="71ff4-104">0.8.355 - interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="71ff4-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="71ff4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="71ff4-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="71ff4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="71ff4-107">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="71ff4-107">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="71ff4-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="71ff4-108">Summary</span></span>

 <span data-ttu-id="71ff4-109">Участников</span><span class="sxs-lookup"><span data-stu-id="71ff4-109">Members</span></span>                        | <span data-ttu-id="71ff4-110">Описания</span><span class="sxs-lookup"><span data-stu-id="71ff4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="71ff4-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="71ff4-111">Invoke</span></span>](#invoke) | <span data-ttu-id="71ff4-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="71ff4-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="71ff4-113">Участников</span><span class="sxs-lookup"><span data-stu-id="71ff4-113">Members</span></span>

#### <span data-ttu-id="71ff4-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="71ff4-114">Invoke</span></span> 

<span data-ttu-id="71ff4-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="71ff4-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="71ff4-116">общедоступный [вызов](#invoke)HRESULT (результат HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="71ff4-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>


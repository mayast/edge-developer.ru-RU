---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebViewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 3459bf9c44dc4f0ce10bc383f6f695d4949023da
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878640"
---
# <span data-ttu-id="27938-104">0.8.355-Interface IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="27938-104">0.8.355 - interface IWebView2CreateWebViewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="27938-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="27938-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="27938-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="27938-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="27938-107">Вызывающий объект реализует этот интерфейс для получения WebView, созданного с помощью CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="27938-107">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="27938-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="27938-108">Summary</span></span>

 <span data-ttu-id="27938-109">Участников</span><span class="sxs-lookup"><span data-stu-id="27938-109">Members</span></span>                        | <span data-ttu-id="27938-110">Описания</span><span class="sxs-lookup"><span data-stu-id="27938-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="27938-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="27938-111">Invoke</span></span>](#invoke) | <span data-ttu-id="27938-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="27938-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="27938-113">Участников</span><span class="sxs-lookup"><span data-stu-id="27938-113">Members</span></span>

#### <span data-ttu-id="27938-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="27938-114">Invoke</span></span> 

<span data-ttu-id="27938-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="27938-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="27938-116">общедоступный [вызов](#invoke)HRESULT (результат HRESULT,[IWebView2WebView](IWebView2WebView.md) \* webView)</span><span class="sxs-lookup"><span data-stu-id="27938-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>


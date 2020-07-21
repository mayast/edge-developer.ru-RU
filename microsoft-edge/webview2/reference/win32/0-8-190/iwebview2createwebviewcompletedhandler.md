---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebViewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 381f46c6682a77905d9caa720e4ba9b2d1d531b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886154"
---
# <span data-ttu-id="81f33-104">0.8.355-Interface IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="81f33-104">0.8.355 - interface IWebView2CreateWebViewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="81f33-105">Вызывающий объект реализует этот интерфейс для получения WebView, созданного с помощью CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="81f33-105">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="81f33-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="81f33-106">Summary</span></span>

 <span data-ttu-id="81f33-107">Участников</span><span class="sxs-lookup"><span data-stu-id="81f33-107">Members</span></span>                        | <span data-ttu-id="81f33-108">Описания</span><span class="sxs-lookup"><span data-stu-id="81f33-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="81f33-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="81f33-109">Invoke</span></span>](#invoke) | <span data-ttu-id="81f33-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="81f33-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="81f33-111">Участников</span><span class="sxs-lookup"><span data-stu-id="81f33-111">Members</span></span>

#### <span data-ttu-id="81f33-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="81f33-112">Invoke</span></span> 

<span data-ttu-id="81f33-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="81f33-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="81f33-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT,[IWebView2WebView](IWebView2WebView.md) \* webView)</span><span class="sxs-lookup"><span data-stu-id="81f33-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>


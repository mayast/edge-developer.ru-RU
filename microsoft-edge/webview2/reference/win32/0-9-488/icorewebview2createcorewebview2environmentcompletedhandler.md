---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1082ea61b98b953277219d78a2944a2487b47a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884444"
---
# <span data-ttu-id="774c0-104">0.9.515-Interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="774c0-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="774c0-105">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="774c0-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="774c0-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="774c0-106">Summary</span></span>

 <span data-ttu-id="774c0-107">Участников</span><span class="sxs-lookup"><span data-stu-id="774c0-107">Members</span></span>                        | <span data-ttu-id="774c0-108">Описания</span><span class="sxs-lookup"><span data-stu-id="774c0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="774c0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="774c0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="774c0-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="774c0-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="774c0-111">Участников</span><span class="sxs-lookup"><span data-stu-id="774c0-111">Members</span></span>

#### <span data-ttu-id="774c0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="774c0-112">Invoke</span></span> 

<span data-ttu-id="774c0-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="774c0-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="774c0-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="774c0-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


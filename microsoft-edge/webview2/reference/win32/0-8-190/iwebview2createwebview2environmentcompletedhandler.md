---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 9937fe08f440ce468f178e4ac17935bbb8a1a8ed
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886173"
---
# <span data-ttu-id="39718-104">0.8.355-Interface IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="39718-104">0.8.355 - interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="39718-105">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="39718-105">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="39718-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="39718-106">Summary</span></span>

 <span data-ttu-id="39718-107">Участников</span><span class="sxs-lookup"><span data-stu-id="39718-107">Members</span></span>                        | <span data-ttu-id="39718-108">Описания</span><span class="sxs-lookup"><span data-stu-id="39718-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="39718-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="39718-109">Invoke</span></span>](#invoke) | <span data-ttu-id="39718-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="39718-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="39718-111">Участников</span><span class="sxs-lookup"><span data-stu-id="39718-111">Members</span></span>

#### <span data-ttu-id="39718-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="39718-112">Invoke</span></span> 

<span data-ttu-id="39718-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="39718-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="39718-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="39718-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>


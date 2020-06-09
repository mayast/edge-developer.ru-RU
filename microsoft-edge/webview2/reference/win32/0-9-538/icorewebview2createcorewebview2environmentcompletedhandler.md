---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: dbc1a3e05f9cdc5b5ced2e0b7d489b06392e6100
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699187"
---
# <span data-ttu-id="a0a85-104">интерфейс ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a0a85-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a0a85-105">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="a0a85-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="a0a85-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a0a85-106">Summary</span></span>

 <span data-ttu-id="a0a85-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a0a85-107">Members</span></span>                        | <span data-ttu-id="a0a85-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a0a85-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0a85-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a0a85-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a0a85-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a0a85-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a0a85-111">Участников</span><span class="sxs-lookup"><span data-stu-id="a0a85-111">Members</span></span>

#### <span data-ttu-id="a0a85-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a0a85-112">Invoke</span></span> 

<span data-ttu-id="a0a85-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a0a85-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a0a85-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="a0a85-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


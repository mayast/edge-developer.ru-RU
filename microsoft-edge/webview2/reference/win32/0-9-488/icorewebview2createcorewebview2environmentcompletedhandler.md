---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: da49c1762ad7b7f3f366754bb9b05b7d16b861b7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654893"
---
# <span data-ttu-id="225fc-104">интерфейс ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="225fc-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="225fc-105">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="225fc-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="225fc-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="225fc-106">Summary</span></span>

 <span data-ttu-id="225fc-107">Участников</span><span class="sxs-lookup"><span data-stu-id="225fc-107">Members</span></span>                        | <span data-ttu-id="225fc-108">Описания</span><span class="sxs-lookup"><span data-stu-id="225fc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="225fc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="225fc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="225fc-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="225fc-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="225fc-111">Участников</span><span class="sxs-lookup"><span data-stu-id="225fc-111">Members</span></span>

#### <span data-ttu-id="225fc-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="225fc-112">Invoke</span></span> 

<span data-ttu-id="225fc-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="225fc-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="225fc-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="225fc-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


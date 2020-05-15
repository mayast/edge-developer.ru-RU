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
ms.openlocfilehash: 49b2baf825d65b97b4b1fa62d06b2f6d6b7bd26d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654897"
---
# <span data-ttu-id="ffe1b-104">интерфейс ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ffe1b-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ffe1b-105">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="ffe1b-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="ffe1b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ffe1b-106">Summary</span></span>

 <span data-ttu-id="ffe1b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ffe1b-107">Members</span></span>                        | <span data-ttu-id="ffe1b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ffe1b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ffe1b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ffe1b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ffe1b-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ffe1b-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ffe1b-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ffe1b-111">Members</span></span>

#### <span data-ttu-id="ffe1b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ffe1b-112">Invoke</span></span> 

<span data-ttu-id="ffe1b-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ffe1b-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ffe1b-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="ffe1b-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


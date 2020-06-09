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
ms.openlocfilehash: 45ac3cf4728f8b09f9ce65a30b53506fc2829c9d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699194"
---
# <span data-ttu-id="7a2c5-104">интерфейс ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7a2c5-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7a2c5-105">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7a2c5-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="7a2c5-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7a2c5-106">Summary</span></span>

 <span data-ttu-id="7a2c5-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7a2c5-107">Members</span></span>                        | <span data-ttu-id="7a2c5-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7a2c5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a2c5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7a2c5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7a2c5-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7a2c5-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7a2c5-111">Участников</span><span class="sxs-lookup"><span data-stu-id="7a2c5-111">Members</span></span>

#### <span data-ttu-id="7a2c5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7a2c5-112">Invoke</span></span> 

<span data-ttu-id="7a2c5-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7a2c5-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7a2c5-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="7a2c5-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


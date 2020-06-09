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
ms.openlocfilehash: a675bede2e1e509f3cfcc7490ac157da3f6d876c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699204"
---
# <span data-ttu-id="989d7-104">интерфейс ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="989d7-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="989d7-105">Вызывающий объект реализует этот интерфейс, чтобы получать результаты выполнения CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="989d7-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="989d7-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="989d7-106">Summary</span></span>

 <span data-ttu-id="989d7-107">Участников</span><span class="sxs-lookup"><span data-stu-id="989d7-107">Members</span></span>                        | <span data-ttu-id="989d7-108">Описания</span><span class="sxs-lookup"><span data-stu-id="989d7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="989d7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="989d7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="989d7-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="989d7-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="989d7-111">Участников</span><span class="sxs-lookup"><span data-stu-id="989d7-111">Members</span></span>

#### <span data-ttu-id="989d7-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="989d7-112">Invoke</span></span> 

<span data-ttu-id="989d7-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="989d7-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="989d7-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="989d7-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


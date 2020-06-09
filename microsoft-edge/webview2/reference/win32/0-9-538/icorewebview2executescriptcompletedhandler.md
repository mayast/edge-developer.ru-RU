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
ms.openlocfilehash: a3dde4581692fb30cada16d9166bda62a0d69179
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699174"
---
# <span data-ttu-id="adee1-104">интерфейс ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="adee1-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="adee1-105">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="adee1-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="adee1-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="adee1-106">Summary</span></span>

 <span data-ttu-id="adee1-107">Участников</span><span class="sxs-lookup"><span data-stu-id="adee1-107">Members</span></span>                        | <span data-ttu-id="adee1-108">Описания</span><span class="sxs-lookup"><span data-stu-id="adee1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="adee1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="adee1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="adee1-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="adee1-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="adee1-111">Участников</span><span class="sxs-lookup"><span data-stu-id="adee1-111">Members</span></span>

#### <span data-ttu-id="adee1-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="adee1-112">Invoke</span></span> 

<span data-ttu-id="adee1-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="adee1-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="adee1-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="adee1-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


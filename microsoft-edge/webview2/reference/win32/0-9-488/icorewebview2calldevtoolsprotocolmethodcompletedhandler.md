---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: fda3ab31405a7d6353af1a670a2804e973577c8e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654826"
---
# <span data-ttu-id="f006d-104">интерфейс ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f006d-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f006d-105">Вызывающий объект реализует этот интерфейс, чтобы получать результаты выполнения CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="f006d-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="f006d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f006d-106">Summary</span></span>

 <span data-ttu-id="f006d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f006d-107">Members</span></span>                        | <span data-ttu-id="f006d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f006d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f006d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f006d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f006d-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="f006d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f006d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="f006d-111">Members</span></span>

#### <span data-ttu-id="f006d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f006d-112">Invoke</span></span> 

<span data-ttu-id="f006d-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="f006d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f006d-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="f006d-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


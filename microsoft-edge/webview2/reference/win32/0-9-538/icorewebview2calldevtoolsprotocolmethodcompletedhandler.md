---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: c991e9e9520bd696c579fdca379295afe253ba5d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877518"
---
# <span data-ttu-id="0f6eb-104">интерфейс ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="0f6eb-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="0f6eb-105">Вызывающий объект реализует этот интерфейс, чтобы получать результаты выполнения CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="0f6eb-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0f6eb-106">Summary</span></span>

 <span data-ttu-id="0f6eb-107">Участников</span><span class="sxs-lookup"><span data-stu-id="0f6eb-107">Members</span></span>                        | <span data-ttu-id="0f6eb-108">Описания</span><span class="sxs-lookup"><span data-stu-id="0f6eb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0f6eb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0f6eb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0f6eb-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="0f6eb-111">Участников</span><span class="sxs-lookup"><span data-stu-id="0f6eb-111">Members</span></span>

#### <span data-ttu-id="0f6eb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="0f6eb-112">Invoke</span></span> 

<span data-ttu-id="0f6eb-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="0f6eb-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="0f6eb-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


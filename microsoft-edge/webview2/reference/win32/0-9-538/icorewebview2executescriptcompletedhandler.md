---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: ee59ef42852fc8f0b0529b9a3ca08e53972dee1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879942"
---
# <span data-ttu-id="37402-104">интерфейс ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="37402-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="37402-105">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="37402-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="37402-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="37402-106">Summary</span></span>

 <span data-ttu-id="37402-107">Участников</span><span class="sxs-lookup"><span data-stu-id="37402-107">Members</span></span>                        | <span data-ttu-id="37402-108">Описания</span><span class="sxs-lookup"><span data-stu-id="37402-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="37402-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="37402-109">Invoke</span></span>](#invoke) | <span data-ttu-id="37402-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="37402-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="37402-111">Участников</span><span class="sxs-lookup"><span data-stu-id="37402-111">Members</span></span>

#### <span data-ttu-id="37402-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="37402-112">Invoke</span></span> 

<span data-ttu-id="37402-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="37402-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="37402-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="37402-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


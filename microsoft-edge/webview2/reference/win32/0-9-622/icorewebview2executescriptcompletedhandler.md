---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: 4a3b5999d38f74fb6b78063e32b3abb0cb59c6b6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012459"
---
# <span data-ttu-id="6c13b-104">интерфейс ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6c13b-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6c13b-105">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="6c13b-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="6c13b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6c13b-106">Summary</span></span>

 <span data-ttu-id="6c13b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="6c13b-107">Members</span></span>                        | <span data-ttu-id="6c13b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="6c13b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c13b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6c13b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6c13b-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="6c13b-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6c13b-111">Участников</span><span class="sxs-lookup"><span data-stu-id="6c13b-111">Members</span></span>

#### <span data-ttu-id="6c13b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6c13b-112">Invoke</span></span> 

<span data-ttu-id="6c13b-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="6c13b-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6c13b-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="6c13b-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


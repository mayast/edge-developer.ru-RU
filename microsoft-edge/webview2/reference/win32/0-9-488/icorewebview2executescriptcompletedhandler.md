---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 82b60e43d059cca25c9c3f44cf6136e32a4469ae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880663"
---
# <span data-ttu-id="df249-104">0.9.515-Interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="df249-104">0.9.515 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="df249-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="df249-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="df249-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="df249-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="df249-107">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="df249-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="df249-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="df249-108">Summary</span></span>

 <span data-ttu-id="df249-109">Участников</span><span class="sxs-lookup"><span data-stu-id="df249-109">Members</span></span>                        | <span data-ttu-id="df249-110">Описания</span><span class="sxs-lookup"><span data-stu-id="df249-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="df249-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="df249-111">Invoke</span></span>](#invoke) | <span data-ttu-id="df249-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="df249-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="df249-113">Участников</span><span class="sxs-lookup"><span data-stu-id="df249-113">Members</span></span>

#### <span data-ttu-id="df249-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="df249-114">Invoke</span></span> 

<span data-ttu-id="df249-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="df249-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="df249-116">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="df249-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


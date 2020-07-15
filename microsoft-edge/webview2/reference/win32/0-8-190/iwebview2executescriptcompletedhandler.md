---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: ecd3215c343925614b81d5da96fbf996350fd5a5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878507"
---
# <span data-ttu-id="559c9-104">0.8.355-Interface IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="559c9-104">0.8.355 - interface IWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="559c9-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="559c9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="559c9-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="559c9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="559c9-107">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="559c9-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="559c9-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="559c9-108">Summary</span></span>

 <span data-ttu-id="559c9-109">Участников</span><span class="sxs-lookup"><span data-stu-id="559c9-109">Members</span></span>                        | <span data-ttu-id="559c9-110">Описания</span><span class="sxs-lookup"><span data-stu-id="559c9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="559c9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="559c9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="559c9-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="559c9-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="559c9-113">Участников</span><span class="sxs-lookup"><span data-stu-id="559c9-113">Members</span></span>

#### <span data-ttu-id="559c9-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="559c9-114">Invoke</span></span> 

<span data-ttu-id="559c9-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="559c9-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="559c9-116">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="559c9-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


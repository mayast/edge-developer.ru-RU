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
ms.openlocfilehash: e3618b7dc7b866031709ee276c80ba45ec89512d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698038"
---
# <span data-ttu-id="7e116-104">интерфейс ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7e116-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7e116-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7e116-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7e116-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="7e116-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7e116-107">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="7e116-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="7e116-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7e116-108">Summary</span></span>

 <span data-ttu-id="7e116-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7e116-109">Members</span></span>                        | <span data-ttu-id="7e116-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7e116-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7e116-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e116-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7e116-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7e116-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7e116-113">Участников</span><span class="sxs-lookup"><span data-stu-id="7e116-113">Members</span></span>

#### <span data-ttu-id="7e116-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e116-114">Invoke</span></span> 

<span data-ttu-id="7e116-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7e116-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7e116-116">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="7e116-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


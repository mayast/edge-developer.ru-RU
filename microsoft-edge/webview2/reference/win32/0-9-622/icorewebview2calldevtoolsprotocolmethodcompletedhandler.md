---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: f6c0037177843d65ce5fe7cc56f206d5661d4b2a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012581"
---
# <span data-ttu-id="0ed4f-104">интерфейс ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="0ed4f-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="0ed4f-105">Вызывающий объект реализует этот интерфейс, чтобы получать результаты выполнения CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="0ed4f-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="0ed4f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0ed4f-106">Summary</span></span>

 <span data-ttu-id="0ed4f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="0ed4f-107">Members</span></span>                        | <span data-ttu-id="0ed4f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="0ed4f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0ed4f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0ed4f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0ed4f-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="0ed4f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="0ed4f-111">Участников</span><span class="sxs-lookup"><span data-stu-id="0ed4f-111">Members</span></span>

#### <span data-ttu-id="0ed4f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="0ed4f-112">Invoke</span></span> 

<span data-ttu-id="0ed4f-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="0ed4f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="0ed4f-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="0ed4f-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


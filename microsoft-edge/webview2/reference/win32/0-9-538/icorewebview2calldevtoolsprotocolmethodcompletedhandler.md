---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: aed9cb6a748730e7bb7872b02e06233e97600e17
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010623"
---
# <span data-ttu-id="03c37-104">0.9.579-Interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="03c37-104">0.9.579 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="03c37-105">Вызывающий объект реализует этот интерфейс, чтобы получать результаты выполнения CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="03c37-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="03c37-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="03c37-106">Summary</span></span>

 <span data-ttu-id="03c37-107">Участников</span><span class="sxs-lookup"><span data-stu-id="03c37-107">Members</span></span>                        | <span data-ttu-id="03c37-108">Описания</span><span class="sxs-lookup"><span data-stu-id="03c37-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="03c37-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="03c37-109">Invoke</span></span>](#invoke) | <span data-ttu-id="03c37-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="03c37-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="03c37-111">Участников</span><span class="sxs-lookup"><span data-stu-id="03c37-111">Members</span></span>

#### <span data-ttu-id="03c37-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="03c37-112">Invoke</span></span> 

<span data-ttu-id="03c37-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="03c37-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="03c37-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="03c37-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


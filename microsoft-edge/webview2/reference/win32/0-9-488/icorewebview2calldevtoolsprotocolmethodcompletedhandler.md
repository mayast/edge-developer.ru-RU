---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 7a983d313e242cc163fb16a9c0d0068a9d6663d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883933"
---
# <span data-ttu-id="835df-104">0.9.515-Interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="835df-104">0.9.515 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="835df-105">Вызывающий объект реализует этот интерфейс, чтобы получать результаты выполнения CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="835df-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="835df-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="835df-106">Summary</span></span>

 <span data-ttu-id="835df-107">Участников</span><span class="sxs-lookup"><span data-stu-id="835df-107">Members</span></span>                        | <span data-ttu-id="835df-108">Описания</span><span class="sxs-lookup"><span data-stu-id="835df-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="835df-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="835df-109">Invoke</span></span>](#invoke) | <span data-ttu-id="835df-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="835df-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="835df-111">Участников</span><span class="sxs-lookup"><span data-stu-id="835df-111">Members</span></span>

#### <span data-ttu-id="835df-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="835df-112">Invoke</span></span> 

<span data-ttu-id="835df-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="835df-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="835df-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="835df-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


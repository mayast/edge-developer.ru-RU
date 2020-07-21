---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9a96e18b8c0b56cd75d4f0fe7b0c90c0634fe68b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884199"
---
# <span data-ttu-id="535c7-104">0.9.430-Interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="535c7-104">0.9.430 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="535c7-105">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="535c7-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="535c7-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="535c7-106">Summary</span></span>

 <span data-ttu-id="535c7-107">Участников</span><span class="sxs-lookup"><span data-stu-id="535c7-107">Members</span></span>                        | <span data-ttu-id="535c7-108">Описания</span><span class="sxs-lookup"><span data-stu-id="535c7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="535c7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="535c7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="535c7-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="535c7-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="535c7-111">Участников</span><span class="sxs-lookup"><span data-stu-id="535c7-111">Members</span></span>

#### <span data-ttu-id="535c7-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="535c7-112">Invoke</span></span> 

<span data-ttu-id="535c7-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="535c7-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="535c7-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="535c7-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


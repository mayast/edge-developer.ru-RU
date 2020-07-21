---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 9a075cf5e5d3e5222e76b9ba7550636a67e5696a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886012"
---
# <span data-ttu-id="cf5db-104">0.8.355-Interface IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="cf5db-104">0.8.355 - interface IWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="cf5db-105">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="cf5db-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="cf5db-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="cf5db-106">Summary</span></span>

 <span data-ttu-id="cf5db-107">Участников</span><span class="sxs-lookup"><span data-stu-id="cf5db-107">Members</span></span>                        | <span data-ttu-id="cf5db-108">Описания</span><span class="sxs-lookup"><span data-stu-id="cf5db-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf5db-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="cf5db-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cf5db-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="cf5db-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="cf5db-111">Участников</span><span class="sxs-lookup"><span data-stu-id="cf5db-111">Members</span></span>

#### <span data-ttu-id="cf5db-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="cf5db-112">Invoke</span></span> 

<span data-ttu-id="cf5db-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="cf5db-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="cf5db-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="cf5db-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


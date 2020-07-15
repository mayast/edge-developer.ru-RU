---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
ms.openlocfilehash: 81b2895f652646991102af37e4da7cd99e789e10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877519"
---
# <span data-ttu-id="c4ffe-104">интерфейс ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="c4ffe-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="c4ffe-105">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="c4ffe-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="c4ffe-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c4ffe-106">Summary</span></span>

 <span data-ttu-id="c4ffe-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c4ffe-107">Members</span></span>                        | <span data-ttu-id="c4ffe-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c4ffe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4ffe-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4ffe-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c4ffe-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="c4ffe-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="c4ffe-111">Участников</span><span class="sxs-lookup"><span data-stu-id="c4ffe-111">Members</span></span>

#### <span data-ttu-id="c4ffe-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4ffe-112">Invoke</span></span> 

<span data-ttu-id="c4ffe-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="c4ffe-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="c4ffe-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode код_ошибки, ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="c4ffe-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>


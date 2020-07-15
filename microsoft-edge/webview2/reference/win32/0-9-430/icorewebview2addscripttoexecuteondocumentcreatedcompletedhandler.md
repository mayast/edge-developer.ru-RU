---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 03b9b229517023421b25f1f14917813a1e8af193
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881174"
---
# <span data-ttu-id="a3b08-104">0.9.430-Interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a3b08-104">0.9.430 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a3b08-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="a3b08-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a3b08-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="a3b08-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a3b08-107">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="a3b08-107">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="a3b08-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a3b08-108">Summary</span></span>

 <span data-ttu-id="a3b08-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a3b08-109">Members</span></span>                        | <span data-ttu-id="a3b08-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a3b08-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a3b08-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a3b08-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a3b08-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a3b08-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a3b08-113">Участников</span><span class="sxs-lookup"><span data-stu-id="a3b08-113">Members</span></span>

#### <span data-ttu-id="a3b08-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="a3b08-114">Invoke</span></span> 

<span data-ttu-id="a3b08-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a3b08-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a3b08-116">общедоступный [вызов](#invoke)HRESULT (ErrorCode код_ошибки, ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="a3b08-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>


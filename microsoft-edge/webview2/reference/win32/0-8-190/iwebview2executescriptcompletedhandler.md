---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 6330542e2a894858bc5e43958faaf19dfee6cc7c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654904"
---
# <span data-ttu-id="89e25-104">интерфейс IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="89e25-104">interface IWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="89e25-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="89e25-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="89e25-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="89e25-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="89e25-107">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="89e25-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="89e25-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="89e25-108">Summary</span></span>

 <span data-ttu-id="89e25-109">Участников</span><span class="sxs-lookup"><span data-stu-id="89e25-109">Members</span></span>                        | <span data-ttu-id="89e25-110">Описания</span><span class="sxs-lookup"><span data-stu-id="89e25-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="89e25-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="89e25-111">Invoke</span></span>](#invoke) | <span data-ttu-id="89e25-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="89e25-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="89e25-113">Участников</span><span class="sxs-lookup"><span data-stu-id="89e25-113">Members</span></span>

#### <span data-ttu-id="89e25-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="89e25-114">Invoke</span></span> 

<span data-ttu-id="89e25-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="89e25-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="89e25-116">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="89e25-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


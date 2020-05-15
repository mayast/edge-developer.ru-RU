---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 53bad68ff50b480b32dab823cefbb611f4de3891
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655028"
---
# <span data-ttu-id="5324d-104">интерфейс ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5324d-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="5324d-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="5324d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="5324d-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="5324d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5324d-107">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="5324d-107">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="5324d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5324d-108">Summary</span></span>

 <span data-ttu-id="5324d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="5324d-109">Members</span></span>                        | <span data-ttu-id="5324d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="5324d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5324d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="5324d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="5324d-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="5324d-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="5324d-113">Участников</span><span class="sxs-lookup"><span data-stu-id="5324d-113">Members</span></span>

#### <span data-ttu-id="5324d-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="5324d-114">Invoke</span></span> 

<span data-ttu-id="5324d-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="5324d-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5324d-116">общедоступный [вызов](#invoke)HRESULT (ErrorCode код_ошибки, ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="5324d-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>


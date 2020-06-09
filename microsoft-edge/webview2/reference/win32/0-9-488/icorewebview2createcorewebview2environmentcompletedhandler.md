---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e838c851df54a7af5e4afe6352abef6d1044c8be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698087"
---
# <span data-ttu-id="a6f47-104">интерфейс ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a6f47-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a6f47-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a6f47-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a6f47-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="a6f47-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a6f47-107">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="a6f47-107">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="a6f47-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a6f47-108">Summary</span></span>

 <span data-ttu-id="a6f47-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a6f47-109">Members</span></span>                        | <span data-ttu-id="a6f47-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a6f47-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a6f47-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a6f47-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a6f47-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a6f47-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a6f47-113">Участников</span><span class="sxs-lookup"><span data-stu-id="a6f47-113">Members</span></span>

#### <span data-ttu-id="a6f47-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="a6f47-114">Invoke</span></span> 

<span data-ttu-id="a6f47-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a6f47-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a6f47-116">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="a6f47-116">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


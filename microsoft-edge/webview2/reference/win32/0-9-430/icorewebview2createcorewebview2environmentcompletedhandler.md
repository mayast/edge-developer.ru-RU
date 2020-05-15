---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 4cac9892e150f64b02b0a08c1164dcaa0aac4b7c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654788"
---
# <span data-ttu-id="7ff94-104">интерфейс ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7ff94-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7ff94-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7ff94-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7ff94-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="7ff94-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7ff94-107">Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="7ff94-107">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="7ff94-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7ff94-108">Summary</span></span>

 <span data-ttu-id="7ff94-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7ff94-109">Members</span></span>                        | <span data-ttu-id="7ff94-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7ff94-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7ff94-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="7ff94-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7ff94-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7ff94-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7ff94-113">Участников</span><span class="sxs-lookup"><span data-stu-id="7ff94-113">Members</span></span>

#### <span data-ttu-id="7ff94-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="7ff94-114">Invoke</span></span> 

<span data-ttu-id="7ff94-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7ff94-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7ff94-116">общедоступный [вызов](#invoke)HRESULT (результат HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="7ff94-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span></span>


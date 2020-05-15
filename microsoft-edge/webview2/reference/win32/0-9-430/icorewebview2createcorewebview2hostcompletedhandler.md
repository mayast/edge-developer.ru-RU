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
ms.openlocfilehash: 1d2956aee178c2bdc581d51a93006e14cfb539e3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654781"
---
# <span data-ttu-id="8583e-104">интерфейс ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8583e-104">interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8583e-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="8583e-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8583e-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="8583e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="8583e-107">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Host, созданного с помощью CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="8583e-107">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="8583e-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8583e-108">Summary</span></span>

 <span data-ttu-id="8583e-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8583e-109">Members</span></span>                        | <span data-ttu-id="8583e-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8583e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8583e-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="8583e-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8583e-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="8583e-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="8583e-113">Участников</span><span class="sxs-lookup"><span data-stu-id="8583e-113">Members</span></span>

#### <span data-ttu-id="8583e-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="8583e-114">Invoke</span></span> 

<span data-ttu-id="8583e-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="8583e-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="8583e-116">общедоступный [вызов](#invoke)HRESULT (результат HRESULT,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="8583e-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9c2b5568e6a276b07dc91bd639c730b2009aa9e5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884283"
---
# <span data-ttu-id="63abd-104">0.9.430-Interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="63abd-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="63abd-105">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Host, созданного с помощью CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="63abd-105">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="63abd-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="63abd-106">Summary</span></span>

 <span data-ttu-id="63abd-107">Участников</span><span class="sxs-lookup"><span data-stu-id="63abd-107">Members</span></span>                        | <span data-ttu-id="63abd-108">Описания</span><span class="sxs-lookup"><span data-stu-id="63abd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="63abd-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="63abd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="63abd-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="63abd-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="63abd-111">Участников</span><span class="sxs-lookup"><span data-stu-id="63abd-111">Members</span></span>

#### <span data-ttu-id="63abd-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="63abd-112">Invoke</span></span> 

<span data-ttu-id="63abd-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="63abd-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="63abd-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="63abd-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>


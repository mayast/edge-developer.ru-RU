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
ms.openlocfilehash: d7f44614e7322759446812481c9fa05c807b5eac
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654794"
---
# <span data-ttu-id="84998-104">интерфейс ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="84998-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="84998-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="84998-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="84998-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="84998-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="84998-107">Вызывающий объект реализует этот интерфейс, чтобы получать результаты выполнения CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="84998-107">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="84998-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="84998-108">Summary</span></span>

 <span data-ttu-id="84998-109">Участников</span><span class="sxs-lookup"><span data-stu-id="84998-109">Members</span></span>                        | <span data-ttu-id="84998-110">Описания</span><span class="sxs-lookup"><span data-stu-id="84998-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="84998-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="84998-111">Invoke</span></span>](#invoke) | <span data-ttu-id="84998-112">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="84998-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="84998-113">Участников</span><span class="sxs-lookup"><span data-stu-id="84998-113">Members</span></span>

#### <span data-ttu-id="84998-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="84998-114">Invoke</span></span> 

<span data-ttu-id="84998-115">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="84998-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="84998-116">общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="84998-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>


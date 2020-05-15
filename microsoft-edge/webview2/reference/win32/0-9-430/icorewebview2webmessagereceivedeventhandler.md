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
ms.openlocfilehash: b59eae6966efb6c2ebfc018be5ec0a5d2d5334c7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654651"
---
# <span data-ttu-id="d84a2-104">интерфейс ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d84a2-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d84a2-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d84a2-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d84a2-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="d84a2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="d84a2-107">Вызывающий объект реализует этот интерфейс для получения события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="d84a2-107">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="d84a2-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d84a2-108">Summary</span></span>

 <span data-ttu-id="d84a2-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d84a2-109">Members</span></span>                        | <span data-ttu-id="d84a2-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d84a2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d84a2-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d84a2-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d84a2-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d84a2-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d84a2-113">Участников</span><span class="sxs-lookup"><span data-stu-id="d84a2-113">Members</span></span>

#### <span data-ttu-id="d84a2-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="d84a2-114">Invoke</span></span> 

<span data-ttu-id="d84a2-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d84a2-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d84a2-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d84a2-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>


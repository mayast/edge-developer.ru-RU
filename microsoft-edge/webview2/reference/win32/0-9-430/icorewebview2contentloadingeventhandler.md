---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 7f227e3b2c45b1088b1ac678477cf1dac5ffed5f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881132"
---
# <span data-ttu-id="7470d-104">0.9.430-Interface ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="7470d-104">0.9.430 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7470d-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7470d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7470d-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="7470d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="7470d-107">Вызывающий объект реализует этот интерфейс для получения события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="7470d-107">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="7470d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7470d-108">Summary</span></span>

 <span data-ttu-id="7470d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7470d-109">Members</span></span>                        | <span data-ttu-id="7470d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7470d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7470d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="7470d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7470d-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7470d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="7470d-113">Участников</span><span class="sxs-lookup"><span data-stu-id="7470d-113">Members</span></span>

#### <span data-ttu-id="7470d-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="7470d-114">Invoke</span></span> 

<span data-ttu-id="7470d-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7470d-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7470d-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2ContentLoadingEventArgs](ICoreWebView2ContentLoadingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7470d-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2ContentLoadingEventArgs](ICoreWebView2ContentLoadingEventArgs.md) \* args)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 161e36312c5acb8612c9399178917158807012a7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877870"
---
# <span data-ttu-id="aa7b4-104">0.9.430-Interface ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="aa7b4-104">0.9.430 - interface ICoreWebView2NavigationStartingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="aa7b4-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="aa7b4-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="aa7b4-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="aa7b4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="aa7b4-107">Вызывающий объект реализует этот интерфейс для получения события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aa7b4-107">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="aa7b4-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="aa7b4-108">Summary</span></span>

 <span data-ttu-id="aa7b4-109">Участников</span><span class="sxs-lookup"><span data-stu-id="aa7b4-109">Members</span></span>                        | <span data-ttu-id="aa7b4-110">Описания</span><span class="sxs-lookup"><span data-stu-id="aa7b4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aa7b4-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="aa7b4-111">Invoke</span></span>](#invoke) | <span data-ttu-id="aa7b4-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="aa7b4-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="aa7b4-113">Участников</span><span class="sxs-lookup"><span data-stu-id="aa7b4-113">Members</span></span>

#### <span data-ttu-id="aa7b4-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="aa7b4-114">Invoke</span></span> 

<span data-ttu-id="aa7b4-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="aa7b4-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="aa7b4-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="aa7b4-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span></span>


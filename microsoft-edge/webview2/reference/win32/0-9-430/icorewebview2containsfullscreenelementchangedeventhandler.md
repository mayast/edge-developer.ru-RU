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
ms.openlocfilehash: 7c5aece49cf2a3e8e6a65eba3fbb4d46f0ff2997
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654792"
---
# <span data-ttu-id="fd49d-104">интерфейс ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fd49d-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="fd49d-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="fd49d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="fd49d-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="fd49d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="fd49d-107">Вызывающий объект реализует этот метод для получения событий ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="fd49d-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="fd49d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fd49d-108">Summary</span></span>

 <span data-ttu-id="fd49d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="fd49d-109">Members</span></span>                        | <span data-ttu-id="fd49d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="fd49d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fd49d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="fd49d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="fd49d-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fd49d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="fd49d-113">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fd49d-113">There are no event args for this event.</span></span>

## <span data-ttu-id="fd49d-114">Участников</span><span class="sxs-lookup"><span data-stu-id="fd49d-114">Members</span></span>

#### <span data-ttu-id="fd49d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="fd49d-115">Invoke</span></span> 

<span data-ttu-id="fd49d-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fd49d-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fd49d-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="fd49d-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="fd49d-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="fd49d-118">There are no event args and the args parameter will be null.</span></span>


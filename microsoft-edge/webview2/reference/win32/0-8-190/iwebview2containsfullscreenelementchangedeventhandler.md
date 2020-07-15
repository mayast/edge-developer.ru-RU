---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 70e9ad7782fe495ffd366664ecb132edd0c57df5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878654"
---
# <span data-ttu-id="3de57-104">0.8.355-Interface IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3de57-104">0.8.355 - interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3de57-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3de57-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3de57-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="3de57-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3de57-107">Вызывающий объект реализует этот метод для получения событий ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="3de57-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="3de57-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3de57-108">Summary</span></span>

 <span data-ttu-id="3de57-109">Участников</span><span class="sxs-lookup"><span data-stu-id="3de57-109">Members</span></span>                        | <span data-ttu-id="3de57-110">Описания</span><span class="sxs-lookup"><span data-stu-id="3de57-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3de57-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="3de57-111">Invoke</span></span>](#invoke) | <span data-ttu-id="3de57-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="3de57-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3de57-113">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="3de57-113">There are no event args for this event.</span></span>

## <span data-ttu-id="3de57-114">Участников</span><span class="sxs-lookup"><span data-stu-id="3de57-114">Members</span></span>

#### <span data-ttu-id="3de57-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="3de57-115">Invoke</span></span> 

<span data-ttu-id="3de57-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="3de57-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3de57-117">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3de57-117">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="3de57-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="3de57-118">There are no event args and the args parameter will be null.</span></span>


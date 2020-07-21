---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: b1d0bf7ea5f472d5a1c3682c2cbef564947ee54b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886187"
---
# <span data-ttu-id="53882-104">0.8.355-Interface IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="53882-104">0.8.355 - interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="53882-105">Вызывающий объект реализует этот метод для получения событий ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="53882-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="53882-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="53882-106">Summary</span></span>

 <span data-ttu-id="53882-107">Участников</span><span class="sxs-lookup"><span data-stu-id="53882-107">Members</span></span>                        | <span data-ttu-id="53882-108">Описания</span><span class="sxs-lookup"><span data-stu-id="53882-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="53882-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="53882-109">Invoke</span></span>](#invoke) | <span data-ttu-id="53882-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="53882-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="53882-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="53882-111">There are no event args for this event.</span></span>

## <span data-ttu-id="53882-112">Участников</span><span class="sxs-lookup"><span data-stu-id="53882-112">Members</span></span>

#### <span data-ttu-id="53882-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="53882-113">Invoke</span></span> 

<span data-ttu-id="53882-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="53882-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="53882-115">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="53882-115">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="53882-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="53882-116">There are no event args and the args parameter will be null.</span></span>


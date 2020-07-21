---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 8b7a588122b93cf56f7ce4473db87a0df16522b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885998"
---
# <span data-ttu-id="95cf9-104">0.8.355-Interface IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="95cf9-104">0.8.355 - interface IWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="95cf9-105">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="95cf9-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="95cf9-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="95cf9-106">Summary</span></span>

 <span data-ttu-id="95cf9-107">Участников</span><span class="sxs-lookup"><span data-stu-id="95cf9-107">Members</span></span>                        | <span data-ttu-id="95cf9-108">Описания</span><span class="sxs-lookup"><span data-stu-id="95cf9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95cf9-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="95cf9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="95cf9-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="95cf9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="95cf9-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="95cf9-111">There are no event args for this event.</span></span>

## <span data-ttu-id="95cf9-112">Участников</span><span class="sxs-lookup"><span data-stu-id="95cf9-112">Members</span></span>

#### <span data-ttu-id="95cf9-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="95cf9-113">Invoke</span></span> 

<span data-ttu-id="95cf9-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="95cf9-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="95cf9-115">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="95cf9-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="95cf9-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="95cf9-116">There are no event args and the args parameter will be null.</span></span>


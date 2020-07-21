---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: cf799ae12b977f66bfba4d1b7664e3abc6241304
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885923"
---
# <span data-ttu-id="7ed6f-104">0.8.355-Interface IWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7ed6f-104">0.8.355 - interface IWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="7ed6f-105">Вызывающий объект реализует этот интерфейс для получения события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="7ed6f-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="7ed6f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7ed6f-106">Summary</span></span>

 <span data-ttu-id="7ed6f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7ed6f-107">Members</span></span>                        | <span data-ttu-id="7ed6f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7ed6f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7ed6f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7ed6f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7ed6f-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7ed6f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="7ed6f-111">Участников</span><span class="sxs-lookup"><span data-stu-id="7ed6f-111">Members</span></span>

#### <span data-ttu-id="7ed6f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7ed6f-112">Invoke</span></span> 

<span data-ttu-id="7ed6f-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7ed6f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7ed6f-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7ed6f-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span></span>


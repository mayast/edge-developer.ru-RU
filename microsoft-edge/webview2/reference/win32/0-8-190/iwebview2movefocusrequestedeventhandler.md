---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: fe84f29798b01aed2787559c717f2893c9eda7f9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885942"
---
# <span data-ttu-id="37429-104">0.8.355-Interface IWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="37429-104">0.8.355 - interface IWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="37429-105">Вызывающий объект реализует этот метод для получения события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="37429-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="37429-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="37429-106">Summary</span></span>

 <span data-ttu-id="37429-107">Участников</span><span class="sxs-lookup"><span data-stu-id="37429-107">Members</span></span>                        | <span data-ttu-id="37429-108">Описания</span><span class="sxs-lookup"><span data-stu-id="37429-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="37429-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="37429-109">Invoke</span></span>](#invoke) | <span data-ttu-id="37429-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="37429-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="37429-111">Участников</span><span class="sxs-lookup"><span data-stu-id="37429-111">Members</span></span>

#### <span data-ttu-id="37429-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="37429-112">Invoke</span></span> 

<span data-ttu-id="37429-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="37429-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="37429-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="37429-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: e6f47382eb3f086618a5d0c46c2eec57a9891ff5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885879"
---
# <span data-ttu-id="2851c-104">0.8.355-Interface IWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="2851c-104">0.8.355 - interface IWebView2NavigationStartingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="2851c-105">Вызывающий объект реализует этот интерфейс для получения события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2851c-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="2851c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2851c-106">Summary</span></span>

 <span data-ttu-id="2851c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2851c-107">Members</span></span>                        | <span data-ttu-id="2851c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2851c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2851c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2851c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2851c-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="2851c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2851c-111">Участников</span><span class="sxs-lookup"><span data-stu-id="2851c-111">Members</span></span>

#### <span data-ttu-id="2851c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2851c-112">Invoke</span></span> 

<span data-ttu-id="2851c-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="2851c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2851c-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2851c-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span></span>


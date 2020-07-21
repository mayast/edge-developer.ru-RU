---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 772ad4ce7bd1ae0c1f02475206380c146ecabf7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885746"
---
# <span data-ttu-id="a449c-104">0.8.355-Interface IWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a449c-104">0.8.355 - interface IWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="a449c-105">Вызывающий объект реализует этот интерфейс для получения события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="a449c-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="a449c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a449c-106">Summary</span></span>

 <span data-ttu-id="a449c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a449c-107">Members</span></span>                        | <span data-ttu-id="a449c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a449c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a449c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a449c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a449c-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a449c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a449c-111">Участников</span><span class="sxs-lookup"><span data-stu-id="a449c-111">Members</span></span>

#### <span data-ttu-id="a449c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a449c-112">Invoke</span></span> 

<span data-ttu-id="a449c-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a449c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a449c-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a449c-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>


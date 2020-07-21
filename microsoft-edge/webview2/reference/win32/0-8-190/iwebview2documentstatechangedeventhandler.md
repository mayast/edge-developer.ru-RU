---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 3d6bf8345e88dde213c15e51c26056d0239f0230
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886113"
---
# <span data-ttu-id="b089f-104">0.8.355-Interface IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b089f-104">0.8.355 - interface IWebView2DocumentStateChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b089f-105">Вызывающий объект реализует этот интерфейс для получения события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="b089f-105">The caller implements this interface to receive the DocumentStateChanged event.</span></span>

## <span data-ttu-id="b089f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b089f-106">Summary</span></span>

 <span data-ttu-id="b089f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b089f-107">Members</span></span>                        | <span data-ttu-id="b089f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b089f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b089f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b089f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b089f-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b089f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b089f-111">Участников</span><span class="sxs-lookup"><span data-stu-id="b089f-111">Members</span></span>

#### <span data-ttu-id="b089f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b089f-112">Invoke</span></span> 

<span data-ttu-id="b089f-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b089f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b089f-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b089f-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span></span>


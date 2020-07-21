---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 2fe743f0ffe39107252a184e2e98cc2904e3c640
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884976"
---
# <span data-ttu-id="4e670-104">0.8.355-Interface IWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4e670-104">0.8.355 - interface IWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="4e670-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="4e670-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="4e670-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4e670-106">Summary</span></span>

 <span data-ttu-id="4e670-107">Участников</span><span class="sxs-lookup"><span data-stu-id="4e670-107">Members</span></span>                        | <span data-ttu-id="4e670-108">Описания</span><span class="sxs-lookup"><span data-stu-id="4e670-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4e670-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4e670-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4e670-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4e670-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4e670-111">Участников</span><span class="sxs-lookup"><span data-stu-id="4e670-111">Members</span></span>

#### <span data-ttu-id="4e670-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4e670-112">Invoke</span></span> 

<span data-ttu-id="4e670-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4e670-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4e670-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4e670-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>


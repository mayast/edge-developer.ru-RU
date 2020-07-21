---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b3eb56101c6e69bab018cbb549339fd5deb2eb3e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885193"
---
# <span data-ttu-id="e79a0-104">0.9.515-Interface ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e79a0-104">0.9.515 - interface ICoreWebView2SourceChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e79a0-105">Вызывающий объект реализует этот интерфейс для получения события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="e79a0-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="e79a0-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e79a0-106">Summary</span></span>

 <span data-ttu-id="e79a0-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e79a0-107">Members</span></span>                        | <span data-ttu-id="e79a0-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e79a0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e79a0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e79a0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e79a0-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e79a0-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e79a0-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e79a0-111">Members</span></span>

#### <span data-ttu-id="e79a0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e79a0-112">Invoke</span></span> 

<span data-ttu-id="e79a0-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e79a0-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e79a0-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e79a0-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


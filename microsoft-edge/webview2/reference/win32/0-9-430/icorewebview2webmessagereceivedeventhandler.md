---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f566cb8aa876304d17e11bb47f24692aefda3b26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883758"
---
# <span data-ttu-id="9baed-104">0.9.430-Interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9baed-104">0.9.430 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="9baed-105">Вызывающий объект реализует этот интерфейс для получения события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="9baed-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="9baed-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9baed-106">Summary</span></span>

 <span data-ttu-id="9baed-107">Участников</span><span class="sxs-lookup"><span data-stu-id="9baed-107">Members</span></span>                        | <span data-ttu-id="9baed-108">Описания</span><span class="sxs-lookup"><span data-stu-id="9baed-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9baed-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9baed-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9baed-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="9baed-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9baed-111">Участников</span><span class="sxs-lookup"><span data-stu-id="9baed-111">Members</span></span>

#### <span data-ttu-id="9baed-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9baed-112">Invoke</span></span> 

<span data-ttu-id="9baed-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="9baed-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9baed-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9baed-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>


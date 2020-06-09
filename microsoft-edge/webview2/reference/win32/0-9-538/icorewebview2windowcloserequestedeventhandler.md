---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 0d02fb1c8605bc6817085748154055cdfa489da8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699248"
---
# <span data-ttu-id="331de-104">интерфейс ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="331de-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="331de-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="331de-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="331de-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="331de-106">Summary</span></span>

 <span data-ttu-id="331de-107">Участников</span><span class="sxs-lookup"><span data-stu-id="331de-107">Members</span></span>                        | <span data-ttu-id="331de-108">Описания</span><span class="sxs-lookup"><span data-stu-id="331de-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="331de-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="331de-109">Invoke</span></span>](#invoke) | <span data-ttu-id="331de-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="331de-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="331de-111">Участников</span><span class="sxs-lookup"><span data-stu-id="331de-111">Members</span></span>

#### <span data-ttu-id="331de-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="331de-112">Invoke</span></span> 

<span data-ttu-id="331de-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="331de-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="331de-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="331de-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="331de-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="331de-115">There are no event args and the args parameter will be null.</span></span>


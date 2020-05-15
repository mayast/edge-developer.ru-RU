---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 30fc5e258c73b880009bc48e9213c647a5542917
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654796"
---
# <span data-ttu-id="e3473-104">интерфейс ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e3473-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="e3473-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="e3473-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="e3473-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e3473-106">Summary</span></span>

 <span data-ttu-id="e3473-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e3473-107">Members</span></span>                        | <span data-ttu-id="e3473-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e3473-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e3473-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e3473-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e3473-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e3473-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e3473-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e3473-111">Members</span></span>

#### <span data-ttu-id="e3473-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e3473-112">Invoke</span></span> 

<span data-ttu-id="e3473-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="e3473-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e3473-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e3473-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


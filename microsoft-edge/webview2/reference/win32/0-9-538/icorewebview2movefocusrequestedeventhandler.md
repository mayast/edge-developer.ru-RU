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
ms.openlocfilehash: a90e7d3479f93d58d72db5c69cca53669a6d4501
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699168"
---
# <span data-ttu-id="0fdf7-104">интерфейс ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0fdf7-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="0fdf7-105">Вызывающий объект реализует этот метод для получения события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="0fdf7-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0fdf7-106">Summary</span></span>

 <span data-ttu-id="0fdf7-107">Участников</span><span class="sxs-lookup"><span data-stu-id="0fdf7-107">Members</span></span>                        | <span data-ttu-id="0fdf7-108">Описания</span><span class="sxs-lookup"><span data-stu-id="0fdf7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0fdf7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0fdf7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0fdf7-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0fdf7-111">Участников</span><span class="sxs-lookup"><span data-stu-id="0fdf7-111">Members</span></span>

#### <span data-ttu-id="0fdf7-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="0fdf7-112">Invoke</span></span> 

<span data-ttu-id="0fdf7-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0fdf7-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0fdf7-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


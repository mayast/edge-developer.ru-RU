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
ms.openlocfilehash: 6fc29b620df5bcd265a7576e4b7ca1c7ebd73e6f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699234"
---
# <span data-ttu-id="9a406-104">интерфейс ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9a406-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9a406-105">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="9a406-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="9a406-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9a406-106">Summary</span></span>

 <span data-ttu-id="9a406-107">Участников</span><span class="sxs-lookup"><span data-stu-id="9a406-107">Members</span></span>                        | <span data-ttu-id="9a406-108">Описания</span><span class="sxs-lookup"><span data-stu-id="9a406-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9a406-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9a406-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9a406-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="9a406-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="9a406-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9a406-111">There are no event args for this event.</span></span>

## <span data-ttu-id="9a406-112">Участников</span><span class="sxs-lookup"><span data-stu-id="9a406-112">Members</span></span>

#### <span data-ttu-id="9a406-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="9a406-113">Invoke</span></span> 

<span data-ttu-id="9a406-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="9a406-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9a406-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9a406-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="9a406-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="9a406-116">There are no event args and the args parameter will be null.</span></span>


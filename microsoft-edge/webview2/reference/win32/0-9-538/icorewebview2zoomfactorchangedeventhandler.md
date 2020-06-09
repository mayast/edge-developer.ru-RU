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
ms.openlocfilehash: f0b90cec451a80225f657386fa06b8740d6e1385
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699247"
---
# <span data-ttu-id="f0e8d-104">интерфейс ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f0e8d-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f0e8d-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="f0e8d-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="f0e8d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f0e8d-106">Summary</span></span>

 <span data-ttu-id="f0e8d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f0e8d-107">Members</span></span>                        | <span data-ttu-id="f0e8d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f0e8d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f0e8d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f0e8d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f0e8d-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f0e8d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f0e8d-111">Используйте свойство ICoreWebView2Controller. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f0e8d-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="f0e8d-112">Участников</span><span class="sxs-lookup"><span data-stu-id="f0e8d-112">Members</span></span>

#### <span data-ttu-id="f0e8d-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="f0e8d-113">Invoke</span></span> 

<span data-ttu-id="f0e8d-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f0e8d-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f0e8d-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f0e8d-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="f0e8d-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="f0e8d-116">There are no event args and the args parameter will be null.</span></span>


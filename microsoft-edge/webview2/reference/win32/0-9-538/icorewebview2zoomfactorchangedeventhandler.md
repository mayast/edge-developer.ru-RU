---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: 74cd0451e111780078714b17e5bd1097c56d6b2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877576"
---
# <span data-ttu-id="f2524-104">интерфейс ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f2524-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f2524-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="f2524-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="f2524-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f2524-106">Summary</span></span>

 <span data-ttu-id="f2524-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f2524-107">Members</span></span>                        | <span data-ttu-id="f2524-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f2524-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f2524-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f2524-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f2524-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f2524-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f2524-111">Используйте свойство ICoreWebView2Controller. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f2524-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="f2524-112">Участников</span><span class="sxs-lookup"><span data-stu-id="f2524-112">Members</span></span>

#### <span data-ttu-id="f2524-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="f2524-113">Invoke</span></span> 

<span data-ttu-id="f2524-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f2524-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f2524-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f2524-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="f2524-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="f2524-116">There are no event args and the args parameter will be null.</span></span>


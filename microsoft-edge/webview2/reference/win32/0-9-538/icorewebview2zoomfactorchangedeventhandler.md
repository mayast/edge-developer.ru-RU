---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: c941629ab8ee87c0c964b00798878bb69265669a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011393"
---
# <span data-ttu-id="a9d97-104">0.9.579-Interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a9d97-104">0.9.579 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="a9d97-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="a9d97-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="a9d97-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a9d97-106">Summary</span></span>

 <span data-ttu-id="a9d97-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a9d97-107">Members</span></span>                        | <span data-ttu-id="a9d97-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a9d97-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a9d97-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a9d97-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a9d97-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a9d97-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="a9d97-111">Используйте свойство ICoreWebView2Controller. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="a9d97-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="a9d97-112">Участников</span><span class="sxs-lookup"><span data-stu-id="a9d97-112">Members</span></span>

#### <span data-ttu-id="a9d97-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="a9d97-113">Invoke</span></span> 

<span data-ttu-id="a9d97-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a9d97-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a9d97-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="a9d97-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="a9d97-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="a9d97-116">There are no event args and the args parameter will be null.</span></span>


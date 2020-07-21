---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 91cd4245ff6c75e72457410211deefd9ab7f09d1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883695"
---
# <span data-ttu-id="b349e-104">0.9.515-Interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b349e-104">0.9.515 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b349e-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="b349e-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="b349e-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b349e-106">Summary</span></span>

 <span data-ttu-id="b349e-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b349e-107">Members</span></span>                        | <span data-ttu-id="b349e-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b349e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b349e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b349e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b349e-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b349e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b349e-111">Используйте свойство ICoreWebView2Controller. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b349e-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="b349e-112">Участников</span><span class="sxs-lookup"><span data-stu-id="b349e-112">Members</span></span>

#### <span data-ttu-id="b349e-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="b349e-113">Invoke</span></span> 

<span data-ttu-id="b349e-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b349e-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b349e-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b349e-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="b349e-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="b349e-116">There are no event args and the args parameter will be null.</span></span>


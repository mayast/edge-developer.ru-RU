---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 22c5e558238e4542ebe70855c3d20837838bebb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883963"
---
# <span data-ttu-id="3f2cc-104">0.9.430-Interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3f2cc-104">0.9.430 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3f2cc-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="3f2cc-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="3f2cc-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3f2cc-106">Summary</span></span>

 <span data-ttu-id="3f2cc-107">Участников</span><span class="sxs-lookup"><span data-stu-id="3f2cc-107">Members</span></span>                        | <span data-ttu-id="3f2cc-108">Описания</span><span class="sxs-lookup"><span data-stu-id="3f2cc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f2cc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3f2cc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3f2cc-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="3f2cc-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3f2cc-111">Используйте свойство ICoreWebView2Host. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="3f2cc-111">Use the ICoreWebView2Host.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="3f2cc-112">Участников</span><span class="sxs-lookup"><span data-stu-id="3f2cc-112">Members</span></span>

#### <span data-ttu-id="3f2cc-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="3f2cc-113">Invoke</span></span> 

<span data-ttu-id="3f2cc-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="3f2cc-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3f2cc-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3f2cc-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="3f2cc-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="3f2cc-116">There are no event args and the args parameter will be null.</span></span>


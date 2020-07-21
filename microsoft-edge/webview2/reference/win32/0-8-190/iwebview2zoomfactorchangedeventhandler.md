---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 237179df5ef704fb88516780696f3a9c10c9a198
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884668"
---
# <span data-ttu-id="389bc-104">0.8.355-Interface IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="389bc-104">0.8.355 - interface IWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="389bc-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="389bc-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="389bc-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="389bc-106">Summary</span></span>

 <span data-ttu-id="389bc-107">Участников</span><span class="sxs-lookup"><span data-stu-id="389bc-107">Members</span></span>                        | <span data-ttu-id="389bc-108">Описания</span><span class="sxs-lookup"><span data-stu-id="389bc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="389bc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="389bc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="389bc-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="389bc-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="389bc-111">Используйте свойство IWebView2WebView. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="389bc-111">Use the IWebView2WebView.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="389bc-112">Участников</span><span class="sxs-lookup"><span data-stu-id="389bc-112">Members</span></span>

#### <span data-ttu-id="389bc-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="389bc-113">Invoke</span></span> 

<span data-ttu-id="389bc-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="389bc-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="389bc-115">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="389bc-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="389bc-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="389bc-116">There are no event args and the args parameter will be null.</span></span>


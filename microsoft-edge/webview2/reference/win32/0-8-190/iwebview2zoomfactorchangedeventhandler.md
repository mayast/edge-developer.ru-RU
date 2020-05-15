---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 7bec193bad86a41cf2bdbbf895b201d28ebb8347
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654612"
---
# <span data-ttu-id="1e06f-104">интерфейс IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1e06f-104">interface IWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="1e06f-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="1e06f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="1e06f-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="1e06f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1e06f-107">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="1e06f-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="1e06f-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1e06f-108">Summary</span></span>

 <span data-ttu-id="1e06f-109">Участников</span><span class="sxs-lookup"><span data-stu-id="1e06f-109">Members</span></span>                        | <span data-ttu-id="1e06f-110">Описания</span><span class="sxs-lookup"><span data-stu-id="1e06f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1e06f-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="1e06f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="1e06f-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1e06f-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1e06f-113">Используйте свойство IWebView2WebView. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1e06f-113">Use the IWebView2WebView.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="1e06f-114">Участников</span><span class="sxs-lookup"><span data-stu-id="1e06f-114">Members</span></span>

#### <span data-ttu-id="1e06f-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="1e06f-115">Invoke</span></span> 

<span data-ttu-id="1e06f-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1e06f-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1e06f-117">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1e06f-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="1e06f-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="1e06f-118">There are no event args and the args parameter will be null.</span></span>


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
ms.openlocfilehash: a3452d30edc595a6d7b2a8b45fb283073d079749
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654640"
---
# <span data-ttu-id="a058b-104">интерфейс IWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a058b-104">interface IWebView2ProcessFailedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a058b-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a058b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a058b-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="a058b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="a058b-107">Вызывающий объект реализует этот интерфейс, чтобы получать события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="a058b-107">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="a058b-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a058b-108">Summary</span></span>

 <span data-ttu-id="a058b-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a058b-109">Members</span></span>                        | <span data-ttu-id="a058b-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a058b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a058b-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a058b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a058b-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a058b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a058b-113">Участников</span><span class="sxs-lookup"><span data-stu-id="a058b-113">Members</span></span>

#### <span data-ttu-id="a058b-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="a058b-114">Invoke</span></span> 

<span data-ttu-id="a058b-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a058b-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a058b-116">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a058b-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 372bd0f6faa3b5ed50c539a2e10809bfe9b95209
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878234"
---
# <span data-ttu-id="8c990-104">0.8.355-Interface IWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8c990-104">0.8.355 - interface IWebView2ProcessFailedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8c990-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="8c990-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="8c990-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="8c990-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="8c990-107">Вызывающий объект реализует этот интерфейс, чтобы получать события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="8c990-107">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="8c990-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8c990-108">Summary</span></span>

 <span data-ttu-id="8c990-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8c990-109">Members</span></span>                        | <span data-ttu-id="8c990-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8c990-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8c990-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="8c990-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8c990-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8c990-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8c990-113">Участников</span><span class="sxs-lookup"><span data-stu-id="8c990-113">Members</span></span>

#### <span data-ttu-id="8c990-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="8c990-114">Invoke</span></span> 

<span data-ttu-id="8c990-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8c990-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8c990-116">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8c990-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span></span>


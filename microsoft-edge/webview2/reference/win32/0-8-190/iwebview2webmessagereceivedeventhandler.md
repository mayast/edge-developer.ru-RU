---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 55ce9b2efc78bd4f0bf153c1e5655ff79d42af94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878157"
---
# <span data-ttu-id="ca268-104">0.8.355-Interface IWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ca268-104">0.8.355 - interface IWebView2WebMessageReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ca268-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="ca268-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="ca268-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="ca268-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="ca268-107">Вызывающий объект реализует этот интерфейс для получения события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="ca268-107">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="ca268-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ca268-108">Summary</span></span>

 <span data-ttu-id="ca268-109">Участников</span><span class="sxs-lookup"><span data-stu-id="ca268-109">Members</span></span>                        | <span data-ttu-id="ca268-110">Описания</span><span class="sxs-lookup"><span data-stu-id="ca268-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca268-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ca268-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ca268-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ca268-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ca268-113">Участников</span><span class="sxs-lookup"><span data-stu-id="ca268-113">Members</span></span>

#### <span data-ttu-id="ca268-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="ca268-114">Invoke</span></span> 

<span data-ttu-id="ca268-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ca268-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ca268-116">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ca268-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>


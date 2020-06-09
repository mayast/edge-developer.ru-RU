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
ms.openlocfilehash: 8bf8dcf40524425a7ef166c5007d60de738efb67
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699196"
---
# <span data-ttu-id="9ff58-104">интерфейс ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="9ff58-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="9ff58-105">Вызывающий объект реализует этот интерфейс для получения события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9ff58-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="9ff58-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9ff58-106">Summary</span></span>

 <span data-ttu-id="9ff58-107">Участников</span><span class="sxs-lookup"><span data-stu-id="9ff58-107">Members</span></span>                        | <span data-ttu-id="9ff58-108">Описания</span><span class="sxs-lookup"><span data-stu-id="9ff58-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ff58-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9ff58-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9ff58-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="9ff58-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9ff58-111">Участников</span><span class="sxs-lookup"><span data-stu-id="9ff58-111">Members</span></span>

#### <span data-ttu-id="9ff58-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9ff58-112">Invoke</span></span> 

<span data-ttu-id="9ff58-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="9ff58-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9ff58-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9ff58-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 889728489b6c4b06cd224915a0e12ee0a4144653
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654665"
---
# <span data-ttu-id="ea38a-104">интерфейс ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ea38a-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="ea38a-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="ea38a-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="ea38a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ea38a-106">Summary</span></span>

 <span data-ttu-id="ea38a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ea38a-107">Members</span></span>                        | <span data-ttu-id="ea38a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ea38a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea38a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ea38a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ea38a-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ea38a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ea38a-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ea38a-111">Members</span></span>

#### <span data-ttu-id="ea38a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ea38a-112">Invoke</span></span> 

<span data-ttu-id="ea38a-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ea38a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ea38a-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ea38a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ea38a-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="ea38a-115">There are no event args and the args parameter will be null.</span></span>


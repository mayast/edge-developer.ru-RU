---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 98f3e114e52dd9b8a044e34e7f24067c0b68148b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884584"
---
# <span data-ttu-id="f723c-104">0.9.430-Interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f723c-104">0.9.430 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f723c-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f723c-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="f723c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f723c-106">Summary</span></span>

 <span data-ttu-id="f723c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f723c-107">Members</span></span>                        | <span data-ttu-id="f723c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f723c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f723c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f723c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f723c-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f723c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f723c-111">Участников</span><span class="sxs-lookup"><span data-stu-id="f723c-111">Members</span></span>

#### <span data-ttu-id="f723c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f723c-112">Invoke</span></span> 

<span data-ttu-id="f723c-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f723c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f723c-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f723c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="f723c-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="f723c-115">There are no event args and the args parameter will be null.</span></span>


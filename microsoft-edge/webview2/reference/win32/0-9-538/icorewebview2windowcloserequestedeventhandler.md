---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: 34b0f941029251824cdc108e0aca41e6eab93695
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011381"
---
# <span data-ttu-id="4b031-104">0.9.579-Interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4b031-104">0.9.579 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="4b031-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="4b031-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="4b031-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4b031-106">Summary</span></span>

 <span data-ttu-id="4b031-107">Участников</span><span class="sxs-lookup"><span data-stu-id="4b031-107">Members</span></span>                        | <span data-ttu-id="4b031-108">Описания</span><span class="sxs-lookup"><span data-stu-id="4b031-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4b031-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4b031-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4b031-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4b031-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4b031-111">Участников</span><span class="sxs-lookup"><span data-stu-id="4b031-111">Members</span></span>

#### <span data-ttu-id="4b031-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4b031-112">Invoke</span></span> 

<span data-ttu-id="4b031-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4b031-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4b031-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4b031-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="4b031-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="4b031-115">There are no event args and the args parameter will be null.</span></span>


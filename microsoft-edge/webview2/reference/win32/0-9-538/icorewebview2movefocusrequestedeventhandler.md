---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: bd07256203944b4d640d859451fa000cbc1fcd46
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011324"
---
# <span data-ttu-id="f6c49-104">0.9.579-Interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f6c49-104">0.9.579 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f6c49-105">Вызывающий объект реализует этот метод для получения события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="f6c49-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="f6c49-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f6c49-106">Summary</span></span>

 <span data-ttu-id="f6c49-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f6c49-107">Members</span></span>                        | <span data-ttu-id="f6c49-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f6c49-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f6c49-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f6c49-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f6c49-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f6c49-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f6c49-111">Участников</span><span class="sxs-lookup"><span data-stu-id="f6c49-111">Members</span></span>

#### <span data-ttu-id="f6c49-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f6c49-112">Invoke</span></span> 

<span data-ttu-id="f6c49-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f6c49-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f6c49-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f6c49-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


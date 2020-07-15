---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: fc952437a9d5ffa7bb709bb6fb322438851babcd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879900"
---
# <span data-ttu-id="8b4ed-104">интерфейс ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8b4ed-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="8b4ed-105">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="8b4ed-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="8b4ed-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8b4ed-106">Summary</span></span>

 <span data-ttu-id="8b4ed-107">Участников</span><span class="sxs-lookup"><span data-stu-id="8b4ed-107">Members</span></span>                        | <span data-ttu-id="8b4ed-108">Описания</span><span class="sxs-lookup"><span data-stu-id="8b4ed-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8b4ed-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8b4ed-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8b4ed-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8b4ed-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="8b4ed-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="8b4ed-111">There are no event args for this event.</span></span>

## <span data-ttu-id="8b4ed-112">Участников</span><span class="sxs-lookup"><span data-stu-id="8b4ed-112">Members</span></span>

#### <span data-ttu-id="8b4ed-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="8b4ed-113">Invoke</span></span> 

<span data-ttu-id="8b4ed-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8b4ed-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8b4ed-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="8b4ed-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="8b4ed-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="8b4ed-116">There are no event args and the args parameter will be null.</span></span>


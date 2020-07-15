---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: f58279d1a3c404715be5aad8bf1be5ef120e1d94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880005"
---
# <span data-ttu-id="48e5c-104">интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="48e5c-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="48e5c-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="48e5c-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="48e5c-106">Вызывающий объект реализует этот интерфейс, чтобы получать события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="48e5c-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="48e5c-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="48e5c-107">Summary</span></span>

 <span data-ttu-id="48e5c-108">Участников</span><span class="sxs-lookup"><span data-stu-id="48e5c-108">Members</span></span>                        | <span data-ttu-id="48e5c-109">Описания</span><span class="sxs-lookup"><span data-stu-id="48e5c-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="48e5c-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="48e5c-110">Invoke</span></span>](#invoke) | <span data-ttu-id="48e5c-111">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="48e5c-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="48e5c-112">Используйте свойство Cursor для получения нового курсора.</span><span class="sxs-lookup"><span data-stu-id="48e5c-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="48e5c-113">Участников</span><span class="sxs-lookup"><span data-stu-id="48e5c-113">Members</span></span>

#### <span data-ttu-id="48e5c-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="48e5c-114">Invoke</span></span> 

<span data-ttu-id="48e5c-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="48e5c-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="48e5c-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="48e5c-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="48e5c-117">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="48e5c-117">There are no event args and the args parameter will be null.</span></span>


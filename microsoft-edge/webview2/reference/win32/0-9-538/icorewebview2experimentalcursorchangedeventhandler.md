---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: 67d0e6e05fb3640e141ec1ae7193746a1200bbd0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884885"
---
# <span data-ttu-id="c37ed-104">интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c37ed-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c37ed-105">Вызывающий объект реализует этот интерфейс, чтобы получать события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="c37ed-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="c37ed-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c37ed-106">Summary</span></span>

 <span data-ttu-id="c37ed-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c37ed-107">Members</span></span>                        | <span data-ttu-id="c37ed-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c37ed-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c37ed-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c37ed-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c37ed-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c37ed-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c37ed-111">Используйте свойство Cursor для получения нового курсора.</span><span class="sxs-lookup"><span data-stu-id="c37ed-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="c37ed-112">Участников</span><span class="sxs-lookup"><span data-stu-id="c37ed-112">Members</span></span>

#### <span data-ttu-id="c37ed-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="c37ed-113">Invoke</span></span> 

<span data-ttu-id="c37ed-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c37ed-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c37ed-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c37ed-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c37ed-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="c37ed-116">There are no event args and the args parameter will be null.</span></span>


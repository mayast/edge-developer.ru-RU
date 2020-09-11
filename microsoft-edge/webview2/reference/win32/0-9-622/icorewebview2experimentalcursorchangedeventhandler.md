---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: 246fc6d23a003a346a20055fbf083421a6fb1b26
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012471"
---
# <span data-ttu-id="99349-104">интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="99349-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="99349-105">Вызывающий объект реализует этот интерфейс, чтобы получать события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="99349-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="99349-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="99349-106">Summary</span></span>

 <span data-ttu-id="99349-107">Участников</span><span class="sxs-lookup"><span data-stu-id="99349-107">Members</span></span>                        | <span data-ttu-id="99349-108">Описания</span><span class="sxs-lookup"><span data-stu-id="99349-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99349-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="99349-109">Invoke</span></span>](#invoke) | <span data-ttu-id="99349-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="99349-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="99349-111">Используйте свойство Cursor для получения нового курсора.</span><span class="sxs-lookup"><span data-stu-id="99349-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="99349-112">Участников</span><span class="sxs-lookup"><span data-stu-id="99349-112">Members</span></span>

#### <span data-ttu-id="99349-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="99349-113">Invoke</span></span> 

<span data-ttu-id="99349-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="99349-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="99349-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="99349-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="99349-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="99349-116">There are no event args and the args parameter will be null.</span></span>


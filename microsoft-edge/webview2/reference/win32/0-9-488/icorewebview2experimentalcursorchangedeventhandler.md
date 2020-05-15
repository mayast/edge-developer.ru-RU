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
ms.openlocfilehash: 9c8cd627275a98382f079bc4f64dd7f565d46630
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655001"
---
# <span data-ttu-id="42d58-104">интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="42d58-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="42d58-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="42d58-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="42d58-106">Вызывающий объект реализует этот интерфейс, чтобы получать события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="42d58-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="42d58-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="42d58-107">Summary</span></span>

 <span data-ttu-id="42d58-108">Участников</span><span class="sxs-lookup"><span data-stu-id="42d58-108">Members</span></span>                        | <span data-ttu-id="42d58-109">Описания</span><span class="sxs-lookup"><span data-stu-id="42d58-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="42d58-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="42d58-110">Invoke</span></span>](#invoke) | <span data-ttu-id="42d58-111">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="42d58-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="42d58-112">Используйте свойство Cursor для получения нового курсора.</span><span class="sxs-lookup"><span data-stu-id="42d58-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="42d58-113">Участников</span><span class="sxs-lookup"><span data-stu-id="42d58-113">Members</span></span>

#### <span data-ttu-id="42d58-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="42d58-114">Invoke</span></span> 

<span data-ttu-id="42d58-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="42d58-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="42d58-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="42d58-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="42d58-117">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="42d58-117">There are no event args and the args parameter will be null.</span></span>


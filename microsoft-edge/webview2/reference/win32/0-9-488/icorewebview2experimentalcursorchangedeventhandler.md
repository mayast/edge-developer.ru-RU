---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6fbcc82409791bc3d2da3bb2f7985732cb344a97
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880628"
---
# <span data-ttu-id="74286-104">0.9.515-Interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="74286-104">0.9.515 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="74286-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="74286-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="74286-106">Вызывающий объект реализует этот интерфейс, чтобы получать события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="74286-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="74286-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="74286-107">Summary</span></span>

 <span data-ttu-id="74286-108">Участников</span><span class="sxs-lookup"><span data-stu-id="74286-108">Members</span></span>                        | <span data-ttu-id="74286-109">Описания</span><span class="sxs-lookup"><span data-stu-id="74286-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="74286-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="74286-110">Invoke</span></span>](#invoke) | <span data-ttu-id="74286-111">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="74286-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="74286-112">Используйте свойство Cursor для получения нового курсора.</span><span class="sxs-lookup"><span data-stu-id="74286-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="74286-113">Участников</span><span class="sxs-lookup"><span data-stu-id="74286-113">Members</span></span>

#### <span data-ttu-id="74286-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="74286-114">Invoke</span></span> 

<span data-ttu-id="74286-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="74286-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="74286-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="74286-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="74286-117">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="74286-117">There are no event args and the args parameter will be null.</span></span>


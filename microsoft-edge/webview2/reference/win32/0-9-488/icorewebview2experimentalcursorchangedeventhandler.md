---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ee6de606d6ed8a9e00dbdacee9bb07b341a6d04e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886488"
---
# <span data-ttu-id="d3d40-104">0.9.515-Interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d3d40-104">0.9.515 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="d3d40-105">Вызывающий объект реализует этот интерфейс, чтобы получать события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="d3d40-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="d3d40-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d3d40-106">Summary</span></span>

 <span data-ttu-id="d3d40-107">Участников</span><span class="sxs-lookup"><span data-stu-id="d3d40-107">Members</span></span>                        | <span data-ttu-id="d3d40-108">Описания</span><span class="sxs-lookup"><span data-stu-id="d3d40-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d3d40-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3d40-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d3d40-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d3d40-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d3d40-111">Используйте свойство Cursor для получения нового курсора.</span><span class="sxs-lookup"><span data-stu-id="d3d40-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="d3d40-112">Участников</span><span class="sxs-lookup"><span data-stu-id="d3d40-112">Members</span></span>

#### <span data-ttu-id="d3d40-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3d40-113">Invoke</span></span> 

<span data-ttu-id="d3d40-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d3d40-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d3d40-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d3d40-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="d3d40-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="d3d40-116">There are no event args and the args parameter will be null.</span></span>


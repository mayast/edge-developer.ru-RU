---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b44bd47f5352179abcc06ef5fd5b8f613bde455e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699173"
---
# <span data-ttu-id="f1fd3-104">интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f1fd3-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f1fd3-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="f1fd3-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f1fd3-106">Вызывающий объект реализует этот интерфейс, чтобы получать события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="f1fd3-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="f1fd3-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f1fd3-107">Summary</span></span>

 <span data-ttu-id="f1fd3-108">Участников</span><span class="sxs-lookup"><span data-stu-id="f1fd3-108">Members</span></span>                        | <span data-ttu-id="f1fd3-109">Описания</span><span class="sxs-lookup"><span data-stu-id="f1fd3-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f1fd3-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="f1fd3-110">Invoke</span></span>](#invoke) | <span data-ttu-id="f1fd3-111">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f1fd3-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f1fd3-112">Используйте свойство Cursor для получения нового курсора.</span><span class="sxs-lookup"><span data-stu-id="f1fd3-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="f1fd3-113">Участников</span><span class="sxs-lookup"><span data-stu-id="f1fd3-113">Members</span></span>

#### <span data-ttu-id="f1fd3-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f1fd3-114">Invoke</span></span> 

<span data-ttu-id="f1fd3-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f1fd3-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f1fd3-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f1fd3-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="f1fd3-117">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="f1fd3-117">There are no event args and the args parameter will be null.</span></span>


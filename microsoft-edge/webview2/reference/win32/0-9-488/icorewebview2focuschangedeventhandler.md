---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 5a0c15cf56283c9d2ba71b9f8261288977c6ef39
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885473"
---
# <span data-ttu-id="1365b-104">0.9.515-Interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1365b-104">0.9.515 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1365b-105">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="1365b-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="1365b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1365b-106">Summary</span></span>

 <span data-ttu-id="1365b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="1365b-107">Members</span></span>                        | <span data-ttu-id="1365b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="1365b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1365b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1365b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1365b-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1365b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1365b-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1365b-111">There are no event args for this event.</span></span>

## <span data-ttu-id="1365b-112">Участников</span><span class="sxs-lookup"><span data-stu-id="1365b-112">Members</span></span>

#### <span data-ttu-id="1365b-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="1365b-113">Invoke</span></span> 

<span data-ttu-id="1365b-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1365b-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1365b-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1365b-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="1365b-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="1365b-116">There are no event args and the args parameter will be null.</span></span>


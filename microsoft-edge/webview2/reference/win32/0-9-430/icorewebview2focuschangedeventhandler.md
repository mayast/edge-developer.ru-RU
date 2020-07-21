---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ff7c4fb51916d17df3fddc3d183fe8831029703a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884150"
---
# <span data-ttu-id="4548f-104">0.9.430-Interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4548f-104">0.9.430 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4548f-105">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="4548f-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="4548f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4548f-106">Summary</span></span>

 <span data-ttu-id="4548f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="4548f-107">Members</span></span>                        | <span data-ttu-id="4548f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="4548f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4548f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4548f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4548f-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4548f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4548f-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="4548f-111">There are no event args for this event.</span></span>

## <span data-ttu-id="4548f-112">Участников</span><span class="sxs-lookup"><span data-stu-id="4548f-112">Members</span></span>

#### <span data-ttu-id="4548f-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="4548f-113">Invoke</span></span> 

<span data-ttu-id="4548f-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4548f-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4548f-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4548f-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="4548f-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="4548f-116">There are no event args and the args parameter will be null.</span></span>


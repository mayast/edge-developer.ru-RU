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
ms.openlocfilehash: 2908ad851a7899d2ea053bfa50616c8b244bca6c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699183"
---
# <span data-ttu-id="4a4f9-104">интерфейс ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4a4f9-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4a4f9-105">Вызывающий объект реализует этот интерфейс, чтобы получать события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="4a4f9-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4a4f9-106">Summary</span></span>

 <span data-ttu-id="4a4f9-107">Участников</span><span class="sxs-lookup"><span data-stu-id="4a4f9-107">Members</span></span>                        | <span data-ttu-id="4a4f9-108">Описания</span><span class="sxs-lookup"><span data-stu-id="4a4f9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4a4f9-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4a4f9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4a4f9-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4a4f9-111">Используйте свойство DocumentTitle, чтобы получить измененный заголовок.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="4a4f9-112">Участников</span><span class="sxs-lookup"><span data-stu-id="4a4f9-112">Members</span></span>

#### <span data-ttu-id="4a4f9-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="4a4f9-113">Invoke</span></span> 

<span data-ttu-id="4a4f9-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4a4f9-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4a4f9-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="4a4f9-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-116">There are no event args and the args parameter will be null.</span></span>


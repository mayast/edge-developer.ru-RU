---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 04859c0a22e8571a4fe8015a089c9b7d708c1dd3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884878"
---
# <span data-ttu-id="7557c-104">0.9.430-Interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="7557c-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="7557c-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="7557c-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="7557c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7557c-106">Summary</span></span>

 <span data-ttu-id="7557c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7557c-107">Members</span></span>                        | <span data-ttu-id="7557c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7557c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7557c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7557c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7557c-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7557c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7557c-111">Для получения нового номера версии используйте get_NewVersion метод [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) .</span><span class="sxs-lookup"><span data-stu-id="7557c-111">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="7557c-112">Участников</span><span class="sxs-lookup"><span data-stu-id="7557c-112">Members</span></span>

#### <span data-ttu-id="7557c-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="7557c-113">Invoke</span></span> 

<span data-ttu-id="7557c-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7557c-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7557c-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7557c-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>


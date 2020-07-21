---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e47ca26475ba1b59fa4ea8c87a7aada0d8d6695f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884136"
---
# <span data-ttu-id="a66f0-104">0.9.430-Interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a66f0-104">0.9.430 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="a66f0-105">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="a66f0-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="a66f0-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a66f0-106">Summary</span></span>

 <span data-ttu-id="a66f0-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a66f0-107">Members</span></span>                        | <span data-ttu-id="a66f0-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a66f0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a66f0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a66f0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a66f0-110">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="a66f0-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="a66f0-111">Участников</span><span class="sxs-lookup"><span data-stu-id="a66f0-111">Members</span></span>

#### <span data-ttu-id="a66f0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a66f0-112">Invoke</span></span> 

<span data-ttu-id="a66f0-113">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="a66f0-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="a66f0-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="a66f0-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>


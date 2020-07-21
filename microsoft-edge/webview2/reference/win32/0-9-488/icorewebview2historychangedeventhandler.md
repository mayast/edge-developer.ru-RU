---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d90f461f6c2a1e573b0514213ec34f83f0d23366
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885501"
---
# <span data-ttu-id="57e51-104">0.9.515-Interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="57e51-104">0.9.515 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="57e51-105">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="57e51-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="57e51-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="57e51-106">Summary</span></span>

 <span data-ttu-id="57e51-107">Участников</span><span class="sxs-lookup"><span data-stu-id="57e51-107">Members</span></span>                        | <span data-ttu-id="57e51-108">Описания</span><span class="sxs-lookup"><span data-stu-id="57e51-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="57e51-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="57e51-109">Invoke</span></span>](#invoke) | <span data-ttu-id="57e51-110">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="57e51-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="57e51-111">Участников</span><span class="sxs-lookup"><span data-stu-id="57e51-111">Members</span></span>

#### <span data-ttu-id="57e51-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="57e51-112">Invoke</span></span> 

<span data-ttu-id="57e51-113">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="57e51-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="57e51-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="57e51-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


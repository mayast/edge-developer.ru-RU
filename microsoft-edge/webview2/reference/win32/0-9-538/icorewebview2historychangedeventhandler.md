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
ms.openlocfilehash: 0f14f8d281d4729d797eb5271a19cff67becafab
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699226"
---
# <span data-ttu-id="7e1cc-104">интерфейс ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7e1cc-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="7e1cc-105">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="7e1cc-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="7e1cc-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7e1cc-106">Summary</span></span>

 <span data-ttu-id="7e1cc-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7e1cc-107">Members</span></span>                        | <span data-ttu-id="7e1cc-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7e1cc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7e1cc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e1cc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7e1cc-110">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="7e1cc-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="7e1cc-111">Участников</span><span class="sxs-lookup"><span data-stu-id="7e1cc-111">Members</span></span>

#### <span data-ttu-id="7e1cc-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e1cc-112">Invoke</span></span> 

<span data-ttu-id="7e1cc-113">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="7e1cc-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="7e1cc-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="7e1cc-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


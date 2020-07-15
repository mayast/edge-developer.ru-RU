---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 5c4807a6f1772354f4448b25d49ea7ea86278f57
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880607"
---
# <span data-ttu-id="1e13a-104">0.9.515-Interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1e13a-104">0.9.515 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="1e13a-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1e13a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1e13a-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="1e13a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1e13a-107">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="1e13a-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="1e13a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1e13a-108">Summary</span></span>

 <span data-ttu-id="1e13a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="1e13a-109">Members</span></span>                        | <span data-ttu-id="1e13a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="1e13a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1e13a-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="1e13a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="1e13a-112">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="1e13a-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="1e13a-113">Участников</span><span class="sxs-lookup"><span data-stu-id="1e13a-113">Members</span></span>

#### <span data-ttu-id="1e13a-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="1e13a-114">Invoke</span></span> 

<span data-ttu-id="1e13a-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="1e13a-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="1e13a-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1e13a-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


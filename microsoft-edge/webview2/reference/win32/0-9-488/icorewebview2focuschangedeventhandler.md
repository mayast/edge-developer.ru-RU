---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: fabe1e9190259306dcaf311e54c6ee6035cd697c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697282"
---
# <span data-ttu-id="d6fec-104">интерфейс ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d6fec-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d6fec-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="d6fec-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d6fec-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="d6fec-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="d6fec-107">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="d6fec-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="d6fec-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d6fec-108">Summary</span></span>

 <span data-ttu-id="d6fec-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d6fec-109">Members</span></span>                        | <span data-ttu-id="d6fec-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d6fec-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d6fec-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d6fec-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d6fec-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d6fec-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d6fec-113">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d6fec-113">There are no event args for this event.</span></span>

## <span data-ttu-id="d6fec-114">Участников</span><span class="sxs-lookup"><span data-stu-id="d6fec-114">Members</span></span>

#### <span data-ttu-id="d6fec-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="d6fec-115">Invoke</span></span> 

<span data-ttu-id="d6fec-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d6fec-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d6fec-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d6fec-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="d6fec-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="d6fec-118">There are no event args and the args parameter will be null.</span></span>


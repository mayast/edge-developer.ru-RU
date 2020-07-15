---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 44e24ef8e0e4b41968835ff7cd70fd9904482c6c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878451"
---
# <span data-ttu-id="0612d-104">0.8.355-Interface IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0612d-104">0.8.355 - interface IWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0612d-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="0612d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0612d-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="0612d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="0612d-107">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="0612d-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="0612d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0612d-108">Summary</span></span>

 <span data-ttu-id="0612d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="0612d-109">Members</span></span>                        | <span data-ttu-id="0612d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="0612d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0612d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="0612d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0612d-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="0612d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="0612d-113">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0612d-113">There are no event args for this event.</span></span>

## <span data-ttu-id="0612d-114">Участников</span><span class="sxs-lookup"><span data-stu-id="0612d-114">Members</span></span>

#### <span data-ttu-id="0612d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="0612d-115">Invoke</span></span> 

<span data-ttu-id="0612d-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="0612d-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0612d-117">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="0612d-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="0612d-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="0612d-118">There are no event args and the args parameter will be null.</span></span>


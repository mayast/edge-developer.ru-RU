---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6a1b472a4a37c31d4914794784767f8e0b9b6b94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877779"
---
# <span data-ttu-id="d0cfc-104">0.9.430-Interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d0cfc-104">0.9.430 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d0cfc-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d0cfc-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="d0cfc-107">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="d0cfc-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d0cfc-108">Summary</span></span>

 <span data-ttu-id="d0cfc-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d0cfc-109">Members</span></span>                        | <span data-ttu-id="d0cfc-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d0cfc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d0cfc-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d0cfc-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d0cfc-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d0cfc-113">Участников</span><span class="sxs-lookup"><span data-stu-id="d0cfc-113">Members</span></span>

#### <span data-ttu-id="d0cfc-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="d0cfc-114">Invoke</span></span> 

<span data-ttu-id="d0cfc-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d0cfc-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d0cfc-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="d0cfc-117">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-117">There are no event args and the args parameter will be null.</span></span>


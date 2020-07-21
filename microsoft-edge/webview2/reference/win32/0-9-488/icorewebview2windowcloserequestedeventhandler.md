---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9163eb811e018e346f610dae71d5fdb7e39de186
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885438"
---
# <span data-ttu-id="95f27-104">0.9.515-Interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="95f27-104">0.9.515 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="95f27-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="95f27-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="95f27-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="95f27-106">Summary</span></span>

 <span data-ttu-id="95f27-107">Участников</span><span class="sxs-lookup"><span data-stu-id="95f27-107">Members</span></span>                        | <span data-ttu-id="95f27-108">Описания</span><span class="sxs-lookup"><span data-stu-id="95f27-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95f27-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="95f27-109">Invoke</span></span>](#invoke) | <span data-ttu-id="95f27-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="95f27-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="95f27-111">Участников</span><span class="sxs-lookup"><span data-stu-id="95f27-111">Members</span></span>

#### <span data-ttu-id="95f27-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="95f27-112">Invoke</span></span> 

<span data-ttu-id="95f27-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="95f27-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="95f27-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="95f27-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="95f27-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="95f27-115">There are no event args and the args parameter will be null.</span></span>


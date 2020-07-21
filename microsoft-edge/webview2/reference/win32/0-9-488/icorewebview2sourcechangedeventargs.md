---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9a98e2afa5b15452d7521183abebc019d51e3a3c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885459"
---
# <span data-ttu-id="bb25d-104">0.9.515-Interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="bb25d-104">0.9.515 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="bb25d-105">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="bb25d-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="bb25d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="bb25d-106">Summary</span></span>

 <span data-ttu-id="bb25d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="bb25d-107">Members</span></span>                        | <span data-ttu-id="bb25d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="bb25d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bb25d-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="bb25d-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="bb25d-110">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="bb25d-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="bb25d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="bb25d-111">Members</span></span>

#### <span data-ttu-id="bb25d-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="bb25d-112">get_IsNewDocument</span></span> 

<span data-ttu-id="bb25d-113">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="bb25d-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="bb25d-114">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="bb25d-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>


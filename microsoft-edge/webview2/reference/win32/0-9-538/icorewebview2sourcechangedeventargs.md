---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: b9350db7d59c0369bfb16d10e30a23ef3f6bffa5
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010462"
---
# <span data-ttu-id="49393-104">0.9.579-Interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="49393-104">0.9.579 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="49393-105">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="49393-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="49393-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="49393-106">Summary</span></span>

 <span data-ttu-id="49393-107">Участников</span><span class="sxs-lookup"><span data-stu-id="49393-107">Members</span></span>                        | <span data-ttu-id="49393-108">Описания</span><span class="sxs-lookup"><span data-stu-id="49393-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49393-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="49393-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="49393-110">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="49393-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="49393-111">Участников</span><span class="sxs-lookup"><span data-stu-id="49393-111">Members</span></span>

#### <span data-ttu-id="49393-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="49393-112">get_IsNewDocument</span></span> 

<span data-ttu-id="49393-113">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="49393-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="49393-114">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="49393-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>


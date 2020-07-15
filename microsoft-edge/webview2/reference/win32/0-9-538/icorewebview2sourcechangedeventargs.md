---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: 3e622a8fb5b8ed43e5a23eaab8bd0aa61ed7d193
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879403"
---
# <span data-ttu-id="330a3-104">интерфейс ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="330a3-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="330a3-105">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="330a3-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="330a3-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="330a3-106">Summary</span></span>

 <span data-ttu-id="330a3-107">Участников</span><span class="sxs-lookup"><span data-stu-id="330a3-107">Members</span></span>                        | <span data-ttu-id="330a3-108">Описания</span><span class="sxs-lookup"><span data-stu-id="330a3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="330a3-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="330a3-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="330a3-110">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="330a3-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="330a3-111">Участников</span><span class="sxs-lookup"><span data-stu-id="330a3-111">Members</span></span>

#### <span data-ttu-id="330a3-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="330a3-112">get_IsNewDocument</span></span> 

<span data-ttu-id="330a3-113">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="330a3-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="330a3-114">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="330a3-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>


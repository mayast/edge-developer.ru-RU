---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: 7417b4790d327bbd5a415dc1237e0604963598e0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012555"
---
# <span data-ttu-id="251d9-104">интерфейс ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="251d9-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="251d9-105">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="251d9-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="251d9-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="251d9-106">Summary</span></span>

 <span data-ttu-id="251d9-107">Участников</span><span class="sxs-lookup"><span data-stu-id="251d9-107">Members</span></span>                        | <span data-ttu-id="251d9-108">Описания</span><span class="sxs-lookup"><span data-stu-id="251d9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="251d9-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="251d9-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="251d9-110">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="251d9-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="251d9-111">Участников</span><span class="sxs-lookup"><span data-stu-id="251d9-111">Members</span></span>

#### <span data-ttu-id="251d9-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="251d9-112">get_IsNewDocument</span></span> 

<span data-ttu-id="251d9-113">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="251d9-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="251d9-114">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="251d9-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2eb2749b71cd9be9dfd25bb686b4ea57e728f179
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883983"
---
# <span data-ttu-id="6b439-104">0.9.430-Interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6b439-104">0.9.430 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="6b439-105">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="6b439-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="6b439-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6b439-106">Summary</span></span>

 <span data-ttu-id="6b439-107">Участников</span><span class="sxs-lookup"><span data-stu-id="6b439-107">Members</span></span>                        | <span data-ttu-id="6b439-108">Описания</span><span class="sxs-lookup"><span data-stu-id="6b439-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6b439-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="6b439-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="6b439-110">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="6b439-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="6b439-111">Участников</span><span class="sxs-lookup"><span data-stu-id="6b439-111">Members</span></span>

#### <span data-ttu-id="6b439-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="6b439-112">get_IsNewDocument</span></span> 

<span data-ttu-id="6b439-113">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="6b439-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="6b439-114">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="6b439-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>


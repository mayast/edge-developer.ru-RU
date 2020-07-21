---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 75741c1ba1d835d1c26c7d1db0845071216e0705
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886124"
---
# <span data-ttu-id="3188c-104">0.8.355-Interface IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3188c-104">0.8.355 - interface IWebView2DocumentStateChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="3188c-105">Аргументы события для события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="3188c-105">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="3188c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3188c-106">Summary</span></span>

 <span data-ttu-id="3188c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="3188c-107">Members</span></span>                        | <span data-ttu-id="3188c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="3188c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3188c-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="3188c-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="3188c-110">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="3188c-110">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="3188c-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3188c-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="3188c-112">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="3188c-112">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="3188c-113">Участников</span><span class="sxs-lookup"><span data-stu-id="3188c-113">Members</span></span>

#### <span data-ttu-id="3188c-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="3188c-114">get_IsNewDocument</span></span> 

<span data-ttu-id="3188c-115">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="3188c-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="3188c-116">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="3188c-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="3188c-117">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3188c-117">get_IsErrorPage</span></span> 

<span data-ttu-id="3188c-118">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="3188c-118">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="3188c-119">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="3188c-119">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>


---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: 571aae9e1e00938c9bf0f3fb872fccf340269105
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877457"
---
# <span data-ttu-id="e52ab-104">интерфейс ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="e52ab-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="e52ab-105">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="e52ab-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="e52ab-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e52ab-106">Summary</span></span>

 <span data-ttu-id="e52ab-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e52ab-107">Members</span></span>                        | <span data-ttu-id="e52ab-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e52ab-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e52ab-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="e52ab-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="e52ab-110">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="e52ab-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="e52ab-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="e52ab-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="e52ab-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="e52ab-112">The ID of the navigation.</span></span>

## <span data-ttu-id="e52ab-113">Участников</span><span class="sxs-lookup"><span data-stu-id="e52ab-113">Members</span></span>

#### <span data-ttu-id="e52ab-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="e52ab-114">get_IsErrorPage</span></span> 

<span data-ttu-id="e52ab-115">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="e52ab-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="e52ab-116">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="e52ab-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="e52ab-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="e52ab-117">get_NavigationId</span></span> 

<span data-ttu-id="e52ab-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="e52ab-118">The ID of the navigation.</span></span>

> <span data-ttu-id="e52ab-119">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="e52ab-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


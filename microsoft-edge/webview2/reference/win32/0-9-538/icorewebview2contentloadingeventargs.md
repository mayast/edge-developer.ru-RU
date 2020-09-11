---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: d70673714e3641e19f5c3d6367278c0c7bd2729b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010301"
---
# <span data-ttu-id="17481-104">0.9.579-Interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="17481-104">0.9.579 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="17481-105">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="17481-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="17481-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="17481-106">Summary</span></span>

 <span data-ttu-id="17481-107">Участников</span><span class="sxs-lookup"><span data-stu-id="17481-107">Members</span></span>                        | <span data-ttu-id="17481-108">Описания</span><span class="sxs-lookup"><span data-stu-id="17481-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17481-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="17481-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="17481-110">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="17481-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="17481-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="17481-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="17481-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="17481-112">The ID of the navigation.</span></span>

## <span data-ttu-id="17481-113">Участников</span><span class="sxs-lookup"><span data-stu-id="17481-113">Members</span></span>

#### <span data-ttu-id="17481-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="17481-114">get_IsErrorPage</span></span> 

<span data-ttu-id="17481-115">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="17481-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="17481-116">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="17481-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="17481-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="17481-117">get_NavigationId</span></span> 

<span data-ttu-id="17481-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="17481-118">The ID of the navigation.</span></span>

> <span data-ttu-id="17481-119">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="17481-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


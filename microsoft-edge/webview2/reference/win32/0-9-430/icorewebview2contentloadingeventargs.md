---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 95fa97268fb5695aebf5c1414752cf12cf1da57b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881146"
---
# <span data-ttu-id="fa933-104">0.9.430-Interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="fa933-104">0.9.430 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="fa933-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="fa933-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="fa933-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="fa933-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="fa933-107">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="fa933-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="fa933-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fa933-108">Summary</span></span>

 <span data-ttu-id="fa933-109">Участников</span><span class="sxs-lookup"><span data-stu-id="fa933-109">Members</span></span>                        | <span data-ttu-id="fa933-110">Описания</span><span class="sxs-lookup"><span data-stu-id="fa933-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fa933-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="fa933-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="fa933-112">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="fa933-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="fa933-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="fa933-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="fa933-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="fa933-114">The ID of the navigation.</span></span>

## <span data-ttu-id="fa933-115">Участников</span><span class="sxs-lookup"><span data-stu-id="fa933-115">Members</span></span>

#### <span data-ttu-id="fa933-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="fa933-116">get_IsErrorPage</span></span> 

<span data-ttu-id="fa933-117">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="fa933-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="fa933-118">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="fa933-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="fa933-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="fa933-119">get_NavigationId</span></span> 

<span data-ttu-id="fa933-120">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="fa933-120">The ID of the navigation.</span></span>

> <span data-ttu-id="fa933-121">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="fa933-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c6bb99078b5574ba89c0d66b49e2c63cd6888d28
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654900"
---
# <span data-ttu-id="3e8e9-104">интерфейс ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="3e8e9-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="3e8e9-105">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="3e8e9-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3e8e9-106">Summary</span></span>

 <span data-ttu-id="3e8e9-107">Участников</span><span class="sxs-lookup"><span data-stu-id="3e8e9-107">Members</span></span>                        | <span data-ttu-id="3e8e9-108">Описания</span><span class="sxs-lookup"><span data-stu-id="3e8e9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3e8e9-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3e8e9-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="3e8e9-110">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="3e8e9-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3e8e9-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="3e8e9-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-112">The ID of the navigation.</span></span>

## <span data-ttu-id="3e8e9-113">Участников</span><span class="sxs-lookup"><span data-stu-id="3e8e9-113">Members</span></span>

#### <span data-ttu-id="3e8e9-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3e8e9-114">get_IsErrorPage</span></span> 

<span data-ttu-id="3e8e9-115">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="3e8e9-116">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="3e8e9-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="3e8e9-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3e8e9-117">get_NavigationId</span></span> 

<span data-ttu-id="3e8e9-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-118">The ID of the navigation.</span></span>

> <span data-ttu-id="3e8e9-119">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="3e8e9-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


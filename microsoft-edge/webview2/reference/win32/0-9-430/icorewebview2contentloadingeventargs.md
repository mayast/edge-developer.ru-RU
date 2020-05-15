---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c3ba6ac3a2478861abb7b26e726a9cbd606b0eb9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654791"
---
# <span data-ttu-id="7e89c-104">интерфейс ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="7e89c-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7e89c-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7e89c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7e89c-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="7e89c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="7e89c-107">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="7e89c-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="7e89c-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7e89c-108">Summary</span></span>

 <span data-ttu-id="7e89c-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7e89c-109">Members</span></span>                        | <span data-ttu-id="7e89c-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7e89c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7e89c-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="7e89c-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="7e89c-112">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="7e89c-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="7e89c-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7e89c-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="7e89c-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="7e89c-114">The ID of the navigation.</span></span>

## <span data-ttu-id="7e89c-115">Участников</span><span class="sxs-lookup"><span data-stu-id="7e89c-115">Members</span></span>

#### <span data-ttu-id="7e89c-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="7e89c-116">get_IsErrorPage</span></span> 

<span data-ttu-id="7e89c-117">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="7e89c-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="7e89c-118">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="7e89c-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="7e89c-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7e89c-119">get_NavigationId</span></span> 

<span data-ttu-id="7e89c-120">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="7e89c-120">The ID of the navigation.</span></span>

> <span data-ttu-id="7e89c-121">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="7e89c-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8acec97ec6060cd53adc3821f6a51db2048935fb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699203"
---
# <span data-ttu-id="6c355-104">интерфейс ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="6c355-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="6c355-105">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="6c355-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="6c355-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6c355-106">Summary</span></span>

 <span data-ttu-id="6c355-107">Участников</span><span class="sxs-lookup"><span data-stu-id="6c355-107">Members</span></span>                        | <span data-ttu-id="6c355-108">Описания</span><span class="sxs-lookup"><span data-stu-id="6c355-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c355-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="6c355-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="6c355-110">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="6c355-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="6c355-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6c355-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="6c355-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="6c355-112">The ID of the navigation.</span></span>

## <span data-ttu-id="6c355-113">Участников</span><span class="sxs-lookup"><span data-stu-id="6c355-113">Members</span></span>

#### <span data-ttu-id="6c355-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="6c355-114">get_IsErrorPage</span></span> 

<span data-ttu-id="6c355-115">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="6c355-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="6c355-116">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="6c355-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="6c355-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6c355-117">get_NavigationId</span></span> 

<span data-ttu-id="6c355-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="6c355-118">The ID of the navigation.</span></span>

> <span data-ttu-id="6c355-119">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="6c355-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


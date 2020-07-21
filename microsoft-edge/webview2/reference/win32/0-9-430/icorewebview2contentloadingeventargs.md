---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 7bccd93aeec2c5cfbc181ce5ab1cf58e29da48ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884297"
---
# <span data-ttu-id="73cb1-104">0.9.430-Interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="73cb1-104">0.9.430 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="73cb1-105">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="73cb1-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="73cb1-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="73cb1-106">Summary</span></span>

 <span data-ttu-id="73cb1-107">Участников</span><span class="sxs-lookup"><span data-stu-id="73cb1-107">Members</span></span>                        | <span data-ttu-id="73cb1-108">Описания</span><span class="sxs-lookup"><span data-stu-id="73cb1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="73cb1-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="73cb1-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="73cb1-110">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="73cb1-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="73cb1-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="73cb1-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="73cb1-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="73cb1-112">The ID of the navigation.</span></span>

## <span data-ttu-id="73cb1-113">Участников</span><span class="sxs-lookup"><span data-stu-id="73cb1-113">Members</span></span>

#### <span data-ttu-id="73cb1-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="73cb1-114">get_IsErrorPage</span></span> 

<span data-ttu-id="73cb1-115">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="73cb1-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="73cb1-116">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="73cb1-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="73cb1-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="73cb1-117">get_NavigationId</span></span> 

<span data-ttu-id="73cb1-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="73cb1-118">The ID of the navigation.</span></span>

> <span data-ttu-id="73cb1-119">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="73cb1-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


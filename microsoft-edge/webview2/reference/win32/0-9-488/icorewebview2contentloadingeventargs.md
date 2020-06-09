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
ms.openlocfilehash: c720b700257554891f13477f5f3508e331ac6b25
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698206"
---
# <span data-ttu-id="d9931-104">интерфейс ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="d9931-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d9931-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="d9931-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d9931-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="d9931-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="d9931-107">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d9931-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="d9931-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d9931-108">Summary</span></span>

 <span data-ttu-id="d9931-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d9931-109">Members</span></span>                        | <span data-ttu-id="d9931-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d9931-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9931-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="d9931-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="d9931-112">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="d9931-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="d9931-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="d9931-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="d9931-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="d9931-114">The ID of the navigation.</span></span>

## <span data-ttu-id="d9931-115">Участников</span><span class="sxs-lookup"><span data-stu-id="d9931-115">Members</span></span>

#### <span data-ttu-id="d9931-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="d9931-116">get_IsErrorPage</span></span> 

<span data-ttu-id="d9931-117">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="d9931-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="d9931-118">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="d9931-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="d9931-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="d9931-119">get_NavigationId</span></span> 

<span data-ttu-id="d9931-120">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="d9931-120">The ID of the navigation.</span></span>

> <span data-ttu-id="d9931-121">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="d9931-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


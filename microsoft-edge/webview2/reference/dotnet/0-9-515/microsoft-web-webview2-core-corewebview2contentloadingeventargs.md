---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 899adcb7cfa171e8c1f6cb9693092e36f2e41a5f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877765"
---
# <span data-ttu-id="89769-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="89769-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2ContentLoadingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="89769-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="89769-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="89769-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="89769-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="89769-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="89769-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="89769-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="89769-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="89769-109">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="89769-109">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="89769-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="89769-110">Summary</span></span>

 <span data-ttu-id="89769-111">Участников</span><span class="sxs-lookup"><span data-stu-id="89769-111">Members</span></span>                        | <span data-ttu-id="89769-112">Описания</span><span class="sxs-lookup"><span data-stu-id="89769-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="89769-113">IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="89769-113">IsErrorPage</span></span>](#iserrorpage) | <span data-ttu-id="89769-114">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="89769-114">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="89769-115">NavigationId</span><span class="sxs-lookup"><span data-stu-id="89769-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="89769-116">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="89769-116">The ID of the navigation.</span></span>

## <span data-ttu-id="89769-117">Участников</span><span class="sxs-lookup"><span data-stu-id="89769-117">Members</span></span>

#### <span data-ttu-id="89769-118">IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="89769-118">IsErrorPage</span></span> 

<span data-ttu-id="89769-119">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="89769-119">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="89769-120">Открытый логический [IsErrorPage](#iserrorpage)</span><span class="sxs-lookup"><span data-stu-id="89769-120">public bool [IsErrorPage](#iserrorpage)</span></span>

#### <span data-ttu-id="89769-121">NavigationId</span><span class="sxs-lookup"><span data-stu-id="89769-121">NavigationId</span></span> 

<span data-ttu-id="89769-122">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="89769-122">The ID of the navigation.</span></span>

> <span data-ttu-id="89769-123">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="89769-123">public ulong [NavigationId](#navigationid)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: abe167548b7e604bd60c792660ea5b52dec9b848
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697303"
---
# <span data-ttu-id="e10e8-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="e10e8-104">Microsoft.Web.WebView2.Core.CoreWebView2ContentLoadingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="e10e8-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e10e8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e10e8-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="e10e8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="e10e8-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e10e8-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e10e8-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="e10e8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e10e8-109">Аргументы события для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="e10e8-109">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="e10e8-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e10e8-110">Summary</span></span>

 <span data-ttu-id="e10e8-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e10e8-111">Members</span></span>                        | <span data-ttu-id="e10e8-112">Описания</span><span class="sxs-lookup"><span data-stu-id="e10e8-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e10e8-113">IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="e10e8-113">IsErrorPage</span></span>](#iserrorpage) | <span data-ttu-id="e10e8-114">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="e10e8-114">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="e10e8-115">NavigationId</span><span class="sxs-lookup"><span data-stu-id="e10e8-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="e10e8-116">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="e10e8-116">The ID of the navigation.</span></span>

## <span data-ttu-id="e10e8-117">Участников</span><span class="sxs-lookup"><span data-stu-id="e10e8-117">Members</span></span>

#### <span data-ttu-id="e10e8-118">IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="e10e8-118">IsErrorPage</span></span> 

<span data-ttu-id="e10e8-119">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="e10e8-119">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="e10e8-120">Открытый логический [IsErrorPage](#iserrorpage)</span><span class="sxs-lookup"><span data-stu-id="e10e8-120">public bool [IsErrorPage](#iserrorpage)</span></span>

#### <span data-ttu-id="e10e8-121">NavigationId</span><span class="sxs-lookup"><span data-stu-id="e10e8-121">NavigationId</span></span> 

<span data-ttu-id="e10e8-122">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="e10e8-122">The ID of the navigation.</span></span>

> <span data-ttu-id="e10e8-123">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="e10e8-123">public ulong [NavigationId](#navigationid)</span></span>


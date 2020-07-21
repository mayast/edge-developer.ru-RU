---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 98cfec908a0e1ad73046f7740f6e9a2efad8a853
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886289"
---
# <span data-ttu-id="440ec-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="440ec-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="440ec-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="440ec-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="440ec-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="440ec-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="440ec-107">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="440ec-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="440ec-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="440ec-108">Summary</span></span>

 <span data-ttu-id="440ec-109">Участников</span><span class="sxs-lookup"><span data-stu-id="440ec-109">Members</span></span>                        | <span data-ttu-id="440ec-110">Описания</span><span class="sxs-lookup"><span data-stu-id="440ec-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="440ec-111">Handled</span><span class="sxs-lookup"><span data-stu-id="440ec-111">Handled</span></span>](#handled) | <span data-ttu-id="440ec-112">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="440ec-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="440ec-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="440ec-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="440ec-114">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="440ec-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="440ec-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="440ec-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="440ec-116">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="440ec-116">Gets the new window.</span></span>
[<span data-ttu-id="440ec-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="440ec-117">Uri</span></span>](#uri) | <span data-ttu-id="440ec-118">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="440ec-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="440ec-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="440ec-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="440ec-120">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="440ec-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="440ec-121">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="440ec-121">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="440ec-122">Участников</span><span class="sxs-lookup"><span data-stu-id="440ec-122">Members</span></span>

#### <span data-ttu-id="440ec-123">Handled</span><span class="sxs-lookup"><span data-stu-id="440ec-123">Handled</span></span> 

<span data-ttu-id="440ec-124">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="440ec-124">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="440ec-125">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="440ec-125">public bool [Handled](#handled)</span></span>

<span data-ttu-id="440ec-126">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="440ec-126">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="440ec-127">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="440ec-127">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="440ec-128">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="440ec-128">Default is false.</span></span>

#### <span data-ttu-id="440ec-129">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="440ec-129">IsUserInitiated</span></span> 

<span data-ttu-id="440ec-130">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="440ec-130">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="440ec-131">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="440ec-131">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="440ec-132">NewWindow</span><span class="sxs-lookup"><span data-stu-id="440ec-132">NewWindow</span></span> 

<span data-ttu-id="440ec-133">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="440ec-133">Gets the new window.</span></span>

> <span data-ttu-id="440ec-134">общедоступная CoreWebView2 [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="440ec-134">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="440ec-135">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="440ec-135">Uri</span></span> 

<span data-ttu-id="440ec-136">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="440ec-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="440ec-137">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="440ec-137">public string [Uri](#uri)</span></span>

<span data-ttu-id="440ec-138">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="440ec-138">The target webview should not be navigated.</span></span> <span data-ttu-id="440ec-139">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="440ec-139">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="440ec-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="440ec-140">GetDeferral</span></span> 

<span data-ttu-id="440ec-141">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="440ec-141">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="440ec-142">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="440ec-142">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="440ec-143">Вы можете использовать объект CoreWebView2Deferral, чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="440ec-143">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="440ec-144">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="440ec-144">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


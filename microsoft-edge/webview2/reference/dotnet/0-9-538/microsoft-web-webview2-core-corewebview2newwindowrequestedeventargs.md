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
ms.openlocfilehash: 54e2c06ef65f64560fbd5687148eace253352203
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699135"
---
# <span data-ttu-id="0c979-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0c979-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="0c979-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0c979-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0c979-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="0c979-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0c979-107">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="0c979-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="0c979-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0c979-108">Summary</span></span>

 <span data-ttu-id="0c979-109">Участников</span><span class="sxs-lookup"><span data-stu-id="0c979-109">Members</span></span>                        | <span data-ttu-id="0c979-110">Описания</span><span class="sxs-lookup"><span data-stu-id="0c979-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0c979-111">Handled</span><span class="sxs-lookup"><span data-stu-id="0c979-111">Handled</span></span>](#handled) | <span data-ttu-id="0c979-112">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="0c979-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="0c979-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0c979-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="0c979-114">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="0c979-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="0c979-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="0c979-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="0c979-116">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="0c979-116">Gets the new window.</span></span>
[<span data-ttu-id="0c979-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="0c979-117">Uri</span></span>](#uri) | <span data-ttu-id="0c979-118">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="0c979-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="0c979-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="0c979-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="0c979-120">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="0c979-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="0c979-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0c979-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="0c979-122">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="0c979-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="0c979-123">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0c979-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="0c979-124">Участников</span><span class="sxs-lookup"><span data-stu-id="0c979-124">Members</span></span>

#### <span data-ttu-id="0c979-125">Handled</span><span class="sxs-lookup"><span data-stu-id="0c979-125">Handled</span></span> 

<span data-ttu-id="0c979-126">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="0c979-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="0c979-127">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="0c979-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="0c979-128">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="0c979-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="0c979-129">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="0c979-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="0c979-130">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="0c979-130">Default is false.</span></span>

#### <span data-ttu-id="0c979-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0c979-131">IsUserInitiated</span></span> 

<span data-ttu-id="0c979-132">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="0c979-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="0c979-133">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="0c979-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="0c979-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="0c979-134">NewWindow</span></span> 

<span data-ttu-id="0c979-135">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="0c979-135">Gets the new window.</span></span>

> <span data-ttu-id="0c979-136">общедоступная CoreWebView2 [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="0c979-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="0c979-137">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="0c979-137">Uri</span></span> 

<span data-ttu-id="0c979-138">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="0c979-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="0c979-139">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="0c979-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="0c979-140">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="0c979-140">The target webview should not be navigated.</span></span> <span data-ttu-id="0c979-141">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="0c979-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="0c979-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="0c979-142">WindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="0c979-143">Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="0c979-143">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="0c979-144">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="0c979-144">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="0c979-145">общедоступная CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="0c979-145">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="0c979-146">Эти функции можно учитывать при размещении и изменении размера новых окон WebView.</span><span class="sxs-lookup"><span data-stu-id="0c979-146">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="0c979-147">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0c979-147">GetDeferral</span></span> 

<span data-ttu-id="0c979-148">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="0c979-148">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="0c979-149">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="0c979-149">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="0c979-150">Вы можете использовать объект CoreWebView2Deferral, чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="0c979-150">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="0c979-151">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="0c979-151">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


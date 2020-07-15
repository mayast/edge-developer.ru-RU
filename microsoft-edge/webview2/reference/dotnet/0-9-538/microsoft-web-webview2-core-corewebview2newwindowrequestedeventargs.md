---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 2a2934e1fef6c601155cb4002a0c97ca1629099e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878808"
---
# <span data-ttu-id="19771-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="19771-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="19771-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="19771-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="19771-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="19771-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="19771-107">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="19771-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="19771-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="19771-108">Summary</span></span>

 <span data-ttu-id="19771-109">Участников</span><span class="sxs-lookup"><span data-stu-id="19771-109">Members</span></span>                        | <span data-ttu-id="19771-110">Описания</span><span class="sxs-lookup"><span data-stu-id="19771-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="19771-111">Handled</span><span class="sxs-lookup"><span data-stu-id="19771-111">Handled</span></span>](#handled) | <span data-ttu-id="19771-112">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="19771-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="19771-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="19771-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="19771-114">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="19771-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="19771-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="19771-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="19771-116">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="19771-116">Gets the new window.</span></span>
[<span data-ttu-id="19771-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="19771-117">Uri</span></span>](#uri) | <span data-ttu-id="19771-118">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="19771-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="19771-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="19771-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="19771-120">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="19771-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="19771-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="19771-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="19771-122">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="19771-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="19771-123">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="19771-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="19771-124">Участников</span><span class="sxs-lookup"><span data-stu-id="19771-124">Members</span></span>

#### <span data-ttu-id="19771-125">Handled</span><span class="sxs-lookup"><span data-stu-id="19771-125">Handled</span></span> 

<span data-ttu-id="19771-126">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="19771-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="19771-127">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="19771-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="19771-128">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="19771-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="19771-129">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="19771-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="19771-130">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="19771-130">Default is false.</span></span>

#### <span data-ttu-id="19771-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="19771-131">IsUserInitiated</span></span> 

<span data-ttu-id="19771-132">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="19771-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="19771-133">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="19771-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="19771-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="19771-134">NewWindow</span></span> 

<span data-ttu-id="19771-135">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="19771-135">Gets the new window.</span></span>

> <span data-ttu-id="19771-136">общедоступная CoreWebView2 [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="19771-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="19771-137">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="19771-137">Uri</span></span> 

<span data-ttu-id="19771-138">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="19771-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="19771-139">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="19771-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="19771-140">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="19771-140">The target webview should not be navigated.</span></span> <span data-ttu-id="19771-141">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="19771-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="19771-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="19771-142">WindowFeatures</span></span> 

<span data-ttu-id="19771-143">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="19771-143">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="19771-144">общедоступная CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="19771-144">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="19771-145">Эти функции можно учитывать при размещении и изменении размера новых окон WebView.</span><span class="sxs-lookup"><span data-stu-id="19771-145">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="19771-146">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="19771-146">GetDeferral</span></span> 

<span data-ttu-id="19771-147">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="19771-147">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="19771-148">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="19771-148">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="19771-149">Вы можете использовать объект CoreWebView2Deferral, чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="19771-149">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="19771-150">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="19771-150">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


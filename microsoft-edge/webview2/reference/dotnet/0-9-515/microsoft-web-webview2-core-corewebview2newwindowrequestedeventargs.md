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
ms.openlocfilehash: cca15ccc5292f5eaf6f317ffb657f46fcd84b4a9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654992"
---
# <span data-ttu-id="d6782-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d6782-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="d6782-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d6782-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d6782-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="d6782-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d6782-107">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d6782-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="d6782-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d6782-108">Summary</span></span>

 <span data-ttu-id="d6782-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d6782-109">Members</span></span>                        | <span data-ttu-id="d6782-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d6782-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d6782-111">Handled</span><span class="sxs-lookup"><span data-stu-id="d6782-111">Handled</span></span>](#handled) | <span data-ttu-id="d6782-112">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="d6782-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="d6782-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d6782-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="d6782-114">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="d6782-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="d6782-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="d6782-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="d6782-116">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="d6782-116">Gets the new window.</span></span>
[<span data-ttu-id="d6782-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="d6782-117">Uri</span></span>](#uri) | <span data-ttu-id="d6782-118">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d6782-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="d6782-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d6782-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d6782-120">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="d6782-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="d6782-121">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d6782-121">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="d6782-122">Участников</span><span class="sxs-lookup"><span data-stu-id="d6782-122">Members</span></span>

#### <span data-ttu-id="d6782-123">Handled</span><span class="sxs-lookup"><span data-stu-id="d6782-123">Handled</span></span> 

<span data-ttu-id="d6782-124">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="d6782-124">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="d6782-125">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="d6782-125">public bool [Handled](#handled)</span></span>

<span data-ttu-id="d6782-126">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="d6782-126">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="d6782-127">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="d6782-127">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="d6782-128">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="d6782-128">Default is false.</span></span>

#### <span data-ttu-id="d6782-129">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d6782-129">IsUserInitiated</span></span> 

<span data-ttu-id="d6782-130">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="d6782-130">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="d6782-131">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="d6782-131">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="d6782-132">NewWindow</span><span class="sxs-lookup"><span data-stu-id="d6782-132">NewWindow</span></span> 

<span data-ttu-id="d6782-133">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="d6782-133">Gets the new window.</span></span>

> <span data-ttu-id="d6782-134">общедоступная CoreWebView2 [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="d6782-134">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="d6782-135">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="d6782-135">Uri</span></span> 

<span data-ttu-id="d6782-136">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d6782-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="d6782-137">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="d6782-137">public string [Uri](#uri)</span></span>

<span data-ttu-id="d6782-138">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="d6782-138">The target webview should not be navigated.</span></span> <span data-ttu-id="d6782-139">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="d6782-139">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="d6782-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d6782-140">GetDeferral</span></span> 

<span data-ttu-id="d6782-141">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="d6782-141">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d6782-142">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="d6782-142">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="d6782-143">Вы можете использовать объект CoreWebView2Deferral, чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="d6782-143">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="d6782-144">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="d6782-144">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


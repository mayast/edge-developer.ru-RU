---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d10154fbaeb8dca0247dc721a2144899feba38df
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880012"
---
# <span data-ttu-id="939bf-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="939bf-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="939bf-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="939bf-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="939bf-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="939bf-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="939bf-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="939bf-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="939bf-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="939bf-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="939bf-109">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="939bf-109">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="939bf-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="939bf-110">Summary</span></span>

 <span data-ttu-id="939bf-111">Участников</span><span class="sxs-lookup"><span data-stu-id="939bf-111">Members</span></span>                        | <span data-ttu-id="939bf-112">Описания</span><span class="sxs-lookup"><span data-stu-id="939bf-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="939bf-113">Handled</span><span class="sxs-lookup"><span data-stu-id="939bf-113">Handled</span></span>](#handled) | <span data-ttu-id="939bf-114">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="939bf-114">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="939bf-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="939bf-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="939bf-116">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="939bf-116">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="939bf-117">NewWindow</span><span class="sxs-lookup"><span data-stu-id="939bf-117">NewWindow</span></span>](#newwindow) | <span data-ttu-id="939bf-118">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="939bf-118">Gets the new window.</span></span>
[<span data-ttu-id="939bf-119">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="939bf-119">Uri</span></span>](#uri) | <span data-ttu-id="939bf-120">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="939bf-120">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="939bf-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="939bf-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="939bf-122">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="939bf-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="939bf-123">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="939bf-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="939bf-124">Участников</span><span class="sxs-lookup"><span data-stu-id="939bf-124">Members</span></span>

#### <span data-ttu-id="939bf-125">Handled</span><span class="sxs-lookup"><span data-stu-id="939bf-125">Handled</span></span> 

<span data-ttu-id="939bf-126">Обрабатываются ли NewWindowRequestedEvent с помощью Host.</span><span class="sxs-lookup"><span data-stu-id="939bf-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="939bf-127">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="939bf-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="939bf-128">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="939bf-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="939bf-129">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="939bf-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="939bf-130">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="939bf-130">Default is false.</span></span>

#### <span data-ttu-id="939bf-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="939bf-131">IsUserInitiated</span></span> 

<span data-ttu-id="939bf-132">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="939bf-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="939bf-133">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="939bf-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="939bf-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="939bf-134">NewWindow</span></span> 

<span data-ttu-id="939bf-135">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="939bf-135">Gets the new window.</span></span>

> <span data-ttu-id="939bf-136">общедоступная CoreWebView2 [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="939bf-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="939bf-137">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="939bf-137">Uri</span></span> 

<span data-ttu-id="939bf-138">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="939bf-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="939bf-139">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="939bf-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="939bf-140">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="939bf-140">The target webview should not be navigated.</span></span> <span data-ttu-id="939bf-141">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="939bf-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="939bf-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="939bf-142">GetDeferral</span></span> 

<span data-ttu-id="939bf-143">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="939bf-143">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="939bf-144">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="939bf-144">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="939bf-145">Вы можете использовать объект CoreWebView2Deferral, чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="939bf-145">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="939bf-146">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="939bf-146">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Справочник по языку WebView2 Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e6e921ca1cae586bef89962c5eb98668a655ad22
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883779"
---
# <span data-ttu-id="e9770-104">Справочник (WebView2 Win32 C++)</span><span class="sxs-lookup"><span data-stu-id="e9770-104">Reference (WebView2 Win32 C++)</span></span>  

<span data-ttu-id="e9770-105">Элемент управления Microsoft Edge WebView2 позволяет размещать веб-содержимое в приложении с помощью [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) в качестве обработчика визуализации.</span><span class="sxs-lookup"><span data-stu-id="e9770-105">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="e9770-106">Дополнительные сведения можно найти в [статье Обзор Microsoft Edge WebView2](../../index.md)) и [Приступая к работе с WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="e9770-106">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="e9770-107">[ICoreWebView2](0-9-538/ICoreWebView2.md) — это удобное место для изучения данных API.</span><span class="sxs-lookup"><span data-stu-id="e9770-107">[ICoreWebView2](0-9-538/ICoreWebView2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="e9770-108">Глобальные настройки</span><span class="sxs-lookup"><span data-stu-id="e9770-108">Globals</span></span>  

*   [<span data-ttu-id="e9770-109">Глобальные настройки</span><span class="sxs-lookup"><span data-stu-id="e9770-109">Globals</span></span>](0-9-538/webview2-idl.md)  

## <span data-ttu-id="e9770-110">Приклад</span><span class="sxs-lookup"><span data-stu-id="e9770-110">Interfaces</span></span>  
*   [<span data-ttu-id="e9770-111">ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="e9770-111">ICoreWebView2</span></span>](0-9-538/icorewebview2.md)
*   [<span data-ttu-id="e9770-112">ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="e9770-112">ICoreWebView2Controller</span></span>](0-9-538/icorewebview2controller.md)
*   [<span data-ttu-id="e9770-113">ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="e9770-113">ICoreWebView2Deferral</span></span>](0-9-538/icorewebview2deferral.md)
*   [<span data-ttu-id="e9770-114">ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="e9770-114">ICoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-538/icorewebview2devtoolsprotocoleventreceiver.md)
*   [<span data-ttu-id="e9770-115">ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="e9770-115">ICoreWebView2Environment</span></span>](0-9-538/icorewebview2environment.md)
*   [<span data-ttu-id="e9770-116">ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="e9770-116">ICoreWebView2EnvironmentOptions</span></span>](0-9-538/icorewebview2environmentoptions.md)
*   [<span data-ttu-id="e9770-117">ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="e9770-117">ICoreWebView2HttpHeadersCollectionIterator</span></span>](0-9-538/icorewebview2httpheaderscollectioniterator.md)
*   [<span data-ttu-id="e9770-118">ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="e9770-118">ICoreWebView2HttpRequestHeaders</span></span>](0-9-538/icorewebview2httprequestheaders.md)
*   [<span data-ttu-id="e9770-119">ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="e9770-119">ICoreWebView2HttpResponseHeaders</span></span>](0-9-538/icorewebview2httpresponseheaders.md)
*   [<span data-ttu-id="e9770-120">ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="e9770-120">ICoreWebView2Settings</span></span>](0-9-538/icorewebview2settings.md)
*   [<span data-ttu-id="e9770-121">ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="e9770-121">ICoreWebView2WebResourceRequest</span></span>](0-9-538/icorewebview2webresourcerequest.md)
*   [<span data-ttu-id="e9770-122">ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="e9770-122">ICoreWebView2WebResourceResponse</span></span>](0-9-538/icorewebview2webresourceresponse.md)

### <span data-ttu-id="e9770-123">Аргументы события</span><span class="sxs-lookup"><span data-stu-id="e9770-123">Event arguments</span></span>

*   [<span data-ttu-id="e9770-124">ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-124">ICoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-538/icorewebview2acceleratorkeypressedeventargs.md)
*   [<span data-ttu-id="e9770-125">ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-125">ICoreWebView2ContentLoadingEventArgs</span></span>](0-9-538/icorewebview2contentloadingeventargs.md)
*   [<span data-ttu-id="e9770-126">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-126">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-538/icorewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [<span data-ttu-id="e9770-127">ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-127">ICoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-538/icorewebview2movefocusrequestedeventargs.md)
*   [<span data-ttu-id="e9770-128">ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-128">ICoreWebView2NavigationCompletedEventArgs</span></span>](0-9-538/icorewebview2navigationcompletedeventargs.md)
*   [<span data-ttu-id="e9770-129">ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-129">ICoreWebView2NavigationStartingEventArgs</span></span>](0-9-538/icorewebview2navigationstartingeventargs.md)
*   [<span data-ttu-id="e9770-130">ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-130">ICoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-538/icorewebview2newwindowrequestedeventargs.md)
*   [<span data-ttu-id="e9770-131">ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-131">ICoreWebView2PermissionRequestedEventArgs</span></span>](0-9-538/icorewebview2permissionrequestedeventargs.md)
*   [<span data-ttu-id="e9770-132">ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-132">ICoreWebView2ProcessFailedEventArgs</span></span>](0-9-538/icorewebview2processfailedeventargs.md)
*   [<span data-ttu-id="e9770-133">ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-133">ICoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-538/icorewebview2scriptdialogopeningeventargs.md)
*   [<span data-ttu-id="e9770-134">ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-134">ICoreWebView2SourceChangedEventArgs</span></span>](0-9-538/icorewebview2sourcechangedeventargs.md)
*   [<span data-ttu-id="e9770-135">ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-135">ICoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-538/icorewebview2webmessagereceivedeventargs.md)
*   [<span data-ttu-id="e9770-136">ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-136">ICoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-538/icorewebview2webresourcerequestedeventargs.md)

### <span data-ttu-id="e9770-137">Делегаты</span><span class="sxs-lookup"><span data-stu-id="e9770-137">Delegates</span></span>

*   [<span data-ttu-id="e9770-138">ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-138">ICoreWebView2AcceleratorKeyPressedEventHandler</span></span>](0-9-538/icorewebview2acceleratorkeypressedeventhandler.md)
*   [<span data-ttu-id="e9770-139">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-139">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-9-538/icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md)
*   [<span data-ttu-id="e9770-140">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-140">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-9-538/icorewebview2calldevtoolsprotocolmethodcompletedhandler.md)
*   [<span data-ttu-id="e9770-141">ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-141">ICoreWebView2CapturePreviewCompletedHandler</span></span>](0-9-538/icorewebview2capturepreviewcompletedhandler.md)
*   [<span data-ttu-id="e9770-142">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-142">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-9-538/icorewebview2containsfullscreenelementchangedeventhandler.md)
*   [<span data-ttu-id="e9770-143">ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-143">ICoreWebView2ContentLoadingEventHandler</span></span>](0-9-538/icorewebview2contentloadingeventhandler.md)
*   [<span data-ttu-id="e9770-144">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-144">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span>](0-9-538/icorewebview2createcorewebview2controllercompletedhandler.md)
*   [<span data-ttu-id="e9770-145">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-145">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span>](0-9-538/icorewebview2createcorewebview2environmentcompletedhandler.md)
*   [<span data-ttu-id="e9770-146">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-146">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-9-538/icorewebview2devtoolsprotocoleventreceivedeventhandler.md)
*   [<span data-ttu-id="e9770-147">ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-147">ICoreWebView2DocumentTitleChangedEventHandler</span></span>](0-9-538/icorewebview2documenttitlechangedeventhandler.md)
*   [<span data-ttu-id="e9770-148">ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-148">ICoreWebView2ExecuteScriptCompletedHandler</span></span>](0-9-538/icorewebview2executescriptcompletedhandler.md)
*   [<span data-ttu-id="e9770-149">ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-149">ICoreWebView2FocusChangedEventHandler</span></span>](0-9-538/icorewebview2focuschangedeventhandler.md)
*   [<span data-ttu-id="e9770-150">ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-150">ICoreWebView2HistoryChangedEventHandler</span></span>](0-9-538/icorewebview2historychangedeventhandler.md)
*   [<span data-ttu-id="e9770-151">ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-151">ICoreWebView2MoveFocusRequestedEventHandler</span></span>](0-9-538/icorewebview2movefocusrequestedeventhandler.md)
*   [<span data-ttu-id="e9770-152">ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-152">ICoreWebView2NavigationCompletedEventHandler</span></span>](0-9-538/icorewebview2navigationcompletedeventhandler.md)
*   [<span data-ttu-id="e9770-153">ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-153">ICoreWebView2NavigationStartingEventHandler</span></span>](0-9-538/icorewebview2navigationstartingeventhandler.md)
*   [<span data-ttu-id="e9770-154">ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-154">ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span>](0-9-538/icorewebview2newbrowserversionavailableeventhandler.md)
*   [<span data-ttu-id="e9770-155">ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-155">ICoreWebView2NewWindowRequestedEventHandler</span></span>](0-9-538/icorewebview2newwindowrequestedeventhandler.md)
*   [<span data-ttu-id="e9770-156">ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-156">ICoreWebView2PermissionRequestedEventHandler</span></span>](0-9-538/icorewebview2permissionrequestedeventhandler.md)
*   [<span data-ttu-id="e9770-157">ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-157">ICoreWebView2ProcessFailedEventHandler</span></span>](0-9-538/icorewebview2processfailedeventhandler.md)
*   [<span data-ttu-id="e9770-158">ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-158">ICoreWebView2ScriptDialogOpeningEventHandler</span></span>](0-9-538/icorewebview2scriptdialogopeningeventhandler.md)
*   [<span data-ttu-id="e9770-159">ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-159">ICoreWebView2SourceChangedEventHandler</span></span>](0-9-538/icorewebview2sourcechangedeventhandler.md)
*   [<span data-ttu-id="e9770-160">ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-160">ICoreWebView2WebMessageReceivedEventHandler</span></span>](0-9-538/icorewebview2webmessagereceivedeventhandler.md)
*   [<span data-ttu-id="e9770-161">ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-161">ICoreWebView2WebResourceRequestedEventHandler</span></span>](0-9-538/icorewebview2webresourcerequestedeventhandler.md)
*   [<span data-ttu-id="e9770-162">ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-162">ICoreWebView2WindowCloseRequestedEventHandler</span></span>](0-9-538/icorewebview2windowcloserequestedeventhandler.md)
*   [<span data-ttu-id="e9770-163">ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-163">ICoreWebView2ZoomFactorChangedEventHandler</span></span>](0-9-538/icorewebview2zoomfactorchangedeventhandler.md)

### <span data-ttu-id="e9770-164">Экспериментальные</span><span class="sxs-lookup"><span data-stu-id="e9770-164">Experimental</span></span>

*   [<span data-ttu-id="e9770-165">ICoreWebView2Experimental</span><span class="sxs-lookup"><span data-stu-id="e9770-165">ICoreWebView2Experimental</span></span>](0-9-538/icorewebview2experimental.md)
*   [<span data-ttu-id="e9770-166">ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="e9770-166">ICoreWebView2ExperimentalCompositionController</span></span>](0-9-538/icorewebview2experimentalcompositioncontroller.md)
*   [<span data-ttu-id="e9770-167">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-167">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span>](0-9-538/icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md)
*   [<span data-ttu-id="e9770-168">ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-168">ICoreWebView2ExperimentalCursorChangedEventHandler</span></span>](0-9-538/icorewebview2experimentalcursorchangedeventhandler.md)
*   [<span data-ttu-id="e9770-169">ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="e9770-169">ICoreWebView2ExperimentalEnvironment</span></span>](0-9-538/icorewebview2experimentalenvironment.md)
*   [<span data-ttu-id="e9770-170">ICoreWebView2ExperimentalEnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="e9770-170">ICoreWebView2ExperimentalEnvironmentOptions</span></span>](0-9-538/icorewebview2experimentalenvironmentoptions.md)
*   [<span data-ttu-id="e9770-171">ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-171">ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span>](0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md)
*   [<span data-ttu-id="e9770-172">ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="e9770-172">ICoreWebView2ExperimentalPointerInfo</span></span>](0-9-538/icorewebview2experimentalpointerinfo.md)
*   [<span data-ttu-id="e9770-173">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9770-173">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span>](0-9-538/icorewebview2experimentalwebresourceresponsereceivedeventargs.md)
*   [<span data-ttu-id="e9770-174">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-174">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span>](0-9-538/icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md)
*   [<span data-ttu-id="e9770-175">ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9770-175">ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span>](0-9-538/icorewebview2experimentalwebresourceresponsereceivedeventhandler.md)
*   [<span data-ttu-id="e9770-176">ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="e9770-176">ICoreWebView2ExperimentalWindowFeatures</span></span>](0-9-538/icorewebview2experimentalwindowfeatures.md)

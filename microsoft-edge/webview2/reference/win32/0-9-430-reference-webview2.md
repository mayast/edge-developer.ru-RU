---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Справочник по языку 0.9.430-WebView2 Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a0095660af031cafa09e5223650d174f525ba3df
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880243"
---
# <span data-ttu-id="f8081-104">0.9.430 - Справочные материалы (WebView2)</span><span class="sxs-lookup"><span data-stu-id="f8081-104">0.9.430 - Reference (WebView2)</span></span>  

> [!NOTE]
> <span data-ttu-id="f8081-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="f8081-105">This reference may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f8081-106">Ознакомьтесь со [справочной](../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="f8081-106">Please refer to [Reference](../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="f8081-107">Элемент управления Microsoft Edge WebView2 позволяет размещать веб-содержимое в приложении с помощью [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) в качестве обработчика визуализации.</span><span class="sxs-lookup"><span data-stu-id="f8081-107">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="f8081-108">Дополнительные сведения можно найти в [статье Обзор Microsoft Edge WebView2](../../index.md)) и [Приступая к работе с WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="f8081-108">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="f8081-109">[ICoreWebView2](0-9-430/ICoreWebView2.md) — это удобное место для изучения данных API.</span><span class="sxs-lookup"><span data-stu-id="f8081-109">[ICoreWebView2](0-9-430/ICoreWebView2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="f8081-110">Глобальные настройки</span><span class="sxs-lookup"><span data-stu-id="f8081-110">Globals</span></span>  

*   [<span data-ttu-id="f8081-111">Глобальные настройки</span><span class="sxs-lookup"><span data-stu-id="f8081-111">Globals</span></span>](0-9-430/webview2-idl.md)  

## <span data-ttu-id="f8081-112">Приклад</span><span class="sxs-lookup"><span data-stu-id="f8081-112">Interfaces</span></span>  
*   [<span data-ttu-id="f8081-113">ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="f8081-113">ICoreWebView2</span></span>](0-9-430/ICoreWebView2.md)
*   [<span data-ttu-id="f8081-114">ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="f8081-114">ICoreWebView2Deferral</span></span>](0-9-430/ICoreWebView2Deferral.md)
*   [<span data-ttu-id="f8081-115">ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="f8081-115">ICoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-430/ICoreWebView2DevToolsProtocolEventReceiver.md)
*   [<span data-ttu-id="f8081-116">ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="f8081-116">ICoreWebView2Environment</span></span>](0-9-430/ICoreWebView2Environment.md)
*   [<span data-ttu-id="f8081-117">ICoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="f8081-117">ICoreWebView2Host</span></span>](0-9-430/ICoreWebView2Host.md)
*   [<span data-ttu-id="f8081-118">ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="f8081-118">ICoreWebView2HttpHeadersCollectionIterator</span></span>](0-9-430/ICoreWebView2HttpHeadersCollectionIterator.md)
*   [<span data-ttu-id="f8081-119">ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="f8081-119">ICoreWebView2HttpRequestHeaders</span></span>](0-9-430/ICoreWebView2HttpRequestHeaders.md)
*   [<span data-ttu-id="f8081-120">ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="f8081-120">ICoreWebView2HttpResponseHeaders</span></span>](0-9-430/ICoreWebView2HttpResponseHeaders.md)
*   [<span data-ttu-id="f8081-121">ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="f8081-121">ICoreWebView2Settings</span></span>](0-9-430/ICoreWebView2Settings.md)
*   [<span data-ttu-id="f8081-122">ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="f8081-122">ICoreWebView2WebResourceRequest</span></span>](0-9-430/ICoreWebView2WebResourceRequest.md)
*   [<span data-ttu-id="f8081-123">ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f8081-123">ICoreWebView2WebResourceResponse</span></span>](0-9-430/ICoreWebView2WebResourceResponse.md)

### <span data-ttu-id="f8081-124">Интерфейсы аргументов событий</span><span class="sxs-lookup"><span data-stu-id="f8081-124">Event argument interfaces</span></span>

*   [<span data-ttu-id="f8081-125">ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-125">ICoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-430/ICoreWebView2AcceleratorKeyPressedEventArgs.md)
*   [<span data-ttu-id="f8081-126">ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-126">ICoreWebView2ContentLoadingEventArgs</span></span>](0-9-430/ICoreWebView2ContentLoadingEventArgs.md)
*   [<span data-ttu-id="f8081-127">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-127">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [<span data-ttu-id="f8081-128">ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-128">ICoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-430/ICoreWebView2MoveFocusRequestedEventArgs.md)
*   [<span data-ttu-id="f8081-129">ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-129">ICoreWebView2NavigationCompletedEventArgs</span></span>](0-9-430/ICoreWebView2NavigationCompletedEventArgs.md)
*   [<span data-ttu-id="f8081-130">ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-130">ICoreWebView2NavigationStartingEventArgs</span></span>](0-9-430/ICoreWebView2NavigationStartingEventArgs.md)
*   [<span data-ttu-id="f8081-131">ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-131">ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span>](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventArgs.md)
*   [<span data-ttu-id="f8081-132">ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-132">ICoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-430/ICoreWebView2NewWindowRequestedEventArgs.md)
*   [<span data-ttu-id="f8081-133">ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-133">ICoreWebView2PermissionRequestedEventArgs</span></span>](0-9-430/ICoreWebView2PermissionRequestedEventArgs.md)
*   [<span data-ttu-id="f8081-134">ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-134">ICoreWebView2ProcessFailedEventArgs</span></span>](0-9-430/ICoreWebView2ProcessFailedEventArgs.md)
*   [<span data-ttu-id="f8081-135">ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-135">ICoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-430/ICoreWebView2ScriptDialogOpeningEventArgs.md)
*   [<span data-ttu-id="f8081-136">ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-136">ICoreWebView2SourceChangedEventArgs</span></span>](0-9-430/ICoreWebView2SourceChangedEventArgs.md)
*   [<span data-ttu-id="f8081-137">ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-137">ICoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-430/ICoreWebView2WebMessageReceivedEventArgs.md)
*   [<span data-ttu-id="f8081-138">ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8081-138">ICoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-430/ICoreWebView2WebResourceRequestedEventArgs.md)

### <span data-ttu-id="f8081-139">Интерфейсы делегатов</span><span class="sxs-lookup"><span data-stu-id="f8081-139">Delegate interfaces</span></span>

*   [<span data-ttu-id="f8081-140">ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-140">ICoreWebView2AcceleratorKeyPressedEventHandler</span></span>](0-9-430/ICoreWebView2AcceleratorKeyPressedEventHandler.md)
*   [<span data-ttu-id="f8081-141">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-141">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-9-430/ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [<span data-ttu-id="f8081-142">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-142">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-9-430/ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [<span data-ttu-id="f8081-143">ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-143">ICoreWebView2CapturePreviewCompletedHandler</span></span>](0-9-430/ICoreWebView2CapturePreviewCompletedHandler.md)
*   [<span data-ttu-id="f8081-144">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-144">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-9-430/ICoreWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [<span data-ttu-id="f8081-145">ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-145">ICoreWebView2ContentLoadingEventHandler</span></span>](0-9-430/ICoreWebView2ContentLoadingEventHandler.md)
*   [<span data-ttu-id="f8081-146">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-146">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span>](0-9-430/ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler.md)
*   [<span data-ttu-id="f8081-147">ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-147">ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span>](0-9-430/ICoreWebView2CreateCoreWebView2HostCompletedHandler.md)
*   [<span data-ttu-id="f8081-148">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-148">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [<span data-ttu-id="f8081-149">ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-149">ICoreWebView2DocumentTitleChangedEventHandler</span></span>](0-9-430/ICoreWebView2DocumentTitleChangedEventHandler.md)
*   [<span data-ttu-id="f8081-150">ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-150">ICoreWebView2ExecuteScriptCompletedHandler</span></span>](0-9-430/ICoreWebView2ExecuteScriptCompletedHandler.md)
*   [<span data-ttu-id="f8081-151">ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-151">ICoreWebView2FocusChangedEventHandler</span></span>](0-9-430/ICoreWebView2FocusChangedEventHandler.md)
*   [<span data-ttu-id="f8081-152">ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-152">ICoreWebView2HistoryChangedEventHandler</span></span>](0-9-430/ICoreWebView2HistoryChangedEventHandler.md)
*   [<span data-ttu-id="f8081-153">ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-153">ICoreWebView2MoveFocusRequestedEventHandler</span></span>](0-9-430/ICoreWebView2MoveFocusRequestedEventHandler.md)
*   [<span data-ttu-id="f8081-154">ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-154">ICoreWebView2NavigationCompletedEventHandler</span></span>](0-9-430/ICoreWebView2NavigationCompletedEventHandler.md)
*   [<span data-ttu-id="f8081-155">ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-155">ICoreWebView2NavigationStartingEventHandler</span></span>](0-9-430/ICoreWebView2NavigationStartingEventHandler.md)
*   [<span data-ttu-id="f8081-156">ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-156">ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span>](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventHandler.md)
*   [<span data-ttu-id="f8081-157">ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-157">ICoreWebView2NewWindowRequestedEventHandler</span></span>](0-9-430/ICoreWebView2NewWindowRequestedEventHandler.md)
*   [<span data-ttu-id="f8081-158">ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-158">ICoreWebView2PermissionRequestedEventHandler</span></span>](0-9-430/ICoreWebView2PermissionRequestedEventHandler.md)
*   [<span data-ttu-id="f8081-159">ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-159">ICoreWebView2ProcessFailedEventHandler</span></span>](0-9-430/ICoreWebView2ProcessFailedEventHandler.md)
*   [<span data-ttu-id="f8081-160">ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-160">ICoreWebView2ScriptDialogOpeningEventHandler</span></span>](0-9-430/ICoreWebView2ScriptDialogOpeningEventHandler.md)
*   [<span data-ttu-id="f8081-161">ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-161">ICoreWebView2SourceChangedEventHandler</span></span>](0-9-430/ICoreWebView2SourceChangedEventHandler.md)
*   [<span data-ttu-id="f8081-162">ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-162">ICoreWebView2WebMessageReceivedEventHandler</span></span>](0-9-430/ICoreWebView2WebMessageReceivedEventHandler.md)
*   [<span data-ttu-id="f8081-163">ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-163">ICoreWebView2WebResourceRequestedEventHandler</span></span>](0-9-430/ICoreWebView2WebResourceRequestedEventHandler.md)
*   [<span data-ttu-id="f8081-164">ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-164">ICoreWebView2WindowCloseRequestedEventHandler</span></span>](0-9-430/ICoreWebView2WindowCloseRequestedEventHandler.md)
*   [<span data-ttu-id="f8081-165">ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8081-165">ICoreWebView2ZoomFactorChangedEventHandler</span></span>](0-9-430/ICoreWebView2ZoomFactorChangedEventHandler.md)

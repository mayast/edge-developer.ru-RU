---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ba3103037db60674d1d3887ac43a8fce5be02bdd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654825"
---
# <span data-ttu-id="a0cf2-104">0.8.190-Reference (WebView2)</span><span class="sxs-lookup"><span data-stu-id="a0cf2-104">0.8.190 - Reference (WebView2)</span></span>  

> [!NOTE]
> <span data-ttu-id="a0cf2-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a0cf2-105">This reference may be altered or unavailable for releases after SDK version 0.8.355.</span></span>  <span data-ttu-id="a0cf2-106">Ознакомьтесь со [справочной](../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="a0cf2-106">Please refer to [Reference](../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="a0cf2-107">Элемент управления Microsoft Edge WebView2 позволяет размещать веб-содержимое в приложении с помощью [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) в качестве обработчика визуализации.</span><span class="sxs-lookup"><span data-stu-id="a0cf2-107">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="a0cf2-108">Дополнительные сведения можно найти в [статье Обзор Microsoft Edge WebView2](../../index.md)) и [Приступая к работе с WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="a0cf2-108">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="a0cf2-109">[IWebView2WebView](0-8-190/IWebView2WebView.md) — это удобное место для изучения данных API.</span><span class="sxs-lookup"><span data-stu-id="a0cf2-109">[IWebView2WebView](0-8-190/IWebView2WebView.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="a0cf2-110">Глобальные</span><span class="sxs-lookup"><span data-stu-id="a0cf2-110">Globals</span></span>  

*   [<span data-ttu-id="a0cf2-111">Глобальные</span><span class="sxs-lookup"><span data-stu-id="a0cf2-111">Globals</span></span>](0-8-190/webview2-idl.md)  

## <span data-ttu-id="a0cf2-112">Приклад</span><span class="sxs-lookup"><span data-stu-id="a0cf2-112">Interfaces</span></span>  
*   [<span data-ttu-id="a0cf2-113">IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="a0cf2-113">IWebView2Deferral</span></span>](0-8-190/IWebView2Deferral.md)
*   [<span data-ttu-id="a0cf2-114">IWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="a0cf2-114">IWebView2Environment</span></span>](0-8-190/IWebView2Environment.md)
*   [<span data-ttu-id="a0cf2-115">IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="a0cf2-115">IWebView2Environment2</span></span>](0-8-190/IWebView2Environment2.md)
*   [<span data-ttu-id="a0cf2-116">IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="a0cf2-116">IWebView2Environment3</span></span>](0-8-190/IWebView2Environment3.md)
*   [<span data-ttu-id="a0cf2-117">IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="a0cf2-117">IWebView2HttpHeadersCollectionIterator</span></span>](0-8-190/IWebView2HttpHeadersCollectionIterator.md)
*   [<span data-ttu-id="a0cf2-118">IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a0cf2-118">IWebView2HttpRequestHeaders</span></span>](0-8-190/IWebView2HttpRequestHeaders.md)
*   [<span data-ttu-id="a0cf2-119">IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="a0cf2-119">IWebView2HttpResponseHeaders</span></span>](0-8-190/IWebView2HttpResponseHeaders.md)
*   [<span data-ttu-id="a0cf2-120">IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="a0cf2-120">IWebView2Settings</span></span>](0-8-190/IWebView2Settings.md)
*   [<span data-ttu-id="a0cf2-121">IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="a0cf2-121">IWebView2Settings2</span></span>](0-8-190/IWebView2Settings2.md)
*   [<span data-ttu-id="a0cf2-122">IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="a0cf2-122">IWebView2WebResourceRequest</span></span>](0-8-190/IWebView2WebResourceRequest.md)
*   [<span data-ttu-id="a0cf2-123">IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="a0cf2-123">IWebView2WebResourceRequestedEventArgs2</span></span>](0-8-190/IWebView2WebResourceRequestedEventArgs2.md)
*   [<span data-ttu-id="a0cf2-124">IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="a0cf2-124">IWebView2WebResourceResponse</span></span>](0-8-190/IWebView2WebResourceResponse.md)
*   [<span data-ttu-id="a0cf2-125">IWebView2WebView</span><span class="sxs-lookup"><span data-stu-id="a0cf2-125">IWebView2WebView</span></span>](0-8-190/IWebView2WebView.md)
*   [<span data-ttu-id="a0cf2-126">IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="a0cf2-126">IWebView2WebView2</span></span>](0-8-190/IWebView2WebView2.md)
*   [<span data-ttu-id="a0cf2-127">IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="a0cf2-127">IWebView2WebView3</span></span>](0-8-190/IWebView2WebView3.md)
*   [<span data-ttu-id="a0cf2-128">IWebView2WebView4</span><span class="sxs-lookup"><span data-stu-id="a0cf2-128">IWebView2WebView4</span></span>](0-8-190/IWebView2WebView4.md)
*   [<span data-ttu-id="a0cf2-129">IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="a0cf2-129">IWebView2WebView5</span></span>](0-8-190/IWebView2WebView5.md)

### <span data-ttu-id="a0cf2-130">Интерфейсы аргументов событий</span><span class="sxs-lookup"><span data-stu-id="a0cf2-130">Event argument interfaces</span></span>

*   [<span data-ttu-id="a0cf2-131">IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-131">IWebView2AcceleratorKeyPressedEventArgs</span></span>](0-8-190/IWebView2AcceleratorKeyPressedEventArgs.md)
*   [<span data-ttu-id="a0cf2-132">IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-132">IWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-8-190/IWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [<span data-ttu-id="a0cf2-133">IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-133">IWebView2DocumentStateChangedEventArgs</span></span>](0-8-190/IWebView2DocumentStateChangedEventArgs.md)
*   [<span data-ttu-id="a0cf2-134">IWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-134">IWebView2MoveFocusRequestedEventArgs</span></span>](0-8-190/IWebView2MoveFocusRequestedEventArgs.md)
*   [<span data-ttu-id="a0cf2-135">IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-135">IWebView2NavigationCompletedEventArgs</span></span>](0-8-190/IWebView2NavigationCompletedEventArgs.md)
*   [<span data-ttu-id="a0cf2-136">IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-136">IWebView2NavigationStartingEventArgs</span></span>](0-8-190/IWebView2NavigationStartingEventArgs.md)
*   [<span data-ttu-id="a0cf2-137">IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-137">IWebView2NewVersionAvailableEventArgs</span></span>](0-8-190/IWebView2NewVersionAvailableEventArgs.md)
*   [<span data-ttu-id="a0cf2-138">IWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-138">IWebView2NewWindowRequestedEventArgs</span></span>](0-8-190/IWebView2NewWindowRequestedEventArgs.md)
*   [<span data-ttu-id="a0cf2-139">IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-139">IWebView2PermissionRequestedEventArgs</span></span>](0-8-190/IWebView2PermissionRequestedEventArgs.md)
*   [<span data-ttu-id="a0cf2-140">IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-140">IWebView2ProcessFailedEventArgs</span></span>](0-8-190/IWebView2ProcessFailedEventArgs.md)
*   [<span data-ttu-id="a0cf2-141">IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-141">IWebView2ScriptDialogOpeningEventArgs</span></span>](0-8-190/IWebView2ScriptDialogOpeningEventArgs.md)
*   [<span data-ttu-id="a0cf2-142">IWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-142">IWebView2WebMessageReceivedEventArgs</span></span>](0-8-190/IWebView2WebMessageReceivedEventArgs.md)
*   [<span data-ttu-id="a0cf2-143">IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cf2-143">IWebView2WebResourceRequestedEventArgs</span></span>](0-8-190/IWebView2WebResourceRequestedEventArgs.md)

### <span data-ttu-id="a0cf2-144">Интерфейсы делегатов</span><span class="sxs-lookup"><span data-stu-id="a0cf2-144">Delegate interfaces</span></span>

*   [<span data-ttu-id="a0cf2-145">IWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-145">IWebView2AcceleratorKeyPressedEventHandler</span></span>](0-8-190/IWebView2AcceleratorKeyPressedEventHandler.md)
*   [<span data-ttu-id="a0cf2-146">IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-146">IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-8-190/IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [<span data-ttu-id="a0cf2-147">IWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-147">IWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-8-190/IWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [<span data-ttu-id="a0cf2-148">IWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-148">IWebView2CapturePreviewCompletedHandler</span></span>](0-8-190/IWebView2CapturePreviewCompletedHandler.md)
*   [<span data-ttu-id="a0cf2-149">IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-149">IWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [<span data-ttu-id="a0cf2-150">IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-150">IWebView2CreateWebView2EnvironmentCompletedHandler</span></span>](0-8-190/IWebView2CreateWebView2EnvironmentCompletedHandler.md)
*   [<span data-ttu-id="a0cf2-151">IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-151">IWebView2CreateWebViewCompletedHandler</span></span>](0-8-190/IWebView2CreateWebViewCompletedHandler.md)
*   [<span data-ttu-id="a0cf2-152">IWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-152">IWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-8-190/IWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [<span data-ttu-id="a0cf2-153">IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-153">IWebView2DocumentStateChangedEventHandler</span></span>](0-8-190/IWebView2DocumentStateChangedEventHandler.md)
*   [<span data-ttu-id="a0cf2-154">IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-154">IWebView2DocumentTitleChangedEventHandler</span></span>](0-8-190/IWebView2DocumentTitleChangedEventHandler.md)
*   [<span data-ttu-id="a0cf2-155">IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-155">IWebView2ExecuteScriptCompletedHandler</span></span>](0-8-190/IWebView2ExecuteScriptCompletedHandler.md)
*   [<span data-ttu-id="a0cf2-156">IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-156">IWebView2FocusChangedEventHandler</span></span>](0-8-190/IWebView2FocusChangedEventHandler.md)
*   [<span data-ttu-id="a0cf2-157">IWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-157">IWebView2MoveFocusRequestedEventHandler</span></span>](0-8-190/IWebView2MoveFocusRequestedEventHandler.md)
*   [<span data-ttu-id="a0cf2-158">IWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-158">IWebView2NavigationCompletedEventHandler</span></span>](0-8-190/IWebView2NavigationCompletedEventHandler.md)
*   [<span data-ttu-id="a0cf2-159">IWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-159">IWebView2NavigationStartingEventHandler</span></span>](0-8-190/IWebView2NavigationStartingEventHandler.md)
*   [<span data-ttu-id="a0cf2-160">IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-160">IWebView2NewVersionAvailableEventHandler</span></span>](0-8-190/IWebView2NewVersionAvailableEventHandler.md)
*   [<span data-ttu-id="a0cf2-161">IWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-161">IWebView2NewWindowRequestedEventHandler</span></span>](0-8-190/IWebView2NewWindowRequestedEventHandler.md)
*   [<span data-ttu-id="a0cf2-162">IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-162">IWebView2PermissionRequestedEventHandler</span></span>](0-8-190/IWebView2PermissionRequestedEventHandler.md)
*   [<span data-ttu-id="a0cf2-163">IWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-163">IWebView2ProcessFailedEventHandler</span></span>](0-8-190/IWebView2ProcessFailedEventHandler.md)
*   [<span data-ttu-id="a0cf2-164">IWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-164">IWebView2ScriptDialogOpeningEventHandler</span></span>](0-8-190/IWebView2ScriptDialogOpeningEventHandler.md)
*   [<span data-ttu-id="a0cf2-165">IWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-165">IWebView2WebMessageReceivedEventHandler</span></span>](0-8-190/IWebView2WebMessageReceivedEventHandler.md)
*   [<span data-ttu-id="a0cf2-166">IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-166">IWebView2WebResourceRequestedEventHandler</span></span>](0-8-190/IWebView2WebResourceRequestedEventHandler.md)
*   [<span data-ttu-id="a0cf2-167">IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a0cf2-167">IWebView2ZoomFactorChangedEventHandler</span></span>](0-8-190/IWebView2ZoomFactorChangedEventHandler.md)

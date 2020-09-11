---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2
ms.openlocfilehash: 6717542349cff327875b609168dff0b82a933668
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012551"
---
# <span data-ttu-id="647d4-104">интерфейс ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="647d4-104">interface ICoreWebView2</span></span> 

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="647d4-105">WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="647d4-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="647d4-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="647d4-106">Summary</span></span>

 <span data-ttu-id="647d4-107">Участников</span><span class="sxs-lookup"><span data-stu-id="647d4-107">Members</span></span>                        | <span data-ttu-id="647d4-108">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="647d4-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="647d4-110">Добавьте обработчик событий для события ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-110">Add an event handler for the ContainsFullScreenElementChanged event.</span></span>
[<span data-ttu-id="647d4-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="647d4-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="647d4-112">Добавьте обработчик событий для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="647d4-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="647d4-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="647d4-114">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="647d4-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="647d4-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="647d4-116">Добавьте обработчик событий для события FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="647d4-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="647d4-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="647d4-118">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="647d4-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="647d4-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="647d4-120">Добавьте обработчик событий для события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-120">Add an event handler for the HistoryChanged event.</span></span>
[<span data-ttu-id="647d4-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="647d4-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="647d4-122">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="647d4-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="647d4-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="647d4-124">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="647d4-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="647d4-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="647d4-126">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="647d4-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="647d4-128">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="647d4-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="647d4-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="647d4-130">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="647d4-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="647d4-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="647d4-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="647d4-132">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="647d4-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="647d4-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="647d4-134">Добавьте обработчик событий для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-134">Add an event handler for the SourceChanged event.</span></span>
[<span data-ttu-id="647d4-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="647d4-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="647d4-136">Добавьте обработчик событий для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="647d4-136">Add an event handler for the WebMessageReceived event.</span></span>
[<span data-ttu-id="647d4-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="647d4-138">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="647d4-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="647d4-140">Добавьте обработчик событий для события WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="647d4-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="647d4-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="647d4-142">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="647d4-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="647d4-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="647d4-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="647d4-144">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="647d4-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="647d4-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="647d4-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="647d4-146">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="647d4-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="647d4-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="647d4-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="647d4-148">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="647d4-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="647d4-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="647d4-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="647d4-150">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="647d4-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="647d4-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="647d4-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="647d4-152">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="647d4-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="647d4-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="647d4-154">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="647d4-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="647d4-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="647d4-156">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="647d4-156">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="647d4-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="647d4-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="647d4-158">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="647d4-158">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="647d4-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="647d4-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="647d4-160">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="647d4-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="647d4-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="647d4-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="647d4-162">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="647d4-162">The title for the current top level document.</span></span>
[<span data-ttu-id="647d4-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="647d4-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="647d4-164">Объект [ICoreWebView2Settings](icorewebview2settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="647d4-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="647d4-165">get_Source</span></span>](#get_source) | <span data-ttu-id="647d4-166">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="647d4-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="647d4-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="647d4-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="647d4-168">Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="647d4-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="647d4-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="647d4-169">GoBack</span></span>](#goback) | <span data-ttu-id="647d4-170">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="647d4-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="647d4-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="647d4-171">GoForward</span></span>](#goforward) | <span data-ttu-id="647d4-172">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="647d4-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="647d4-173">Которому</span><span class="sxs-lookup"><span data-stu-id="647d4-173">Navigate</span></span>](#navigate) | <span data-ttu-id="647d4-174">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="647d4-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="647d4-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="647d4-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="647d4-176">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="647d4-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="647d4-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="647d4-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="647d4-178">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="647d4-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="647d4-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="647d4-180">Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="647d4-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="647d4-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="647d4-182">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="647d4-183">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="647d4-183">Reload</span></span>](#reload) | <span data-ttu-id="647d4-184">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="647d4-184">Reload the current page.</span></span>
[<span data-ttu-id="647d4-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="647d4-186">Удалите обработчик событий, добавленный ранее add_ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-186">Remove an event handler previously added with add_ContainsFullScreenElementChanged.</span></span>
[<span data-ttu-id="647d4-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="647d4-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="647d4-188">Удалите обработчик событий, добавленный ранее add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="647d4-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="647d4-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="647d4-190">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="647d4-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="647d4-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="647d4-192">Удалите обработчик событий, добавленный ранее add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="647d4-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="647d4-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="647d4-194">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="647d4-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="647d4-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="647d4-196">Удалите обработчик событий, добавленный ранее add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="647d4-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="647d4-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="647d4-198">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="647d4-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="647d4-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="647d4-200">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="647d4-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="647d4-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="647d4-202">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="647d4-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="647d4-204">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="647d4-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="647d4-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="647d4-206">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="647d4-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="647d4-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="647d4-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="647d4-208">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="647d4-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="647d4-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="647d4-210">Удалите обработчик событий, добавленный ранее add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="647d4-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="647d4-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="647d4-212">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="647d4-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="647d4-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="647d4-214">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="647d4-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="647d4-216">Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="647d4-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="647d4-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="647d4-218">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="647d4-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="647d4-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="647d4-220">Удалите соответствующий сценарий JavaScript, который добавляется с использованием `AddScriptToExecuteOnDocumentCreated` указанного идентификатора сценария.</span><span class="sxs-lookup"><span data-stu-id="647d4-220">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>
[<span data-ttu-id="647d4-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="647d4-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="647d4-222">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="647d4-223">Stop</span><span class="sxs-lookup"><span data-stu-id="647d4-223">Stop</span></span>](#stop) | <span data-ttu-id="647d4-224">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="647d4-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="647d4-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="647d4-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="647d4-226">Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="647d4-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="647d4-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="647d4-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="647d4-228">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="647d4-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="647d4-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="647d4-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="647d4-230">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="647d4-230">Reason for moving focus.</span></span>
[<span data-ttu-id="647d4-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="647d4-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="647d4-232">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="647d4-232">The type of a permission request.</span></span>
[<span data-ttu-id="647d4-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="647d4-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="647d4-234">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="647d4-234">Response to a permission request.</span></span>
[<span data-ttu-id="647d4-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="647d4-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="647d4-236">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="647d4-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="647d4-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="647d4-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="647d4-238">Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="647d4-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="647d4-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="647d4-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="647d4-240">Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="647d4-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="647d4-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="647d4-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="647d4-242">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="647d4-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="647d4-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="647d4-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="647d4-244">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="647d4-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="647d4-245">Участников</span><span class="sxs-lookup"><span data-stu-id="647d4-245">Members</span></span>

#### <span data-ttu-id="647d4-246">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-246">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="647d4-247">Добавьте обработчик событий для события ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-247">Add an event handler for the ContainsFullScreenElementChanged event.</span></span>

> <span data-ttu-id="647d4-248">общедоступные значения HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-248">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-249">ContainsFullScreenElementChanged активируется при изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="647d4-249">ContainsFullScreenElementChanged fires when the ContainsFullScreenElement property changes.</span></span> <span data-ttu-id="647d4-250">Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран.</span><span class="sxs-lookup"><span data-stu-id="647d4-250">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="647d4-251">Это событие полезно, если, например, элемент видео запрашивается на весь экран.</span><span class="sxs-lookup"><span data-stu-id="647d4-251">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="647d4-252">Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.</span><span class="sxs-lookup"><span data-stu-id="647d4-252">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="647d4-253">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="647d4-253">add_ContentLoading</span></span> 

<span data-ttu-id="647d4-254">Добавьте обработчик событий для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="647d4-254">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="647d4-255">общедоступные значения HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-255">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-256">ContentLoading срабатывает перед загрузкой содержимого, включая сценарии, добавленные в AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="647d4-256">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="647d4-257">ContentLoading не срабатывает, если выполняется та же Навигация по страницам (например, с помощью навигации фрагментов или истории. pushState навигации).</span><span class="sxs-lookup"><span data-stu-id="647d4-257">ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="647d4-258">Это следует за событиями NavigationStarting и SourceChanged и предшествовать событиям HistoryChanged и NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-258">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="647d4-259">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-259">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="647d4-260">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-260">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="647d4-261">общедоступные значения HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-261">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-262">DocumentTitleChanged активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-262">DocumentTitleChanged fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="647d4-263">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="647d4-263">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="647d4-264">Добавьте обработчик событий для события FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-264">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="647d4-265">общедоступные значения HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-265">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-266">FrameNavigationCompleted активируется, когда дочерний кадр полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="647d4-266">FrameNavigationCompleted fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the FrameNavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    CHECK_FAILURE(m_webView->add_FrameNavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    std::wstring error_msg = WebErrorStatusToString(webErrorStatus);
                    MessageBox(nullptr,
                       (std::wstring(L"IFrame navigation failed with the ") +
                         L"give in error " + error_msg).c_str(),
                       L"Navigation Failure", MB_OK);
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_frameNavigationCompletedToken));
```

#### <span data-ttu-id="647d4-267">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="647d4-267">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="647d4-268">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="647d4-268">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="647d4-269">общедоступные значения HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-269">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-270">FrameNavigationStarting активируется, когда дочерний кадр в WebView запрашивает разрешение на переход к другому URI.</span><span class="sxs-lookup"><span data-stu-id="647d4-270">FrameNavigationStarting fires when a child frame in the WebView requests permission to navigate to a different URI.</span></span> <span data-ttu-id="647d4-271">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="647d4-271">This will fire for redirects as well.</span></span>

<span data-ttu-id="647d4-272">Соответствующие навигации можно блокировать до тех пор, пока обработчик событий не вернется.</span><span class="sxs-lookup"><span data-stu-id="647d4-272">Corresponding navigations can be blocked until the event handler returns.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### <span data-ttu-id="647d4-273">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-273">add_HistoryChanged</span></span> 

<span data-ttu-id="647d4-274">Добавьте обработчик событий для события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-274">Add an event handler for the HistoryChanged event.</span></span>

> <span data-ttu-id="647d4-275">общедоступные значения HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-275">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-276">HistoryChanged прослушивает изменение истории переходов для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="647d4-276">HistoryChanged listens to the change of navigation history for the top level document.</span></span> <span data-ttu-id="647d4-277">Используйте HistoryChanged, чтобы проверить, изменилось ли значение CanGoBack/CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="647d4-277">Use HistoryChanged to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="647d4-278">HistoryChanged также срабатывает для использования GoBack и GoForward.</span><span class="sxs-lookup"><span data-stu-id="647d4-278">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="647d4-279">HistoryChanged срабатывает после SourceChanged и ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="647d4-279">HistoryChanged fires after SourceChanged and ContentLoading.</span></span>

```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                m_toolbar->SetItemEnabled(Toolbar::Item_BackButton, canGoBack);
                m_toolbar->SetItemEnabled(Toolbar::Item_ForwardButton, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="647d4-280">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="647d4-280">add_NavigationCompleted</span></span> 

<span data-ttu-id="647d4-281">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-281">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="647d4-282">общедоступные значения HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-282">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-283">NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="647d4-283">NavigationCompleted fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
                m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="647d4-284">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="647d4-284">add_NavigationStarting</span></span> 

<span data-ttu-id="647d4-285">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="647d4-285">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="647d4-286">общедоступные значения HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-286">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-287">NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI.</span><span class="sxs-lookup"><span data-stu-id="647d4-287">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="647d4-288">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="647d4-288">This will fire for redirects as well.</span></span>

<span data-ttu-id="647d4-289">Соответствующие навигации можно блокировать до тех пор, пока обработчик событий не вернется.</span><span class="sxs-lookup"><span data-stu-id="647d4-289">Corresponding navigations can be blocked until the event handler returns.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
        }
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### <span data-ttu-id="647d4-290">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-290">add_NewWindowRequested</span></span> 

<span data-ttu-id="647d4-291">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-291">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="647d4-292">общедоступные значения HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-292">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-293">NewWindowRequested активируется, когда содержимое в WebView запрашивает, чтобы открыть новое окно, например с помощью Window. Open.</span><span class="sxs-lookup"><span data-stu-id="647d4-293">NewWindowRequested fires when content inside the WebView requests to open a new window, such as through window.open.</span></span> <span data-ttu-id="647d4-294">Приложение может передавать целевую WebView, которая будет считаться открытым окном.</span><span class="sxs-lookup"><span data-stu-id="647d4-294">The app can pass a target WebView that will be considered the opened window.</span></span>

<span data-ttu-id="647d4-295">Результаты сценариев в новом окне могут быть заблокированы до тех пор, пока обработчик событий не вернется в том случае, если для аргументов события не будет получено требование будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="647d4-295">Scripts resulted in the new window requested can be blocked until the event handler returns if a deferral is not taken on the event args.</span></span> <span data-ttu-id="647d4-296">Если выводится РБП, сценарии блокируются до тех пор, пока не будет завершена отсрочка.</span><span class="sxs-lookup"><span data-stu-id="647d4-296">If a deferral is taken, then scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));
                AppWindow* newAppWindow;

                wil::com_ptr<ICoreWebView2WindowFeatures> windowFeatures;
                CHECK_FAILURE(args->get_WindowFeatures(&windowFeatures));

                RECT windowRect = {0};
                UINT32 left = 0;
                UINT32 top = 0;
                UINT32 height = 0;
                UINT32 width = 0;
                BOOL shouldHaveToolbar = true;

                BOOL hasPosition = FALSE;
                BOOL hasSize = FALSE;
                CHECK_FAILURE(windowFeatures->HasPosition(&hasPosition));
                CHECK_FAILURE(windowFeatures->HasSize(&hasSize));

                bool useDefaultWindow = true;

                if (!!hasPosition && !!hasSize)
                {
                    CHECK_FAILURE(windowFeatures->get_Left(&left));
                    CHECK_FAILURE(windowFeatures->get_Top(&top));
                    CHECK_FAILURE(windowFeatures->get_Height(&height));
                    CHECK_FAILURE(windowFeatures->get_Width(&width));
                    useDefaultWindow = false;
                }
                CHECK_FAILURE(windowFeatures->get_Toolbar(&shouldHaveToolbar));

                windowRect.left = left;
                windowRect.right = left + (width < s_minNewWindowSize ? s_minNewWindowSize : width);
                windowRect.top = top;
                windowRect.bottom = top + (height < s_minNewWindowSize ? s_minNewWindowSize : height);

                if (!useDefaultWindow)
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"", false, nullptr, true, windowRect, !!shouldHaveToolbar);
                }
                else
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"");
                }
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="647d4-297">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-297">add_PermissionRequested</span></span> 

<span data-ttu-id="647d4-298">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-298">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="647d4-299">общедоступные значения HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-299">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-300">PermissionRequested активируется, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="647d4-300">PermissionRequested fires when content in a WebView requests permission to access some privileged resources.</span></span>

<span data-ttu-id="647d4-301">Если для аргументов события не используется РБП, последующие сценарии можно блокировать до тех пор, пока обработчик событий не вернется.</span><span class="sxs-lookup"><span data-stu-id="647d4-301">If a deferral is not taken on the event args, the subsequent scripts can be blocked until the event handler returns.</span></span> <span data-ttu-id="647d4-302">Если предпринимается отсрочка, сценарии блокируются до тех пор, пока не будет завершена отсрочка.</span><span class="sxs-lookup"><span data-stu-id="647d4-302">If a deferral is taken, then the scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        COREWEBVIEW2_PERMISSION_KIND kind = COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        COREWEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? COREWEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? COREWEBVIEW2_PERMISSION_STATE_DENY
            :                     COREWEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="647d4-303">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="647d4-303">add_ProcessFailed</span></span> 

<span data-ttu-id="647d4-304">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="647d4-304">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="647d4-305">общедоступные значения HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-305">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-306">ProcessFailed активируется, когда процесс WebView неожиданно завершает работу или перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="647d4-306">ProcessFailed fires when a WebView process is terminated unexpectedly or becomes unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        COREWEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process exited unexpectedly. Reload page?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                CHECK_FAILURE(m_webView->Reload());
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="647d4-307">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="647d4-307">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="647d4-308">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="647d4-308">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="647d4-309">общедоступные значения HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-309">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-310">ScriptDialogOpening активируется, когда диалоговое окно JavaScript (Alert, Confirm, Prompt или beforeunload) будет отображаться для WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-310">ScriptDialogOpening fires when a JavaScript dialog (alert, confirm, prompt, or beforeunload) will show for the webview.</span></span> <span data-ttu-id="647d4-311">Это событие срабатывает только в том случае, если свойству ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled задано значение false.</span><span class="sxs-lookup"><span data-stu-id="647d4-311">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="647d4-312">Событие ScriptDialogOpening можно использовать, чтобы подавить диалоговые окна или заменить диалоговые окна по умолчанию пользовательскими диалоговыми окноми.</span><span class="sxs-lookup"><span data-stu-id="647d4-312">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

<span data-ttu-id="647d4-313">Если для аргументов события не используется РБП, последующие сценарии можно блокировать до тех пор, пока обработчик событий не вернется.</span><span class="sxs-lookup"><span data-stu-id="647d4-313">If a deferral is not taken on the event args, the subsequent scripts can be blocked until the event handler returns.</span></span> <span data-ttu-id="647d4-314">Если предпринимается отсрочка, сценарии блокируются до тех пор, пока не будет завершена отсрочка.</span><span class="sxs-lookup"><span data-stu-id="647d4-314">If a deferral is taken, then the scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            COREWEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### <span data-ttu-id="647d4-315">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-315">add_SourceChanged</span></span> 

<span data-ttu-id="647d4-316">Добавьте обработчик событий для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-316">Add an event handler for the SourceChanged event.</span></span>

> <span data-ttu-id="647d4-317">общедоступные значения HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-317">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-318">SourceChanged активируется при изменении свойства Source.</span><span class="sxs-lookup"><span data-stu-id="647d4-318">SourceChanged fires when the Source property changes.</span></span> <span data-ttu-id="647d4-319">SourceChanged срабатывает для переходов на другой сайт или элементы навигации фрагментов.</span><span class="sxs-lookup"><span data-stu-id="647d4-319">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="647d4-320">Она не будет срабатывать для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="647d4-320">It will not fire for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="647d4-321">SourceChanged срабатывает перед ContentLoading для перехода к новому документу.</span><span class="sxs-lookup"><span data-stu-id="647d4-321">SourceChanged fires before ContentLoading for navigation to a new document.</span></span>

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="647d4-322">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="647d4-322">add_WebMessageReceived</span></span> 

<span data-ttu-id="647d4-323">Добавьте обработчик событий для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="647d4-323">Add an event handler for the WebMessageReceived event.</span></span>

> <span data-ttu-id="647d4-324">общедоступные значения HRESULT [add_WebMessageReceived](#add_webmessagereceived)(обработчик[ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-324">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-325">WebMessageReceived активируется, когда установлен параметр ICoreWebView2Settings:: IsWebMessageEnabled и документ верхнего уровня о WebViewных звонках `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="647d4-325">WebMessageReceived fires when the ICoreWebView2Settings::IsWebMessageEnabled setting is set and the top level document of the WebView calls `window.chrome.webview.postMessage`.</span></span> <span data-ttu-id="647d4-326">Функция i, в `void postMessage(object)` которой объект — это любой объект, поддерживаемый преобразованием JSON.</span><span class="sxs-lookup"><span data-stu-id="647d4-326">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```html
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```
 <span data-ttu-id="647d4-327">При вызове сообщения вызывается метод Invoke обработчика с параметром объекта i, преобразованным в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="647d4-327">When postMessage is called, the handler's Invoke method will be called with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="647d4-328">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-328">add_WebResourceRequested</span></span> 

<span data-ttu-id="647d4-329">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-329">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="647d4-330">общедоступные значения HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-330">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-331">WebResourceRequested активируется, когда WebView выполняет запрос URL-адреса к соответствующему URL-адресу и фильтру контекст ресурсов, добавленный в AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="647d4-331">WebResourceRequested fires when the WebView is performing a URL request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="647d4-332">Для срабатывания события необходимо добавить хотя бы один фильтр.</span><span class="sxs-lookup"><span data-stu-id="647d4-332">At least one filter must be added for the event to fire.</span></span>

<span data-ttu-id="647d4-333">Запрашиваемый веб-ресурс может быть заблокирован до тех пор, пока обработчик событий не вернется в том случае, если для аргументов события не будет получено значение расхода.</span><span class="sxs-lookup"><span data-stu-id="647d4-333">The web resource requested can be blocked until the event handler returns if a deferral is not taken on the event args.</span></span> <span data-ttu-id="647d4-334">Если вы закончите РБП, запрашиваемый веб-ресурс блокируется до тех пор, пока не будет завершена отсрочка.</span><span class="sxs-lookup"><span data-stu-id="647d4-334">If a deferral is taken, then the web resource requested is blocked until the deferral is completed.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="647d4-335">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-335">add_WindowCloseRequested</span></span> 

<span data-ttu-id="647d4-336">Добавьте обработчик событий для события WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-336">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="647d4-337">общедоступные значения HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="647d4-337">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647d4-338">WindowCloseRequested активируется, когда содержимое в WebView запрашивается, чтобы закрыть окно, например после вызова Window. Close.</span><span class="sxs-lookup"><span data-stu-id="647d4-338">WindowCloseRequested fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="647d4-339">Приложение должно закрыть окно WebView и связанное приложение, если это понятно приложению.</span><span class="sxs-lookup"><span data-stu-id="647d4-339">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>([this](
                                                                    ICoreWebView2* sender,
                                                                    IUnknown* args) {
            if (m_isPopupWindow)
            {
                CloseAppWindow();
            }
            return S_OK;
        }).Get(),
        nullptr));
```

#### <span data-ttu-id="647d4-340">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="647d4-340">AddHostObjectToScript</span></span> 

<span data-ttu-id="647d4-341">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="647d4-341">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="647d4-342">общедоступные значения HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(имя LPCWSTR, переменная \* объект)</span><span class="sxs-lookup"><span data-stu-id="647d4-342">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="647d4-343">Объекты узла предоставляются как прокси объекта hosts через `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="647d4-343">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="647d4-344">Прокси-серверы объектов являются обещанными и разрешаются в объект, представляющий объект Host.</span><span class="sxs-lookup"><span data-stu-id="647d4-344">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="647d4-345">Обещание отклонено, если приложение не добавило объект с именем.</span><span class="sxs-lookup"><span data-stu-id="647d4-345">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="647d4-346">Когда код JavaScript обращается к свойству или методу объекта, для него возвращается значение, которое будет обрабатываться в соответствии со значением, возвращенным из хоста для свойства или метода, или отброшено в случае ошибки, например, отсутствие такого свойства или метода для объекта или параметров недопустимым.</span><span class="sxs-lookup"><span data-stu-id="647d4-346">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="647d4-347">Например, когда код приложения делает следующее:</span><span class="sxs-lookup"><span data-stu-id="647d4-347">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="647d4-348">Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject:</span><span class="sxs-lookup"><span data-stu-id="647d4-348">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="647d4-349">Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="647d4-349">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="647d4-350">Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch.</span><span class="sxs-lookup"><span data-stu-id="647d4-350">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="647d4-351">Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID.</span><span class="sxs-lookup"><span data-stu-id="647d4-351">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="647d4-352">Вложенные массивы поддерживаются до 3 уровней.</span><span class="sxs-lookup"><span data-stu-id="647d4-352">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="647d4-353">Массивы по типам ссылок не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="647d4-353">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="647d4-354">VT_EMPTY и VT_NULL сопоставлены в JavaScript как null.</span><span class="sxs-lookup"><span data-stu-id="647d4-354">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="647d4-355">В JavaScript NULL и undefine сопоставляются с VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="647d4-355">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="647d4-356">Кроме того, все объекты узла предоставляются как `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="647d4-356">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="647d4-357">Здесь объекты узла предоставляются как синхронные прокси объектов узла.</span><span class="sxs-lookup"><span data-stu-id="647d4-357">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="647d4-358">Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста.</span><span class="sxs-lookup"><span data-stu-id="647d4-358">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="647d4-359">Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.hostObjects.<name>` описанный выше.</span><span class="sxs-lookup"><span data-stu-id="647d4-359">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="647d4-360">Синхронные прокси-серверы узлов и асинхронные прокси объектов узла могут обоим образом доявляться прокси для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="647d4-360">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="647d4-361">Удаленные изменения, внесенные одним прокси-сервером, будут отражаться на любом другом прокси того же объекта узла, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.</span><span class="sxs-lookup"><span data-stu-id="647d4-361">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="647d4-362">Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-362">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="647d4-363">При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="647d4-363">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="647d4-364">Прокси объектов узла — это прокси-объекты JavaScript, которые перехватывают все вызовы свойств Get, Set и Method.</span><span class="sxs-lookup"><span data-stu-id="647d4-364">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="647d4-365">Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="647d4-365">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="647d4-366">Кроме того, любое свойство или метод в массиве `chrome.webview.hostObjects.options.forceLocalProperties` также будет выполняться локально.</span><span class="sxs-lookup"><span data-stu-id="647d4-366">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="647d4-367">Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="647d4-367">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="647d4-368">При необходимости вы можете добавить в этот массив дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="647d4-368">You can add more to this array as required.</span></span>

<span data-ttu-id="647d4-369">Существует метод `chrome.webview.hostObjects.cleanupSome` , который наилучшим способом является сбор прокси объектов хоста сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="647d4-369">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="647d4-370">Прокси-серверы узла дополнительно обладают следующими методами, которые выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="647d4-370">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="647d4-371">applyHostFunction, getHostProperty, setHostProperty: выполняйте вызов метода, свойство get или свойство Set для объекта Host.</span><span class="sxs-lookup"><span data-stu-id="647d4-371">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="647d4-372">Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство.</span><span class="sxs-lookup"><span data-stu-id="647d4-372">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="647d4-373">Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="647d4-373">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="647d4-374">Но `proxy.applyHostFunction('toString')` выполняется `toString` вместо объекта прокси-сервера узла.</span><span class="sxs-lookup"><span data-stu-id="647d4-374">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="647d4-375">getLocalProperty, setLocalProperty: выполнение свойства Get или установка свойства локально.</span><span class="sxs-lookup"><span data-stu-id="647d4-375">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="647d4-376">Эти методы можно использовать, чтобы принудительно получить или задать свойство для прокси объекта основного приложения, а не для объекта узла, который он представляет.</span><span class="sxs-lookup"><span data-stu-id="647d4-376">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="647d4-377">Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из объекта прокси-сервера узла.</span><span class="sxs-lookup"><span data-stu-id="647d4-377">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="647d4-378">Но `proxy.getLocalProperty('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.</span><span class="sxs-lookup"><span data-stu-id="647d4-378">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="647d4-379">Sync: асинхронные прокси-серверы узлов предоставляют метод Sync, возвращающий обещание для прокси объекта хоста синхронный для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="647d4-379">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="647d4-380">Например, `chrome.webview.hostObjects.sample.methodCall()` возвращает асинхронный прокси объекта хоста.</span><span class="sxs-lookup"><span data-stu-id="647d4-380">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="647d4-381">Вы можете использовать этот `sync` метод, чтобы получить для него синхронный прокси-сервер объекта узла:</span><span class="sxs-lookup"><span data-stu-id="647d4-381">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="647d4-382">Async: синхронные прокси-серверы узлов предоставляют асинхронный метод, который блокирует и возвращает асинхронный прокси объекта хоста для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="647d4-382">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="647d4-383">Например, `chrome.webview.hostObjects.sync.sample.methodCall()` возвращает синхронный прокси объекта узла.</span><span class="sxs-lookup"><span data-stu-id="647d4-383">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="647d4-384">Вызов `async` метода на этих блоках и возврат прокси-сервера асинхронного объекта узла для того же объекта узла:</span><span class="sxs-lookup"><span data-stu-id="647d4-384">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="647d4-385">затем: асинхронные прокси-объекты узла имеют метод then.</span><span class="sxs-lookup"><span data-stu-id="647d4-385">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="647d4-386">Это позволит им доставлять ожидающие.</span><span class="sxs-lookup"><span data-stu-id="647d4-386">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="647d4-387">будет возвращать обещание, которое разрешается с представлением объекта Host.</span><span class="sxs-lookup"><span data-stu-id="647d4-387">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="647d4-388">Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально.</span><span class="sxs-lookup"><span data-stu-id="647d4-388">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="647d4-389">Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания.</span><span class="sxs-lookup"><span data-stu-id="647d4-389">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="647d4-390">Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве прокси объектов Host.</span><span class="sxs-lookup"><span data-stu-id="647d4-390">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="647d4-391">Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно.</span><span class="sxs-lookup"><span data-stu-id="647d4-391">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="647d4-392">Асинхронные прокси-объекты узла возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства.</span><span class="sxs-lookup"><span data-stu-id="647d4-392">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="647d4-393">Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции.</span><span class="sxs-lookup"><span data-stu-id="647d4-393">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="647d4-394">Синхронные прокси объекта узла работают одинаково, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.</span><span class="sxs-lookup"><span data-stu-id="647d4-394">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="647d4-395">Установка свойства для прокси-сервера асинхронного узла выполняется немного по-другому.</span><span class="sxs-lookup"><span data-stu-id="647d4-395">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="647d4-396">Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано.</span><span class="sxs-lookup"><span data-stu-id="647d4-396">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="647d4-397">Это требование для прокси-объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-397">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="647d4-398">Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setHostProperty, который возвращает обещание, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="647d4-398">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="647d4-399">Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.</span><span class="sxs-lookup"><span data-stu-id="647d4-399">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="647d4-400">Например, предположим, что у вас есть COM-объект со следующим интерфейсом</span><span class="sxs-lookup"><span data-stu-id="647d4-400">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IHostObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        [propget] HRESULT IndexedProperty(INT index, [out, retval] BSTR * stringResult);
        [propput] HRESULT IndexedProperty(INT index, [in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);

    };
```
 <span data-ttu-id="647d4-401">Мы можем добавить экземпляр этого интерфейса в наш сценарий JavaScript `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="647d4-401">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="647d4-402">В этом случае мы присвойте ему имя `sample` :</span><span class="sxs-lookup"><span data-stu-id="647d4-402">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_hostObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddHostObjectToScript multiple times in a row without
            // calling RemoveHostObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(
                m_webView->AddHostObjectToScript(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```
 <span data-ttu-id="647d4-403">Затем в HTML-документе мы можем использовать этот COM-объект через `chrome.webview.hostObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="647d4-403">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

```html
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = await chrome.webview.hostObjects.sample.property;
        document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
        const propertyValue = chrome.webview.hostObjects.sync.sample.property;
        document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyAsyncInput").value;
        // The following line will work but it will return immediately before the property value has actually been set.
        // If you need to set the property and wait for the property to change value, use the setHostProperty function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setHostProperty function.
        await chrome.webview.hostObjects.sample.setHostProperty("property", propertyValue);
        document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
        const propertyValue = document.getElementById("setPropertySyncInput").value;
        chrome.webview.hostObjects.sync.sample.property = propertyValue;
        document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("getIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("getIndexedPropertyAsyncParam").value);
        const resultValue = await chrome.webview.hostObjects.sample.IndexedProperty[index];
        document.getElementById("getIndexedPropertyAsyncOutput").textContent = resultValue;
        });
        document.getElementById("setIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("setIndexedPropertyAsyncParam1").value);
        const value = document.getElementById("setIndexedPropertyAsyncParam2").value;;
        chrome.webview.hostObjects.sample.IndexedProperty[index] = value;
        document.getElementById("setIndexedPropertyAsyncOutput").textContent = "Set";
        });
        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
        const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
        const resultValue = await chrome.webview.hostObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
        const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
        const resultValue = chrome.webview.hostObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
        chrome.webview.hostObjects.sample.CallCallbackAsynchronously(() => {
        document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
        });
        });
```
<span data-ttu-id="647d4-404">Предоставление доступа к объектам узла для сценария имеет угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="647d4-404">Exposing host objects to script has security risk.</span></span> <span data-ttu-id="647d4-405">Пожалуйста, [следуйте рекомендациям](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span><span class="sxs-lookup"><span data-stu-id="647d4-405">Please follow [best practices](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span></span>

#### <span data-ttu-id="647d4-406">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="647d4-406">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="647d4-407">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="647d4-407">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="647d4-408">общедоступные значения HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="647d4-408">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="647d4-409">Этот метод вставляет сценарий, который запускается на всех документах верхнего уровня и дочерних переходах между страницами фреймов.</span><span class="sxs-lookup"><span data-stu-id="647d4-409">This method injects a script that runs on all top-level document and child frame page navigations.</span></span> <span data-ttu-id="647d4-410">Этот метод выполняется асинхронно, и вы должны дождаться завершения обработчика завершения перед тем, как вставленный сценарий будет готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="647d4-410">This method runs asynchronously, and you must wait for the completion handler to finish before the injected script is ready to run.</span></span> <span data-ttu-id="647d4-411">Когда этот метод завершает работу, метод обработчика `Invoke` вызывается с использованием `id` вставленного сценария.</span><span class="sxs-lookup"><span data-stu-id="647d4-411">When this method completes, the handler's `Invoke` method is called with the `id` of the injected script.</span></span> `id` <span data-ttu-id="647d4-412">является строкой.</span><span class="sxs-lookup"><span data-stu-id="647d4-412">is a string.</span></span> <span data-ttu-id="647d4-413">Чтобы удалить вставленный сценарий, используйте `RemoveScriptToExecuteOnDocumentCreated` .</span><span class="sxs-lookup"><span data-stu-id="647d4-413">To remove the injected script, use `RemoveScriptToExecuteOnDocumentCreated`.</span></span>

<span data-ttu-id="647d4-414">Обратите внимание, что если в HTML-документе есть изолированная [Среда с определенными свойствами или](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [заголовок HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , это повлияет на выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="647d4-414">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="647d4-415">Таким образом, например, если ключевое слово "Allow-Modal" не задано, вызовы `alert` функции будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="647d4-415">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="647d4-416">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="647d4-416">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="647d4-417">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="647d4-417">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="647d4-418">общедоступный HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="647d4-418">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="647d4-419">Параметр URI может быть строкой с подстановочными знаками ("\*": ноль или более, "?": только один).</span><span class="sxs-lookup"><span data-stu-id="647d4-419">The URI parameter can be a wildcard string ('\*': zero or more, '?': exactly one).</span></span> <span data-ttu-id="647d4-420">nullptr эквивалентен L "".</span><span class="sxs-lookup"><span data-stu-id="647d4-420">nullptr is equivalent to L"".</span></span> <span data-ttu-id="647d4-421">Описание фильтров контекста ресурсов приведено в разделе COREWEBVIEW2_WEB_RESOURCE_CONTEXT перечисление.</span><span class="sxs-lookup"><span data-stu-id="647d4-421">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="647d4-422">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="647d4-422">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="647d4-423">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="647d4-423">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="647d4-424">общедоступные значения HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="647d4-424">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="647d4-425">Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="647d4-425">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="647d4-426">Параметр methodName — это полное имя метода в формате `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="647d4-426">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="647d4-427">Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода.</span><span class="sxs-lookup"><span data-stu-id="647d4-427">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="647d4-428">Метод Invoke обработчика вызывается, когда метод асинхронно завершается.</span><span class="sxs-lookup"><span data-stu-id="647d4-428">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="647d4-429">Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="647d4-429">Invoke will be called with the method's return object as a JSON string.</span></span>

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="647d4-430">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="647d4-430">CapturePreview</span></span> 

<span data-ttu-id="647d4-431">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="647d4-431">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="647d4-432">Public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="647d4-432">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="647d4-433">Укажите формат изображения с помощью параметра imageFormat.</span><span class="sxs-lookup"><span data-stu-id="647d4-433">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="647d4-434">Результирующие двоичные данные изображения записываются в указанный параметр imageStream.</span><span class="sxs-lookup"><span data-stu-id="647d4-434">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="647d4-435">Когда CapturePreview закончит запись в поток, вызывается метод Invoke в указанном параметре обработчика.</span><span class="sxs-lookup"><span data-stu-id="647d4-435">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="647d4-436">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="647d4-436">ExecuteScript</span></span> 

<span data-ttu-id="647d4-437">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-437">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="647d4-438">общедоступные значения HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="647d4-438">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="647d4-439">Это выполняется асинхронно и по завершении, если обработчик предоставлен в параметре ExecuteScriptCompletedHandler, вызывается его метод Invoke с результатом вычисления предоставленного JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-439">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="647d4-440">Результирующее значение — это строка в кодировке JSON.</span><span class="sxs-lookup"><span data-stu-id="647d4-440">The result value is a JSON encoded string.</span></span> <span data-ttu-id="647d4-441">Если результат не определен, содержит цикл ссылки или не может быть закодирован в JSON, значение NULL JSON будет возвращено в виде строки null.</span><span class="sxs-lookup"><span data-stu-id="647d4-441">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="647d4-442">Обратите внимание, что функция без явного возвращаемого значения возвращает значение undefine.</span><span class="sxs-lookup"><span data-stu-id="647d4-442">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="647d4-443">Если выполняемый сценарий создает необработанное исключение, результат также равен null.</span><span class="sxs-lookup"><span data-stu-id="647d4-443">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="647d4-444">Этот метод применяется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="647d4-444">This method is applied asynchronously.</span></span> <span data-ttu-id="647d4-445">Если метод вызывается после события NavigationStarting во время навигации, сценарий будет выполнен в новом документе при его загрузке, вокруг которого возникает время ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="647d4-445">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="647d4-446">ExecuteScript будет работать даже в том случае, если ICoreWebView2Settings:: IsScriptEnabled имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="647d4-446">ExecuteScript will work even if ICoreWebView2Settings::IsScriptEnabled is set to FALSE.</span></span>

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### <span data-ttu-id="647d4-447">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="647d4-447">get_BrowserProcessId</span></span> 

<span data-ttu-id="647d4-448">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-448">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="647d4-449">общедоступные значения HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="647d4-449">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="647d4-450">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="647d4-450">get_CanGoBack</span></span> 

<span data-ttu-id="647d4-451">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="647d4-451">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="647d4-452">общедоступные значения HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="647d4-452">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="647d4-453">Событие HistoryChanged будет срабатывать, если CanGoBack изменит значение.</span><span class="sxs-lookup"><span data-stu-id="647d4-453">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="647d4-454">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="647d4-454">get_CanGoForward</span></span> 

<span data-ttu-id="647d4-455">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="647d4-455">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="647d4-456">общедоступные значения HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="647d4-456">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="647d4-457">Событие HistoryChanged будет срабатывать, если CanGoForward изменит значение.</span><span class="sxs-lookup"><span data-stu-id="647d4-457">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="647d4-458">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="647d4-458">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="647d4-459">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="647d4-459">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="647d4-460">общедоступные значения HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="647d4-460">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="647d4-461">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="647d4-461">get_DocumentTitle</span></span> 

<span data-ttu-id="647d4-462">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="647d4-462">The title for the current top level document.</span></span>

> <span data-ttu-id="647d4-463">общедоступные значения HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="647d4-463">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="647d4-464">Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.</span><span class="sxs-lookup"><span data-stu-id="647d4-464">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="647d4-465">get_Settings</span><span class="sxs-lookup"><span data-stu-id="647d4-465">get_Settings</span></span> 

<span data-ttu-id="647d4-466">Объект [ICoreWebView2Settings](icorewebview2settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-466">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="647d4-467">общедоступные значения HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \* \* параметры)</span><span class="sxs-lookup"><span data-stu-id="647d4-467">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="647d4-468">get_Source</span><span class="sxs-lookup"><span data-stu-id="647d4-468">get_Source</span></span> 

<span data-ttu-id="647d4-469">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="647d4-469">The URI of the current top level document.</span></span>

> <span data-ttu-id="647d4-470">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="647d4-470">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="647d4-471">Это значение может изменяться в рамках обработки события SourceChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту.</span><span class="sxs-lookup"><span data-stu-id="647d4-471">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="647d4-472">Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="647d4-472">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="647d4-473">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="647d4-473">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="647d4-474">Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="647d4-474">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="647d4-475">общедоступные значения HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* ресивер)</span><span class="sxs-lookup"><span data-stu-id="647d4-475">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="647d4-476">Параметр eventName — это полное имя события в формате `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="647d4-476">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="647d4-477">Список событий протоколов DevTools и аргументов событий можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="647d4-477">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="647d4-478">GoBack</span><span class="sxs-lookup"><span data-stu-id="647d4-478">GoBack</span></span> 

<span data-ttu-id="647d4-479">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="647d4-479">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="647d4-480">общедоступное значение HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="647d4-480">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="647d4-481">GoForward</span><span class="sxs-lookup"><span data-stu-id="647d4-481">GoForward</span></span> 

<span data-ttu-id="647d4-482">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="647d4-482">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="647d4-483">общедоступные значения HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="647d4-483">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="647d4-484">Которому</span><span class="sxs-lookup"><span data-stu-id="647d4-484">Navigate</span></span> 

<span data-ttu-id="647d4-485">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="647d4-485">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="647d4-486">общедоступное значение HRESULT [навигации](#navigate)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="647d4-486">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="647d4-487">Дополнительные сведения приведены в разделе события навигации.</span><span class="sxs-lookup"><span data-stu-id="647d4-487">See the navigation events for more information.</span></span> <span data-ttu-id="647d4-488">Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.</span><span class="sxs-lookup"><span data-stu-id="647d4-488">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(GetAddressBar());
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(GetAddressBar(), buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
}
```

#### <span data-ttu-id="647d4-489">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="647d4-489">NavigateToString</span></span> 

<span data-ttu-id="647d4-490">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="647d4-490">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="647d4-491">общедоступные значения HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="647d4-491">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="647d4-492">Параметр htmlContent не может быть больше 2 МБ в полном размере.</span><span class="sxs-lookup"><span data-stu-id="647d4-492">The htmlContent parameter may not be larger than 2 MB in total size.</span></span> <span data-ttu-id="647d4-493">В качестве источника новой страницы будет указано пустое значение.</span><span class="sxs-lookup"><span data-stu-id="647d4-493">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="647d4-494">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="647d4-494">OpenDevToolsWindow</span></span> 

<span data-ttu-id="647d4-495">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-495">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="647d4-496">общедоступные значения HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="647d4-496">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="647d4-497">Ничего не происходит, если он вызывается, когда окно DevTools уже открыто.</span><span class="sxs-lookup"><span data-stu-id="647d4-497">Does nothing if called when the DevTools window is already open.</span></span>

#### <span data-ttu-id="647d4-498">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="647d4-498">PostWebMessageAsJson</span></span> 

<span data-ttu-id="647d4-499">Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-499">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="647d4-500">общедоступные значения HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="647d4-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="647d4-501">Срабатывает событие Window. Chrome. WebView для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="647d4-501">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="647d4-502">JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий:</span><span class="sxs-lookup"><span data-stu-id="647d4-502">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="647d4-503">Аргументы события представляют собой экземпляр `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="647d4-503">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="647d4-504">Параметр ICoreWebView2Settings:: IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="647d4-504">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="647d4-505">Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-505">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="647d4-506">Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект.</span><span class="sxs-lookup"><span data-stu-id="647d4-506">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="647d4-507">Сведения об отправке сообщений из HTML-документа WebView на узел можно найти в разделе add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="647d4-507">See add_WebMessageReceived for information on sending messages from the HTML document in the WebView to the host.</span></span> <span data-ttu-id="647d4-508">Это сообщение отправляется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="647d4-508">This message is sent asynchronously.</span></span> <span data-ttu-id="647d4-509">Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.</span><span class="sxs-lookup"><span data-stu-id="647d4-509">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="647d4-510">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="647d4-510">PostWebMessageAsString</span></span> 

<span data-ttu-id="647d4-511">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-511">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="647d4-512">общедоступные значения HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="647d4-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="647d4-513">Это выполняется точно так же, как и PostWebMessageAsJson, но `window.chrome.webview` свойство Data события ARG имеет строковое значение с тем же значением, что и webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="647d4-513">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="647d4-514">Используйте это вместо PostWebMessageAsJson, если вы хотите общаться с помощью простых строк, а не объектов JSON.</span><span class="sxs-lookup"><span data-stu-id="647d4-514">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="647d4-515">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="647d4-515">Reload</span></span> 

<span data-ttu-id="647d4-516">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="647d4-516">Reload the current page.</span></span>

> <span data-ttu-id="647d4-517">общедоступная [Перезагрузка](#reload)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="647d4-517">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="647d4-518">Это похоже на то, что переход к URI текущего документа верхнего уровня, включая все события навигации, которые обрабатывались, и учитывает любые записи в кэше HTTP.</span><span class="sxs-lookup"><span data-stu-id="647d4-518">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="647d4-519">Но история «назад» и «вперед» не будет изменена.</span><span class="sxs-lookup"><span data-stu-id="647d4-519">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="647d4-520">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-520">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="647d4-521">Удалите обработчик событий, добавленный ранее add_ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-521">Remove an event handler previously added with add_ContainsFullScreenElementChanged.</span></span>

> <span data-ttu-id="647d4-522">общедоступные значения HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-522">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-523">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="647d4-523">remove_ContentLoading</span></span> 

<span data-ttu-id="647d4-524">Удалите обработчик событий, добавленный ранее add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="647d4-524">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="647d4-525">общедоступные значения HRESULT [remove_ContentLoading](#remove_contentloading)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-525">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-526">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-526">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="647d4-527">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-527">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="647d4-528">общедоступные значения HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-528">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-529">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="647d4-529">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="647d4-530">Удалите обработчик событий, добавленный ранее add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-530">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="647d4-531">общедоступные значения HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-531">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-532">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="647d4-532">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="647d4-533">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="647d4-533">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="647d4-534">общедоступные значения HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-534">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-535">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-535">remove_HistoryChanged</span></span> 

<span data-ttu-id="647d4-536">Удалите обработчик событий, добавленный ранее add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-536">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="647d4-537">общедоступные значения HRESULT [remove_HistoryChanged](#remove_historychanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-537">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-538">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="647d4-538">remove_NavigationCompleted</span></span> 

<span data-ttu-id="647d4-539">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="647d4-539">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="647d4-540">общедоступные значения HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-540">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-541">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="647d4-541">remove_NavigationStarting</span></span> 

<span data-ttu-id="647d4-542">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="647d4-542">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="647d4-543">общедоступные значения HRESULT [remove_NavigationStarting](#remove_navigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-543">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-544">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-544">remove_NewWindowRequested</span></span> 

<span data-ttu-id="647d4-545">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-545">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="647d4-546">общедоступные значения HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-546">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-547">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-547">remove_PermissionRequested</span></span> 

<span data-ttu-id="647d4-548">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-548">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="647d4-549">общедоступные значения HRESULT [remove_PermissionRequested](#remove_permissionrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-549">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-550">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="647d4-550">remove_ProcessFailed</span></span> 

<span data-ttu-id="647d4-551">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="647d4-551">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="647d4-552">общедоступные значения HRESULT [remove_ProcessFailed](#remove_processfailed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-552">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-553">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="647d4-553">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="647d4-554">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="647d4-554">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="647d4-555">общедоступные значения HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-555">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-556">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="647d4-556">remove_SourceChanged</span></span> 

<span data-ttu-id="647d4-557">Удалите обработчик событий, добавленный ранее add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="647d4-557">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="647d4-558">общедоступные значения HRESULT [remove_SourceChanged](#remove_sourcechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-558">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-559">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="647d4-559">remove_WebMessageReceived</span></span> 

<span data-ttu-id="647d4-560">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="647d4-560">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="647d4-561">общедоступные значения HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-561">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-562">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-562">remove_WebResourceRequested</span></span> 

<span data-ttu-id="647d4-563">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-563">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="647d4-564">общедоступные значения HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-564">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-565">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="647d4-565">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="647d4-566">Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-566">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="647d4-567">общедоступные значения HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="647d4-567">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647d4-568">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="647d4-568">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="647d4-569">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-569">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="647d4-570">общедоступное значение HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="647d4-570">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="647d4-571">Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="647d4-571">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="647d4-572">Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="647d4-572">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="647d4-573">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="647d4-573">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="647d4-574">Удалите соответствующий сценарий JavaScript, который добавляется с использованием `AddScriptToExecuteOnDocumentCreated` указанного идентификатора сценария.</span><span class="sxs-lookup"><span data-stu-id="647d4-574">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>

> <span data-ttu-id="647d4-575">общедоступные значения HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="647d4-575">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="647d4-576">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="647d4-576">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="647d4-577">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="647d4-577">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="647d4-578">общедоступный HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="647d4-578">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="647d4-579">Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного.</span><span class="sxs-lookup"><span data-stu-id="647d4-579">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="647d4-580">Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.</span><span class="sxs-lookup"><span data-stu-id="647d4-580">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="647d4-581">Stop</span><span class="sxs-lookup"><span data-stu-id="647d4-581">Stop</span></span> 

<span data-ttu-id="647d4-582">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="647d4-582">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="647d4-583">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="647d4-583">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="647d4-584">Не останавливает сценарии.</span><span class="sxs-lookup"><span data-stu-id="647d4-584">Does not stop scripts.</span></span>

#### <span data-ttu-id="647d4-585">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="647d4-585">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="647d4-586">Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="647d4-586">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="647d4-587">[COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-587">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="647d4-588">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-588">Values</span></span>                         | <span data-ttu-id="647d4-589">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-589">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-590">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="647d4-590">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="647d4-591">Формат изображения PNG.</span><span class="sxs-lookup"><span data-stu-id="647d4-591">PNG image format.</span></span>
<span data-ttu-id="647d4-592">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="647d4-592">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="647d4-593">Формат изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="647d4-593">JPEG image format.</span></span>

#### <span data-ttu-id="647d4-594">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="647d4-594">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="647d4-595">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="647d4-595">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="647d4-596">[COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-596">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="647d4-597">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-597">Values</span></span>                         | <span data-ttu-id="647d4-598">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-598">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-599">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="647d4-599">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="647d4-600">ВыWM_KEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="647d4-600">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="647d4-601">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="647d4-601">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="647d4-602">ВыWM_KEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="647d4-602">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="647d4-603">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="647d4-603">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="647d4-604">ВыWM_SYSKEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="647d4-604">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="647d4-605">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="647d4-605">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="647d4-606">ВыWM_SYSKEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="647d4-606">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="647d4-607">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="647d4-607">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="647d4-608">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="647d4-608">Reason for moving focus.</span></span>

> <span data-ttu-id="647d4-609">[COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-609">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="647d4-610">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-610">Values</span></span>                         | <span data-ttu-id="647d4-611">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-611">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-612">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="647d4-612">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="647d4-613">Настройка кода фокуса на WebView.</span><span class="sxs-lookup"><span data-stu-id="647d4-613">Code setting focus into WebView.</span></span>
<span data-ttu-id="647d4-614">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="647d4-614">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="647d4-615">Перемещение фокуса из-за прохождения вкладки вперед.</span><span class="sxs-lookup"><span data-stu-id="647d4-615">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="647d4-616">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="647d4-616">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="647d4-617">Перемещение фокуса из-за перемещения по табуляции назад.</span><span class="sxs-lookup"><span data-stu-id="647d4-617">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="647d4-618">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="647d4-618">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="647d4-619">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="647d4-619">The type of a permission request.</span></span>

> <span data-ttu-id="647d4-620">[COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-620">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="647d4-621">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-621">Values</span></span>                         | <span data-ttu-id="647d4-622">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-622">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-623">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="647d4-623">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="647d4-624">Неизвестное разрешение.</span><span class="sxs-lookup"><span data-stu-id="647d4-624">Unknown permission.</span></span>
<span data-ttu-id="647d4-625">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="647d4-625">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="647d4-626">Разрешение на запись звука.</span><span class="sxs-lookup"><span data-stu-id="647d4-626">Permission to capture audio.</span></span>
<span data-ttu-id="647d4-627">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="647d4-627">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="647d4-628">Разрешение на захват видео.</span><span class="sxs-lookup"><span data-stu-id="647d4-628">Permission to capture video.</span></span>
<span data-ttu-id="647d4-629">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="647d4-629">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="647d4-630">Разрешение на доступ к географической позиции.</span><span class="sxs-lookup"><span data-stu-id="647d4-630">Permission to access geolocation.</span></span>
<span data-ttu-id="647d4-631">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="647d4-631">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="647d4-632">Разрешение на отправку веб-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="647d4-632">Permission to send web notifications.</span></span>
<span data-ttu-id="647d4-633">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="647d4-633">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="647d4-634">Разрешение на доступ к универсальному датчику.</span><span class="sxs-lookup"><span data-stu-id="647d4-634">Permission to access generic sensor.</span></span>
<span data-ttu-id="647d4-635">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="647d4-635">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="647d4-636">Разрешение на чтение системного буфера обмена без жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="647d4-636">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="647d4-637">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="647d4-637">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="647d4-638">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="647d4-638">Response to a permission request.</span></span>

> <span data-ttu-id="647d4-639">[COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-639">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="647d4-640">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-640">Values</span></span>                         | <span data-ttu-id="647d4-641">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-641">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-642">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="647d4-642">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="647d4-643">Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.</span><span class="sxs-lookup"><span data-stu-id="647d4-643">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="647d4-644">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="647d4-644">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="647d4-645">Предоставьте разрешение на запрос.</span><span class="sxs-lookup"><span data-stu-id="647d4-645">Grant the permission request.</span></span>
<span data-ttu-id="647d4-646">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="647d4-646">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="647d4-647">Отказ от запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="647d4-647">Deny the permission request.</span></span>

#### <span data-ttu-id="647d4-648">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="647d4-648">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="647d4-649">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="647d4-649">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="647d4-650">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="647d4-650">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="647d4-651">Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="647d4-651">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="647d4-652">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="647d4-652">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="647d4-653">Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="647d4-653">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="647d4-654">[COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-654">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="647d4-655">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-655">Values</span></span>                         | <span data-ttu-id="647d4-656">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-656">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-657">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="647d4-657">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="647d4-658">Указывает, что процесс браузера неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="647d4-658">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="647d4-659">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="647d4-659">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="647d4-660">Указывает, что процесс обработки неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="647d4-660">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="647d4-661">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="647d4-661">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="647d4-662">Указывает на то, что процесс рендеринга перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="647d4-662">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="647d4-663">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="647d4-663">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="647d4-664">Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="647d4-664">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="647d4-665">[COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-665">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="647d4-666">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-666">Values</span></span>                         | <span data-ttu-id="647d4-667">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-668">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="647d4-668">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="647d4-669">Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-669">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="647d4-670">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="647d4-670">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="647d4-671">Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-671">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="647d4-672">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="647d4-672">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="647d4-673">Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="647d4-673">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="647d4-674">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="647d4-674">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="647d4-675">Диалоговое окно, вызываемое с помощью события JavaScript beforeunload.</span><span class="sxs-lookup"><span data-stu-id="647d4-675">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="647d4-676">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="647d4-676">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="647d4-677">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="647d4-677">Error status values for web navigations.</span></span>

> <span data-ttu-id="647d4-678">[COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-678">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="647d4-679">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-679">Values</span></span>                         | <span data-ttu-id="647d4-680">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-680">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-681">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="647d4-681">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="647d4-682">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="647d4-682">An unknown error occurred.</span></span>
<span data-ttu-id="647d4-683">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="647d4-683">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="647d4-684">Общее имя сертификата SSL не совпадает с веб-адресом.</span><span class="sxs-lookup"><span data-stu-id="647d4-684">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="647d4-685">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="647d4-685">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="647d4-686">Срок действия сертификата SSL истек.</span><span class="sxs-lookup"><span data-stu-id="647d4-686">The SSL certificate has expired.</span></span>
<span data-ttu-id="647d4-687">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="647d4-687">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="647d4-688">SSL-сертификат клиента включает ошибки.</span><span class="sxs-lookup"><span data-stu-id="647d4-688">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="647d4-689">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="647d4-689">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="647d4-690">SSL-сертификат отозван.</span><span class="sxs-lookup"><span data-stu-id="647d4-690">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="647d4-691">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="647d4-691">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="647d4-692">Недопустимый сертификат SSL &ndash; это может означать, что сертификат не соответствует ПИН-контактам открытого ключа для имени узла. сертификат подписан недоверенным центром или с использованием слабого алгоритма, который нарушает ограничения на имена, сертификат содержит слабый ключ, срок действия сертификата является слишком длинным, не хватает сведений об отзыве или механизме отзыва, неоднозначное имя узла, отсутствие сведений о прозрачности сертификата, или сертификат связан с [прежним корнем Symantec](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span><span class="sxs-lookup"><span data-stu-id="647d4-692">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="647d4-693">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="647d4-693">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="647d4-694">Узел недостижим.</span><span class="sxs-lookup"><span data-stu-id="647d4-694">The host is unreachable.</span></span>
<span data-ttu-id="647d4-695">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="647d4-695">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="647d4-696">Время ожидания соединения истекло.</span><span class="sxs-lookup"><span data-stu-id="647d4-696">The connection has timed out.</span></span>
<span data-ttu-id="647d4-697">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="647d4-697">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="647d4-698">Сервер вернул недопустимый или нераспознанный ответ.</span><span class="sxs-lookup"><span data-stu-id="647d4-698">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="647d4-699">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="647d4-699">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="647d4-700">Соединение было прервано.</span><span class="sxs-lookup"><span data-stu-id="647d4-700">The connection was aborted.</span></span>
<span data-ttu-id="647d4-701">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="647d4-701">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="647d4-702">Подключение было сброшено.</span><span class="sxs-lookup"><span data-stu-id="647d4-702">The connection was reset.</span></span>
<span data-ttu-id="647d4-703">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="647d4-703">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="647d4-704">Соединение с Интернетом разорвано.</span><span class="sxs-lookup"><span data-stu-id="647d4-704">The Internet connection has been lost.</span></span>
<span data-ttu-id="647d4-705">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="647d4-705">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="647d4-706">Не удается подключиться к конечному объекту.</span><span class="sxs-lookup"><span data-stu-id="647d4-706">Cannot connect to destination.</span></span>
<span data-ttu-id="647d4-707">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="647d4-707">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="647d4-708">Не удалось разрешить указанное имя узла.</span><span class="sxs-lookup"><span data-stu-id="647d4-708">Could not resolve provided host name.</span></span>
<span data-ttu-id="647d4-709">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="647d4-709">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="647d4-710">Операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="647d4-710">The operation was canceled.</span></span>
<span data-ttu-id="647d4-711">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="647d4-711">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="647d4-712">Перенаправление запроса завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="647d4-712">The request redirect failed.</span></span>
<span data-ttu-id="647d4-713">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="647d4-713">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="647d4-714">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="647d4-714">An unexpected error occurred.</span></span>

#### <span data-ttu-id="647d4-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="647d4-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="647d4-716">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="647d4-716">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="647d4-717">[COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) перечисления</span><span class="sxs-lookup"><span data-stu-id="647d4-717">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="647d4-718">Данные</span><span class="sxs-lookup"><span data-stu-id="647d4-718">Values</span></span>                         | <span data-ttu-id="647d4-719">Описания</span><span class="sxs-lookup"><span data-stu-id="647d4-719">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="647d4-720">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="647d4-720">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="647d4-721">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="647d4-721">All resources.</span></span>
<span data-ttu-id="647d4-722">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="647d4-722">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="647d4-723">Ресурсы документов.</span><span class="sxs-lookup"><span data-stu-id="647d4-723">Document resources.</span></span>
<span data-ttu-id="647d4-724">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="647d4-724">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="647d4-725">Ресурсы CSS.</span><span class="sxs-lookup"><span data-stu-id="647d4-725">CSS resources.</span></span>
<span data-ttu-id="647d4-726">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="647d4-726">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="647d4-727">Графические ресурсы.</span><span class="sxs-lookup"><span data-stu-id="647d4-727">Image resources.</span></span>
<span data-ttu-id="647d4-728">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="647d4-728">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="647d4-729">Другие мультимедийные ресурсы, например видео.</span><span class="sxs-lookup"><span data-stu-id="647d4-729">Other media resources such as videos.</span></span>
<span data-ttu-id="647d4-730">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="647d4-730">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="647d4-731">Ресурсы шрифта.</span><span class="sxs-lookup"><span data-stu-id="647d4-731">Font resources.</span></span>
<span data-ttu-id="647d4-732">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="647d4-732">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="647d4-733">Ресурсы сценария.</span><span class="sxs-lookup"><span data-stu-id="647d4-733">Script resources.</span></span>
<span data-ttu-id="647d4-734">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="647d4-734">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="647d4-735">HTTP-запросы.</span><span class="sxs-lookup"><span data-stu-id="647d4-735">XML HTTP requests.</span></span>
<span data-ttu-id="647d4-736">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="647d4-736">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="647d4-737">Получение взаимодействия API.</span><span class="sxs-lookup"><span data-stu-id="647d4-737">Fetch API communication.</span></span>
<span data-ttu-id="647d4-738">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="647d4-738">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="647d4-739">TextTrack ресурсы.</span><span class="sxs-lookup"><span data-stu-id="647d4-739">TextTrack resources.</span></span>
<span data-ttu-id="647d4-740">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="647d4-740">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="647d4-741">Взаимодействие API EventSource.</span><span class="sxs-lookup"><span data-stu-id="647d4-741">EventSource API communication.</span></span>
<span data-ttu-id="647d4-742">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="647d4-742">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="647d4-743">Взаимодействие API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="647d4-743">WebSocket API communication.</span></span>
<span data-ttu-id="647d4-744">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="647d4-744">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="647d4-745">Манифесты веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="647d4-745">Web App Manifests.</span></span>
<span data-ttu-id="647d4-746">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="647d4-746">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="647d4-747">Обмен подписанными HTTP-сообщениями.</span><span class="sxs-lookup"><span data-stu-id="647d4-747">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="647d4-748">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="647d4-748">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="647d4-749">Запросы ping.</span><span class="sxs-lookup"><span data-stu-id="647d4-749">Ping requests.</span></span>
<span data-ttu-id="647d4-750">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="647d4-750">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="647d4-751">Отчеты о нарушениях CSP.</span><span class="sxs-lookup"><span data-stu-id="647d4-751">CSP Violation Reports.</span></span>
<span data-ttu-id="647d4-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="647d4-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="647d4-753">Другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="647d4-753">Other resources.</span></span>


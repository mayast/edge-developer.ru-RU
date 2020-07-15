---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e01f0e56c2ec8486a666a72c7e5fb25fd49bd8d9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880985"
---
# <span data-ttu-id="64930-104">0.9.515-Interface ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="64930-104">0.9.515 - interface ICoreWebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="64930-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="64930-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="64930-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="64930-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="64930-107">WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="64930-107">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="64930-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="64930-108">Summary</span></span>

 <span data-ttu-id="64930-109">Участников</span><span class="sxs-lookup"><span data-stu-id="64930-109">Members</span></span>                        | <span data-ttu-id="64930-110">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64930-111">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="64930-111">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="64930-112">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="64930-112">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="64930-113">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="64930-113">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="64930-114">Добавьте обработчик событий для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="64930-114">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="64930-115">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="64930-115">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="64930-116">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-116">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="64930-117">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="64930-117">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="64930-118">Добавьте обработчик событий для события FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-118">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="64930-119">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="64930-119">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="64930-120">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-120">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="64930-121">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="64930-121">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="64930-122">Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="64930-122">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="64930-123">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="64930-123">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="64930-124">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-124">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="64930-125">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="64930-125">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="64930-126">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-126">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="64930-127">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="64930-127">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="64930-128">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-128">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="64930-129">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="64930-129">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="64930-130">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-130">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="64930-131">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="64930-131">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="64930-132">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="64930-132">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="64930-133">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="64930-133">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="64930-134">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="64930-134">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="64930-135">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="64930-135">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="64930-136">SourceChanged активируется при изменении свойства Source.</span><span class="sxs-lookup"><span data-stu-id="64930-136">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="64930-137">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="64930-137">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="64930-138">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="64930-138">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="64930-139">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="64930-139">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="64930-140">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-140">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="64930-141">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="64930-141">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="64930-142">Добавьте обработчик событий для события WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-142">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="64930-143">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="64930-143">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="64930-144">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="64930-144">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="64930-145">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="64930-145">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="64930-146">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="64930-146">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="64930-147">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="64930-147">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="64930-148">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64930-148">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="64930-149">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="64930-149">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="64930-150">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="64930-150">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="64930-151">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="64930-151">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="64930-152">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="64930-152">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="64930-153">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="64930-153">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="64930-154">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-154">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="64930-155">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="64930-155">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="64930-156">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-156">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="64930-157">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="64930-157">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="64930-158">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="64930-158">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="64930-159">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="64930-159">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="64930-160">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="64930-160">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="64930-161">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="64930-161">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="64930-162">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="64930-162">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="64930-163">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="64930-163">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="64930-164">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="64930-164">The title for the current top level document.</span></span>
[<span data-ttu-id="64930-165">get_Settings</span><span class="sxs-lookup"><span data-stu-id="64930-165">get_Settings</span></span>](#get_settings) | <span data-ttu-id="64930-166">Объект [ICoreWebView2Settings](icorewebview2settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-166">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="64930-167">get_Source</span><span class="sxs-lookup"><span data-stu-id="64930-167">get_Source</span></span>](#get_source) | <span data-ttu-id="64930-168">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="64930-168">The URI of the current top level document.</span></span>
[<span data-ttu-id="64930-169">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="64930-169">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="64930-170">Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="64930-170">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="64930-171">GoBack</span><span class="sxs-lookup"><span data-stu-id="64930-171">GoBack</span></span>](#goback) | <span data-ttu-id="64930-172">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="64930-172">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="64930-173">GoForward</span><span class="sxs-lookup"><span data-stu-id="64930-173">GoForward</span></span>](#goforward) | <span data-ttu-id="64930-174">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="64930-174">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="64930-175">Которому</span><span class="sxs-lookup"><span data-stu-id="64930-175">Navigate</span></span>](#navigate) | <span data-ttu-id="64930-176">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="64930-176">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="64930-177">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="64930-177">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="64930-178">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="64930-178">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="64930-179">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="64930-179">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="64930-180">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-180">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="64930-181">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="64930-181">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="64930-182">Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-182">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="64930-183">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="64930-183">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="64930-184">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-184">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="64930-185">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="64930-185">Reload</span></span>](#reload) | <span data-ttu-id="64930-186">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="64930-186">Reload the current page.</span></span>
[<span data-ttu-id="64930-187">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="64930-187">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="64930-188">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="64930-188">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="64930-189">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="64930-189">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="64930-190">Удалите обработчик событий, добавленный ранее add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="64930-190">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="64930-191">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="64930-191">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="64930-192">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-192">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="64930-193">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="64930-193">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="64930-194">Удалите обработчик событий, добавленный ранее add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-194">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="64930-195">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="64930-195">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="64930-196">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-196">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="64930-197">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="64930-197">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="64930-198">Удалите обработчик событий, добавленный ранее add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-198">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="64930-199">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="64930-199">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="64930-200">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-200">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="64930-201">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="64930-201">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="64930-202">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-202">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="64930-203">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="64930-203">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="64930-204">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-204">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="64930-205">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="64930-205">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="64930-206">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-206">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="64930-207">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="64930-207">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="64930-208">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="64930-208">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="64930-209">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="64930-209">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="64930-210">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="64930-210">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="64930-211">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="64930-211">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="64930-212">Удалите обработчик событий, добавленный ранее add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-212">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="64930-213">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="64930-213">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="64930-214">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="64930-214">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="64930-215">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="64930-215">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="64930-216">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-216">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="64930-217">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="64930-217">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="64930-218">Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-218">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="64930-219">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="64930-219">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="64930-220">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-220">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="64930-221">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="64930-221">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="64930-222">Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="64930-222">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="64930-223">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="64930-223">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="64930-224">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-224">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="64930-225">Stop</span><span class="sxs-lookup"><span data-stu-id="64930-225">Stop</span></span>](#stop) | <span data-ttu-id="64930-226">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64930-226">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="64930-227">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="64930-227">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="64930-228">Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="64930-228">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="64930-229">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="64930-229">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="64930-230">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="64930-230">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="64930-231">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="64930-231">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="64930-232">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="64930-232">Reason for moving focus.</span></span>
[<span data-ttu-id="64930-233">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="64930-233">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="64930-234">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="64930-234">The type of a permission request.</span></span>
[<span data-ttu-id="64930-235">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="64930-235">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="64930-236">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="64930-236">Response to a permission request.</span></span>
[<span data-ttu-id="64930-237">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="64930-237">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="64930-238">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="64930-238">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="64930-239">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="64930-239">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="64930-240">Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="64930-240">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="64930-241">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="64930-241">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="64930-242">Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="64930-242">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="64930-243">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="64930-243">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="64930-244">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="64930-244">Error status values for web navigations.</span></span>
[<span data-ttu-id="64930-245">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="64930-245">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="64930-246">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64930-246">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="64930-247">События навигации</span><span class="sxs-lookup"><span data-stu-id="64930-247">Navigation events</span></span>

<span data-ttu-id="64930-248">Обычной последовательностью событий навигации является NavigationStarting, SourceChanged, ContentLoading, а затем NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-248">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="64930-250">Обратите внимание, что это для событий навигации с одинаковым событием NavigationId arg.</span><span class="sxs-lookup"><span data-stu-id="64930-250">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="64930-251">События навигации с различными аргументы события NavigationId могут перекрывать друг друга.</span><span class="sxs-lookup"><span data-stu-id="64930-251">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="64930-252">Например, если вы запускаете навигацию для события NavigationStarting, а затем запускаете другую навигацию, вы увидите NavigationStarting для первой навигации, за которой следует NavigationStarting второй переход, а затем — NavigationCompleted для первого перехода, а затем все оставшиеся события навигации для второй навигации.</span><span class="sxs-lookup"><span data-stu-id="64930-252">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="64930-253">В случае возникновения ошибок может возникнуть или не быть событием ContentLoading в зависимости от того, проявляется ли переход на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="64930-253">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="64930-254">В случае перенаправления HTTP в строке есть несколько событий NavigationStarting, для которых после первого будет задано значение параметра redirect.</span><span class="sxs-lookup"><span data-stu-id="64930-254">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="64930-255">Чтобы отслеживать или отменять навигацию внутри подкадров в WebView, используйте FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-255">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="64930-256">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="64930-256">Process model</span></span>

<span data-ttu-id="64930-257">WebView2 использует ту же модель процессов, что и веб-браузер EDGE.</span><span class="sxs-lookup"><span data-stu-id="64930-257">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="64930-258">В сеансе пользователя имеется один процесс браузера Edge для определенного каталога данных пользователя, который будет обрабатывать любой процесс вызова WebView2, указывающий на этот каталог данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="64930-258">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="64930-259">Это означает, что один процесс браузера Edge может обслуживать несколько процессов вызова и один процесс вызова может использовать несколько процессов браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="64930-259">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="64930-261">В процессе работы с браузером может быть некоторое количество процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="64930-261">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="64930-262">Они создаются по мере необходимости для того, чтобы обслуживать потенциально несколько кадров в разных представлениях.</span><span class="sxs-lookup"><span data-stu-id="64930-262">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="64930-263">Количество процессов обработки может различаться в зависимости от функции браузера "изоляция сайта" и количества отдельных отключенных относящихся к отсоединенным источникам, отображаемым в соответствующих веб-представлениях.</span><span class="sxs-lookup"><span data-stu-id="64930-263">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="64930-265">Вы можете реагировать на сбои и зависания в этих процессах браузера и отрисовки с помощью события ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="64930-265">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="64930-266">С помощью метода Close можно безопасно завершить работу связанных браузеров и процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="64930-266">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="64930-267">Потоковая модель</span><span class="sxs-lookup"><span data-stu-id="64930-267">Threading model</span></span>

<span data-ttu-id="64930-268">WebView2 должен создаваться в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="64930-268">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="64930-269">В частности, поток с конвейером сообщений.</span><span class="sxs-lookup"><span data-stu-id="64930-269">Specifically a thread with a message pump.</span></span> <span data-ttu-id="64930-270">Все обратные вызовы будут происходить в этом потоке, и звонки в WebView должны выполняться в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="64930-270">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="64930-271">Небезопасно использовать WebView из другого потока.</span><span class="sxs-lookup"><span data-stu-id="64930-271">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="64930-272">Обратные вызовы, включая обработчики событий и обработчики завершения выполняются последовательно.</span><span class="sxs-lookup"><span data-stu-id="64930-272">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="64930-273">Это значит, что если у вас есть обработчик событий и начало цикла обработки сообщений, другие обработчики событий или обратные вызовы завершения будут запущены повторно.</span><span class="sxs-lookup"><span data-stu-id="64930-273">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="64930-274">Безопасность</span><span class="sxs-lookup"><span data-stu-id="64930-274">Security</span></span>

<span data-ttu-id="64930-275">Всегда проверяйте свойство Source объекта WebView, прежде чем использовать ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString или любой другой метод для отправки данных в WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-275">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="64930-276">WebView может перейти на другую страницу с помощью конечного пользователя, взаимодействующего со страницей или сценарием на странице, вызывающем навигацию.</span><span class="sxs-lookup"><span data-stu-id="64930-276">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="64930-277">Также будьте внимательны с AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="64930-277">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="64930-278">Все будущие переходы запустят этот сценарий и предоставляют доступ к сведениям, предназначенным только для определенного происхождения, может быть предоставлен доступ к любому HTML-документу.</span><span class="sxs-lookup"><span data-stu-id="64930-278">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="64930-279">При исследовании результата вызова метода ExecuteScript, события WebMessageReceived, всегда следует проверять источник отправителя или любой другой механизм получения данных из HTML-документа в WebView проверять URI HTML-документа, что вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="64930-279">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="64930-280">Когда вы создаете сообщение для отправки в WebView, предпочитать использование PostWebMessageAsJson и создавайте строковый параметр JSON с помощью библиотеки JSON.</span><span class="sxs-lookup"><span data-stu-id="64930-280">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="64930-281">Это позволит избежать возможного ДТП данных в строку или сценарий JSON и убедиться, что злоумышленник, управляющий неуправляемым вводом, может изменить оставшуюся часть сообщения JSON или выполнить произвольный сценарий.</span><span class="sxs-lookup"><span data-stu-id="64930-281">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="64930-282">Типы строк</span><span class="sxs-lookup"><span data-stu-id="64930-282">String types</span></span>

<span data-ttu-id="64930-283">Выход из параметров строки: LPWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="64930-283">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="64930-284">Вызываемый объект выделяет строку с помощью функции CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="64930-284">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="64930-285">Владение передается вызывающему абоненту и вызывающему абоненту, чтобы освободить память с помощью CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="64930-285">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="64930-286">Строка в параметрах — LPCWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="64930-286">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="64930-287">Вызывающий объект гарантирует допустимость строки в течение синхронного вызова функции.</span><span class="sxs-lookup"><span data-stu-id="64930-287">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="64930-288">Если вызываемый объект должен сохранить это значение в некоторой точке после завершения вызова функции, вызываемый объект должен выделять собственную копию строкового значения.</span><span class="sxs-lookup"><span data-stu-id="64930-288">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="64930-289">Синтаксический анализ URI и JSON</span><span class="sxs-lookup"><span data-stu-id="64930-289">URI and JSON parsing</span></span>

<span data-ttu-id="64930-290">Различные методы предоставляют или допускают URI и JSON в виде строк.</span><span class="sxs-lookup"><span data-stu-id="64930-290">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="64930-291">Для синтаксического анализа и создания этих строк используйте собственную библиотеку предпочтительных.</span><span class="sxs-lookup"><span data-stu-id="64930-291">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="64930-292">Если приложение WinRT доступно для вашего приложения, вы можете использовать для `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` анализа или создания строк JSON либо `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` для синтаксического анализа и создания URI.</span><span class="sxs-lookup"><span data-stu-id="64930-292">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="64930-293">Обе эти операции работают в приложениях Win32.</span><span class="sxs-lookup"><span data-stu-id="64930-293">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="64930-294">Если вы используете IUri и CreateUri для синтаксического анализа URI, вы можете использовать следующие флаги создания URI, чтобы поведение CreateUri более точно соответствовало синтаксическому анализу URI в WebView:</span><span class="sxs-lookup"><span data-stu-id="64930-294">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="64930-295">Отладка</span><span class="sxs-lookup"><span data-stu-id="64930-295">Debugging</span></span>

<span data-ttu-id="64930-296">Откройте DevTools с помощью стандартных сочетаний клавиш: `F12` или `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="64930-296">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="64930-297">Вы можете использовать `--auto-open-devtools-for-tabs` параметр аргумента Command, чтобы окно DevTools было открыто немедленно при первом создании WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-297">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="64930-298">Сведения о том, как предоставить дополнительные аргументы командной строки для процесса браузера, можно найти в документации CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="64930-298">See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="64930-299">Изучите раздел реестра LoaderOverride для использования разных сборок WebView2 без изменения вашего приложения в документации CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="64930-299">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.</span></span>

## <span data-ttu-id="64930-300">Управление версиями</span><span class="sxs-lookup"><span data-stu-id="64930-300">Versioning</span></span>

<span data-ttu-id="64930-301">После того как вы использовали определенную версию SDK для создания приложения, ваше приложение может завершить работу с более ранней или более поздней версией установленных двоичных файлов браузера.</span><span class="sxs-lookup"><span data-stu-id="64930-301">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="64930-302">До версии 1.0.0.0 WebView2 на этапе обновления могут возрушиться изменения, которые не позволят пакету SDK работать с различными версиями установленных двоичных файлов браузера.</span><span class="sxs-lookup"><span data-stu-id="64930-302">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="64930-303">После того как версия 1.0.0.0 может работать с различными версиями пакета SDK, следуйте приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="64930-303">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="64930-304">Для учета критических изменений в API убедитесь, что при вызове функции экспорта DLL CreateCoreWebView2Environment и при вызове QueryInterface для любого объекта CoreWebView2 возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="64930-304">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="64930-305">Возвращаемое значение E_NOINTERFACE может указывать на то, что пакет SDK несовместим с двоичными файлами браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="64930-305">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="64930-306">Проверка сбоя из QueryInterface также учитывает ситуации, в которых пакет SDK более новый, чем версия браузера EDGE, и ваше приложение пытается использовать интерфейс, на котором нет браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="64930-306">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="64930-307">Если интерфейс недоступен, вы можете отключать связанный компонент, если это возможно, или иным образом информировать конечного пользователя о необходимости обновления браузера.</span><span class="sxs-lookup"><span data-stu-id="64930-307">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="64930-308">Участников</span><span class="sxs-lookup"><span data-stu-id="64930-308">Members</span></span>

#### <span data-ttu-id="64930-309">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="64930-309">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="64930-310">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="64930-310">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="64930-311">общедоступные значения HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-311">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-312">Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран.</span><span class="sxs-lookup"><span data-stu-id="64930-312">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="64930-313">Это событие полезно, если, например, элемент видео запрашивается на весь экран.</span><span class="sxs-lookup"><span data-stu-id="64930-313">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="64930-314">Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.</span><span class="sxs-lookup"><span data-stu-id="64930-314">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="64930-315">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="64930-315">add_ContentLoading</span></span> 

<span data-ttu-id="64930-316">Добавьте обработчик событий для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="64930-316">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="64930-317">общедоступные значения HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-317">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-318">ContentLoading срабатывает перед загрузкой содержимого, в том числе сценариев, добавленных с помощью AddScriptToExecuteOnDocumentCreated ContentLoading, не будет срабатывать при выполнении одной навигации по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации).</span><span class="sxs-lookup"><span data-stu-id="64930-318">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="64930-319">Это следует за событиями NavigationStarting и SourceChanged и предшествовать событиям HistoryChanged и NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-319">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="64930-320">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="64930-320">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="64930-321">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-321">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="64930-322">общедоступные значения HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-322">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-323">Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-323">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="64930-324">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="64930-324">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="64930-325">Добавьте обработчик событий для события FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-325">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="64930-326">общедоступные значения HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-326">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-327">Событие FrameNavigationCompleted вызывается, когда дочерний кадр полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="64930-327">FrameNavigationCompleted event fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="64930-328">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="64930-328">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="64930-329">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-329">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="64930-330">общедоступные значения HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-330">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-331">FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI.</span><span class="sxs-lookup"><span data-stu-id="64930-331">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="64930-332">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="64930-332">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="64930-333">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="64930-333">add_HistoryChanged</span></span> 

<span data-ttu-id="64930-334">Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="64930-334">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="64930-335">общедоступные значения HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-335">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-336">Используйте Счетовизменение сведений об, чтобы проверить, изменилось ли значение CanGoBack/CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="64930-336">Use HistoryChange to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="64930-337">HistoryChanged также срабатывает для использования GoBack и GoForward.</span><span class="sxs-lookup"><span data-stu-id="64930-337">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="64930-338">HistoryChanged срабатывает после SourceChanged и ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="64930-338">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="64930-339">Добавьте обработчик событий для события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-339">Add an event handler for the HistoryChanged event.</span></span> 
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
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="64930-340">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="64930-340">add_NavigationCompleted</span></span> 

<span data-ttu-id="64930-341">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-341">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="64930-342">общедоступные значения HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-342">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-343">Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="64930-343">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="64930-344">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="64930-344">add_NavigationStarting</span></span> 

<span data-ttu-id="64930-345">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-345">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="64930-346">общедоступные значения HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-346">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-347">NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI.</span><span class="sxs-lookup"><span data-stu-id="64930-347">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="64930-348">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="64930-348">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="64930-349">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="64930-349">add_NewWindowRequested</span></span> 

<span data-ttu-id="64930-350">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-350">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="64930-351">общедоступные значения HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-351">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-352">Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open.</span><span class="sxs-lookup"><span data-stu-id="64930-352">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="64930-353">Приложение может передавать целевую WebView, которая будет считаться открытым окном.</span><span class="sxs-lookup"><span data-stu-id="64930-353">The app can pass a target webview that will be considered the opened window.</span></span>

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

                newAppWindow = new AppWindow(m_creationModeId, L"");
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

#### <span data-ttu-id="64930-354">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="64930-354">add_PermissionRequested</span></span> 

<span data-ttu-id="64930-355">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-355">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="64930-356">общедоступные значения HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-356">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-357">Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="64930-357">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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

#### <span data-ttu-id="64930-358">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="64930-358">add_ProcessFailed</span></span> 

<span data-ttu-id="64930-359">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="64930-359">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="64930-360">общедоступные значения HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-360">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-361">Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="64930-361">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

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

#### <span data-ttu-id="64930-362">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="64930-362">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="64930-363">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="64930-363">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="64930-364">общедоступные значения HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-364">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-365">Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-365">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="64930-366">Это событие срабатывает только в том случае, если свойству ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled задано значение false.</span><span class="sxs-lookup"><span data-stu-id="64930-366">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="64930-367">Событие ScriptDialogOpening можно использовать, чтобы подавить диалоговые окна или заменить диалоговые окна по умолчанию пользовательскими диалоговыми окноми.</span><span class="sxs-lookup"><span data-stu-id="64930-367">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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

#### <span data-ttu-id="64930-368">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="64930-368">add_SourceChanged</span></span> 

<span data-ttu-id="64930-369">SourceChanged активируется при изменении свойства Source.</span><span class="sxs-lookup"><span data-stu-id="64930-369">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="64930-370">общедоступные значения HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-370">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-371">SourceChanged срабатывает для переходов на другой сайт или элементы навигации фрагментов.</span><span class="sxs-lookup"><span data-stu-id="64930-371">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="64930-372">Она не будет срабатывать для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="64930-372">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="64930-373">SourceChanged срабатывает перед ContentLoading для перехода к новому документу.</span><span class="sxs-lookup"><span data-stu-id="64930-373">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="64930-374">Добавьте обработчик событий для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-374">Add an event handler for the SourceChanged event.</span></span> 
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
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="64930-375">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="64930-375">add_WebMessageReceived</span></span> 

<span data-ttu-id="64930-376">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="64930-376">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="64930-377">общедоступные значения HRESULT [add_WebMessageReceived](#add_webmessagereceived)(обработчик[ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-377">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-378">Функция i, в `void postMessage(object)` которой объект — это любой объект, поддерживаемый преобразованием JSON.</span><span class="sxs-lookup"><span data-stu-id="64930-378">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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
 <span data-ttu-id="64930-379">При вызове [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) набор с помощью этого метода SetWebMessageReceivedEventHandler вызывается с помощью параметра объекта i, преобразованного в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="64930-379">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="64930-380">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="64930-380">add_WebResourceRequested</span></span> 

<span data-ttu-id="64930-381">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-381">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="64930-382">общедоступные значения HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-382">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-383">Активируется, когда WebView выполняет запрос HTTP к соответствующему URL-адресу и фильтру контекста ресурсов, добавленному с помощью AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="64930-383">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="64930-384">Для срабатывания события необходимо добавить хотя бы один фильтр.</span><span class="sxs-lookup"><span data-stu-id="64930-384">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="64930-385">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="64930-385">add_WindowCloseRequested</span></span> 

<span data-ttu-id="64930-386">Добавьте обработчик событий для события WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-386">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="64930-387">общедоступные значения HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64930-387">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64930-388">Вызывается, когда содержимое в WebView запрашивает закрытие окна, например после вызова Window. Close.</span><span class="sxs-lookup"><span data-stu-id="64930-388">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="64930-389">Приложение должно закрыть окно WebView и связанное приложение, если это понятно приложению.</span><span class="sxs-lookup"><span data-stu-id="64930-389">The app should close the WebView and related app window if that makes sense to the app.</span></span>

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

#### <span data-ttu-id="64930-390">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="64930-390">AddHostObjectToScript</span></span> 

<span data-ttu-id="64930-391">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="64930-391">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="64930-392">общедоступные значения HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(имя LPCWSTR, переменная \* объект)</span><span class="sxs-lookup"><span data-stu-id="64930-392">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="64930-393">Объекты узла предоставляются как прокси объекта hosts через `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="64930-393">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="64930-394">Прокси-серверы объектов являются обещанными и разрешаются в объект, представляющий объект Host.</span><span class="sxs-lookup"><span data-stu-id="64930-394">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="64930-395">Обещание отклонено, если приложение не добавило объект с именем.</span><span class="sxs-lookup"><span data-stu-id="64930-395">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="64930-396">Когда код JavaScript обращается к свойству или методу объекта, для него возвращается значение, которое будет обрабатываться в соответствии со значением, возвращенным из хоста для свойства или метода, или отброшено в случае ошибки, например, отсутствие такого свойства или метода для объекта или параметров недопустимым.</span><span class="sxs-lookup"><span data-stu-id="64930-396">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="64930-397">Например, когда код приложения делает следующее:</span><span class="sxs-lookup"><span data-stu-id="64930-397">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="64930-398">Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject:</span><span class="sxs-lookup"><span data-stu-id="64930-398">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="64930-399">Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="64930-399">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="64930-400">Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch.</span><span class="sxs-lookup"><span data-stu-id="64930-400">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="64930-401">Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID.</span><span class="sxs-lookup"><span data-stu-id="64930-401">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="64930-402">Вложенные массивы поддерживаются до 3 уровней.</span><span class="sxs-lookup"><span data-stu-id="64930-402">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="64930-403">Массивы по типам ссылок не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="64930-403">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="64930-404">VT_EMPTY и VT_NULL сопоставлены в JavaScript как null.</span><span class="sxs-lookup"><span data-stu-id="64930-404">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="64930-405">В JavaScript NULL и undefine сопоставляются с VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="64930-405">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="64930-406">Кроме того, все объекты узла предоставляются как `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="64930-406">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="64930-407">Здесь объекты узла предоставляются как синхронные прокси объектов узла.</span><span class="sxs-lookup"><span data-stu-id="64930-407">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="64930-408">Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста.</span><span class="sxs-lookup"><span data-stu-id="64930-408">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="64930-409">Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.hostObjects.<name>` описанный выше.</span><span class="sxs-lookup"><span data-stu-id="64930-409">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="64930-410">Синхронные прокси-серверы узлов и асинхронные прокси объектов узла могут обоим образом доявляться прокси для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="64930-410">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="64930-411">Удаленные изменения, внесенные одним прокси-сервером, будут отражаться на любом другом прокси того же объекта узла, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.</span><span class="sxs-lookup"><span data-stu-id="64930-411">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="64930-412">Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-412">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="64930-413">При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="64930-413">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="64930-414">Прокси объектов узла — это прокси-объекты JavaScript, которые перехватывают все вызовы свойств Get, Set и Method.</span><span class="sxs-lookup"><span data-stu-id="64930-414">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="64930-415">Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="64930-415">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="64930-416">Кроме того, любое свойство или метод в массиве `chrome.webview.hostObjects.options.forceLocalProperties` также будет выполняться локально.</span><span class="sxs-lookup"><span data-stu-id="64930-416">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="64930-417">Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="64930-417">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="64930-418">При необходимости вы можете добавить в этот массив дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="64930-418">You can add more to this array as required.</span></span>

<span data-ttu-id="64930-419">Существует метод `chrome.webview.hostObjects.cleanupSome` , который наилучшим способом является сбор прокси объектов хоста сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="64930-419">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="64930-420">Прокси-серверы узла дополнительно обладают следующими методами, которые выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="64930-420">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="64930-421">applyHostFunction, getHostProperty, setHostProperty: выполняйте вызов метода, свойство get или свойство Set для объекта Host.</span><span class="sxs-lookup"><span data-stu-id="64930-421">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="64930-422">Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство.</span><span class="sxs-lookup"><span data-stu-id="64930-422">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="64930-423">Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="64930-423">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="64930-424">Но `proxy.applyHostFunction('toString')` выполняется `toString` вместо объекта прокси-сервера узла.</span><span class="sxs-lookup"><span data-stu-id="64930-424">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="64930-425">getLocalProperty, setLocalProperty: выполнение свойства Get или установка свойства локально.</span><span class="sxs-lookup"><span data-stu-id="64930-425">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="64930-426">Эти методы можно использовать, чтобы принудительно получить или задать свойство для прокси объекта основного приложения, а не для объекта узла, который он представляет.</span><span class="sxs-lookup"><span data-stu-id="64930-426">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="64930-427">Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из объекта прокси-сервера узла.</span><span class="sxs-lookup"><span data-stu-id="64930-427">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="64930-428">Но `proxy.getLocalProperty('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.</span><span class="sxs-lookup"><span data-stu-id="64930-428">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="64930-429">Sync: асинхронные прокси-серверы узлов предоставляют метод Sync, возвращающий обещание для прокси объекта хоста синхронный для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="64930-429">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="64930-430">Например, `chrome.webview.hostObjects.sample.methodCall()` возвращает асинхронный прокси объекта хоста.</span><span class="sxs-lookup"><span data-stu-id="64930-430">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="64930-431">Вы можете использовать этот `sync` метод, чтобы получить для него синхронный прокси-сервер объекта узла:</span><span class="sxs-lookup"><span data-stu-id="64930-431">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="64930-432">Async: синхронные прокси-серверы узлов предоставляют асинхронный метод, который блокирует и возвращает асинхронный прокси объекта хоста для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="64930-432">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="64930-433">Например, `chrome.webview.hostObjects.sync.sample.methodCall()` возвращает синхронный прокси объекта узла.</span><span class="sxs-lookup"><span data-stu-id="64930-433">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="64930-434">Вызов `async` метода на этих блоках и возврат прокси-сервера асинхронного объекта узла для того же объекта узла:</span><span class="sxs-lookup"><span data-stu-id="64930-434">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="64930-435">затем: асинхронные прокси-объекты узла имеют метод then.</span><span class="sxs-lookup"><span data-stu-id="64930-435">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="64930-436">Это позволит им доставлять ожидающие.</span><span class="sxs-lookup"><span data-stu-id="64930-436">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="64930-437">будет возвращать обещание, которое разрешается с представлением объекта Host.</span><span class="sxs-lookup"><span data-stu-id="64930-437">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="64930-438">Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально.</span><span class="sxs-lookup"><span data-stu-id="64930-438">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="64930-439">Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания.</span><span class="sxs-lookup"><span data-stu-id="64930-439">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="64930-440">Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве прокси объектов Host.</span><span class="sxs-lookup"><span data-stu-id="64930-440">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="64930-441">Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно.</span><span class="sxs-lookup"><span data-stu-id="64930-441">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="64930-442">Асинхронные прокси-объекты узла возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства.</span><span class="sxs-lookup"><span data-stu-id="64930-442">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="64930-443">Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции.</span><span class="sxs-lookup"><span data-stu-id="64930-443">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="64930-444">Синхронные прокси объекта узла работают одинаково, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.</span><span class="sxs-lookup"><span data-stu-id="64930-444">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="64930-445">Установка свойства для прокси-сервера асинхронного узла выполняется немного по-другому.</span><span class="sxs-lookup"><span data-stu-id="64930-445">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="64930-446">Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано.</span><span class="sxs-lookup"><span data-stu-id="64930-446">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="64930-447">Это требование для прокси-объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-447">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="64930-448">Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setHostProperty, который возвращает обещание, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="64930-448">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="64930-449">Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.</span><span class="sxs-lookup"><span data-stu-id="64930-449">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="64930-450">Например, предположим, что у вас есть COM-объект со следующим интерфейсом</span><span class="sxs-lookup"><span data-stu-id="64930-450">For example, suppose you have a COM object with the following interface</span></span>

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
 <span data-ttu-id="64930-451">Мы можем добавить экземпляр этого интерфейса в наш сценарий JavaScript `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="64930-451">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="64930-452">В этом случае мы присвойте ему имя `sample` :</span><span class="sxs-lookup"><span data-stu-id="64930-452">In this case we name it `sample`:</span></span>

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
 <span data-ttu-id="64930-453">Затем в HTML-документе мы можем использовать этот COM-объект через `chrome.webview.hostObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="64930-453">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

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
        // If you need to set the property and wait for the property to change value, use the setRemote function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setRemote function.
        await chrome.webview.hostObjects.sample.setRemote("property", propertyValue);
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

#### <span data-ttu-id="64930-454">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="64930-454">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="64930-455">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="64930-455">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="64930-456">общедоступные значения HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="64930-456">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="64930-457">Вставленный сценарий будет применяться ко всем документам верхнего уровня и дочерним элементам навигации, пока они не будут удалены с помощью RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="64930-457">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="64930-458">Это применяется асинхронно, и вы должны дождаться выполнения обработчика завершения, прежде чем можно будет убедиться, что сценарий готов к выполнению для навигации в будущем.</span><span class="sxs-lookup"><span data-stu-id="64930-458">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="64930-459">Обратите внимание, что если в HTML-документе есть изолированная [Среда с определенными свойствами или](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) [заголовок HTTP Content-Security-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) , это повлияет на выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="64930-459">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="64930-460">Таким образом, например, если ключевое слово "Allow-Modal" не задано, вызовы `alert` функции будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="64930-460">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="64930-461">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="64930-461">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="64930-462">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64930-462">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="64930-463">общедоступный HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="64930-463">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="64930-464">Параметр URI может быть строкой с подстановочными знаками ("": ноль или больше; "?": только один).</span><span class="sxs-lookup"><span data-stu-id="64930-464">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="64930-465">nullptr эквивалентен L "".</span><span class="sxs-lookup"><span data-stu-id="64930-465">nullptr is equivalent to L"".</span></span> <span data-ttu-id="64930-466">Описание фильтров контекста ресурсов приведено в разделе COREWEBVIEW2_WEB_RESOURCE_CONTEXT перечисление.</span><span class="sxs-lookup"><span data-stu-id="64930-466">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="64930-467">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="64930-467">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="64930-468">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="64930-468">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="64930-469">общедоступные значения HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="64930-469">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="64930-470">Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="64930-470">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="64930-471">Параметр methodName — это полное имя метода в формате `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="64930-471">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="64930-472">Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода.</span><span class="sxs-lookup"><span data-stu-id="64930-472">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="64930-473">Метод Invoke обработчика вызывается, когда метод асинхронно завершается.</span><span class="sxs-lookup"><span data-stu-id="64930-473">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="64930-474">Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="64930-474">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="64930-475">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="64930-475">CapturePreview</span></span> 

<span data-ttu-id="64930-476">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="64930-476">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="64930-477">Public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="64930-477">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="64930-478">Укажите формат изображения с помощью параметра imageFormat.</span><span class="sxs-lookup"><span data-stu-id="64930-478">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="64930-479">Результирующие двоичные данные изображения записываются в указанный параметр imageStream.</span><span class="sxs-lookup"><span data-stu-id="64930-479">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="64930-480">Когда CapturePreview закончит запись в поток, вызывается метод Invoke в указанном параметре обработчика.</span><span class="sxs-lookup"><span data-stu-id="64930-480">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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

#### <span data-ttu-id="64930-481">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="64930-481">ExecuteScript</span></span> 

<span data-ttu-id="64930-482">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-482">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="64930-483">общедоступные значения HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="64930-483">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="64930-484">Это выполняется асинхронно и по завершении, если обработчик предоставлен в параметре ExecuteScriptCompletedHandler, вызывается его метод Invoke с результатом вычисления предоставленного JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-484">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="64930-485">Результирующее значение — это строка в кодировке JSON.</span><span class="sxs-lookup"><span data-stu-id="64930-485">The result value is a JSON encoded string.</span></span> <span data-ttu-id="64930-486">Если результат не определен, содержит цикл ссылки или не может быть закодирован в JSON, значение NULL JSON будет возвращено в виде строки null.</span><span class="sxs-lookup"><span data-stu-id="64930-486">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="64930-487">Обратите внимание, что функция без явного возвращаемого значения возвращает значение undefine.</span><span class="sxs-lookup"><span data-stu-id="64930-487">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="64930-488">Если выполняемый сценарий создает необработанное исключение, результат также равен null.</span><span class="sxs-lookup"><span data-stu-id="64930-488">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="64930-489">Этот метод применяется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="64930-489">This method is applied asynchronously.</span></span> <span data-ttu-id="64930-490">Если метод вызывается после события NavigationStarting во время навигации, сценарий будет выполнен в новом документе при его загрузке, вокруг которого возникает время ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="64930-490">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="64930-491">ExecuteScript будет работать даже в том случае, если IsScriptEnabled имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="64930-491">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="64930-492">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="64930-492">get_BrowserProcessId</span></span> 

<span data-ttu-id="64930-493">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-493">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="64930-494">общедоступные значения HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="64930-494">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="64930-495">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="64930-495">get_CanGoBack</span></span> 

<span data-ttu-id="64930-496">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="64930-496">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="64930-497">общедоступные значения HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="64930-497">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="64930-498">Событие HistoryChanged будет срабатывать, если CanGoBack изменит значение.</span><span class="sxs-lookup"><span data-stu-id="64930-498">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="64930-499">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="64930-499">get_CanGoForward</span></span> 

<span data-ttu-id="64930-500">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="64930-500">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="64930-501">общедоступные значения HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="64930-501">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="64930-502">Событие HistoryChanged будет срабатывать, если CanGoForward изменит значение.</span><span class="sxs-lookup"><span data-stu-id="64930-502">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="64930-503">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="64930-503">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="64930-504">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="64930-504">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="64930-505">общедоступные значения HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="64930-505">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="64930-506">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="64930-506">get_DocumentTitle</span></span> 

<span data-ttu-id="64930-507">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="64930-507">The title for the current top level document.</span></span>

> <span data-ttu-id="64930-508">общедоступные значения HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="64930-508">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="64930-509">Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.</span><span class="sxs-lookup"><span data-stu-id="64930-509">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="64930-510">get_Settings</span><span class="sxs-lookup"><span data-stu-id="64930-510">get_Settings</span></span> 

<span data-ttu-id="64930-511">Объект [ICoreWebView2Settings](icorewebview2settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-511">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="64930-512">общедоступные значения HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \* \* параметры)</span><span class="sxs-lookup"><span data-stu-id="64930-512">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="64930-513">get_Source</span><span class="sxs-lookup"><span data-stu-id="64930-513">get_Source</span></span> 

<span data-ttu-id="64930-514">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="64930-514">The URI of the current top level document.</span></span>

> <span data-ttu-id="64930-515">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="64930-515">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="64930-516">Это значение может изменяться в рамках обработки события SourceChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту.</span><span class="sxs-lookup"><span data-stu-id="64930-516">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="64930-517">Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="64930-517">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="64930-518">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="64930-518">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="64930-519">Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="64930-519">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="64930-520">общедоступные значения HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* ресивер)</span><span class="sxs-lookup"><span data-stu-id="64930-520">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="64930-521">Параметр eventName — это полное имя события в формате `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="64930-521">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="64930-522">Список событий протоколов DevTools и аргументов событий можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="64930-522">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="64930-523">GoBack</span><span class="sxs-lookup"><span data-stu-id="64930-523">GoBack</span></span> 

<span data-ttu-id="64930-524">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="64930-524">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="64930-525">общедоступное значение HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="64930-525">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="64930-526">GoForward</span><span class="sxs-lookup"><span data-stu-id="64930-526">GoForward</span></span> 

<span data-ttu-id="64930-527">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="64930-527">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="64930-528">общедоступные значения HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="64930-528">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="64930-529">Которому</span><span class="sxs-lookup"><span data-stu-id="64930-529">Navigate</span></span> 

<span data-ttu-id="64930-530">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="64930-530">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="64930-531">общедоступное значение HRESULT [навигации](#navigate)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="64930-531">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="64930-532">Дополнительные сведения приведены в разделе события навигации.</span><span class="sxs-lookup"><span data-stu-id="64930-532">See the navigation events for more information.</span></span> <span data-ttu-id="64930-533">Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.</span><span class="sxs-lookup"><span data-stu-id="64930-533">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

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

#### <span data-ttu-id="64930-534">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="64930-534">NavigateToString</span></span> 

<span data-ttu-id="64930-535">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="64930-535">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="64930-536">общедоступные значения HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="64930-536">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="64930-537">Параметр htmlContent не может быть больше 2 МБ символов.</span><span class="sxs-lookup"><span data-stu-id="64930-537">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="64930-538">В качестве источника новой страницы будет указано пустое значение.</span><span class="sxs-lookup"><span data-stu-id="64930-538">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="64930-539">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="64930-539">OpenDevToolsWindow</span></span> 

<span data-ttu-id="64930-540">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-540">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="64930-541">общедоступные значения HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="64930-541">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="64930-542">Ничего не происходит, если он вызывается, когда окно DevTools уже открыто</span><span class="sxs-lookup"><span data-stu-id="64930-542">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="64930-543">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="64930-543">PostWebMessageAsJson</span></span> 

<span data-ttu-id="64930-544">Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-544">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="64930-545">общедоступные значения HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="64930-545">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="64930-546">Срабатывает событие Window. Chrome. WebView для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="64930-546">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="64930-547">JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий:</span><span class="sxs-lookup"><span data-stu-id="64930-547">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="64930-548">Аргументы события представляют собой экземпляр `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="64930-548">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="64930-549">Параметр ICoreWebView2Settings:: IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="64930-549">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="64930-550">Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-550">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="64930-551">Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект.</span><span class="sxs-lookup"><span data-stu-id="64930-551">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="64930-552">Сведения о том, как отправлять сообщения из HTML-документа на WebView на узел, можно найти в SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="64930-552">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="64930-553">Это сообщение отправляется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="64930-553">This message is sent asynchronously.</span></span> <span data-ttu-id="64930-554">Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.</span><span class="sxs-lookup"><span data-stu-id="64930-554">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="64930-555">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="64930-555">PostWebMessageAsString</span></span> 

<span data-ttu-id="64930-556">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-556">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="64930-557">общедоступные значения HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="64930-557">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="64930-558">Это выполняется точно так же, как и PostWebMessageAsJson, но `window.chrome.webview` свойство Data события ARG имеет строковое значение с тем же значением, что и webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="64930-558">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="64930-559">Используйте это вместо PostWebMessageAsJson, если вы хотите общаться с помощью простых строк, а не объектов JSON.</span><span class="sxs-lookup"><span data-stu-id="64930-559">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="64930-560">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="64930-560">Reload</span></span> 

<span data-ttu-id="64930-561">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="64930-561">Reload the current page.</span></span>

> <span data-ttu-id="64930-562">общедоступная [Перезагрузка](#reload)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="64930-562">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="64930-563">Это похоже на то, что переход к URI текущего документа верхнего уровня, включая все события навигации, которые обрабатывались, и учитывает любые записи в кэше HTTP.</span><span class="sxs-lookup"><span data-stu-id="64930-563">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="64930-564">Но история «назад» и «вперед» не будет изменена.</span><span class="sxs-lookup"><span data-stu-id="64930-564">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="64930-565">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="64930-565">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="64930-566">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="64930-566">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="64930-567">общедоступные значения HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-567">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-568">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="64930-568">remove_ContentLoading</span></span> 

<span data-ttu-id="64930-569">Удалите обработчик событий, добавленный ранее add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="64930-569">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="64930-570">общедоступные значения HRESULT [remove_ContentLoading](#remove_contentloading)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-570">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-571">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="64930-571">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="64930-572">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-572">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="64930-573">общедоступные значения HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-573">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-574">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="64930-574">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="64930-575">Удалите обработчик событий, добавленный ранее add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-575">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="64930-576">общедоступные значения HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-576">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-577">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="64930-577">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="64930-578">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-578">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="64930-579">общедоступные значения HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-579">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-580">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="64930-580">remove_HistoryChanged</span></span> 

<span data-ttu-id="64930-581">Удалите обработчик событий, добавленный ранее add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-581">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="64930-582">общедоступные значения HRESULT [remove_HistoryChanged](#remove_historychanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-582">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-583">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="64930-583">remove_NavigationCompleted</span></span> 

<span data-ttu-id="64930-584">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="64930-584">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="64930-585">общедоступные значения HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-585">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-586">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="64930-586">remove_NavigationStarting</span></span> 

<span data-ttu-id="64930-587">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64930-587">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="64930-588">общедоступные значения HRESULT [remove_NavigationStarting](#remove_navigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-588">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-589">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="64930-589">remove_NewWindowRequested</span></span> 

<span data-ttu-id="64930-590">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-590">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="64930-591">общедоступные значения HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-591">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-592">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="64930-592">remove_PermissionRequested</span></span> 

<span data-ttu-id="64930-593">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-593">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="64930-594">общедоступные значения HRESULT [remove_PermissionRequested](#remove_permissionrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-594">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-595">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="64930-595">remove_ProcessFailed</span></span> 

<span data-ttu-id="64930-596">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="64930-596">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="64930-597">общедоступные значения HRESULT [remove_ProcessFailed](#remove_processfailed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-597">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-598">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="64930-598">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="64930-599">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="64930-599">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="64930-600">общедоступные значения HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-600">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-601">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="64930-601">remove_SourceChanged</span></span> 

<span data-ttu-id="64930-602">Удалите обработчик событий, добавленный ранее add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="64930-602">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="64930-603">общедоступные значения HRESULT [remove_SourceChanged](#remove_sourcechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-603">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-604">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="64930-604">remove_WebMessageReceived</span></span> 

<span data-ttu-id="64930-605">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="64930-605">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="64930-606">общедоступные значения HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-606">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-607">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="64930-607">remove_WebResourceRequested</span></span> 

<span data-ttu-id="64930-608">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-608">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="64930-609">общедоступные значения HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-609">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-610">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="64930-610">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="64930-611">Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-611">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="64930-612">общедоступные значения HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64930-612">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64930-613">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="64930-613">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="64930-614">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-614">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="64930-615">общедоступное значение HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="64930-615">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="64930-616">Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="64930-616">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="64930-617">Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="64930-617">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="64930-618">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="64930-618">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="64930-619">Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="64930-619">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="64930-620">общедоступные значения HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="64930-620">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="64930-621">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="64930-621">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="64930-622">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="64930-622">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="64930-623">общедоступный HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="64930-623">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="64930-624">Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного.</span><span class="sxs-lookup"><span data-stu-id="64930-624">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="64930-625">Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.</span><span class="sxs-lookup"><span data-stu-id="64930-625">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="64930-626">Stop</span><span class="sxs-lookup"><span data-stu-id="64930-626">Stop</span></span> 

<span data-ttu-id="64930-627">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64930-627">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="64930-628">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="64930-628">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="64930-629">Не останавливает сценарии.</span><span class="sxs-lookup"><span data-stu-id="64930-629">Does not stop scripts.</span></span>

#### <span data-ttu-id="64930-630">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="64930-630">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="64930-631">Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="64930-631">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="64930-632">[COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-632">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="64930-633">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-633">Values</span></span>                         | <span data-ttu-id="64930-634">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-634">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-635">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="64930-635">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="64930-636">Формат изображения PNG.</span><span class="sxs-lookup"><span data-stu-id="64930-636">PNG image format.</span></span>
<span data-ttu-id="64930-637">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="64930-637">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="64930-638">Формат изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="64930-638">JPEG image format.</span></span>

#### <span data-ttu-id="64930-639">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="64930-639">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="64930-640">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="64930-640">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="64930-641">[COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-641">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="64930-642">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-642">Values</span></span>                         | <span data-ttu-id="64930-643">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-643">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-644">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="64930-644">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="64930-645">ВыWM_KEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="64930-645">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="64930-646">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="64930-646">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="64930-647">ВыWM_KEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="64930-647">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="64930-648">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="64930-648">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="64930-649">ВыWM_SYSKEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="64930-649">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="64930-650">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="64930-650">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="64930-651">ВыWM_SYSKEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="64930-651">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="64930-652">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="64930-652">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="64930-653">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="64930-653">Reason for moving focus.</span></span>

> <span data-ttu-id="64930-654">[COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-654">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="64930-655">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-655">Values</span></span>                         | <span data-ttu-id="64930-656">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-656">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-657">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="64930-657">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="64930-658">Настройка кода фокуса на WebView.</span><span class="sxs-lookup"><span data-stu-id="64930-658">Code setting focus into WebView.</span></span>
<span data-ttu-id="64930-659">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="64930-659">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="64930-660">Перемещение фокуса из-за прохождения вкладки вперед.</span><span class="sxs-lookup"><span data-stu-id="64930-660">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="64930-661">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="64930-661">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="64930-662">Перемещение фокуса из-за перемещения по табуляции назад.</span><span class="sxs-lookup"><span data-stu-id="64930-662">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="64930-663">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="64930-663">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="64930-664">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="64930-664">The type of a permission request.</span></span>

> <span data-ttu-id="64930-665">[COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-665">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="64930-666">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-666">Values</span></span>                         | <span data-ttu-id="64930-667">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-668">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="64930-668">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="64930-669">Неизвестное разрешение.</span><span class="sxs-lookup"><span data-stu-id="64930-669">Unknown permission.</span></span>
<span data-ttu-id="64930-670">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="64930-670">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="64930-671">Разрешение на запись звука.</span><span class="sxs-lookup"><span data-stu-id="64930-671">Permission to capture audio.</span></span>
<span data-ttu-id="64930-672">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="64930-672">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="64930-673">Разрешение на захват видео.</span><span class="sxs-lookup"><span data-stu-id="64930-673">Permission to capture video.</span></span>
<span data-ttu-id="64930-674">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="64930-674">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="64930-675">Разрешение на доступ к географической позиции.</span><span class="sxs-lookup"><span data-stu-id="64930-675">Permission to access geolocation.</span></span>
<span data-ttu-id="64930-676">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="64930-676">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="64930-677">Разрешение на отправку веб-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="64930-677">Permission to send web notifications.</span></span>
<span data-ttu-id="64930-678">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="64930-678">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="64930-679">Разрешение на доступ к универсальному датчику.</span><span class="sxs-lookup"><span data-stu-id="64930-679">Permission to access generic sensor.</span></span>
<span data-ttu-id="64930-680">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="64930-680">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="64930-681">Разрешение на чтение системного буфера обмена без жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="64930-681">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="64930-682">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="64930-682">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="64930-683">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="64930-683">Response to a permission request.</span></span>

> <span data-ttu-id="64930-684">[COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-684">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="64930-685">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-685">Values</span></span>                         | <span data-ttu-id="64930-686">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-686">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-687">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="64930-687">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="64930-688">Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.</span><span class="sxs-lookup"><span data-stu-id="64930-688">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="64930-689">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="64930-689">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="64930-690">Предоставьте разрешение на запрос.</span><span class="sxs-lookup"><span data-stu-id="64930-690">Grant the permission request.</span></span>
<span data-ttu-id="64930-691">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="64930-691">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="64930-692">Отказ от запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="64930-692">Deny the permission request.</span></span>

#### <span data-ttu-id="64930-693">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="64930-693">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="64930-694">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="64930-694">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="64930-695">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="64930-695">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="64930-696">Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="64930-696">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="64930-697">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="64930-697">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="64930-698">Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="64930-698">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="64930-699">[COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-699">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="64930-700">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-700">Values</span></span>                         | <span data-ttu-id="64930-701">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-701">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-702">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="64930-702">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="64930-703">Указывает, что процесс браузера неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="64930-703">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="64930-704">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="64930-704">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="64930-705">Указывает, что процесс обработки неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="64930-705">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="64930-706">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="64930-706">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="64930-707">Указывает на то, что процесс рендеринга перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="64930-707">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="64930-708">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="64930-708">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="64930-709">Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="64930-709">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="64930-710">[COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-710">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="64930-711">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-711">Values</span></span>                         | <span data-ttu-id="64930-712">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-712">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-713">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="64930-713">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="64930-714">Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-714">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="64930-715">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="64930-715">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="64930-716">Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-716">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="64930-717">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="64930-717">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="64930-718">Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64930-718">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="64930-719">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="64930-719">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="64930-720">Диалоговое окно, вызываемое с помощью события JavaScript beforeunload.</span><span class="sxs-lookup"><span data-stu-id="64930-720">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="64930-721">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="64930-721">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="64930-722">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="64930-722">Error status values for web navigations.</span></span>

> <span data-ttu-id="64930-723">[COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-723">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="64930-724">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-724">Values</span></span>                         | <span data-ttu-id="64930-725">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-725">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-726">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="64930-726">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="64930-727">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="64930-727">An unknown error occurred.</span></span>
<span data-ttu-id="64930-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="64930-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="64930-729">Общее имя сертификата SSL не совпадает с веб-адресом.</span><span class="sxs-lookup"><span data-stu-id="64930-729">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="64930-730">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="64930-730">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="64930-731">Срок действия сертификата SSL истек.</span><span class="sxs-lookup"><span data-stu-id="64930-731">The SSL certificate has expired.</span></span>
<span data-ttu-id="64930-732">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="64930-732">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="64930-733">SSL-сертификат клиента включает ошибки.</span><span class="sxs-lookup"><span data-stu-id="64930-733">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="64930-734">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="64930-734">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="64930-735">SSL-сертификат отозван.</span><span class="sxs-lookup"><span data-stu-id="64930-735">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="64930-736">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="64930-736">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="64930-737">Недопустимый сертификат SSL &ndash; это может означать, что сертификат не соответствует ПИН-контактам открытого ключа для имени узла. сертификат подписан недоверенным центром или с использованием слабого алгоритма, который нарушает ограничения на имена, сертификат содержит слабый ключ, срок действия сертификата является слишком длинным, не хватает сведений об отзыве или механизме отзыва, неоднозначное имя узла, отсутствие сведений о прозрачности сертификата, или сертификат связан с [прежним корнем Symantec](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span><span class="sxs-lookup"><span data-stu-id="64930-737">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="64930-738">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="64930-738">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="64930-739">Узел недостижим.</span><span class="sxs-lookup"><span data-stu-id="64930-739">The host is unreachable.</span></span>
<span data-ttu-id="64930-740">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="64930-740">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="64930-741">Время ожидания соединения истекло.</span><span class="sxs-lookup"><span data-stu-id="64930-741">The connection has timed out.</span></span>
<span data-ttu-id="64930-742">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="64930-742">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="64930-743">Сервер вернул недопустимый или нераспознанный ответ.</span><span class="sxs-lookup"><span data-stu-id="64930-743">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="64930-744">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="64930-744">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="64930-745">Соединение было прервано.</span><span class="sxs-lookup"><span data-stu-id="64930-745">The connection was aborted.</span></span>
<span data-ttu-id="64930-746">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="64930-746">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="64930-747">Подключение было сброшено.</span><span class="sxs-lookup"><span data-stu-id="64930-747">The connection was reset.</span></span>
<span data-ttu-id="64930-748">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="64930-748">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="64930-749">Соединение с Интернетом разорвано.</span><span class="sxs-lookup"><span data-stu-id="64930-749">The Internet connection has been lost.</span></span>
<span data-ttu-id="64930-750">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="64930-750">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="64930-751">Не удается подключиться к конечному объекту.</span><span class="sxs-lookup"><span data-stu-id="64930-751">Cannot connect to destination.</span></span>
<span data-ttu-id="64930-752">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="64930-752">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="64930-753">Не удалось разрешить указанное имя узла.</span><span class="sxs-lookup"><span data-stu-id="64930-753">Could not resolve provided host name.</span></span>
<span data-ttu-id="64930-754">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="64930-754">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="64930-755">Операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="64930-755">The operation was canceled.</span></span>
<span data-ttu-id="64930-756">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="64930-756">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="64930-757">Перенаправление запроса завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="64930-757">The request redirect failed.</span></span>
<span data-ttu-id="64930-758">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="64930-758">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="64930-759">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="64930-759">An unexpected error occurred.</span></span>

#### <span data-ttu-id="64930-760">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="64930-760">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="64930-761">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64930-761">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="64930-762">[COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) перечисления</span><span class="sxs-lookup"><span data-stu-id="64930-762">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="64930-763">Данные</span><span class="sxs-lookup"><span data-stu-id="64930-763">Values</span></span>                         | <span data-ttu-id="64930-764">Описания</span><span class="sxs-lookup"><span data-stu-id="64930-764">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64930-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="64930-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="64930-766">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="64930-766">All resources.</span></span>
<span data-ttu-id="64930-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="64930-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="64930-768">Ресурсы документов.</span><span class="sxs-lookup"><span data-stu-id="64930-768">Document resources.</span></span>
<span data-ttu-id="64930-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="64930-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="64930-770">Ресурсы CSS.</span><span class="sxs-lookup"><span data-stu-id="64930-770">CSS resources.</span></span>
<span data-ttu-id="64930-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="64930-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="64930-772">Графические ресурсы.</span><span class="sxs-lookup"><span data-stu-id="64930-772">Image resources.</span></span>
<span data-ttu-id="64930-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="64930-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="64930-774">Другие мультимедийные ресурсы, например видео.</span><span class="sxs-lookup"><span data-stu-id="64930-774">Other media resources such as videos.</span></span>
<span data-ttu-id="64930-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="64930-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="64930-776">Ресурсы шрифта.</span><span class="sxs-lookup"><span data-stu-id="64930-776">Font resources.</span></span>
<span data-ttu-id="64930-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="64930-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="64930-778">Ресурсы сценария.</span><span class="sxs-lookup"><span data-stu-id="64930-778">Script resources.</span></span>
<span data-ttu-id="64930-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="64930-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="64930-780">HTTP-запросы.</span><span class="sxs-lookup"><span data-stu-id="64930-780">XML HTTP requests.</span></span>
<span data-ttu-id="64930-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="64930-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="64930-782">Получение взаимодействия API.</span><span class="sxs-lookup"><span data-stu-id="64930-782">Fetch API communication.</span></span>
<span data-ttu-id="64930-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="64930-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="64930-784">TextTrack ресурсы.</span><span class="sxs-lookup"><span data-stu-id="64930-784">TextTrack resources.</span></span>
<span data-ttu-id="64930-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="64930-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="64930-786">Взаимодействие API EventSource.</span><span class="sxs-lookup"><span data-stu-id="64930-786">EventSource API communication.</span></span>
<span data-ttu-id="64930-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="64930-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="64930-788">Взаимодействие API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="64930-788">WebSocket API communication.</span></span>
<span data-ttu-id="64930-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="64930-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="64930-790">Манифесты веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="64930-790">Web App Manifests.</span></span>
<span data-ttu-id="64930-791">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="64930-791">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="64930-792">Обмен подписанными HTTP-сообщениями.</span><span class="sxs-lookup"><span data-stu-id="64930-792">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="64930-793">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="64930-793">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="64930-794">Запросы ping.</span><span class="sxs-lookup"><span data-stu-id="64930-794">Ping requests.</span></span>
<span data-ttu-id="64930-795">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="64930-795">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="64930-796">Отчеты о нарушениях CSP.</span><span class="sxs-lookup"><span data-stu-id="64930-796">CSP Violation Reports.</span></span>
<span data-ttu-id="64930-797">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="64930-797">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="64930-798">Другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="64930-798">Other resources.</span></span>


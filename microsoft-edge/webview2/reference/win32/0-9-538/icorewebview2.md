---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2
ms.openlocfilehash: 81bc222324db9649439afa2a7c3c84f715fa2ae3
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894328"
---
# <span data-ttu-id="f2bf5-104">интерфейс ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="f2bf5-104">interface ICoreWebView2</span></span> 

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="f2bf5-105">WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="f2bf5-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f2bf5-106">Summary</span></span>

 <span data-ttu-id="f2bf5-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f2bf5-107">Members</span></span>                        | <span data-ttu-id="f2bf5-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f2bf5-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="f2bf5-110">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="f2bf5-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="f2bf5-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="f2bf5-112">Добавьте обработчик событий для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="f2bf5-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="f2bf5-114">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="f2bf5-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="f2bf5-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="f2bf5-116">Добавьте обработчик событий для события FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="f2bf5-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="f2bf5-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="f2bf5-118">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="f2bf5-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="f2bf5-120">Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-120">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="f2bf5-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="f2bf5-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="f2bf5-122">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="f2bf5-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="f2bf5-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="f2bf5-124">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="f2bf5-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="f2bf5-126">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="f2bf5-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="f2bf5-128">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="f2bf5-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="f2bf5-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="f2bf5-130">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="f2bf5-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="f2bf5-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="f2bf5-132">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="f2bf5-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="f2bf5-134">SourceChanged активируется при изменении свойства Source.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-134">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="f2bf5-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="f2bf5-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="f2bf5-136">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-136">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="f2bf5-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="f2bf5-138">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="f2bf5-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="f2bf5-140">Добавьте обработчик событий для события WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="f2bf5-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="f2bf5-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="f2bf5-142">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="f2bf5-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="f2bf5-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="f2bf5-144">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="f2bf5-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="f2bf5-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="f2bf5-146">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="f2bf5-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="f2bf5-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="f2bf5-148">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="f2bf5-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="f2bf5-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="f2bf5-150">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="f2bf5-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="f2bf5-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="f2bf5-152">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="f2bf5-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="f2bf5-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="f2bf5-154">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="f2bf5-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="f2bf5-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="f2bf5-156">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-156">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="f2bf5-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="f2bf5-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="f2bf5-158">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-158">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="f2bf5-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="f2bf5-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="f2bf5-160">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="f2bf5-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="f2bf5-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="f2bf5-162">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-162">The title for the current top level document.</span></span>
[<span data-ttu-id="f2bf5-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="f2bf5-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="f2bf5-164">Объект [ICoreWebView2Settings](icorewebview2settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="f2bf5-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="f2bf5-165">get_Source</span></span>](#get_source) | <span data-ttu-id="f2bf5-166">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="f2bf5-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="f2bf5-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="f2bf5-168">Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="f2bf5-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="f2bf5-169">GoBack</span></span>](#goback) | <span data-ttu-id="f2bf5-170">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="f2bf5-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="f2bf5-171">GoForward</span></span>](#goforward) | <span data-ttu-id="f2bf5-172">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="f2bf5-173">Которому</span><span class="sxs-lookup"><span data-stu-id="f2bf5-173">Navigate</span></span>](#navigate) | <span data-ttu-id="f2bf5-174">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="f2bf5-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="f2bf5-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="f2bf5-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="f2bf5-176">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="f2bf5-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="f2bf5-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="f2bf5-178">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="f2bf5-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="f2bf5-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="f2bf5-180">Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="f2bf5-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="f2bf5-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="f2bf5-182">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="f2bf5-183">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="f2bf5-183">Reload</span></span>](#reload) | <span data-ttu-id="f2bf5-184">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-184">Reload the current page.</span></span>
[<span data-ttu-id="f2bf5-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="f2bf5-186">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-186">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="f2bf5-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="f2bf5-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="f2bf5-188">Удалите обработчик событий, добавленный ранее add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="f2bf5-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="f2bf5-190">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="f2bf5-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="f2bf5-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="f2bf5-192">Удалите обработчик событий, добавленный ранее add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="f2bf5-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="f2bf5-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="f2bf5-194">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="f2bf5-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="f2bf5-196">Удалите обработчик событий, добавленный ранее add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="f2bf5-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="f2bf5-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="f2bf5-198">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="f2bf5-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="f2bf5-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="f2bf5-200">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="f2bf5-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="f2bf5-202">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="f2bf5-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="f2bf5-204">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="f2bf5-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="f2bf5-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="f2bf5-206">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="f2bf5-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="f2bf5-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="f2bf5-208">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="f2bf5-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="f2bf5-210">Удалите обработчик событий, добавленный ранее add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="f2bf5-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="f2bf5-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="f2bf5-212">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="f2bf5-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="f2bf5-214">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="f2bf5-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="f2bf5-216">Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="f2bf5-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="f2bf5-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="f2bf5-218">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="f2bf5-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="f2bf5-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="f2bf5-220">Удалите соответствующий сценарий JavaScript, который добавляется с использованием `AddScriptToExecuteOnDocumentCreated` указанного идентификатора сценария.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-220">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>
[<span data-ttu-id="f2bf5-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="f2bf5-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="f2bf5-222">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="f2bf5-223">Stop</span><span class="sxs-lookup"><span data-stu-id="f2bf5-223">Stop</span></span>](#stop) | <span data-ttu-id="f2bf5-224">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="f2bf5-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="f2bf5-226">Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="f2bf5-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="f2bf5-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="f2bf5-228">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="f2bf5-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="f2bf5-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="f2bf5-230">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-230">Reason for moving focus.</span></span>
[<span data-ttu-id="f2bf5-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="f2bf5-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="f2bf5-232">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-232">The type of a permission request.</span></span>
[<span data-ttu-id="f2bf5-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="f2bf5-234">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-234">Response to a permission request.</span></span>
[<span data-ttu-id="f2bf5-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="f2bf5-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="f2bf5-236">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="f2bf5-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="f2bf5-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="f2bf5-238">Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="f2bf5-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="f2bf5-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="f2bf5-240">Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="f2bf5-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="f2bf5-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="f2bf5-242">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="f2bf5-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="f2bf5-244">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="f2bf5-245">События навигации</span><span class="sxs-lookup"><span data-stu-id="f2bf5-245">Navigation events</span></span>

<span data-ttu-id="f2bf5-246">Обычной последовательностью событий навигации является NavigationStarting, SourceChanged, ContentLoading, а затем NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-246">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span> <span data-ttu-id="f2bf5-247">Следующие события описывают состояние WebView во время каждой навигации: NavigationStarting: WebView начинает навигацию, и навигация приводит к появлению сетевого запроса.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-247">The following events describe the state of WebView during each navigation: NavigationStarting: WebView is starting to navigate and the navigation will result in a network request.</span></span> <span data-ttu-id="f2bf5-248">Узел может отключить запрос в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-248">The host can disallow the request at this time.</span></span> <span data-ttu-id="f2bf5-249">SourceChanged: источник WebView изменится на новый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-249">SourceChanged: The source of WebView is changed to a new URL.</span></span> <span data-ttu-id="f2bf5-250">Это может быть также вызвано навигацией, которая не вызывает сетевой запрос, например навигацию по фрагменту.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-250">This may also be due to a navigation that doesn't cause a network request such as a fragment navigation.</span></span> <span data-ttu-id="f2bf5-251">HistoryChanged: История WebView была обновлена в результате навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-251">HistoryChanged: WebView's history has been updated as a result of the navigation.</span></span> <span data-ttu-id="f2bf5-252">ContentLoading: WebView начал Загрузка нового содержимого.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-252">ContentLoading: WebView has started loading new content.</span></span> <span data-ttu-id="f2bf5-253">NavigationCompleted: WebView завершил загрузку контента на новой странице.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-253">NavigationCompleted: WebView has completed loading content on the new page.</span></span> <span data-ttu-id="f2bf5-254">Разработчики могут отслеживать переходы по каждому новому документу с помощью идентификатора навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-254">Developers can track navigations to each new document by the navigation ID.</span></span> <span data-ttu-id="f2bf5-255">Изменения идентификатора навигации WebView при каждом успешном переходе на новый документ.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-255">WebView's navigation ID changes every time there is a successful navigation to a new document.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="f2bf5-257">Обратите внимание, что это для событий навигации с одинаковым событием NavigationId arg.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-257">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="f2bf5-258">События навигации с различными аргументы события NavigationId могут перекрывать друг друга.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-258">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="f2bf5-259">Например, если вы запускаете навигацию для события NavigationStarting, а затем запускаете другую навигацию, вы увидите NavigationStarting для первой навигации, за которой следует NavigationStarting второй переход, а затем — NavigationCompleted для первого перехода, а затем все оставшиеся события навигации для второй навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-259">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="f2bf5-260">В случае возникновения ошибок может возникнуть или не быть событием ContentLoading в зависимости от того, проявляется ли переход на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-260">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="f2bf5-261">В случае перенаправления HTTP в строке есть несколько событий NavigationStarting, в которых после первого будет задано значение параметра "перенаправление", но идентификатор навигации останется прежним.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-261">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set, however navigation ID remains the same.</span></span> <span data-ttu-id="f2bf5-262">Одни и те же навигации по документу не приводят к событию NavigationStarting, а также не возвращают идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-262">Same document navigations do not result in NavigationStarting event and also do not increment the navigation ID.</span></span>

<span data-ttu-id="f2bf5-263">Чтобы отслеживать или отменять навигацию внутри подкадров в WebView, используйте FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-263">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="f2bf5-264">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="f2bf5-264">Process model</span></span>

<span data-ttu-id="f2bf5-265">WebView2 использует ту же модель процессов, что и веб-браузер EDGE.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-265">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="f2bf5-266">В сеансе пользователя имеется один процесс браузера Edge для определенного каталога данных пользователя, который будет обрабатывать любой процесс вызова WebView2, указывающий на этот каталог данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-266">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="f2bf5-267">Это означает, что один процесс браузера Edge может обслуживать несколько процессов вызова и один процесс вызова может использовать несколько процессов браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-267">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="f2bf5-269">В процессе работы с браузером может быть некоторое количество процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-269">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="f2bf5-270">Они создаются по мере необходимости для того, чтобы обслуживать потенциально несколько кадров в разных представлениях.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-270">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="f2bf5-271">Количество процессов обработки может различаться в зависимости от функции браузера "изоляция сайта" и количества отдельных отключенных относящихся к отсоединенным источникам, отображаемым в соответствующих веб-представлениях.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-271">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="f2bf5-273">Вы можете реагировать на сбои и зависания в этих процессах браузера и отрисовки с помощью события ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-273">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="f2bf5-274">С помощью метода Close можно безопасно завершить работу связанных браузеров и процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-274">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="f2bf5-275">Потоковая модель</span><span class="sxs-lookup"><span data-stu-id="f2bf5-275">Threading model</span></span>

<span data-ttu-id="f2bf5-276">WebView2 должен создаваться в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-276">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="f2bf5-277">В частности, поток с конвейером сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-277">Specifically a thread with a message pump.</span></span> <span data-ttu-id="f2bf5-278">Все обратные вызовы будут происходить в этом потоке, и звонки в WebView должны выполняться в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-278">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="f2bf5-279">Небезопасно использовать WebView из другого потока.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-279">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="f2bf5-280">Обратные вызовы, включая обработчики событий и обработчики завершения выполняются последовательно.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-280">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="f2bf5-281">Это значит, что если у вас есть обработчик событий и начало цикла обработки сообщений, другие обработчики событий или обратные вызовы завершения будут запущены повторно.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-281">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="f2bf5-282">Типы строк</span><span class="sxs-lookup"><span data-stu-id="f2bf5-282">String types</span></span>

<span data-ttu-id="f2bf5-283">Выход из параметров строки: LPWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-283">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="f2bf5-284">Вызываемый объект выделяет строку с помощью функции CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-284">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="f2bf5-285">Владение передается вызывающему абоненту и вызывающему абоненту, чтобы освободить память с помощью CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-285">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="f2bf5-286">Строка в параметрах — LPCWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-286">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="f2bf5-287">Вызывающий объект гарантирует допустимость строки в течение синхронного вызова функции.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-287">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="f2bf5-288">Если вызываемый объект должен сохранить это значение в некоторой точке после завершения вызова функции, вызываемый объект должен выделять собственную копию строкового значения.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-288">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="f2bf5-289">Синтаксический анализ URI и JSON</span><span class="sxs-lookup"><span data-stu-id="f2bf5-289">URI and JSON parsing</span></span>

<span data-ttu-id="f2bf5-290">Различные методы предоставляют или допускают URI и JSON в виде строк.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-290">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="f2bf5-291">Для синтаксического анализа и создания этих строк используйте собственную библиотеку предпочтительных.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-291">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="f2bf5-292">Если приложение WinRT доступно для вашего приложения, вы можете использовать для `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` анализа или создания строк JSON либо `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` для синтаксического анализа и создания URI.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-292">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="f2bf5-293">Обе эти операции работают в приложениях Win32.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-293">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="f2bf5-294">Если вы используете IUri и CreateUri для синтаксического анализа URI, вы можете использовать следующие флаги создания URI, чтобы поведение CreateUri более точно соответствовало синтаксическому анализу URI в WebView:</span><span class="sxs-lookup"><span data-stu-id="f2bf5-294">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="f2bf5-295">Участников</span><span class="sxs-lookup"><span data-stu-id="f2bf5-295">Members</span></span>

#### <span data-ttu-id="f2bf5-296">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-296">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="f2bf5-297">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-297">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="f2bf5-298">общедоступные значения HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-298">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-299">Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-299">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="f2bf5-300">Это событие полезно, если, например, элемент видео запрашивается на весь экран.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-300">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="f2bf5-301">Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-301">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="f2bf5-302">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="f2bf5-302">add_ContentLoading</span></span> 

<span data-ttu-id="f2bf5-303">Добавьте обработчик событий для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-303">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="f2bf5-304">общедоступные значения HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-304">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-305">ContentLoading срабатывает перед загрузкой содержимого, в том числе сценариев, добавленных с помощью AddScriptToExecuteOnDocumentCreated ContentLoading, не будет срабатывать при выполнении одной навигации по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации).</span><span class="sxs-lookup"><span data-stu-id="f2bf5-305">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="f2bf5-306">Это следует за событиями NavigationStarting и SourceChanged и предшествовать событиям HistoryChanged и NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-306">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="f2bf5-307">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-307">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="f2bf5-308">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-308">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="f2bf5-309">общедоступные значения HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-309">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-310">Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-310">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="f2bf5-311">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="f2bf5-311">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="f2bf5-312">Добавьте обработчик событий для события FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-312">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="f2bf5-313">общедоступные значения HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-313">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-314">Событие FrameNavigationCompleted вызывается, когда дочерний кадр полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-314">FrameNavigationCompleted event fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="f2bf5-315">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="f2bf5-315">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="f2bf5-316">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-316">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="f2bf5-317">общедоступные значения HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-317">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-318">FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-318">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="f2bf5-319">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-319">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="f2bf5-320">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-320">add_HistoryChanged</span></span> 

<span data-ttu-id="f2bf5-321">Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-321">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="f2bf5-322">общедоступные значения HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-322">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-323">Используйте Счетовизменение сведений об, чтобы проверить, изменилось ли значение CanGoBack/CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-323">Use HistoryChange to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="f2bf5-324">HistoryChanged также срабатывает для использования GoBack и GoForward.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-324">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="f2bf5-325">HistoryChanged срабатывает после SourceChanged и ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-325">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="f2bf5-326">Добавьте обработчик событий для события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-326">Add an event handler for the HistoryChanged event.</span></span> 
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

#### <span data-ttu-id="f2bf5-327">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="f2bf5-327">add_NavigationCompleted</span></span> 

<span data-ttu-id="f2bf5-328">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-328">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="f2bf5-329">общедоступные значения HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-329">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-330">Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-330">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="f2bf5-331">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="f2bf5-331">add_NavigationStarting</span></span> 

<span data-ttu-id="f2bf5-332">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-332">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="f2bf5-333">общедоступные значения HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-333">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-334">NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-334">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="f2bf5-335">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-335">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="f2bf5-336">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-336">add_NewWindowRequested</span></span> 

<span data-ttu-id="f2bf5-337">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-337">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="f2bf5-338">общедоступные значения HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-338">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-339">Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-339">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="f2bf5-340">Приложение может передавать целевую WebView, которая будет считаться открытым окном.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-340">The app can pass a target webview that will be considered the opened window.</span></span>

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

                wil::com_ptr<ICoreWebView2ExperimentalNewWindowRequestedEventArgs>
                    experimentalArgs;
                CHECK_FAILURE(args->QueryInterface(IID_PPV_ARGS(&experimentalArgs)));
                wil::com_ptr<ICoreWebView2ExperimentalWindowFeatures> windowFeatures;
                CHECK_FAILURE(experimentalArgs->get_WindowFeatures(&windowFeatures));

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
                  newAppWindow = new AppWindow(m_creationModeId, L"", nullptr, true, windowRect, !!shouldHaveToolbar);
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

#### <span data-ttu-id="f2bf5-341">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-341">add_PermissionRequested</span></span> 

<span data-ttu-id="f2bf5-342">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-342">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="f2bf5-343">общедоступные значения HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-343">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-344">Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-344">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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

#### <span data-ttu-id="f2bf5-345">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="f2bf5-345">add_ProcessFailed</span></span> 

<span data-ttu-id="f2bf5-346">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-346">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="f2bf5-347">общедоступные значения HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-347">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-348">Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-348">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

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

#### <span data-ttu-id="f2bf5-349">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="f2bf5-349">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="f2bf5-350">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-350">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="f2bf5-351">общедоступные значения HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-351">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-352">Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-352">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="f2bf5-353">Это событие срабатывает только в том случае, если свойству ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled задано значение false.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-353">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="f2bf5-354">Событие ScriptDialogOpening можно использовать, чтобы подавить диалоговые окна или заменить диалоговые окна по умолчанию пользовательскими диалоговыми окноми.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-354">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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

#### <span data-ttu-id="f2bf5-355">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-355">add_SourceChanged</span></span> 

<span data-ttu-id="f2bf5-356">SourceChanged активируется при изменении свойства Source.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-356">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="f2bf5-357">общедоступные значения HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-357">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-358">SourceChanged срабатывает для переходов на другой сайт или элементы навигации фрагментов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-358">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="f2bf5-359">Она не будет срабатывать для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-359">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="f2bf5-360">SourceChanged срабатывает перед ContentLoading для перехода к новому документу.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-360">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="f2bf5-361">Добавьте обработчик событий для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-361">Add an event handler for the SourceChanged event.</span></span> 
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

#### <span data-ttu-id="f2bf5-362">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="f2bf5-362">add_WebMessageReceived</span></span> 

<span data-ttu-id="f2bf5-363">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-363">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="f2bf5-364">общедоступные значения HRESULT [add_WebMessageReceived](#add_webmessagereceived)(обработчик[ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-364">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-365">Функция i, в `void postMessage(object)` которой объект — это любой объект, поддерживаемый преобразованием JSON.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-365">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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
 <span data-ttu-id="f2bf5-366">При вызове [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) набор с помощью этого метода SetWebMessageReceivedEventHandler вызывается с помощью параметра объекта i, преобразованного в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-366">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="f2bf5-367">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-367">add_WebResourceRequested</span></span> 

<span data-ttu-id="f2bf5-368">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-368">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="f2bf5-369">общедоступные значения HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-369">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-370">Активируется, когда WebView выполняет запрос URL-адреса к соответствующему URL-адресу и фильтру контекст ресурсов, добавленный с помощью AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-370">Fires when the WebView is performing a URL request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="f2bf5-371">Для срабатывания события необходимо добавить хотя бы один фильтр.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-371">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="f2bf5-372">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-372">add_WindowCloseRequested</span></span> 

<span data-ttu-id="f2bf5-373">Добавьте обработчик событий для события WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-373">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="f2bf5-374">общедоступные значения HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-374">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f2bf5-375">Вызывается, когда содержимое в WebView запрашивает закрытие окна, например после вызова Window. Close.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-375">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="f2bf5-376">Приложение должно закрыть окно WebView и связанное приложение, если это понятно приложению.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-376">The app should close the WebView and related app window if that makes sense to the app.</span></span>

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

#### <span data-ttu-id="f2bf5-377">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="f2bf5-377">AddHostObjectToScript</span></span> 

<span data-ttu-id="f2bf5-378">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-378">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="f2bf5-379">общедоступные значения HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(имя LPCWSTR, переменная \* объект)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-379">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="f2bf5-380">Объекты узла предоставляются как прокси объекта hosts через `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-380">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="f2bf5-381">Прокси-серверы объектов являются обещанными и разрешаются в объект, представляющий объект Host.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-381">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="f2bf5-382">Обещание отклонено, если приложение не добавило объект с именем.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-382">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="f2bf5-383">Когда код JavaScript обращается к свойству или методу объекта, для него возвращается значение, которое будет обрабатываться в соответствии со значением, возвращенным из хоста для свойства или метода, или отброшено в случае ошибки, например, отсутствие такого свойства или метода для объекта или параметров недопустимым.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-383">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="f2bf5-384">Например, когда код приложения делает следующее:</span><span class="sxs-lookup"><span data-stu-id="f2bf5-384">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="f2bf5-385">Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject:</span><span class="sxs-lookup"><span data-stu-id="f2bf5-385">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="f2bf5-386">Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-386">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="f2bf5-387">Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-387">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="f2bf5-388">Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-388">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="f2bf5-389">Вложенные массивы поддерживаются до 3 уровней.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-389">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="f2bf5-390">Массивы по типам ссылок не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-390">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="f2bf5-391">VT_EMPTY и VT_NULL сопоставлены в JavaScript как null.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-391">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="f2bf5-392">В JavaScript NULL и undefine сопоставляются с VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-392">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="f2bf5-393">Кроме того, все объекты узла предоставляются как `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-393">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="f2bf5-394">Здесь объекты узла предоставляются как синхронные прокси объектов узла.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-394">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="f2bf5-395">Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-395">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="f2bf5-396">Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.hostObjects.<name>` описанный выше.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-396">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="f2bf5-397">Синхронные прокси-серверы узлов и асинхронные прокси объектов узла могут обоим образом доявляться прокси для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-397">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="f2bf5-398">Удаленные изменения, внесенные одним прокси-сервером, будут отражаться на любом другом прокси того же объекта узла, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-398">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="f2bf5-399">Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-399">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="f2bf5-400">При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="f2bf5-400">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="f2bf5-401">Прокси объектов узла — это прокси-объекты JavaScript, которые перехватывают все вызовы свойств Get, Set и Method.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-401">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="f2bf5-402">Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-402">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="f2bf5-403">Кроме того, любое свойство или метод в массиве `chrome.webview.hostObjects.options.forceLocalProperties` также будет выполняться локально.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-403">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="f2bf5-404">Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-404">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="f2bf5-405">При необходимости вы можете добавить в этот массив дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-405">You can add more to this array as required.</span></span>

<span data-ttu-id="f2bf5-406">Существует метод `chrome.webview.hostObjects.cleanupSome` , который наилучшим способом является сбор прокси объектов хоста сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-406">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="f2bf5-407">Прокси-серверы узла дополнительно обладают следующими методами, которые выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-407">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="f2bf5-408">applyHostFunction, getHostProperty, setHostProperty: выполняйте вызов метода, свойство get или свойство Set для объекта Host.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-408">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="f2bf5-409">Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-409">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="f2bf5-410">Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-410">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="f2bf5-411">Но `proxy.applyHostFunction('toString')` выполняется `toString` вместо объекта прокси-сервера узла.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-411">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="f2bf5-412">getLocalProperty, setLocalProperty: выполнение свойства Get или установка свойства локально.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-412">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="f2bf5-413">Эти методы можно использовать, чтобы принудительно получить или задать свойство для прокси объекта основного приложения, а не для объекта узла, который он представляет.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-413">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="f2bf5-414">Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из объекта прокси-сервера узла.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-414">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="f2bf5-415">Но `proxy.getLocalProperty('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-415">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="f2bf5-416">Sync: асинхронные прокси-серверы узлов предоставляют метод Sync, возвращающий обещание для прокси объекта хоста синхронный для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-416">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="f2bf5-417">Например, `chrome.webview.hostObjects.sample.methodCall()` возвращает асинхронный прокси объекта хоста.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-417">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="f2bf5-418">Вы можете использовать этот `sync` метод, чтобы получить для него синхронный прокси-сервер объекта узла:</span><span class="sxs-lookup"><span data-stu-id="f2bf5-418">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="f2bf5-419">Async: синхронные прокси-серверы узлов предоставляют асинхронный метод, который блокирует и возвращает асинхронный прокси объекта хоста для одного и того же объекта узла.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-419">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="f2bf5-420">Например, `chrome.webview.hostObjects.sync.sample.methodCall()` возвращает синхронный прокси объекта узла.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-420">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="f2bf5-421">Вызов `async` метода на этих блоках и возврат прокси-сервера асинхронного объекта узла для того же объекта узла:</span><span class="sxs-lookup"><span data-stu-id="f2bf5-421">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="f2bf5-422">затем: асинхронные прокси-объекты узла имеют метод then.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-422">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="f2bf5-423">Это позволит им доставлять ожидающие.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-423">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="f2bf5-424">будет возвращать обещание, которое разрешается с представлением объекта Host.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-424">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="f2bf5-425">Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-425">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="f2bf5-426">Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-426">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="f2bf5-427">Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве прокси объектов Host.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-427">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="f2bf5-428">Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-428">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="f2bf5-429">Асинхронные прокси-объекты узла возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-429">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="f2bf5-430">Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-430">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="f2bf5-431">Синхронные прокси объекта узла работают одинаково, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-431">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="f2bf5-432">Установка свойства для прокси-сервера асинхронного узла выполняется немного по-другому.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-432">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="f2bf5-433">Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-433">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="f2bf5-434">Это требование для прокси-объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-434">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="f2bf5-435">Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setHostProperty, который возвращает обещание, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-435">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="f2bf5-436">Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-436">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="f2bf5-437">Например, предположим, что у вас есть COM-объект со следующим интерфейсом</span><span class="sxs-lookup"><span data-stu-id="f2bf5-437">For example, suppose you have a COM object with the following interface</span></span>

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
 <span data-ttu-id="f2bf5-438">Мы можем добавить экземпляр этого интерфейса в наш сценарий JavaScript `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-438">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="f2bf5-439">В этом случае мы присвойте ему имя `sample` :</span><span class="sxs-lookup"><span data-stu-id="f2bf5-439">In this case we name it `sample`:</span></span>

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
 <span data-ttu-id="f2bf5-440">Затем в HTML-документе мы можем использовать этот COM-объект через `chrome.webview.hostObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="f2bf5-440">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

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
<span data-ttu-id="f2bf5-441">Предоставление доступа к объектам узла для сценария имеет угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-441">Exposing host objects to script has security risk.</span></span> <span data-ttu-id="f2bf5-442">Пожалуйста, [следуйте рекомендациям](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span><span class="sxs-lookup"><span data-stu-id="f2bf5-442">Please follow [best practices](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span></span>

#### <span data-ttu-id="f2bf5-443">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="f2bf5-443">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="f2bf5-444">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-444">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="f2bf5-445">общедоступные значения HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-445">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="f2bf5-446">Этот метод вставляет сценарий, который запускается на всех документах верхнего уровня и дочерних переходах между страницами фреймов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-446">This method injects a script that runs on all top-level document and child frame page navigations.</span></span> <span data-ttu-id="f2bf5-447">Этот метод выполняется асинхронно, и вы должны дождаться завершения обработчика завершения перед тем, как вставленный сценарий будет готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-447">This method runs asynchronously, and you must wait for the completion handler to finish before the injected script is ready to run.</span></span> <span data-ttu-id="f2bf5-448">Когда этот метод завершает работу, метод обработчика `Invoke` вызывается с использованием `id` вставленного сценария.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-448">When this method completes, the handler's `Invoke` method is called with the `id` of the injected script.</span></span> `id` <span data-ttu-id="f2bf5-449">является строкой.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-449">is a string.</span></span> <span data-ttu-id="f2bf5-450">Чтобы удалить вставленный сценарий, используйте `RemoveScriptToExecuteOnDocumentCreated` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-450">To remove the injected script, use `RemoveScriptToExecuteOnDocumentCreated`.</span></span>

<span data-ttu-id="f2bf5-451">Обратите внимание, что если в HTML-документе есть изолированная [Среда с определенными свойствами или](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) [заголовок HTTP Content-Security-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) , это повлияет на выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-451">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="f2bf5-452">Таким образом, например, если ключевое слово "Allow-Modal" не задано, вызовы `alert` функции будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-452">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="f2bf5-453">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="f2bf5-453">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="f2bf5-454">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-454">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="f2bf5-455">общедоступный HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-455">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="f2bf5-456">Параметр URI может быть строкой с подстановочными знаками ("": ноль или больше; "?": только один).</span><span class="sxs-lookup"><span data-stu-id="f2bf5-456">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="f2bf5-457">nullptr эквивалентен L "".</span><span class="sxs-lookup"><span data-stu-id="f2bf5-457">nullptr is equivalent to L"".</span></span> <span data-ttu-id="f2bf5-458">Описание фильтров контекста ресурсов приведено в разделе COREWEBVIEW2_WEB_RESOURCE_CONTEXT перечисление.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-458">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="f2bf5-459">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="f2bf5-459">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="f2bf5-460">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-460">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="f2bf5-461">общедоступные значения HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-461">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="f2bf5-462">Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-462">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="f2bf5-463">Параметр methodName — это полное имя метода в формате `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-463">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="f2bf5-464">Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-464">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="f2bf5-465">Метод Invoke обработчика вызывается, когда метод асинхронно завершается.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-465">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="f2bf5-466">Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-466">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="f2bf5-467">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="f2bf5-467">CapturePreview</span></span> 

<span data-ttu-id="f2bf5-468">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-468">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="f2bf5-469">Public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-469">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="f2bf5-470">Укажите формат изображения с помощью параметра imageFormat.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-470">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="f2bf5-471">Результирующие двоичные данные изображения записываются в указанный параметр imageStream.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-471">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="f2bf5-472">Когда CapturePreview закончит запись в поток, вызывается метод Invoke в указанном параметре обработчика.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-472">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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

#### <span data-ttu-id="f2bf5-473">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="f2bf5-473">ExecuteScript</span></span> 

<span data-ttu-id="f2bf5-474">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-474">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="f2bf5-475">общедоступные значения HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-475">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="f2bf5-476">Это выполняется асинхронно и по завершении, если обработчик предоставлен в параметре ExecuteScriptCompletedHandler, вызывается его метод Invoke с результатом вычисления предоставленного JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-476">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="f2bf5-477">Результирующее значение — это строка в кодировке JSON.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-477">The result value is a JSON encoded string.</span></span> <span data-ttu-id="f2bf5-478">Если результат не определен, содержит цикл ссылки или не может быть закодирован в JSON, значение NULL JSON будет возвращено в виде строки null.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-478">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="f2bf5-479">Обратите внимание, что функция без явного возвращаемого значения возвращает значение undefine.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-479">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="f2bf5-480">Если выполняемый сценарий создает необработанное исключение, результат также равен null.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-480">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="f2bf5-481">Этот метод применяется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-481">This method is applied asynchronously.</span></span> <span data-ttu-id="f2bf5-482">Если метод вызывается после события NavigationStarting во время навигации, сценарий будет выполнен в новом документе при его загрузке, вокруг которого возникает время ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-482">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="f2bf5-483">ExecuteScript будет работать даже в том случае, если IsScriptEnabled имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-483">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="f2bf5-484">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="f2bf5-484">get_BrowserProcessId</span></span> 

<span data-ttu-id="f2bf5-485">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-485">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="f2bf5-486">общедоступные значения HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-486">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="f2bf5-487">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="f2bf5-487">get_CanGoBack</span></span> 

<span data-ttu-id="f2bf5-488">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-488">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="f2bf5-489">общедоступные значения HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-489">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="f2bf5-490">Событие HistoryChanged будет срабатывать, если CanGoBack изменит значение.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-490">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="f2bf5-491">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="f2bf5-491">get_CanGoForward</span></span> 

<span data-ttu-id="f2bf5-492">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-492">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="f2bf5-493">общедоступные значения HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-493">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="f2bf5-494">Событие HistoryChanged будет срабатывать, если CanGoForward изменит значение.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-494">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="f2bf5-495">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="f2bf5-495">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="f2bf5-496">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-496">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="f2bf5-497">общедоступные значения HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-497">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="f2bf5-498">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="f2bf5-498">get_DocumentTitle</span></span> 

<span data-ttu-id="f2bf5-499">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-499">The title for the current top level document.</span></span>

> <span data-ttu-id="f2bf5-500">общедоступные значения HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-500">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="f2bf5-501">Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-501">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="f2bf5-502">get_Settings</span><span class="sxs-lookup"><span data-stu-id="f2bf5-502">get_Settings</span></span> 

<span data-ttu-id="f2bf5-503">Объект [ICoreWebView2Settings](icorewebview2settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-503">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="f2bf5-504">общедоступные значения HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \* \* параметры)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-504">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="f2bf5-505">get_Source</span><span class="sxs-lookup"><span data-stu-id="f2bf5-505">get_Source</span></span> 

<span data-ttu-id="f2bf5-506">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-506">The URI of the current top level document.</span></span>

> <span data-ttu-id="f2bf5-507">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-507">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="f2bf5-508">Это значение может изменяться в рамках обработки события SourceChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-508">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="f2bf5-509">Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-509">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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

#### <span data-ttu-id="f2bf5-510">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="f2bf5-510">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="f2bf5-511">Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-511">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="f2bf5-512">общедоступные значения HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* ресивер)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-512">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="f2bf5-513">Параметр eventName — это полное имя события в формате `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-513">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="f2bf5-514">Список событий протоколов DevTools и аргументов событий можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-514">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="f2bf5-515">GoBack</span><span class="sxs-lookup"><span data-stu-id="f2bf5-515">GoBack</span></span> 

<span data-ttu-id="f2bf5-516">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-516">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="f2bf5-517">общедоступное значение HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="f2bf5-517">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="f2bf5-518">GoForward</span><span class="sxs-lookup"><span data-stu-id="f2bf5-518">GoForward</span></span> 

<span data-ttu-id="f2bf5-519">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-519">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="f2bf5-520">общедоступные значения HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="f2bf5-520">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="f2bf5-521">Которому</span><span class="sxs-lookup"><span data-stu-id="f2bf5-521">Navigate</span></span> 

<span data-ttu-id="f2bf5-522">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="f2bf5-522">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="f2bf5-523">общедоступное значение HRESULT [навигации](#navigate)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-523">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="f2bf5-524">Дополнительные сведения приведены в разделе события навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-524">See the navigation events for more information.</span></span> <span data-ttu-id="f2bf5-525">Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-525">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

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

#### <span data-ttu-id="f2bf5-526">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="f2bf5-526">NavigateToString</span></span> 

<span data-ttu-id="f2bf5-527">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-527">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="f2bf5-528">общедоступные значения HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-528">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="f2bf5-529">Параметр htmlContent не может быть больше 2 МБ символов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-529">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="f2bf5-530">В качестве источника новой страницы будет указано пустое значение.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-530">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="f2bf5-531">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="f2bf5-531">OpenDevToolsWindow</span></span> 

<span data-ttu-id="f2bf5-532">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-532">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="f2bf5-533">общедоступные значения HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="f2bf5-533">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="f2bf5-534">Ничего не происходит, если он вызывается, когда окно DevTools уже открыто</span><span class="sxs-lookup"><span data-stu-id="f2bf5-534">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="f2bf5-535">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="f2bf5-535">PostWebMessageAsJson</span></span> 

<span data-ttu-id="f2bf5-536">Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-536">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="f2bf5-537">общедоступные значения HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-537">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="f2bf5-538">Срабатывает событие Window. Chrome. WebView для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-538">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="f2bf5-539">JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий:</span><span class="sxs-lookup"><span data-stu-id="f2bf5-539">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="f2bf5-540">Аргументы события представляют собой экземпляр `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="f2bf5-540">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="f2bf5-541">Параметр ICoreWebView2Settings:: IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-541">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="f2bf5-542">Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-542">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="f2bf5-543">Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-543">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="f2bf5-544">Сведения о том, как отправлять сообщения из HTML-документа на WebView на узел, можно найти в SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-544">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="f2bf5-545">Это сообщение отправляется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-545">This message is sent asynchronously.</span></span> <span data-ttu-id="f2bf5-546">Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-546">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="f2bf5-547">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="f2bf5-547">PostWebMessageAsString</span></span> 

<span data-ttu-id="f2bf5-548">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-548">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="f2bf5-549">общедоступные значения HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-549">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="f2bf5-550">Это выполняется точно так же, как и PostWebMessageAsJson, но `window.chrome.webview` свойство Data события ARG имеет строковое значение с тем же значением, что и webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-550">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="f2bf5-551">Используйте это вместо PostWebMessageAsJson, если вы хотите общаться с помощью простых строк, а не объектов JSON.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-551">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="f2bf5-552">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="f2bf5-552">Reload</span></span> 

<span data-ttu-id="f2bf5-553">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-553">Reload the current page.</span></span>

> <span data-ttu-id="f2bf5-554">общедоступная [Перезагрузка](#reload)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="f2bf5-554">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="f2bf5-555">Это похоже на то, что переход к URI текущего документа верхнего уровня, включая все события навигации, которые обрабатывались, и учитывает любые записи в кэше HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-555">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="f2bf5-556">Но история «назад» и «вперед» не будет изменена.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-556">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="f2bf5-557">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-557">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="f2bf5-558">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-558">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="f2bf5-559">общедоступные значения HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-559">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-560">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="f2bf5-560">remove_ContentLoading</span></span> 

<span data-ttu-id="f2bf5-561">Удалите обработчик событий, добавленный ранее add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-561">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="f2bf5-562">общедоступные значения HRESULT [remove_ContentLoading](#remove_contentloading)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-562">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-563">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-563">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="f2bf5-564">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-564">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="f2bf5-565">общедоступные значения HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-565">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-566">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="f2bf5-566">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="f2bf5-567">Удалите обработчик событий, добавленный ранее add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-567">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="f2bf5-568">общедоступные значения HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-568">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-569">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="f2bf5-569">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="f2bf5-570">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-570">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="f2bf5-571">общедоступные значения HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-571">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-572">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-572">remove_HistoryChanged</span></span> 

<span data-ttu-id="f2bf5-573">Удалите обработчик событий, добавленный ранее add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-573">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="f2bf5-574">общедоступные значения HRESULT [remove_HistoryChanged](#remove_historychanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-574">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-575">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="f2bf5-575">remove_NavigationCompleted</span></span> 

<span data-ttu-id="f2bf5-576">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-576">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="f2bf5-577">общедоступные значения HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-577">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-578">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="f2bf5-578">remove_NavigationStarting</span></span> 

<span data-ttu-id="f2bf5-579">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-579">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="f2bf5-580">общедоступные значения HRESULT [remove_NavigationStarting](#remove_navigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-580">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-581">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-581">remove_NewWindowRequested</span></span> 

<span data-ttu-id="f2bf5-582">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-582">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="f2bf5-583">общедоступные значения HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-583">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-584">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-584">remove_PermissionRequested</span></span> 

<span data-ttu-id="f2bf5-585">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-585">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="f2bf5-586">общедоступные значения HRESULT [remove_PermissionRequested](#remove_permissionrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-586">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-587">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="f2bf5-587">remove_ProcessFailed</span></span> 

<span data-ttu-id="f2bf5-588">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-588">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="f2bf5-589">общедоступные значения HRESULT [remove_ProcessFailed](#remove_processfailed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-589">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-590">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="f2bf5-590">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="f2bf5-591">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-591">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="f2bf5-592">общедоступные значения HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-592">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-593">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="f2bf5-593">remove_SourceChanged</span></span> 

<span data-ttu-id="f2bf5-594">Удалите обработчик событий, добавленный ранее add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-594">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="f2bf5-595">общедоступные значения HRESULT [remove_SourceChanged](#remove_sourcechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-595">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-596">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="f2bf5-596">remove_WebMessageReceived</span></span> 

<span data-ttu-id="f2bf5-597">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-597">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="f2bf5-598">общедоступные значения HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-598">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-599">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-599">remove_WebResourceRequested</span></span> 

<span data-ttu-id="f2bf5-600">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-600">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="f2bf5-601">общедоступные значения HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-601">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-602">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="f2bf5-602">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="f2bf5-603">Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-603">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="f2bf5-604">общедоступные значения HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-604">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f2bf5-605">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="f2bf5-605">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="f2bf5-606">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-606">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="f2bf5-607">общедоступное значение HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-607">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="f2bf5-608">Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-608">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="f2bf5-609">Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-609">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="f2bf5-610">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="f2bf5-610">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="f2bf5-611">Удалите соответствующий сценарий JavaScript, который добавляется с использованием `AddScriptToExecuteOnDocumentCreated` указанного идентификатора сценария.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-611">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>

> <span data-ttu-id="f2bf5-612">общедоступные значения HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-612">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="f2bf5-613">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="f2bf5-613">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="f2bf5-614">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-614">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="f2bf5-615">общедоступный HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-615">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="f2bf5-616">Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-616">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="f2bf5-617">Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-617">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="f2bf5-618">Stop</span><span class="sxs-lookup"><span data-stu-id="f2bf5-618">Stop</span></span> 

<span data-ttu-id="f2bf5-619">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-619">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="f2bf5-620">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="f2bf5-620">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="f2bf5-621">Не останавливает сценарии.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-621">Does not stop scripts.</span></span>

#### <span data-ttu-id="f2bf5-622">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-622">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="f2bf5-623">Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-623">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="f2bf5-624">[COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-624">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="f2bf5-625">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-625">Values</span></span>                         | <span data-ttu-id="f2bf5-626">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-626">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-627">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="f2bf5-627">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="f2bf5-628">Формат изображения PNG.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-628">PNG image format.</span></span>
<span data-ttu-id="f2bf5-629">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="f2bf5-629">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="f2bf5-630">Формат изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-630">JPEG image format.</span></span>

#### <span data-ttu-id="f2bf5-631">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="f2bf5-631">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="f2bf5-632">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-632">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="f2bf5-633">[COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-633">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="f2bf5-634">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-634">Values</span></span>                         | <span data-ttu-id="f2bf5-635">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-635">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-636">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="f2bf5-636">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="f2bf5-637">ВыWM_KEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-637">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="f2bf5-638">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="f2bf5-638">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="f2bf5-639">ВыWM_KEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-639">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="f2bf5-640">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="f2bf5-640">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="f2bf5-641">ВыWM_SYSKEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-641">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="f2bf5-642">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="f2bf5-642">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="f2bf5-643">ВыWM_SYSKEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-643">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="f2bf5-644">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="f2bf5-644">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="f2bf5-645">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-645">Reason for moving focus.</span></span>

> <span data-ttu-id="f2bf5-646">[COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-646">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="f2bf5-647">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-647">Values</span></span>                         | <span data-ttu-id="f2bf5-648">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-648">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-649">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="f2bf5-649">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="f2bf5-650">Настройка кода фокуса на WebView.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-650">Code setting focus into WebView.</span></span>
<span data-ttu-id="f2bf5-651">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-651">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="f2bf5-652">Перемещение фокуса из-за прохождения вкладки вперед.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-652">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="f2bf5-653">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="f2bf5-653">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="f2bf5-654">Перемещение фокуса из-за перемещения по табуляции назад.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-654">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="f2bf5-655">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="f2bf5-655">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="f2bf5-656">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-656">The type of a permission request.</span></span>

> <span data-ttu-id="f2bf5-657">[COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-657">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="f2bf5-658">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-658">Values</span></span>                         | <span data-ttu-id="f2bf5-659">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-659">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-660">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="f2bf5-660">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="f2bf5-661">Неизвестное разрешение.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-661">Unknown permission.</span></span>
<span data-ttu-id="f2bf5-662">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-662">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="f2bf5-663">Разрешение на запись звука.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-663">Permission to capture audio.</span></span>
<span data-ttu-id="f2bf5-664">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="f2bf5-664">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="f2bf5-665">Разрешение на захват видео.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-665">Permission to capture video.</span></span>
<span data-ttu-id="f2bf5-666">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="f2bf5-666">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="f2bf5-667">Разрешение на доступ к географической позиции.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-667">Permission to access geolocation.</span></span>
<span data-ttu-id="f2bf5-668">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="f2bf5-668">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="f2bf5-669">Разрешение на отправку веб-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-669">Permission to send web notifications.</span></span>
<span data-ttu-id="f2bf5-670">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="f2bf5-670">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="f2bf5-671">Разрешение на доступ к универсальному датчику.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-671">Permission to access generic sensor.</span></span>
<span data-ttu-id="f2bf5-672">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="f2bf5-672">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="f2bf5-673">Разрешение на чтение системного буфера обмена без жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-673">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="f2bf5-674">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-674">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="f2bf5-675">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-675">Response to a permission request.</span></span>

> <span data-ttu-id="f2bf5-676">[COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-676">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="f2bf5-677">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-677">Values</span></span>                         | <span data-ttu-id="f2bf5-678">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-678">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-679">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-679">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="f2bf5-680">Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-680">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="f2bf5-681">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="f2bf5-681">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="f2bf5-682">Предоставьте разрешение на запрос.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-682">Grant the permission request.</span></span>
<span data-ttu-id="f2bf5-683">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="f2bf5-683">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="f2bf5-684">Отказ от запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-684">Deny the permission request.</span></span>

#### <span data-ttu-id="f2bf5-685">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="f2bf5-685">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="f2bf5-686">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-686">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="f2bf5-687">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-687">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="f2bf5-688">Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="f2bf5-688">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="f2bf5-689">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="f2bf5-689">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="f2bf5-690">Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-690">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="f2bf5-691">[COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-691">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="f2bf5-692">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-692">Values</span></span>                         | <span data-ttu-id="f2bf5-693">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-693">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-694">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-694">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="f2bf5-695">Указывает, что процесс браузера неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-695">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="f2bf5-696">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-696">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="f2bf5-697">Указывает, что процесс обработки неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-697">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="f2bf5-698">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-698">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="f2bf5-699">Указывает на то, что процесс рендеринга перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-699">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="f2bf5-700">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="f2bf5-700">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="f2bf5-701">Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-701">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="f2bf5-702">[COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-702">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="f2bf5-703">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-703">Values</span></span>                         | <span data-ttu-id="f2bf5-704">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-704">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-705">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-705">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="f2bf5-706">Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-706">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="f2bf5-707">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="f2bf5-707">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="f2bf5-708">Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-708">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="f2bf5-709">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-709">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="f2bf5-710">Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-710">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="f2bf5-711">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="f2bf5-711">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="f2bf5-712">Диалоговое окно, вызываемое с помощью события JavaScript beforeunload.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-712">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="f2bf5-713">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="f2bf5-713">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="f2bf5-714">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-714">Error status values for web navigations.</span></span>

> <span data-ttu-id="f2bf5-715">[COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-715">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="f2bf5-716">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-716">Values</span></span>                         | <span data-ttu-id="f2bf5-717">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-717">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-718">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="f2bf5-718">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="f2bf5-719">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-719">An unknown error occurred.</span></span>
<span data-ttu-id="f2bf5-720">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-720">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="f2bf5-721">Общее имя сертификата SSL не совпадает с веб-адресом.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-721">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="f2bf5-722">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-722">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="f2bf5-723">Срок действия сертификата SSL истек.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-723">The SSL certificate has expired.</span></span>
<span data-ttu-id="f2bf5-724">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f2bf5-724">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="f2bf5-725">SSL-сертификат клиента включает ошибки.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-725">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="f2bf5-726">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-726">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="f2bf5-727">SSL-сертификат отозван.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-727">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="f2bf5-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="f2bf5-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="f2bf5-729">Недопустимый сертификат SSL &ndash; это может означать, что сертификат не соответствует ПИН-контактам открытого ключа для имени узла. сертификат подписан недоверенным центром или с использованием слабого алгоритма, который нарушает ограничения на имена, сертификат содержит слабый ключ, срок действия сертификата является слишком длинным, не хватает сведений об отзыве или механизме отзыва, неоднозначное имя узла, отсутствие сведений о прозрачности сертификата, или сертификат связан с [прежним корнем Symantec](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span><span class="sxs-lookup"><span data-stu-id="f2bf5-729">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="f2bf5-730">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-730">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="f2bf5-731">Узел недостижим.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-731">The host is unreachable.</span></span>
<span data-ttu-id="f2bf5-732">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-732">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="f2bf5-733">Время ожидания соединения истекло.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-733">The connection has timed out.</span></span>
<span data-ttu-id="f2bf5-734">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-734">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="f2bf5-735">Сервер вернул недопустимый или нераспознанный ответ.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-735">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="f2bf5-736">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-736">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="f2bf5-737">Соединение было прервано.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-737">The connection was aborted.</span></span>
<span data-ttu-id="f2bf5-738">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="f2bf5-738">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="f2bf5-739">Подключение было сброшено.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-739">The connection was reset.</span></span>
<span data-ttu-id="f2bf5-740">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-740">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="f2bf5-741">Соединение с Интернетом разорвано.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-741">The Internet connection has been lost.</span></span>
<span data-ttu-id="f2bf5-742">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-742">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="f2bf5-743">Не удается подключиться к конечному объекту.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-743">Cannot connect to destination.</span></span>
<span data-ttu-id="f2bf5-744">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-744">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="f2bf5-745">Не удалось разрешить указанное имя узла.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-745">Could not resolve provided host name.</span></span>
<span data-ttu-id="f2bf5-746">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-746">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="f2bf5-747">Операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-747">The operation was canceled.</span></span>
<span data-ttu-id="f2bf5-748">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="f2bf5-748">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="f2bf5-749">Перенаправление запроса завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-749">The request redirect failed.</span></span>
<span data-ttu-id="f2bf5-750">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="f2bf5-750">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="f2bf5-751">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-751">An unexpected error occurred.</span></span>

#### <span data-ttu-id="f2bf5-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="f2bf5-753">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-753">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="f2bf5-754">[COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) перечисления</span><span class="sxs-lookup"><span data-stu-id="f2bf5-754">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="f2bf5-755">Данные</span><span class="sxs-lookup"><span data-stu-id="f2bf5-755">Values</span></span>                         | <span data-ttu-id="f2bf5-756">Описания</span><span class="sxs-lookup"><span data-stu-id="f2bf5-756">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="f2bf5-757">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="f2bf5-757">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="f2bf5-758">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-758">All resources.</span></span>
<span data-ttu-id="f2bf5-759">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-759">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="f2bf5-760">Ресурсы документов.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-760">Document resources.</span></span>
<span data-ttu-id="f2bf5-761">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="f2bf5-761">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="f2bf5-762">Ресурсы CSS.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-762">CSS resources.</span></span>
<span data-ttu-id="f2bf5-763">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-763">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="f2bf5-764">Графические ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-764">Image resources.</span></span>
<span data-ttu-id="f2bf5-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="f2bf5-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="f2bf5-766">Другие мультимедийные ресурсы, например видео.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-766">Other media resources such as videos.</span></span>
<span data-ttu-id="f2bf5-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="f2bf5-768">Ресурсы шрифта.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-768">Font resources.</span></span>
<span data-ttu-id="f2bf5-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="f2bf5-770">Ресурсы сценария.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-770">Script resources.</span></span>
<span data-ttu-id="f2bf5-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="f2bf5-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="f2bf5-772">HTTP-запросы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-772">XML HTTP requests.</span></span>
<span data-ttu-id="f2bf5-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="f2bf5-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="f2bf5-774">Получение взаимодействия API.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-774">Fetch API communication.</span></span>
<span data-ttu-id="f2bf5-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="f2bf5-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="f2bf5-776">TextTrack ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-776">TextTrack resources.</span></span>
<span data-ttu-id="f2bf5-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="f2bf5-778">Взаимодействие API EventSource.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-778">EventSource API communication.</span></span>
<span data-ttu-id="f2bf5-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="f2bf5-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="f2bf5-780">Взаимодействие API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-780">WebSocket API communication.</span></span>
<span data-ttu-id="f2bf5-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="f2bf5-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="f2bf5-782">Манифесты веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-782">Web App Manifests.</span></span>
<span data-ttu-id="f2bf5-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="f2bf5-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="f2bf5-784">Обмен подписанными HTTP-сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-784">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="f2bf5-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="f2bf5-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="f2bf5-786">Запросы ping.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-786">Ping requests.</span></span>
<span data-ttu-id="f2bf5-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="f2bf5-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="f2bf5-788">Отчеты о нарушениях CSP.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-788">CSP Violation Reports.</span></span>
<span data-ttu-id="f2bf5-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="f2bf5-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="f2bf5-790">Другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f2bf5-790">Other resources.</span></span>


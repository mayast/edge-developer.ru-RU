---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d80570a82559fccb6ae3896f7543ed75959436fa
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884430"
---
# <span data-ttu-id="d04d0-104">0.9.430-Interface ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="d04d0-104">0.9.430 - interface ICoreWebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="d04d0-105">WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="d04d0-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="d04d0-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d04d0-106">Summary</span></span>

 <span data-ttu-id="d04d0-107">Участников</span><span class="sxs-lookup"><span data-stu-id="d04d0-107">Members</span></span>                        | <span data-ttu-id="d04d0-108">Описания</span><span class="sxs-lookup"><span data-stu-id="d04d0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d04d0-109">get_Settings</span><span class="sxs-lookup"><span data-stu-id="d04d0-109">get_Settings</span></span>](#get_settings) | <span data-ttu-id="d04d0-110">Объект ICoreWebView2Settings, содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-110">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="d04d0-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="d04d0-111">get_Source</span></span>](#get_source) | <span data-ttu-id="d04d0-112">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d04d0-112">The URI of the current top level document.</span></span>
[<span data-ttu-id="d04d0-113">Которому</span><span class="sxs-lookup"><span data-stu-id="d04d0-113">Navigate</span></span>](#navigate) | <span data-ttu-id="d04d0-114">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="d04d0-114">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="d04d0-115">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="d04d0-115">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="d04d0-116">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="d04d0-116">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="d04d0-117">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d04d0-117">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="d04d0-118">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-118">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="d04d0-119">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d04d0-119">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="d04d0-120">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-120">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="d04d0-121">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="d04d0-121">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="d04d0-122">Добавьте обработчик событий для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d04d0-122">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="d04d0-123">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="d04d0-123">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="d04d0-124">Удалите обработчик событий, добавленный ранее add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d04d0-124">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="d04d0-125">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-125">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="d04d0-126">SourceChanged активируется при изменении свойства Source.</span><span class="sxs-lookup"><span data-stu-id="d04d0-126">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="d04d0-127">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-127">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="d04d0-128">Удалите обработчик событий, добавленный ранее add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-128">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="d04d0-129">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-129">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="d04d0-130">Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d04d0-130">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="d04d0-131">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-131">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="d04d0-132">Удалите обработчик событий, добавленный ранее add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-132">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="d04d0-133">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="d04d0-133">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="d04d0-134">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d04d0-134">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="d04d0-135">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="d04d0-135">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="d04d0-136">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d04d0-136">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="d04d0-137">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d04d0-137">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="d04d0-138">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-138">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="d04d0-139">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d04d0-139">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="d04d0-140">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-140">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="d04d0-141">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="d04d0-141">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="d04d0-142">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d04d0-142">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="d04d0-143">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="d04d0-143">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="d04d0-144">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d04d0-144">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="d04d0-145">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-145">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="d04d0-146">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-146">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="d04d0-147">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-147">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="d04d0-148">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-148">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="d04d0-149">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="d04d0-149">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="d04d0-150">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d04d0-150">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="d04d0-151">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="d04d0-151">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="d04d0-152">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d04d0-152">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="d04d0-153">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="d04d0-153">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="d04d0-154">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="d04d0-154">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="d04d0-155">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="d04d0-155">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="d04d0-156">Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d04d0-156">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="d04d0-157">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="d04d0-157">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="d04d0-158">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-158">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="d04d0-159">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="d04d0-159">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="d04d0-160">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="d04d0-160">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="d04d0-161">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="d04d0-161">Reload</span></span>](#reload) | <span data-ttu-id="d04d0-162">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="d04d0-162">Reload the current page.</span></span>
[<span data-ttu-id="d04d0-163">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="d04d0-163">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="d04d0-164">Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-164">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="d04d0-165">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="d04d0-165">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="d04d0-166">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-166">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="d04d0-167">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="d04d0-167">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="d04d0-168">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-168">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="d04d0-169">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="d04d0-169">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="d04d0-170">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="d04d0-170">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="d04d0-171">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="d04d0-171">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="d04d0-172">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="d04d0-172">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="d04d0-173">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="d04d0-173">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="d04d0-174">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-174">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="d04d0-175">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="d04d0-175">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="d04d0-176">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-176">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="d04d0-177">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="d04d0-177">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="d04d0-178">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-178">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="d04d0-179">GoBack</span><span class="sxs-lookup"><span data-stu-id="d04d0-179">GoBack</span></span>](#goback) | <span data-ttu-id="d04d0-180">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="d04d0-180">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="d04d0-181">GoForward</span><span class="sxs-lookup"><span data-stu-id="d04d0-181">GoForward</span></span>](#goforward) | <span data-ttu-id="d04d0-182">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="d04d0-182">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="d04d0-183">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="d04d0-183">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="d04d0-184">Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="d04d0-184">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="d04d0-185">Stop</span><span class="sxs-lookup"><span data-stu-id="d04d0-185">Stop</span></span>](#stop) | <span data-ttu-id="d04d0-186">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-186">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="d04d0-187">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-187">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="d04d0-188">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-188">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="d04d0-189">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-189">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="d04d0-190">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-190">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="d04d0-191">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-191">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="d04d0-192">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-192">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="d04d0-193">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-193">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="d04d0-194">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-194">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="d04d0-195">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="d04d0-195">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="d04d0-196">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d04d0-196">The title for the current top level document.</span></span>
[<span data-ttu-id="d04d0-197">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d04d0-197">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="d04d0-198">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="d04d0-198">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="d04d0-199">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d04d0-199">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="d04d0-200">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-200">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="d04d0-201">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="d04d0-201">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="d04d0-202">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-202">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="d04d0-203">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-203">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="d04d0-204">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="d04d0-204">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="d04d0-205">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-205">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="d04d0-206">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="d04d0-206">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="d04d0-207">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="d04d0-207">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="d04d0-208">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="d04d0-208">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="d04d0-209">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-209">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="d04d0-210">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-210">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="d04d0-211">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-211">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="d04d0-212">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-212">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="d04d0-213">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="d04d0-213">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="d04d0-214">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-214">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="d04d0-215">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="d04d0-215">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="d04d0-216">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-216">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="d04d0-217">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-217">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="d04d0-218">Добавьте обработчик событий для события WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-218">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="d04d0-219">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-219">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="d04d0-220">Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-220">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="d04d0-221">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="d04d0-221">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#core_webview2_capture_preview_image_format) | <span data-ttu-id="d04d0-222">Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="d04d0-222">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="d04d0-223">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="d04d0-223">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#core_webview2_script_dialog_kind) | <span data-ttu-id="d04d0-224">Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d04d0-224">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="d04d0-225">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="d04d0-225">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#core_webview2_process_failed_kind) | <span data-ttu-id="d04d0-226">Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d04d0-226">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="d04d0-227">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="d04d0-227">CORE_WEBVIEW2_PERMISSION_KIND</span></span>](#core_webview2_permission_kind) | <span data-ttu-id="d04d0-228">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-228">The type of a permission request.</span></span>
[<span data-ttu-id="d04d0-229">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="d04d0-229">CORE_WEBVIEW2_PERMISSION_STATE</span></span>](#core_webview2_permission_state) | <span data-ttu-id="d04d0-230">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-230">Response to a permission request.</span></span>
[<span data-ttu-id="d04d0-231">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="d04d0-231">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span>](#core_webview2_web_error_status) | <span data-ttu-id="d04d0-232">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="d04d0-232">Error status values for web navigations.</span></span>
[<span data-ttu-id="d04d0-233">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="d04d0-233">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#core_webview2_web_resource_context) | <span data-ttu-id="d04d0-234">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-234">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="d04d0-235">События навигации</span><span class="sxs-lookup"><span data-stu-id="d04d0-235">Navigation events</span></span>

<span data-ttu-id="d04d0-236">Обычной последовательностью событий навигации является NavigationStarting, SourceChanged, ContentLoading, а затем NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d04d0-236">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="d04d0-238">Обратите внимание, что это для событий навигации с одинаковым событием NavigationId arg.</span><span class="sxs-lookup"><span data-stu-id="d04d0-238">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="d04d0-239">События навигации с различными аргументы события NavigationId могут перекрывать друг друга.</span><span class="sxs-lookup"><span data-stu-id="d04d0-239">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="d04d0-240">Например, если вы запускаете навигацию для события NavigationStarting, а затем запускаете другую навигацию, вы увидите NavigationStarting для первой навигации, за которой следует NavigationStarting второй переход, а затем — NavigationCompleted для первого перехода, а затем все оставшиеся события навигации для второй навигации.</span><span class="sxs-lookup"><span data-stu-id="d04d0-240">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="d04d0-241">В случае возникновения ошибок может возникнуть или не быть событием ContentLoading в зависимости от того, проявляется ли переход на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="d04d0-241">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="d04d0-242">В случае перенаправления HTTP в строке есть несколько событий NavigationStarting, для которых после первого будет задано значение параметра redirect.</span><span class="sxs-lookup"><span data-stu-id="d04d0-242">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="d04d0-243">Чтобы отслеживать или отменять навигацию внутри подкадров в WebView, используйте FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-243">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="d04d0-244">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="d04d0-244">Process model</span></span>

<span data-ttu-id="d04d0-245">WebView2 использует ту же модель процессов, что и веб-браузер EDGE.</span><span class="sxs-lookup"><span data-stu-id="d04d0-245">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="d04d0-246">В сеансе пользователя имеется один процесс браузера Edge для определенного каталога данных пользователя, который будет обрабатывать любой процесс вызова WebView2, указывающий на этот каталог данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="d04d0-246">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="d04d0-247">Это означает, что один процесс браузера Edge может обслуживать несколько процессов вызова и один процесс вызова может использовать несколько процессов браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="d04d0-247">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="d04d0-249">В процессе работы с браузером может быть некоторое количество процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="d04d0-249">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="d04d0-250">Они создаются по мере необходимости для того, чтобы обслуживать потенциально несколько кадров в разных представлениях.</span><span class="sxs-lookup"><span data-stu-id="d04d0-250">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="d04d0-251">Количество процессов обработки может различаться в зависимости от функции браузера "изоляция сайта" и количества отдельных отключенных относящихся к отсоединенным источникам, отображаемым в соответствующих веб-представлениях.</span><span class="sxs-lookup"><span data-stu-id="d04d0-251">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="d04d0-253">Вы можете реагировать на сбои и зависания в этих процессах браузера и отрисовки с помощью события ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="d04d0-253">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="d04d0-254">С помощью метода Close можно безопасно завершить работу связанных браузеров и процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="d04d0-254">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="d04d0-255">Потоковая модель</span><span class="sxs-lookup"><span data-stu-id="d04d0-255">Threading model</span></span>

<span data-ttu-id="d04d0-256">WebView2 должен создаваться в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d04d0-256">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="d04d0-257">В частности, поток с конвейером сообщений.</span><span class="sxs-lookup"><span data-stu-id="d04d0-257">Specifically a thread with a message pump.</span></span> <span data-ttu-id="d04d0-258">Все обратные вызовы будут происходить в этом потоке, и звонки в WebView должны выполняться в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="d04d0-258">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="d04d0-259">Небезопасно использовать WebView из другого потока.</span><span class="sxs-lookup"><span data-stu-id="d04d0-259">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="d04d0-260">Обратные вызовы, включая обработчики событий и обработчики завершения выполняются последовательно.</span><span class="sxs-lookup"><span data-stu-id="d04d0-260">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="d04d0-261">Это значит, что если у вас есть обработчик событий и начало цикла обработки сообщений, другие обработчики событий или обратные вызовы завершения будут запущены повторно.</span><span class="sxs-lookup"><span data-stu-id="d04d0-261">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="d04d0-262">Безопасность</span><span class="sxs-lookup"><span data-stu-id="d04d0-262">Security</span></span>

<span data-ttu-id="d04d0-263">Всегда проверяйте свойство Source объекта WebView, прежде чем использовать ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString или любой другой метод для отправки данных в WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-263">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="d04d0-264">WebView может перейти на другую страницу с помощью конечного пользователя, взаимодействующего со страницей или сценарием на странице, вызывающем навигацию.</span><span class="sxs-lookup"><span data-stu-id="d04d0-264">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="d04d0-265">Также будьте внимательны с AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d04d0-265">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="d04d0-266">Все будущие переходы запустят этот сценарий и предоставляют доступ к сведениям, предназначенным только для определенного происхождения, может быть предоставлен доступ к любому HTML-документу.</span><span class="sxs-lookup"><span data-stu-id="d04d0-266">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="d04d0-267">При исследовании результата вызова метода ExecuteScript, события WebMessageReceived, всегда следует проверять источник отправителя или любой другой механизм получения данных из HTML-документа в WebView проверять URI HTML-документа, что вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="d04d0-267">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="d04d0-268">Когда вы создаете сообщение для отправки в WebView, предпочитать использование PostWebMessageAsJson и создавайте строковый параметр JSON с помощью библиотеки JSON.</span><span class="sxs-lookup"><span data-stu-id="d04d0-268">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="d04d0-269">Это позволит избежать возможного ДТП данных в строку или сценарий JSON и убедиться, что злоумышленник, управляющий неуправляемым вводом, может изменить оставшуюся часть сообщения JSON или выполнить произвольный сценарий.</span><span class="sxs-lookup"><span data-stu-id="d04d0-269">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="d04d0-270">Типы строк</span><span class="sxs-lookup"><span data-stu-id="d04d0-270">String types</span></span>

<span data-ttu-id="d04d0-271">Выход из параметров строки: LPWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="d04d0-271">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="d04d0-272">Вызываемый объект выделяет строку с помощью функции CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="d04d0-272">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="d04d0-273">Владение передается вызывающему абоненту и вызывающему абоненту, чтобы освободить память с помощью CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="d04d0-273">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="d04d0-274">Строка в параметрах — LPCWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="d04d0-274">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="d04d0-275">Вызывающий объект гарантирует допустимость строки в течение синхронного вызова функции.</span><span class="sxs-lookup"><span data-stu-id="d04d0-275">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="d04d0-276">Если вызываемый объект должен сохранить это значение в некоторой точке после завершения вызова функции, вызываемый объект должен выделять собственную копию строкового значения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-276">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="d04d0-277">Синтаксический анализ URI и JSON</span><span class="sxs-lookup"><span data-stu-id="d04d0-277">URI and JSON parsing</span></span>

<span data-ttu-id="d04d0-278">Различные методы предоставляют или допускают URI и JSON в виде строк.</span><span class="sxs-lookup"><span data-stu-id="d04d0-278">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="d04d0-279">Для синтаксического анализа и создания этих строк используйте собственную библиотеку предпочтительных.</span><span class="sxs-lookup"><span data-stu-id="d04d0-279">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="d04d0-280">Если приложение WinRT доступно для вашего приложения, вы можете использовать для `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` анализа или создания строк JSON либо `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` для синтаксического анализа и создания URI.</span><span class="sxs-lookup"><span data-stu-id="d04d0-280">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="d04d0-281">Обе эти операции работают в приложениях Win32.</span><span class="sxs-lookup"><span data-stu-id="d04d0-281">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="d04d0-282">Если вы используете IUri и CreateUri для синтаксического анализа URI, вы можете использовать следующие флаги создания URI, чтобы поведение CreateUri более точно соответствовало синтаксическому анализу URI в WebView:</span><span class="sxs-lookup"><span data-stu-id="d04d0-282">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="d04d0-283">Отладка</span><span class="sxs-lookup"><span data-stu-id="d04d0-283">Debugging</span></span>

<span data-ttu-id="d04d0-284">Откройте DevTools с помощью стандартных сочетаний клавиш: `F12` или `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-284">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="d04d0-285">Вы можете использовать `--auto-open-devtools-for-tabs` параметр аргумента Command, чтобы окно DevTools было открыто немедленно при первом создании WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-285">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="d04d0-286">Сведения о том, как предоставить дополнительные аргументы командной строки для процесса браузера, можно найти в документации CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="d04d0-286">See CreateCoreWebView2Host documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="d04d0-287">Изучите раздел реестра LoaderOverride для использования разных сборок WebView2 без изменения вашего приложения в документации CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="d04d0-287">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Host documentation.</span></span>

## <span data-ttu-id="d04d0-288">Управление версиями</span><span class="sxs-lookup"><span data-stu-id="d04d0-288">Versioning</span></span>

<span data-ttu-id="d04d0-289">После того как вы использовали определенную версию SDK для создания приложения, ваше приложение может завершить работу с более ранней или более поздней версией установленных двоичных файлов браузера.</span><span class="sxs-lookup"><span data-stu-id="d04d0-289">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="d04d0-290">До версии 1.0.0.0 WebView2 на этапе обновления могут возрушиться изменения, которые не позволят пакету SDK работать с различными версиями установленных двоичных файлов браузера.</span><span class="sxs-lookup"><span data-stu-id="d04d0-290">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="d04d0-291">После того как версия 1.0.0.0 может работать с различными версиями пакета SDK, следуйте приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="d04d0-291">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="d04d0-292">Для учета критических изменений в API убедитесь, что при вызове функции экспорта DLL CreateCoreWebView2Environment и при вызове QueryInterface для любого объекта CoreWebView2 возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="d04d0-292">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="d04d0-293">Возвращаемое значение E_NOINTERFACE может указывать на то, что пакет SDK несовместим с двоичными файлами браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="d04d0-293">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="d04d0-294">Проверка сбоя из QueryInterface также учитывает ситуации, в которых пакет SDK более новый, чем версия браузера EDGE, и ваше приложение пытается использовать интерфейс, на котором нет браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="d04d0-294">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="d04d0-295">Если интерфейс недоступен, вы можете отключать связанный компонент, если это возможно, или иным образом информировать конечного пользователя о необходимости обновления браузера.</span><span class="sxs-lookup"><span data-stu-id="d04d0-295">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="d04d0-296">Участников</span><span class="sxs-lookup"><span data-stu-id="d04d0-296">Members</span></span>

#### <span data-ttu-id="d04d0-297">get_Settings</span><span class="sxs-lookup"><span data-stu-id="d04d0-297">get_Settings</span></span> 

<span data-ttu-id="d04d0-298">Объект ICoreWebView2Settings, содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-298">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="d04d0-299">общедоступные значения HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings \* \* параметры)</span><span class="sxs-lookup"><span data-stu-id="d04d0-299">public HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings \*\* settings)</span></span>

#### <span data-ttu-id="d04d0-300">get_Source</span><span class="sxs-lookup"><span data-stu-id="d04d0-300">get_Source</span></span> 

<span data-ttu-id="d04d0-301">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d04d0-301">The URI of the current top level document.</span></span>

> <span data-ttu-id="d04d0-302">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="d04d0-302">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="d04d0-303">Это значение может изменяться в рамках обработки события SourceChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту.</span><span class="sxs-lookup"><span data-stu-id="d04d0-303">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="d04d0-304">Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-304">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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

#### <span data-ttu-id="d04d0-305">Которому</span><span class="sxs-lookup"><span data-stu-id="d04d0-305">Navigate</span></span> 

<span data-ttu-id="d04d0-306">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="d04d0-306">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="d04d0-307">общедоступное значение HRESULT [навигации](#navigate)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d04d0-307">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="d04d0-308">Дополнительные сведения приведены в разделе события навигации.</span><span class="sxs-lookup"><span data-stu-id="d04d0-308">See the navigation events for more information.</span></span> <span data-ttu-id="d04d0-309">Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.</span><span class="sxs-lookup"><span data-stu-id="d04d0-309">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

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

#### <span data-ttu-id="d04d0-310">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="d04d0-310">NavigateToString</span></span> 

<span data-ttu-id="d04d0-311">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="d04d0-311">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="d04d0-312">общедоступные значения HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="d04d0-312">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="d04d0-313">Параметр htmlContent не может быть больше 2 МБ символов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-313">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="d04d0-314">В качестве источника новой страницы будет указано пустое значение.</span><span class="sxs-lookup"><span data-stu-id="d04d0-314">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="d04d0-315">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d04d0-315">add_NavigationStarting</span></span> 

<span data-ttu-id="d04d0-316">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-316">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="d04d0-317">общедоступные значения HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-317">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-318">NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI.</span><span class="sxs-lookup"><span data-stu-id="d04d0-318">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="d04d0-319">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="d04d0-319">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="d04d0-320">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d04d0-320">remove_NavigationStarting</span></span> 

<span data-ttu-id="d04d0-321">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-321">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="d04d0-322">общедоступные значения HRESULT [remove_NavigationStarting](#remove_navigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-322">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-323">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="d04d0-323">add_ContentLoading</span></span> 

<span data-ttu-id="d04d0-324">Добавьте обработчик событий для события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d04d0-324">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="d04d0-325">общедоступные значения HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-325">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-326">ContentLoading срабатывает перед загрузкой содержимого, в том числе сценариев, добавленных с помощью AddScriptToExecuteOnDocumentCreated ContentLoading, не будет срабатывать при выполнении одной навигации по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации).</span><span class="sxs-lookup"><span data-stu-id="d04d0-326">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="d04d0-327">Это следует за событиями NavigationStarting и SourceChanged и предшествовать событиям HistoryChanged и NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d04d0-327">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="d04d0-328">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="d04d0-328">remove_ContentLoading</span></span> 

<span data-ttu-id="d04d0-329">Удалите обработчик событий, добавленный ранее add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d04d0-329">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="d04d0-330">общедоступные значения HRESULT [remove_ContentLoading](#remove_contentloading)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-330">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-331">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-331">add_SourceChanged</span></span> 

<span data-ttu-id="d04d0-332">SourceChanged активируется при изменении свойства Source.</span><span class="sxs-lookup"><span data-stu-id="d04d0-332">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="d04d0-333">общедоступные значения HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-333">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-334">SourceChanged срабатывает для переходов на другой сайт или элементы навигации фрагментов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-334">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="d04d0-335">Она не будет срабатывать для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-335">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="d04d0-336">SourceChanged срабатывает перед ContentLoading для перехода к новому документу.</span><span class="sxs-lookup"><span data-stu-id="d04d0-336">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="d04d0-337">Добавьте обработчик событий для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-337">Add an event handler for the SourceChanged event.</span></span> 

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

#### <span data-ttu-id="d04d0-338">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-338">remove_SourceChanged</span></span> 

<span data-ttu-id="d04d0-339">Удалите обработчик событий, добавленный ранее add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-339">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="d04d0-340">общедоступные значения HRESULT [remove_SourceChanged](#remove_sourcechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-340">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-341">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-341">add_HistoryChanged</span></span> 

<span data-ttu-id="d04d0-342">Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d04d0-342">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="d04d0-343">общедоступные значения HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-343">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-344">Используйте Счетовизменение сведений об, чтобы проверить, изменилось ли get_CanGoBack/get_CanGoForward значения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-344">Use HistoryChange to check if get_CanGoBack/get_CanGoForward value has changed.</span></span> <span data-ttu-id="d04d0-345">HistoryChanged также срабатывает для использования GoBack и GoForward.</span><span class="sxs-lookup"><span data-stu-id="d04d0-345">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="d04d0-346">HistoryChanged срабатывает после SourceChanged и ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d04d0-346">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="d04d0-347">Добавьте обработчик событий для события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-347">Add an event handler for the HistoryChanged event.</span></span> 

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

#### <span data-ttu-id="d04d0-348">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-348">remove_HistoryChanged</span></span> 

<span data-ttu-id="d04d0-349">Удалите обработчик событий, добавленный ранее add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-349">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="d04d0-350">общедоступные значения HRESULT [remove_HistoryChanged](#remove_historychanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-350">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-351">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="d04d0-351">add_NavigationCompleted</span></span> 

<span data-ttu-id="d04d0-352">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d04d0-352">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="d04d0-353">общедоступные значения HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-353">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-354">Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d04d0-354">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
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

#### <span data-ttu-id="d04d0-355">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="d04d0-355">remove_NavigationCompleted</span></span> 

<span data-ttu-id="d04d0-356">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d04d0-356">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="d04d0-357">общедоступные значения HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-357">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-358">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d04d0-358">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="d04d0-359">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-359">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="d04d0-360">общедоступные значения HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-360">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-361">FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI.</span><span class="sxs-lookup"><span data-stu-id="d04d0-361">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="d04d0-362">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="d04d0-362">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="d04d0-363">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d04d0-363">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="d04d0-364">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d04d0-364">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="d04d0-365">общедоступные значения HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-365">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-366">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="d04d0-366">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="d04d0-367">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d04d0-367">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="d04d0-368">общедоступные значения HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-368">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-369">Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-369">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="d04d0-370">Это событие срабатывает только в том случае, если свойству ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled задано значение false.</span><span class="sxs-lookup"><span data-stu-id="d04d0-370">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="d04d0-371">Событие ScriptDialogOpening можно использовать, чтобы подавить диалоговые окна или заменить диалоговые окна по умолчанию пользовательскими диалоговыми окноми.</span><span class="sxs-lookup"><span data-stu-id="d04d0-371">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
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

#### <span data-ttu-id="d04d0-372">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="d04d0-372">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="d04d0-373">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d04d0-373">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="d04d0-374">общедоступные значения HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-374">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-375">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-375">add_PermissionRequested</span></span> 

<span data-ttu-id="d04d0-376">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-376">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="d04d0-377">общедоступные значения HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-377">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-378">Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="d04d0-378">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
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

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="d04d0-379">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-379">remove_PermissionRequested</span></span> 

<span data-ttu-id="d04d0-380">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-380">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="d04d0-381">общедоступные значения HRESULT [remove_PermissionRequested](#remove_permissionrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-381">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-382">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="d04d0-382">add_ProcessFailed</span></span> 

<span data-ttu-id="d04d0-383">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d04d0-383">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="d04d0-384">общедоступные значения HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-384">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-385">Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-385">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
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
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="d04d0-386">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="d04d0-386">remove_ProcessFailed</span></span> 

<span data-ttu-id="d04d0-387">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d04d0-387">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="d04d0-388">общедоступные значения HRESULT [remove_ProcessFailed](#remove_processfailed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-388">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-389">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="d04d0-389">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="d04d0-390">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="d04d0-390">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="d04d0-391">общедоступные значения HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="d04d0-391">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="d04d0-392">Вставленный сценарий будет применяться ко всем документам верхнего уровня и дочерним элементам навигации, пока они не будут удалены с помощью RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d04d0-392">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="d04d0-393">Это применяется асинхронно, и вы должны дождаться выполнения обработчика завершения, прежде чем можно будет убедиться, что сценарий готов к выполнению для навигации в будущем.</span><span class="sxs-lookup"><span data-stu-id="d04d0-393">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="d04d0-394">Обратите внимание, что если в HTML-документе есть изолированная [Среда с определенными свойствами или](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [заголовок HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , это повлияет на выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="d04d0-394">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="d04d0-395">Таким образом, например, если ключевое слово "Allow-Modal" не задано, вызовы `alert` функции будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="d04d0-395">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="d04d0-396">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="d04d0-396">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="d04d0-397">Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d04d0-397">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="d04d0-398">общедоступные значения HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d04d0-398">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="d04d0-399">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="d04d0-399">ExecuteScript</span></span> 

<span data-ttu-id="d04d0-400">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-400">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="d04d0-401">общедоступные значения HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="d04d0-401">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="d04d0-402">Это выполняется асинхронно и по завершении, если обработчик предоставлен в параметре ExecuteScriptCompletedHandler, вызывается его метод Invoke с результатом вычисления предоставленного JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-402">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="d04d0-403">Результирующее значение — это строка в кодировке JSON.</span><span class="sxs-lookup"><span data-stu-id="d04d0-403">The result value is a JSON encoded string.</span></span> <span data-ttu-id="d04d0-404">Если результат не определен, содержит цикл ссылки или не может быть закодирован в JSON, значение NULL JSON будет возвращено в виде строки null.</span><span class="sxs-lookup"><span data-stu-id="d04d0-404">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="d04d0-405">Обратите внимание, что функция без явного возвращаемого значения возвращает значение undefine.</span><span class="sxs-lookup"><span data-stu-id="d04d0-405">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="d04d0-406">Если выполняемый сценарий создает необработанное исключение, результат также равен null.</span><span class="sxs-lookup"><span data-stu-id="d04d0-406">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="d04d0-407">Этот метод применяется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d04d0-407">This method is applied asynchronously.</span></span> <span data-ttu-id="d04d0-408">Если вызов выполняется, когда WebView находится на одном документе, а переход происходит после того, как вызов выполнен, но перед выполнением JavaScript, то сценарий не будет выполнен, а обработчик будет вызван с E_FAIL для параметра errorCode.</span><span class="sxs-lookup"><span data-stu-id="d04d0-408">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="d04d0-409">ExecuteScript будет работать даже в том случае, если IsScriptEnabled имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="d04d0-409">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="d04d0-410">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="d04d0-410">CapturePreview</span></span> 

<span data-ttu-id="d04d0-411">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="d04d0-411">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="d04d0-412">Public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="d04d0-412">public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="d04d0-413">Укажите формат изображения с помощью параметра imageFormat.</span><span class="sxs-lookup"><span data-stu-id="d04d0-413">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="d04d0-414">Результирующие двоичные данные изображения записываются в указанный параметр imageStream.</span><span class="sxs-lookup"><span data-stu-id="d04d0-414">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="d04d0-415">Когда CapturePreview закончит запись в поток, вызывается метод Invoke в указанном параметре обработчика.</span><span class="sxs-lookup"><span data-stu-id="d04d0-415">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
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

#### <span data-ttu-id="d04d0-416">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="d04d0-416">Reload</span></span> 

<span data-ttu-id="d04d0-417">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="d04d0-417">Reload the current page.</span></span>

> <span data-ttu-id="d04d0-418">общедоступная [Перезагрузка](#reload)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="d04d0-418">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="d04d0-419">Это похоже на то, что переход к URI текущего документа верхнего уровня, включая все события навигации, которые обрабатывались, и учитывает любые записи в кэше HTTP.</span><span class="sxs-lookup"><span data-stu-id="d04d0-419">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="d04d0-420">Но история «назад» и «вперед» не будет изменена.</span><span class="sxs-lookup"><span data-stu-id="d04d0-420">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="d04d0-421">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="d04d0-421">PostWebMessageAsJson</span></span> 

<span data-ttu-id="d04d0-422">Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-422">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="d04d0-423">общедоступные значения HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="d04d0-423">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="d04d0-424">Срабатывает событие Window. Chrome. WebView для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d04d0-424">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="d04d0-425">JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий:</span><span class="sxs-lookup"><span data-stu-id="d04d0-425">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="d04d0-426">Аргументы события представляют собой экземпляр `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-426">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="d04d0-427">Параметр ICoreWebView2Settings:: IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d04d0-427">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="d04d0-428">Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-428">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="d04d0-429">Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект.</span><span class="sxs-lookup"><span data-stu-id="d04d0-429">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="d04d0-430">Сведения о том, как отправлять сообщения из HTML-документа на WebView на узел, можно найти в SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d04d0-430">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="d04d0-431">Это сообщение отправляется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d04d0-431">This message is sent asynchronously.</span></span> <span data-ttu-id="d04d0-432">Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.</span><span class="sxs-lookup"><span data-stu-id="d04d0-432">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="d04d0-433">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="d04d0-433">PostWebMessageAsString</span></span> 

<span data-ttu-id="d04d0-434">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-434">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="d04d0-435">общедоступные значения HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="d04d0-435">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="d04d0-436">Это выполняется точно так же, как и PostWebMessageAsJson, но `window.chrome.webview` свойство Data события ARG имеет строковое значение с тем же значением, что и webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="d04d0-436">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="d04d0-437">Используйте это вместо PostWebMessageAsJson, если вы хотите общаться с помощью простых строк, а не объектов JSON.</span><span class="sxs-lookup"><span data-stu-id="d04d0-437">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="d04d0-438">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="d04d0-438">add_WebMessageReceived</span></span> 

<span data-ttu-id="d04d0-439">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-439">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="d04d0-440">общедоступные значения HRESULT [add_WebMessageReceived](#add_webmessagereceived)(обработчик[ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-440">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-441">Функция i, в `void postMessage(object)` которой объект — это любой объект, поддерживаемый преобразованием JSON.</span><span class="sxs-lookup"><span data-stu-id="d04d0-441">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```cpp
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

 <span data-ttu-id="d04d0-442">При вызове [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) набор с помощью этого метода SetWebMessageReceivedEventHandler вызывается с помощью параметра объекта i, преобразованного в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="d04d0-442">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="d04d0-443">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="d04d0-443">remove_WebMessageReceived</span></span> 

<span data-ttu-id="d04d0-444">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="d04d0-444">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="d04d0-445">общедоступные значения HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-445">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-446">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="d04d0-446">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="d04d0-447">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="d04d0-447">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="d04d0-448">общедоступные значения HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="d04d0-448">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="d04d0-449">Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="d04d0-449">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="d04d0-450">Параметр methodName — это полное имя метода в формате `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-450">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="d04d0-451">Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода.</span><span class="sxs-lookup"><span data-stu-id="d04d0-451">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="d04d0-452">Метод Invoke обработчика вызывается, когда метод асинхронно завершается.</span><span class="sxs-lookup"><span data-stu-id="d04d0-452">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="d04d0-453">Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="d04d0-453">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="d04d0-454">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="d04d0-454">get_BrowserProcessId</span></span> 

<span data-ttu-id="d04d0-455">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-455">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="d04d0-456">общедоступные значения HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="d04d0-456">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="d04d0-457">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="d04d0-457">get_CanGoBack</span></span> 

<span data-ttu-id="d04d0-458">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-458">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="d04d0-459">общедоступные значения HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="d04d0-459">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="d04d0-460">Событие HistoryChanged будет срабатывать, если get_CanGoBack изменит значение.</span><span class="sxs-lookup"><span data-stu-id="d04d0-460">The HistoryChanged event will fire if get_CanGoBack changes value.</span></span>

#### <span data-ttu-id="d04d0-461">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="d04d0-461">get_CanGoForward</span></span> 

<span data-ttu-id="d04d0-462">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-462">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="d04d0-463">общедоступные значения HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="d04d0-463">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="d04d0-464">Событие HistoryChanged будет срабатывать, если get_CanGoForward изменит значение.</span><span class="sxs-lookup"><span data-stu-id="d04d0-464">The HistoryChanged event will fire if get_CanGoForward changes value.</span></span>

#### <span data-ttu-id="d04d0-465">GoBack</span><span class="sxs-lookup"><span data-stu-id="d04d0-465">GoBack</span></span> 

<span data-ttu-id="d04d0-466">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="d04d0-466">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="d04d0-467">общедоступное значение HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="d04d0-467">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="d04d0-468">GoForward</span><span class="sxs-lookup"><span data-stu-id="d04d0-468">GoForward</span></span> 

<span data-ttu-id="d04d0-469">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="d04d0-469">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="d04d0-470">общедоступные значения HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="d04d0-470">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="d04d0-471">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="d04d0-471">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="d04d0-472">Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="d04d0-472">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="d04d0-473">общедоступные значения HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \* \* ресивер)</span><span class="sxs-lookup"><span data-stu-id="d04d0-473">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="d04d0-474">Параметр eventName — это полное имя события в формате `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-474">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="d04d0-475">Список событий протоколов DevTools и аргументов событий можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="d04d0-475">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="d04d0-476">Stop</span><span class="sxs-lookup"><span data-stu-id="d04d0-476">Stop</span></span> 

<span data-ttu-id="d04d0-477">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-477">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="d04d0-478">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="d04d0-478">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="d04d0-479">Не останавливает сценарии.</span><span class="sxs-lookup"><span data-stu-id="d04d0-479">Does not stop scripts.</span></span>

#### <span data-ttu-id="d04d0-480">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-480">add_NewWindowRequested</span></span> 

<span data-ttu-id="d04d0-481">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-481">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="d04d0-482">общедоступные значения HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-482">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-483">Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open.</span><span class="sxs-lookup"><span data-stu-id="d04d0-483">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="d04d0-484">Приложение может передавать целевую WebView, которая будет считаться открытым окном.</span><span class="sxs-lookup"><span data-stu-id="d04d0-484">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
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

#### <span data-ttu-id="d04d0-485">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-485">remove_NewWindowRequested</span></span> 

<span data-ttu-id="d04d0-486">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-486">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="d04d0-487">общедоступные значения HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-487">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-488">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-488">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="d04d0-489">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-489">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="d04d0-490">общедоступные значения HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-490">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-491">Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d04d0-491">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="d04d0-492">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-492">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="d04d0-493">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="d04d0-493">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="d04d0-494">общедоступные значения HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-494">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-495">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="d04d0-495">get_DocumentTitle</span></span> 

<span data-ttu-id="d04d0-496">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d04d0-496">The title for the current top level document.</span></span>

> <span data-ttu-id="d04d0-497">общедоступные значения HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="d04d0-497">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="d04d0-498">Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.</span><span class="sxs-lookup"><span data-stu-id="d04d0-498">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="d04d0-499">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d04d0-499">AddRemoteObject</span></span> 

<span data-ttu-id="d04d0-500">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="d04d0-500">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="d04d0-501">общедоступные значения HRESULT [AddRemoteObject](#addremoteobject)(имя LPCWSTR, переменная \* объект)</span><span class="sxs-lookup"><span data-stu-id="d04d0-501">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="d04d0-502">Объекты узла предоставляются как прокси удаленных объектов через `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-502">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="d04d0-503">Удаленные прокси-объекты являются обещанными и разрешаются в объект, представляющий объект Host.</span><span class="sxs-lookup"><span data-stu-id="d04d0-503">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="d04d0-504">Обещание отклонено, если приложение не добавило объект с именем.</span><span class="sxs-lookup"><span data-stu-id="d04d0-504">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="d04d0-505">Когда код JavaScript обращается к свойству или методу объекта, для него возвращается значение, которое будет обрабатываться в соответствии со значением, возвращенным из хоста для свойства или метода, или отброшено в случае ошибки, например, отсутствие такого свойства или метода для объекта или параметров недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d04d0-505">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="d04d0-506">Например, когда код приложения делает следующее:</span><span class="sxs-lookup"><span data-stu-id="d04d0-506">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="d04d0-507">Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject:</span><span class="sxs-lookup"><span data-stu-id="d04d0-507">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="d04d0-508">Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d04d0-508">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="d04d0-509">Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch.</span><span class="sxs-lookup"><span data-stu-id="d04d0-509">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="d04d0-510">Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID.</span><span class="sxs-lookup"><span data-stu-id="d04d0-510">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="d04d0-511">Вложенные массивы поддерживаются до 3 уровней.</span><span class="sxs-lookup"><span data-stu-id="d04d0-511">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="d04d0-512">Массивы по типам ссылок не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d04d0-512">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="d04d0-513">VT_EMPTY и VT_NULL сопоставлены в JavaScript как null.</span><span class="sxs-lookup"><span data-stu-id="d04d0-513">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="d04d0-514">В JavaScript NULL и undefine сопоставляются с VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="d04d0-514">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="d04d0-515">Кроме того, все удаленные объекты представляются как `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-515">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="d04d0-516">Здесь объекты узла предоставляются как синхронные удаленные прокси-объекты.</span><span class="sxs-lookup"><span data-stu-id="d04d0-516">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="d04d0-517">Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста.</span><span class="sxs-lookup"><span data-stu-id="d04d0-517">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="d04d0-518">Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.remoteObjects.<name>` описанный выше.</span><span class="sxs-lookup"><span data-stu-id="d04d0-518">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="d04d0-519">Синхронные удаленные прокси-объекты и асинхронные удаленные прокси-объекты могут одновременно выполнять прокси для одного и того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d04d0-519">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="d04d0-520">Удаленные изменения, внесенные одним прокси-сервером, будут отражаться в любом другом прокси того же удаленного объекта, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.</span><span class="sxs-lookup"><span data-stu-id="d04d0-520">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="d04d0-521">Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-521">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="d04d0-522">При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="d04d0-522">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="d04d0-523">Удаленные прокси-объекты — это прокси JavaScript, который перехватывает все вызовы свойств Get, Set и Method.</span><span class="sxs-lookup"><span data-stu-id="d04d0-523">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="d04d0-524">Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="d04d0-524">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="d04d0-525">Кроме того, любое свойство или метод в массиве `chrome.webview.remoteObjects.options.forceLocalProperties` также будет выполняться локально.</span><span class="sxs-lookup"><span data-stu-id="d04d0-525">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="d04d0-526">Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-526">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="d04d0-527">При необходимости вы можете добавить в этот массив дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-527">You can add more to this array as required.</span></span>

<span data-ttu-id="d04d0-528">Существует метод `chrome.webview.remoteObjects.cleanupSome` , который лучше всего подходит для сборщиков мусора удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-528">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="d04d0-529">Удаленные прокси-объекты также обладают следующими методами, которые выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="d04d0-529">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="d04d0-530">applyRemote,-Remote, setRemote: выполняет вызов метода, свойство get или набор свойств для удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d04d0-530">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="d04d0-531">Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство.</span><span class="sxs-lookup"><span data-stu-id="d04d0-531">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="d04d0-532">Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="d04d0-532">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="d04d0-533">Но `proxy.applyRemote('toString')` выполняется `toString` на удаленном прокси-объекте.</span><span class="sxs-lookup"><span data-stu-id="d04d0-533">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="d04d0-534">"по локальной, setLocal" — выполнение свойства Get или установка свойства локально.</span><span class="sxs-lookup"><span data-stu-id="d04d0-534">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="d04d0-535">Эти методы можно использовать, чтобы принудительно получить или задать свойство в самом удаленном прокси-объекте, а не на удаленном объекте, который он представляет.</span><span class="sxs-lookup"><span data-stu-id="d04d0-535">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="d04d0-536">Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из удаленного прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="d04d0-536">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="d04d0-537">Но `proxy.getLocal('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.</span><span class="sxs-lookup"><span data-stu-id="d04d0-537">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="d04d0-538">Синхронизация: асинхронные удаленные прокси-объекты предоставляют метод синхронизации, возвращающий обещание для синхронного удаленного объектного прокси для того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d04d0-538">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="d04d0-539">Например, `chrome.webview.remoteObjects.sample.methodCall()` возвращает асинхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="d04d0-539">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="d04d0-540">Вы можете использовать этот `sync` метод, чтобы получить для него синхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="d04d0-540">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="d04d0-541">Async: синхронные удаленные прокси-объекты предоставляют метод async, который блокирует и возвращает асинхронный удаленный прокси-объект для того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d04d0-541">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="d04d0-542">Например, `chrome.webview.remoteObjects.sync.sample.methodCall()` возвращает синхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="d04d0-542">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="d04d0-543">При вызове `async` метода на этих блоках возвращается асинхронный удаленный прокси-объект для того же удаленного объекта:</span><span class="sxs-lookup"><span data-stu-id="d04d0-543">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="d04d0-544">затем: асинхронные удаленные прокси-объекты имеют метод then.</span><span class="sxs-lookup"><span data-stu-id="d04d0-544">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="d04d0-545">Это позволит им доставлять ожидающие.</span><span class="sxs-lookup"><span data-stu-id="d04d0-545">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="d04d0-546">Возвращает обещание, которое разрешается с представлением удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d04d0-546">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="d04d0-547">Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально.</span><span class="sxs-lookup"><span data-stu-id="d04d0-547">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="d04d0-548">Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания.</span><span class="sxs-lookup"><span data-stu-id="d04d0-548">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="d04d0-549">Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве удаленных прокси-объектов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-549">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="d04d0-550">Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно.</span><span class="sxs-lookup"><span data-stu-id="d04d0-550">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="d04d0-551">Асинхронные удаленные прокси-объекты возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства.</span><span class="sxs-lookup"><span data-stu-id="d04d0-551">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="d04d0-552">Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции.</span><span class="sxs-lookup"><span data-stu-id="d04d0-552">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="d04d0-553">Синхронные удаленные прокси-объекты работают точно так же, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.</span><span class="sxs-lookup"><span data-stu-id="d04d0-553">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="d04d0-554">Установка свойства для прокси-сервера асинхронного удаленного объекта немного не изменилась.</span><span class="sxs-lookup"><span data-stu-id="d04d0-554">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="d04d0-555">Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано.</span><span class="sxs-lookup"><span data-stu-id="d04d0-555">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="d04d0-556">Это требование для прокси-объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-556">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="d04d0-557">Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setRemote, который возвращает обещание, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="d04d0-557">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="d04d0-558">Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.</span><span class="sxs-lookup"><span data-stu-id="d04d0-558">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="d04d0-559">Например, предположим, что у вас есть COM-объект со следующим интерфейсом</span><span class="sxs-lookup"><span data-stu-id="d04d0-559">For example, suppose you have a COM object with the following interface</span></span>

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 <span data-ttu-id="d04d0-560">Мы можем добавить экземпляр этого интерфейса в наш сценарий JavaScript `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="d04d0-560">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="d04d0-561">В этом случае мы присвойте ему имя `sample` :</span><span class="sxs-lookup"><span data-stu-id="d04d0-561">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 <span data-ttu-id="d04d0-562">Затем в HTML-документе мы можем использовать этот COM-объект через `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="d04d0-562">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### <span data-ttu-id="d04d0-563">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d04d0-563">RemoveRemoteObject</span></span> 

<span data-ttu-id="d04d0-564">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-564">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="d04d0-565">общедоступное значение HRESULT [RemoveRemoteObject](#removeremoteobject)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d04d0-565">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="d04d0-566">Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="d04d0-566">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="d04d0-567">Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="d04d0-567">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="d04d0-568">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="d04d0-568">OpenDevToolsWindow</span></span> 

<span data-ttu-id="d04d0-569">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="d04d0-569">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="d04d0-570">общедоступные значения HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="d04d0-570">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="d04d0-571">Ничего не происходит, если он вызывается, когда окно DevTools уже открыто</span><span class="sxs-lookup"><span data-stu-id="d04d0-571">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="d04d0-572">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-572">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="d04d0-573">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="d04d0-573">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="d04d0-574">общедоступные значения HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-574">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-575">Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран.</span><span class="sxs-lookup"><span data-stu-id="d04d0-575">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="d04d0-576">Это событие полезно, если, например, элемент видео запрашивается на весь экран.</span><span class="sxs-lookup"><span data-stu-id="d04d0-576">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="d04d0-577">Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.</span><span class="sxs-lookup"><span data-stu-id="d04d0-577">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="d04d0-578">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="d04d0-578">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="d04d0-579">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="d04d0-579">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="d04d0-580">общедоступные значения HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-580">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-581">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="d04d0-581">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="d04d0-582">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="d04d0-582">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="d04d0-583">общедоступные значения HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="d04d0-583">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="d04d0-584">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-584">add_WebResourceRequested</span></span> 

<span data-ttu-id="d04d0-585">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-585">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="d04d0-586">общедоступные значения HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-586">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-587">Активируется, когда WebView выполняет запрос HTTP к соответствующему URL-адресу и фильтру контекста ресурсов, добавленному с помощью AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="d04d0-587">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="d04d0-588">Для срабатывания события необходимо добавить хотя бы один фильтр.</span><span class="sxs-lookup"><span data-stu-id="d04d0-588">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
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

#### <span data-ttu-id="d04d0-589">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-589">remove_WebResourceRequested</span></span> 

<span data-ttu-id="d04d0-590">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-590">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="d04d0-591">общедоступные значения HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-591">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-592">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="d04d0-592">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="d04d0-593">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-593">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="d04d0-594">общедоступный HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="d04d0-594">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="d04d0-595">Параметр URI может быть строкой с подстановочными знаками ("": ноль или больше; "?": только один).</span><span class="sxs-lookup"><span data-stu-id="d04d0-595">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="d04d0-596">nullptr эквивалентен L "".</span><span class="sxs-lookup"><span data-stu-id="d04d0-596">nullptr is equivalent to L"".</span></span> <span data-ttu-id="d04d0-597">Описание фильтров контекста ресурсов приведено в разделе CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT перечисление.</span><span class="sxs-lookup"><span data-stu-id="d04d0-597">See CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="d04d0-598">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="d04d0-598">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="d04d0-599">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-599">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="d04d0-600">общедоступный HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="d04d0-600">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="d04d0-601">Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного.</span><span class="sxs-lookup"><span data-stu-id="d04d0-601">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="d04d0-602">Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.</span><span class="sxs-lookup"><span data-stu-id="d04d0-602">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="d04d0-603">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-603">add_WindowCloseRequested</span></span> 

<span data-ttu-id="d04d0-604">Добавьте обработчик событий для события WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-604">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="d04d0-605">общедоступные значения HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d04d0-605">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d04d0-606">Вызывается, когда содержимое в WebView запрашивает закрытие окна, например после вызова Window. Close.</span><span class="sxs-lookup"><span data-stu-id="d04d0-606">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="d04d0-607">Приложение должно закрыть окно WebView и связанное приложение, если это понятно приложению.</span><span class="sxs-lookup"><span data-stu-id="d04d0-607">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="d04d0-608">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="d04d0-608">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="d04d0-609">Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="d04d0-609">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="d04d0-610">общедоступные значения HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d04d0-610">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d04d0-611">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="d04d0-611">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="d04d0-612">Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="d04d0-612">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="d04d0-613">[CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) перечисления</span><span class="sxs-lookup"><span data-stu-id="d04d0-613">enum [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="d04d0-614">Данные</span><span class="sxs-lookup"><span data-stu-id="d04d0-614">Values</span></span>                         | <span data-ttu-id="d04d0-615">Описания</span><span class="sxs-lookup"><span data-stu-id="d04d0-615">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d04d0-616">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="d04d0-616">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="d04d0-617">Формат изображения PNG.</span><span class="sxs-lookup"><span data-stu-id="d04d0-617">PNG image format.</span></span>
<span data-ttu-id="d04d0-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="d04d0-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="d04d0-619">Формат изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="d04d0-619">JPEG image format.</span></span>

#### <span data-ttu-id="d04d0-620">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="d04d0-620">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="d04d0-621">Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d04d0-621">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="d04d0-622">[CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="d04d0-622">enum [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="d04d0-623">Данные</span><span class="sxs-lookup"><span data-stu-id="d04d0-623">Values</span></span>                         | <span data-ttu-id="d04d0-624">Описания</span><span class="sxs-lookup"><span data-stu-id="d04d0-624">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d04d0-625">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="d04d0-625">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="d04d0-626">Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-626">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="d04d0-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="d04d0-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="d04d0-628">Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-628">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="d04d0-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="d04d0-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="d04d0-630">Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d04d0-630">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="d04d0-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="d04d0-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="d04d0-632">Диалоговое окно, вызываемое с помощью события JavaScript beforeunload.</span><span class="sxs-lookup"><span data-stu-id="d04d0-632">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="d04d0-633">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="d04d0-633">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="d04d0-634">Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d04d0-634">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="d04d0-635">[CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="d04d0-635">enum [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span></span>

 <span data-ttu-id="d04d0-636">Данные</span><span class="sxs-lookup"><span data-stu-id="d04d0-636">Values</span></span>                         | <span data-ttu-id="d04d0-637">Описания</span><span class="sxs-lookup"><span data-stu-id="d04d0-637">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d04d0-638">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="d04d0-638">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="d04d0-639">Указывает, что процесс браузера неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="d04d0-639">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="d04d0-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="d04d0-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="d04d0-641">Указывает, что процесс обработки неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="d04d0-641">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="d04d0-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="d04d0-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="d04d0-643">Указывает на то, что процесс рендеринга перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-643">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="d04d0-644">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="d04d0-644">CORE_WEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="d04d0-645">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-645">The type of a permission request.</span></span>

> <span data-ttu-id="d04d0-646">[CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="d04d0-646">enum [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span></span>

 <span data-ttu-id="d04d0-647">Данные</span><span class="sxs-lookup"><span data-stu-id="d04d0-647">Values</span></span>                         | <span data-ttu-id="d04d0-648">Описания</span><span class="sxs-lookup"><span data-stu-id="d04d0-648">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d04d0-649">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="d04d0-649">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="d04d0-650">Неизвестное разрешение.</span><span class="sxs-lookup"><span data-stu-id="d04d0-650">Unknown permission.</span></span>
<span data-ttu-id="d04d0-651">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="d04d0-651">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="d04d0-652">Разрешение на запись звука.</span><span class="sxs-lookup"><span data-stu-id="d04d0-652">Permission to capture audio.</span></span>
<span data-ttu-id="d04d0-653">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="d04d0-653">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="d04d0-654">Разрешение на захват видео.</span><span class="sxs-lookup"><span data-stu-id="d04d0-654">Permission to capture video.</span></span>
<span data-ttu-id="d04d0-655">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="d04d0-655">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="d04d0-656">Разрешение на доступ к географической позиции.</span><span class="sxs-lookup"><span data-stu-id="d04d0-656">Permission to access geolocation.</span></span>
<span data-ttu-id="d04d0-657">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="d04d0-657">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="d04d0-658">Разрешение на отправку веб-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d04d0-658">Permission to send web notifications.</span></span>
<span data-ttu-id="d04d0-659">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="d04d0-659">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="d04d0-660">Разрешение на доступ к универсальному датчику.</span><span class="sxs-lookup"><span data-stu-id="d04d0-660">Permission to access generic sensor.</span></span>
<span data-ttu-id="d04d0-661">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="d04d0-661">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="d04d0-662">Разрешение на чтение системного буфера обмена без жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="d04d0-662">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="d04d0-663">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="d04d0-663">CORE_WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="d04d0-664">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-664">Response to a permission request.</span></span>

> <span data-ttu-id="d04d0-665">[CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) перечисления</span><span class="sxs-lookup"><span data-stu-id="d04d0-665">enum [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span></span>

 <span data-ttu-id="d04d0-666">Данные</span><span class="sxs-lookup"><span data-stu-id="d04d0-666">Values</span></span>                         | <span data-ttu-id="d04d0-667">Описания</span><span class="sxs-lookup"><span data-stu-id="d04d0-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d04d0-668">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d04d0-668">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="d04d0-669">Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.</span><span class="sxs-lookup"><span data-stu-id="d04d0-669">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="d04d0-670">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="d04d0-670">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="d04d0-671">Предоставьте разрешение на запрос.</span><span class="sxs-lookup"><span data-stu-id="d04d0-671">Grant the permission request.</span></span>
<span data-ttu-id="d04d0-672">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="d04d0-672">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="d04d0-673">Отказ от запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-673">Deny the permission request.</span></span>

#### <span data-ttu-id="d04d0-674">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="d04d0-674">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="d04d0-675">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="d04d0-675">Error status values for web navigations.</span></span>

> <span data-ttu-id="d04d0-676">[CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) перечисления</span><span class="sxs-lookup"><span data-stu-id="d04d0-676">enum [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span></span>

 <span data-ttu-id="d04d0-677">Данные</span><span class="sxs-lookup"><span data-stu-id="d04d0-677">Values</span></span>                         | <span data-ttu-id="d04d0-678">Описания</span><span class="sxs-lookup"><span data-stu-id="d04d0-678">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d04d0-679">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="d04d0-679">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="d04d0-680">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d04d0-680">An unknown error occurred.</span></span>
<span data-ttu-id="d04d0-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="d04d0-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="d04d0-682">Общее имя сертификата SSL не совпадает с веб-адресом.</span><span class="sxs-lookup"><span data-stu-id="d04d0-682">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="d04d0-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="d04d0-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="d04d0-684">Срок действия сертификата SSL истек.</span><span class="sxs-lookup"><span data-stu-id="d04d0-684">The SSL certificate has expired.</span></span>
<span data-ttu-id="d04d0-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d04d0-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="d04d0-686">SSL-сертификат клиента включает ошибки.</span><span class="sxs-lookup"><span data-stu-id="d04d0-686">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="d04d0-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="d04d0-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="d04d0-688">SSL-сертификат отозван.</span><span class="sxs-lookup"><span data-stu-id="d04d0-688">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="d04d0-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="d04d0-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="d04d0-690">Недопустимый сертификат SSL &ndash; это может означать, что сертификат не соответствует ПИН-контактам открытого ключа для имени узла. сертификат подписан недоверенным центром или с использованием слабого алгоритма, который нарушает ограничения на имена, сертификат содержит слабый ключ, срок действия сертификата является слишком длинным, не хватает сведений об отзыве или механизме отзыва, неоднозначное имя узла, отсутствие сведений о прозрачности сертификата, или сертификат связан с [прежним корнем Symantec](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span><span class="sxs-lookup"><span data-stu-id="d04d0-690">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="d04d0-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="d04d0-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="d04d0-692">Узел недостижим.</span><span class="sxs-lookup"><span data-stu-id="d04d0-692">The host is unreachable.</span></span>
<span data-ttu-id="d04d0-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d04d0-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="d04d0-694">Время ожидания соединения истекло.</span><span class="sxs-lookup"><span data-stu-id="d04d0-694">The connection has timed out.</span></span>
<span data-ttu-id="d04d0-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="d04d0-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="d04d0-696">Сервер вернул недопустимый или нераспознанный ответ.</span><span class="sxs-lookup"><span data-stu-id="d04d0-696">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="d04d0-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="d04d0-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="d04d0-698">Соединение было прервано.</span><span class="sxs-lookup"><span data-stu-id="d04d0-698">The connection was aborted.</span></span>
<span data-ttu-id="d04d0-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="d04d0-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="d04d0-700">Подключение было сброшено.</span><span class="sxs-lookup"><span data-stu-id="d04d0-700">The connection was reset.</span></span>
<span data-ttu-id="d04d0-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="d04d0-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="d04d0-702">Соединение с Интернетом разорвано.</span><span class="sxs-lookup"><span data-stu-id="d04d0-702">The Internet connection has been lost.</span></span>
<span data-ttu-id="d04d0-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="d04d0-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="d04d0-704">Не удается подключиться к конечному объекту.</span><span class="sxs-lookup"><span data-stu-id="d04d0-704">Cannot connect to destination.</span></span>
<span data-ttu-id="d04d0-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="d04d0-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="d04d0-706">Не удалось разрешить указанное имя узла.</span><span class="sxs-lookup"><span data-stu-id="d04d0-706">Could not resolve provided host name.</span></span>
<span data-ttu-id="d04d0-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="d04d0-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="d04d0-708">Операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="d04d0-708">The operation was canceled.</span></span>
<span data-ttu-id="d04d0-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="d04d0-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="d04d0-710">Перенаправление запроса завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="d04d0-710">The request redirect failed.</span></span>
<span data-ttu-id="d04d0-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="d04d0-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="d04d0-712">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d04d0-712">An unexpected error occurred.</span></span>

#### <span data-ttu-id="d04d0-713">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="d04d0-713">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="d04d0-714">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-714">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="d04d0-715">[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) перечисления</span><span class="sxs-lookup"><span data-stu-id="d04d0-715">enum [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span></span>

 <span data-ttu-id="d04d0-716">Данные</span><span class="sxs-lookup"><span data-stu-id="d04d0-716">Values</span></span>                         | <span data-ttu-id="d04d0-717">Описания</span><span class="sxs-lookup"><span data-stu-id="d04d0-717">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d04d0-718">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="d04d0-718">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="d04d0-719">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-719">All resources.</span></span>
<span data-ttu-id="d04d0-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="d04d0-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="d04d0-721">Ресурсы документов.</span><span class="sxs-lookup"><span data-stu-id="d04d0-721">Document resources.</span></span>
<span data-ttu-id="d04d0-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="d04d0-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="d04d0-723">Ресурсы CSS.</span><span class="sxs-lookup"><span data-stu-id="d04d0-723">CSS resources.</span></span>
<span data-ttu-id="d04d0-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="d04d0-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="d04d0-725">Графические ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-725">Image resources.</span></span>
<span data-ttu-id="d04d0-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="d04d0-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="d04d0-727">Другие мультимедийные ресурсы, например видео.</span><span class="sxs-lookup"><span data-stu-id="d04d0-727">Other media resources such as videos.</span></span>
<span data-ttu-id="d04d0-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="d04d0-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="d04d0-729">Ресурсы шрифта.</span><span class="sxs-lookup"><span data-stu-id="d04d0-729">Font resources.</span></span>
<span data-ttu-id="d04d0-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="d04d0-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="d04d0-731">Ресурсы сценария.</span><span class="sxs-lookup"><span data-stu-id="d04d0-731">Script resources.</span></span>
<span data-ttu-id="d04d0-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="d04d0-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="d04d0-733">HTTP-запросы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-733">XML HTTP requests.</span></span>
<span data-ttu-id="d04d0-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="d04d0-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="d04d0-735">Получение взаимодействия API.</span><span class="sxs-lookup"><span data-stu-id="d04d0-735">Fetch API communication.</span></span>
<span data-ttu-id="d04d0-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="d04d0-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="d04d0-737">TextTrack ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-737">TextTrack resources.</span></span>
<span data-ttu-id="d04d0-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="d04d0-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="d04d0-739">Взаимодействие API EventSource.</span><span class="sxs-lookup"><span data-stu-id="d04d0-739">EventSource API communication.</span></span>
<span data-ttu-id="d04d0-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="d04d0-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="d04d0-741">Взаимодействие API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="d04d0-741">WebSocket API communication.</span></span>
<span data-ttu-id="d04d0-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="d04d0-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="d04d0-743">Манифесты веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d04d0-743">Web App Manifests.</span></span>
<span data-ttu-id="d04d0-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="d04d0-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="d04d0-745">Обмен подписанными HTTP-сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d04d0-745">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="d04d0-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="d04d0-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="d04d0-747">Запросы ping.</span><span class="sxs-lookup"><span data-stu-id="d04d0-747">Ping requests.</span></span>
<span data-ttu-id="d04d0-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="d04d0-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="d04d0-749">Отчеты о нарушениях CSP.</span><span class="sxs-lookup"><span data-stu-id="d04d0-749">CSP Violation Reports.</span></span>
<span data-ttu-id="d04d0-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="d04d0-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="d04d0-751">Другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d04d0-751">Other resources.</span></span>

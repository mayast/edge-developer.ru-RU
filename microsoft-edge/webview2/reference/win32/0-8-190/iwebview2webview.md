---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 5711a1dbf501df55fefc9709763c1fe225865e11
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886432"
---
# <span data-ttu-id="2cd39-104">0.8.355-Interface IWebView2WebView</span><span class="sxs-lookup"><span data-stu-id="2cd39-104">0.8.355 - interface IWebView2WebView</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView
  : public IUnknown
```

<span data-ttu-id="2cd39-105">WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="2cd39-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="2cd39-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2cd39-106">Summary</span></span>

 <span data-ttu-id="2cd39-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2cd39-107">Members</span></span>                        | <span data-ttu-id="2cd39-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2cd39-109">get_Settings</span><span class="sxs-lookup"><span data-stu-id="2cd39-109">get_Settings</span></span>](#get_settings) | <span data-ttu-id="2cd39-110">Объект [IWebView2Settings](IWebView2Settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-110">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="2cd39-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="2cd39-111">get_Source</span></span>](#get_source) | <span data-ttu-id="2cd39-112">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="2cd39-112">The URI of the current top level document.</span></span>
[<span data-ttu-id="2cd39-113">Которому</span><span class="sxs-lookup"><span data-stu-id="2cd39-113">Navigate</span></span>](#navigate) | <span data-ttu-id="2cd39-114">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="2cd39-114">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="2cd39-115">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-115">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="2cd39-116">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-116">Move focus into WebView.</span></span>
[<span data-ttu-id="2cd39-117">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="2cd39-117">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="2cd39-118">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="2cd39-118">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="2cd39-119">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2cd39-119">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="2cd39-120">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2cd39-120">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="2cd39-121">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2cd39-121">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="2cd39-122">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2cd39-122">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="2cd39-123">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="2cd39-123">add_DocumentStateChanged</span></span>](#add_documentstatechanged) | <span data-ttu-id="2cd39-124">Добавьте обработчик событий для события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-124">Add an event handler for the DocumentStateChanged event.</span></span>
[<span data-ttu-id="2cd39-125">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="2cd39-125">remove_DocumentStateChanged</span></span>](#remove_documentstatechanged) | <span data-ttu-id="2cd39-126">Удалите обработчик событий, добавленный ранее add_DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-126">Remove an event handler previously added with add_DocumentStateChanged.</span></span>
[<span data-ttu-id="2cd39-127">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2cd39-127">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="2cd39-128">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2cd39-128">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="2cd39-129">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2cd39-129">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="2cd39-130">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2cd39-130">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="2cd39-131">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2cd39-131">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="2cd39-132">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2cd39-132">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="2cd39-133">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2cd39-133">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="2cd39-134">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2cd39-134">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="2cd39-135">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-135">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="2cd39-136">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-136">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="2cd39-137">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-137">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="2cd39-138">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-138">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="2cd39-139">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-139">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="2cd39-140">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="2cd39-140">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="2cd39-141">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-141">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="2cd39-142">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="2cd39-142">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="2cd39-143">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-143">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="2cd39-144">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="2cd39-144">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="2cd39-145">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-145">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="2cd39-146">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="2cd39-146">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="2cd39-147">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="2cd39-147">add_WebResourceRequested_deprecated</span></span>](#add_webresourcerequested_deprecated) | <span data-ttu-id="2cd39-148">Этот API будет устаревшим, воспользуйтесь новым add_WebResourceRequested API.</span><span class="sxs-lookup"><span data-stu-id="2cd39-148">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>
[<span data-ttu-id="2cd39-149">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-149">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="2cd39-150">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-150">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="2cd39-151">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="2cd39-151">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="2cd39-152">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2cd39-152">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="2cd39-153">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="2cd39-153">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="2cd39-154">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2cd39-154">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="2cd39-155">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="2cd39-155">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="2cd39-156">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-156">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="2cd39-157">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="2cd39-157">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="2cd39-158">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-158">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="2cd39-159">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-159">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="2cd39-160">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-160">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="2cd39-161">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-161">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="2cd39-162">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-162">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="2cd39-163">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="2cd39-163">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="2cd39-164">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2cd39-164">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="2cd39-165">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="2cd39-165">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="2cd39-166">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2cd39-166">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="2cd39-167">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="2cd39-167">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="2cd39-168">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="2cd39-168">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="2cd39-169">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="2cd39-169">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="2cd39-170">Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2cd39-170">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="2cd39-171">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="2cd39-171">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="2cd39-172">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-172">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="2cd39-173">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="2cd39-173">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="2cd39-174">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="2cd39-174">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="2cd39-175">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="2cd39-175">Reload</span></span>](#reload) | <span data-ttu-id="2cd39-176">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="2cd39-176">Reload the current page.</span></span>
[<span data-ttu-id="2cd39-177">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="2cd39-177">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="2cd39-178">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-178">The webview bounds.</span></span>
[<span data-ttu-id="2cd39-179">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="2cd39-179">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="2cd39-180">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="2cd39-180">Set the Bounds property.</span></span>
[<span data-ttu-id="2cd39-181">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="2cd39-181">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="2cd39-182">Коэффициент увеличения для текущей страницы в WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-182">The zoom factor for the current page in the WebView.</span></span>
[<span data-ttu-id="2cd39-183">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="2cd39-183">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="2cd39-184">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="2cd39-184">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="2cd39-185">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="2cd39-185">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="2cd39-186">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-186">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="2cd39-187">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="2cd39-187">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="2cd39-188">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="2cd39-188">Set the IsVisible property.</span></span>
[<span data-ttu-id="2cd39-189">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="2cd39-189">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="2cd39-190">Опубликуйте указанное сообщение в документе верхнего уровня в этом [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="2cd39-190">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>
[<span data-ttu-id="2cd39-191">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="2cd39-191">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="2cd39-192">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2cd39-192">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="2cd39-193">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2cd39-193">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="2cd39-194">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="2cd39-194">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="2cd39-195">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2cd39-195">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="2cd39-196">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="2cd39-196">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="2cd39-197">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="2cd39-197">Close</span></span>](#close) | <span data-ttu-id="2cd39-198">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="2cd39-198">Closes the webview and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="2cd39-199">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="2cd39-199">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="2cd39-200">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="2cd39-200">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="2cd39-201">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="2cd39-201">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="2cd39-202">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="2cd39-202">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="2cd39-203">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="2cd39-203">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="2cd39-204">Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="2cd39-204">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>
[<span data-ttu-id="2cd39-205">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="2cd39-205">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="2cd39-206">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-206">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="2cd39-207">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="2cd39-207">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="2cd39-208">Можно переходить по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-208">Can navigate the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="2cd39-209">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="2cd39-209">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="2cd39-210">Можно переходить по WebView на следующую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-210">Can navigate the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="2cd39-211">GoBack</span><span class="sxs-lookup"><span data-stu-id="2cd39-211">GoBack</span></span>](#goback) | <span data-ttu-id="2cd39-212">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-212">Navigates the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="2cd39-213">GoForward</span><span class="sxs-lookup"><span data-stu-id="2cd39-213">GoForward</span></span>](#goforward) | <span data-ttu-id="2cd39-214">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-214">Navigates the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="2cd39-215">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="2cd39-215">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#webview2_capture_preview_image_format) | <span data-ttu-id="2cd39-216">Формат изображения, используемый в методе [IWebView2WebView:: CapturePreview](#capturepreview) .</span><span class="sxs-lookup"><span data-stu-id="2cd39-216">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>
[<span data-ttu-id="2cd39-217">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="2cd39-217">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#webview2_script_dialog_kind) | <span data-ttu-id="2cd39-218">Диалоговое окно вида JavaScript, используемое в интерфейсе [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd39-218">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>
[<span data-ttu-id="2cd39-219">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="2cd39-219">WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#webview2_process_failed_kind) | <span data-ttu-id="2cd39-220">Состояние сбоя процесса, используемого в интерфейсе [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd39-220">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>
[<span data-ttu-id="2cd39-221">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="2cd39-221">WEBVIEW2_PERMISSION_TYPE</span></span>](#webview2_permission_type) | <span data-ttu-id="2cd39-222">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-222">The type of a permission request.</span></span>
[<span data-ttu-id="2cd39-223">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="2cd39-223">WEBVIEW2_PERMISSION_STATE</span></span>](#webview2_permission_state) | <span data-ttu-id="2cd39-224">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-224">Response to a permission request.</span></span>
[<span data-ttu-id="2cd39-225">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="2cd39-225">WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#webview2_move_focus_reason) | <span data-ttu-id="2cd39-226">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="2cd39-226">Reason for moving focus.</span></span>
[<span data-ttu-id="2cd39-227">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="2cd39-227">WEBVIEW2_WEB_ERROR_STATUS</span></span>](#webview2_web_error_status) | <span data-ttu-id="2cd39-228">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="2cd39-228">Error status values for web navigations.</span></span>
[<span data-ttu-id="2cd39-229">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="2cd39-229">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#webview2_web_resource_context) | <span data-ttu-id="2cd39-230">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cd39-230">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="2cd39-231">События навигации</span><span class="sxs-lookup"><span data-stu-id="2cd39-231">Navigation events</span></span>

<span data-ttu-id="2cd39-232">Обычной последовательностью событий навигации является NavigationStarting, DocumentStateChanged и NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2cd39-232">The normal sequence of navigation events is NavigationStarting, DocumentStateChanged and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="2cd39-234">Обратите внимание, что это для событий навигации с одинаковым событием NavigationId arg.</span><span class="sxs-lookup"><span data-stu-id="2cd39-234">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="2cd39-235">События навигации с различными аргументы события NavigationId могут перекрывать друг друга.</span><span class="sxs-lookup"><span data-stu-id="2cd39-235">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="2cd39-236">Например, если вы запускаете навигацию для события NavigationStarting, а затем запускаете другую навигацию, вы увидите NavigationStarting для первой навигации, за которой следует NavigationStarting второй переход, а затем — NavigationCompleted для первого перехода, а затем все оставшиеся события навигации для второй навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-236">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="2cd39-237">В случае возникновения ошибок может возникнуть или не быть событием DocumentStateChanged в зависимости от того, проявляется ли переход на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="2cd39-237">In error cases there may or may not be a DocumentStateChanged event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="2cd39-238">В случае перенаправления HTTP в строке есть несколько событий NavigationStarting, для которых после первого будет задано значение параметра redirect.</span><span class="sxs-lookup"><span data-stu-id="2cd39-238">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="2cd39-239">Для подразделов внутри WebView создается только событие NavigationStarting, которое дает узлу возможность блокировать навигацию по подфреймам.</span><span class="sxs-lookup"><span data-stu-id="2cd39-239">For subframes inside WebView, the only navigation event fired is the NavigationStarting event which gives host the ability to block subframe navigations.</span></span>

## <span data-ttu-id="2cd39-240">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="2cd39-240">Process model</span></span>

<span data-ttu-id="2cd39-241">WebView2 использует ту же модель процессов, что и веб-браузер EDGE.</span><span class="sxs-lookup"><span data-stu-id="2cd39-241">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="2cd39-242">В сеансе пользователя имеется один процесс браузера Edge для определенного каталога данных пользователя, который будет обрабатывать любой процесс вызова WebView2, указывающий на этот каталог данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="2cd39-242">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="2cd39-243">Это означает, что один процесс браузера Edge может обслуживать несколько процессов вызова и один процесс вызова может использовать несколько процессов браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="2cd39-243">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="2cd39-245">В процессе работы с браузером может быть некоторое количество процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="2cd39-245">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="2cd39-246">Они создаются по мере необходимости для того, чтобы обслуживать потенциально несколько кадров в разных представлениях.</span><span class="sxs-lookup"><span data-stu-id="2cd39-246">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="2cd39-247">Количество процессов обработки может различаться в зависимости от функции браузера "изоляция сайта" и количества отдельных отключенных относящихся к отсоединенным источникам, отображаемым в соответствующих веб-представлениях.</span><span class="sxs-lookup"><span data-stu-id="2cd39-247">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="2cd39-249">Вы можете реагировать на сбои и зависания в этих процессах браузера и отрисовки с помощью события ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="2cd39-249">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="2cd39-250">С помощью метода Close можно безопасно завершить работу связанных браузеров и процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="2cd39-250">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="2cd39-251">Потоковая модель</span><span class="sxs-lookup"><span data-stu-id="2cd39-251">Threading model</span></span>

<span data-ttu-id="2cd39-252">WebView2 должен создаваться в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2cd39-252">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="2cd39-253">В частности, поток с конвейером сообщений.</span><span class="sxs-lookup"><span data-stu-id="2cd39-253">Specifically a thread with a message pump.</span></span> <span data-ttu-id="2cd39-254">Все обратные вызовы будут происходить в этом потоке, и звонки в WebView должны выполняться в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="2cd39-254">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="2cd39-255">Небезопасно использовать WebView из другого потока.</span><span class="sxs-lookup"><span data-stu-id="2cd39-255">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="2cd39-256">Обратные вызовы, включая обработчики событий и обработчики завершения выполняются последовательно.</span><span class="sxs-lookup"><span data-stu-id="2cd39-256">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="2cd39-257">Это значит, что если у вас есть обработчик событий и начало цикла обработки сообщений, другие обработчики событий или обратные вызовы завершения будут запущены повторно.</span><span class="sxs-lookup"><span data-stu-id="2cd39-257">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="2cd39-258">Безопасность</span><span class="sxs-lookup"><span data-stu-id="2cd39-258">Security</span></span>

<span data-ttu-id="2cd39-259">Всегда проверяйте свойство Source объекта WebView, прежде чем использовать ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString или любой другой метод для отправки данных в WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-259">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="2cd39-260">WebView может перейти на другую страницу с помощью конечного пользователя, взаимодействующего со страницей или сценарием на странице, вызывающем навигацию.</span><span class="sxs-lookup"><span data-stu-id="2cd39-260">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="2cd39-261">Также будьте внимательны с AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2cd39-261">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="2cd39-262">Все будущие переходы запустят этот сценарий и предоставляют доступ к сведениям, предназначенным только для определенного происхождения, может быть предоставлен доступ к любому HTML-документу.</span><span class="sxs-lookup"><span data-stu-id="2cd39-262">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="2cd39-263">При исследовании результата вызова метода ExecuteScript, события WebMessageReceived, всегда следует проверять источник отправителя или любой другой механизм получения данных из HTML-документа в WebView проверять URI HTML-документа, что вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="2cd39-263">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="2cd39-264">Когда вы создаете сообщение для отправки в WebView, предпочитать использование PostWebMessageAsJson и создавайте строковый параметр JSON с помощью библиотеки JSON.</span><span class="sxs-lookup"><span data-stu-id="2cd39-264">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="2cd39-265">Это позволит избежать возможного ДТП данных в строку или сценарий JSON и убедиться, что злоумышленник, управляющий неуправляемым вводом, может изменить оставшуюся часть сообщения JSON или выполнить произвольный сценарий.</span><span class="sxs-lookup"><span data-stu-id="2cd39-265">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="2cd39-266">Типы строк</span><span class="sxs-lookup"><span data-stu-id="2cd39-266">String types</span></span>

<span data-ttu-id="2cd39-267">Выход из параметров строки: LPWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="2cd39-267">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="2cd39-268">Вызываемый объект выделяет строку с помощью функции CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="2cd39-268">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="2cd39-269">Владение передается вызывающему абоненту и вызывающему абоненту, чтобы освободить память с помощью CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="2cd39-269">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="2cd39-270">Строка в параметрах — LPCWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="2cd39-270">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="2cd39-271">Вызывающий объект гарантирует допустимость строки в течение синхронного вызова функции.</span><span class="sxs-lookup"><span data-stu-id="2cd39-271">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="2cd39-272">Если вызываемый объект должен сохранить это значение в некоторой точке после завершения вызова функции, вызываемый объект должен выделять собственную копию строкового значения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-272">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="2cd39-273">Синтаксический анализ URI и JSON</span><span class="sxs-lookup"><span data-stu-id="2cd39-273">URI and JSON parsing</span></span>

<span data-ttu-id="2cd39-274">Различные методы предоставляют или допускают URI и JSON в виде строк.</span><span class="sxs-lookup"><span data-stu-id="2cd39-274">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="2cd39-275">Для синтаксического анализа и создания этих строк используйте собственную библиотеку предпочтительных.</span><span class="sxs-lookup"><span data-stu-id="2cd39-275">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="2cd39-276">Если приложение WinRT доступно для вашего приложения, вы можете использовать для `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` анализа или создания строк JSON либо `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` для синтаксического анализа и создания URI.</span><span class="sxs-lookup"><span data-stu-id="2cd39-276">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="2cd39-277">Обе эти операции работают в приложениях Win32.</span><span class="sxs-lookup"><span data-stu-id="2cd39-277">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="2cd39-278">Если вы используете IUri и CreateUri для синтаксического анализа URI, вы можете использовать следующие флаги создания URI, чтобы поведение CreateUri более точно соответствовало синтаксическому анализу URI в WebView:</span><span class="sxs-lookup"><span data-stu-id="2cd39-278">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="2cd39-279">Отладка</span><span class="sxs-lookup"><span data-stu-id="2cd39-279">Debugging</span></span>

<span data-ttu-id="2cd39-280">Откройте DevTools с помощью стандартных сочетаний клавиш: `F12` или `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="2cd39-280">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="2cd39-281">Вы можете использовать `--auto-open-devtools-for-tabs` параметр аргумента Command, чтобы окно DevTools было открыто немедленно при первом создании WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-281">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="2cd39-282">Сведения о том, как предоставить дополнительные аргументы командной строки для процесса браузера, можно найти в документации CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-282">See CreateWebView documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="2cd39-283">Изучите раздел реестра LoaderOverride для использования разных сборок WebView2 без изменения вашего приложения в документации CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-283">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateWebView documentation.</span></span>

## <span data-ttu-id="2cd39-284">Управление версиями</span><span class="sxs-lookup"><span data-stu-id="2cd39-284">Versioning</span></span>

<span data-ttu-id="2cd39-285">После того как вы использовали определенную версию SDK для создания приложения, ваше приложение может завершить работу с более ранней или более поздней версией установленных двоичных файлов браузера.</span><span class="sxs-lookup"><span data-stu-id="2cd39-285">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="2cd39-286">До версии 1.0.0.0 WebView2 на этапе обновления могут возрушиться изменения, которые не позволят пакету SDK работать с различными версиями установленных двоичных файлов браузера.</span><span class="sxs-lookup"><span data-stu-id="2cd39-286">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="2cd39-287">После того как версия 1.0.0.0 может работать с различными версиями пакета SDK, следуйте приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="2cd39-287">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="2cd39-288">Для учета критических изменений в API убедитесь, что при вызове функции экспорта DLL CreateWebView2Environment и при вызове QueryInterface для любого объекта WebView2 возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="2cd39-288">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateWebView2Environment and when calling QueryInterface on any WebView2 object.</span></span> <span data-ttu-id="2cd39-289">Возвращаемое значение E_NOINTERFACE может указывать на то, что пакет SDK несовместим с двоичными файлами браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="2cd39-289">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="2cd39-290">Проверка сбоя из QueryInterface также учитывает ситуации, в которых пакет SDK более новый, чем версия браузера EDGE, и ваше приложение пытается использовать интерфейс, на котором нет браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="2cd39-290">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="2cd39-291">Если интерфейс недоступен, вы можете отключать связанный компонент, если это возможно, или иным образом информировать конечного пользователя о необходимости обновления браузера.</span><span class="sxs-lookup"><span data-stu-id="2cd39-291">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="2cd39-292">Участников</span><span class="sxs-lookup"><span data-stu-id="2cd39-292">Members</span></span>

#### <span data-ttu-id="2cd39-293">get_Settings</span><span class="sxs-lookup"><span data-stu-id="2cd39-293">get_Settings</span></span> 

<span data-ttu-id="2cd39-294">Объект [IWebView2Settings](IWebView2Settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-294">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="2cd39-295">общедоступные значения HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \* \* параметры)</span><span class="sxs-lookup"><span data-stu-id="2cd39-295">public HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="2cd39-296">get_Source</span><span class="sxs-lookup"><span data-stu-id="2cd39-296">get_Source</span></span> 

<span data-ttu-id="2cd39-297">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="2cd39-297">The URI of the current top level document.</span></span>

> <span data-ttu-id="2cd39-298">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2cd39-298">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="2cd39-299">Это значение может изменяться в рамках обработки события DocumentStateChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту.</span><span class="sxs-lookup"><span data-stu-id="2cd39-299">This value potentially changes as a part of the DocumentStateChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="2cd39-300">Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-300">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
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
        &m_documentStateChangedToken));
```

#### <span data-ttu-id="2cd39-301">Которому</span><span class="sxs-lookup"><span data-stu-id="2cd39-301">Navigate</span></span> 

<span data-ttu-id="2cd39-302">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="2cd39-302">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="2cd39-303">общедоступное значение HRESULT [навигации](#navigate)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2cd39-303">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="2cd39-304">Дополнительные сведения приведены в разделе события навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-304">See the navigation events for more information.</span></span> <span data-ttu-id="2cd39-305">Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-305">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### <span data-ttu-id="2cd39-306">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-306">MoveFocus</span></span> 

<span data-ttu-id="2cd39-307">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-307">Move focus into WebView.</span></span>

> <span data-ttu-id="2cd39-308">общедоступные значения HRESULT [MoveFocus](#movefocus)(причина[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) )</span><span class="sxs-lookup"><span data-stu-id="2cd39-308">public HRESULT [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="2cd39-309">WebView получит фокус, и фокус будет установлен на элемент корреспондента на странице, которая размещена в WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-309">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="2cd39-310">В целях программной причины фокус установлен на ранее сфокусированный элемент или элемент по умолчанию, если нет ранее фокусируемого элемента.</span><span class="sxs-lookup"><span data-stu-id="2cd39-310">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="2cd39-311">В следующей причине фокус задается для первого элемента.</span><span class="sxs-lookup"><span data-stu-id="2cd39-311">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="2cd39-312">По этой причине фокус установлен на последний элемент.</span><span class="sxs-lookup"><span data-stu-id="2cd39-312">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="2cd39-313">WebView также может сосредоточиться на взаимодействии с пользователем, например, щелкнув на WebView или TAB.</span><span class="sxs-lookup"><span data-stu-id="2cd39-313">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="2cd39-314">Для табуляции приложение может вызвать MoveFocus с помощью кнопки Далее или назад, чтобы выровнять элементы Tab и SHIFT + TAB, если это необходимо, если WebView является следующим элементом с вкладками.</span><span class="sxs-lookup"><span data-stu-id="2cd39-314">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="2cd39-315">Кроме того, приложение может вызвать IsDialogMessage как часть цикла обработки сообщений, чтобы платформа автоматически обрабатывала табуляцию.</span><span class="sxs-lookup"><span data-stu-id="2cd39-315">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="2cd39-316">Платформа будет повернута на все окна с помощью WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="2cd39-316">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="2cd39-317">Когда WebView получает фокус из IsDialogMessage, он будет внутренне размещать фокус на первом или последнем элементе Tab и Shift + Tab соответственно.</span><span class="sxs-lookup"><span data-stu-id="2cd39-317">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (int i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="2cd39-318">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="2cd39-318">NavigateToString</span></span> 

<span data-ttu-id="2cd39-319">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="2cd39-319">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="2cd39-320">общедоступные значения HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="2cd39-320">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="2cd39-321">Параметр htmlContent не может быть больше 2 МБ символов.</span><span class="sxs-lookup"><span data-stu-id="2cd39-321">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="2cd39-322">В качестве источника новой страницы будет указано пустое значение.</span><span class="sxs-lookup"><span data-stu-id="2cd39-322">The origin of the new page will be about:blank.</span></span>

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="2cd39-323">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2cd39-323">add_NavigationStarting</span></span> 

<span data-ttu-id="2cd39-324">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2cd39-324">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="2cd39-325">общедоступные значения HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-325">public HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-326">NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI.</span><span class="sxs-lookup"><span data-stu-id="2cd39-326">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="2cd39-327">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2cd39-327">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
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

#### <span data-ttu-id="2cd39-328">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2cd39-328">remove_NavigationStarting</span></span> 

<span data-ttu-id="2cd39-329">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2cd39-329">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="2cd39-330">общедоступные значения HRESULT [remove_NavigationStarting](#remove_navigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-330">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-331">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="2cd39-331">add_DocumentStateChanged</span></span> 

<span data-ttu-id="2cd39-332">Добавьте обработчик событий для события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-332">Add an event handler for the DocumentStateChanged event.</span></span>

> <span data-ttu-id="2cd39-333">общедоступные значения HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-333">public HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-334">DocumentStateChanged активируется, когда начнется загрузка нового содержимого в основной кадр WebView или происходит та же Навигация по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации).</span><span class="sxs-lookup"><span data-stu-id="2cd39-334">DocumentStateChanged fires when new content has started loading on the webview's main frame or if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="2cd39-335">Это следует за событием NavigationStarting и предшествует событию NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2cd39-335">This follows the NavigationStarting event and precedes the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
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
        &m_documentStateChangedToken));
```

#### <span data-ttu-id="2cd39-336">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="2cd39-336">remove_DocumentStateChanged</span></span> 

<span data-ttu-id="2cd39-337">Удалите обработчик событий, добавленный ранее add_DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-337">Remove an event handler previously added with add_DocumentStateChanged.</span></span>

> <span data-ttu-id="2cd39-338">общедоступные значения HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-338">public HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-339">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2cd39-339">add_NavigationCompleted</span></span> 

<span data-ttu-id="2cd39-340">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2cd39-340">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="2cd39-341">общедоступные значения HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-341">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-342">Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2cd39-342">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="2cd39-343">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2cd39-343">remove_NavigationCompleted</span></span> 

<span data-ttu-id="2cd39-344">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2cd39-344">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="2cd39-345">общедоступные значения HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-345">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-346">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2cd39-346">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="2cd39-347">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2cd39-347">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="2cd39-348">общедоступные значения HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-348">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-349">FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI.</span><span class="sxs-lookup"><span data-stu-id="2cd39-349">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="2cd39-350">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2cd39-350">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### <span data-ttu-id="2cd39-351">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2cd39-351">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="2cd39-352">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2cd39-352">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="2cd39-353">общедоступные значения HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-353">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-354">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-354">add_MoveFocusRequested</span></span> 

<span data-ttu-id="2cd39-355">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-355">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="2cd39-356">общедоступные значения HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-356">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-357">MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-357">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="2cd39-358">При срабатывании этого события фокус WebView не изменился.</span><span class="sxs-lookup"><span data-stu-id="2cd39-358">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="2cd39-359">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-359">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="2cd39-360">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-360">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="2cd39-361">общедоступные значения HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-361">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-362">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-362">add_GotFocus</span></span> 

<span data-ttu-id="2cd39-363">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="2cd39-363">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="2cd39-364">общедоступные значения HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-364">public HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-365">Получение фокуса срабатывает, когда WebView получил фокусировку.</span><span class="sxs-lookup"><span data-stu-id="2cd39-365">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="2cd39-366">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-366">remove_GotFocus</span></span> 

<span data-ttu-id="2cd39-367">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="2cd39-367">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="2cd39-368">общедоступные значения HRESULT [remove_GotFocus](#remove_gotfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-368">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-369">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-369">add_LostFocus</span></span> 

<span data-ttu-id="2cd39-370">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="2cd39-370">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="2cd39-371">общедоступные значения HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-371">public HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-372">LostFocus вызывается, когда WebView теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="2cd39-372">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="2cd39-373">В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-373">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="2cd39-374">Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-374">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="2cd39-375">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="2cd39-375">remove_LostFocus</span></span> 

<span data-ttu-id="2cd39-376">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="2cd39-376">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="2cd39-377">общедоступные значения HRESULT [remove_LostFocus](#remove_lostfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-377">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-378">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="2cd39-378">add_WebResourceRequested_deprecated</span></span> 

<span data-ttu-id="2cd39-379">Этот API будет устаревшим, воспользуйтесь новым add_WebResourceRequested API.</span><span class="sxs-lookup"><span data-stu-id="2cd39-379">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>

> <span data-ttu-id="2cd39-380">открытые значения HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \* const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \* const resourceContextFilter, SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-380">public HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \*const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \*const resourceContextFilter,SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-381">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-381">Add an event handler for the WebResourceRequested event.</span></span> <span data-ttu-id="2cd39-382">Активируется, когда WebView выполняет HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="2cd39-382">Fires when the WebView has performs any HTTP request.</span></span> <span data-ttu-id="2cd39-383">Используйте urlFilter для передачи списка с размером filterLength URL-адресов для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="2cd39-383">Use urlFilter to pass in a list with size filterLength of urls to listen for.</span></span> <span data-ttu-id="2cd39-384">Каждый элемент URL-адреса также поддерживает подстановочные знаки: "\*" соответствует нулю или нескольким символам, а "?" соответствует одному символу.</span><span class="sxs-lookup"><span data-stu-id="2cd39-384">Each url entry also supports wildcards: '\*' matches zero or more characters, and '?' matches exactly one character.</span></span> <span data-ttu-id="2cd39-385">Для каждой записи urlFilter укажите соответствующие resourceContextFilter, представляющие типы ресурсов, которые должны срабатывать WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-385">For each urlFilter entry, provide a matching resourceContextFilter representing the types of resources for which WebResourceRequested should fire.</span></span> <span data-ttu-id="2cd39-386">Если filterLength 0, то событие будет срабатывать для всех сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="2cd39-386">If filterLength is 0, the event will fire for all network requests.</span></span> <span data-ttu-id="2cd39-387">Поддерживаются следующие контексты ресурсов: документ, таблица стилей, изображение, мультимедиа, шрифт, сценарий, XHR, выборка.</span><span class="sxs-lookup"><span data-stu-id="2cd39-387">The supported resource contexts are: Document, Stylesheet, Image, Media, Font, Script, XHR, Fetch.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
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

#### <span data-ttu-id="2cd39-388">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-388">remove_WebResourceRequested</span></span> 

<span data-ttu-id="2cd39-389">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-389">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="2cd39-390">общедоступные значения HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-390">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-391">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="2cd39-391">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="2cd39-392">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2cd39-392">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="2cd39-393">общедоступные значения HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-393">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-394">Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-394">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="2cd39-395">Это событие срабатывает только в том случае, если свойству IWebView2Settings:: AreDefaultScriptDialogsEnabled задано значение false.</span><span class="sxs-lookup"><span data-stu-id="2cd39-395">This event only fires if the IWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
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

#### <span data-ttu-id="2cd39-396">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="2cd39-396">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="2cd39-397">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2cd39-397">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="2cd39-398">общедоступные значения HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-398">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-399">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="2cd39-399">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="2cd39-400">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-400">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="2cd39-401">общедоступные значения HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-401">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-402">Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-402">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="2cd39-403">Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб.</span><span class="sxs-lookup"><span data-stu-id="2cd39-403">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="2cd39-404">При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится.</span><span class="sxs-lookup"><span data-stu-id="2cd39-404">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="2cd39-405">WebView связывает последний использованный коэффициент масштабирования для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="2cd39-405">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="2cd39-406">Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="2cd39-406">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="2cd39-407">При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-407">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the DocumentStateChanged event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="2cd39-408">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="2cd39-408">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="2cd39-409">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-409">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="2cd39-410">общедоступные значения HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-410">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-411">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-411">add_PermissionRequested</span></span> 

<span data-ttu-id="2cd39-412">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-412">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="2cd39-413">общедоступные значения HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-413">public HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-414">Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="2cd39-414">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="2cd39-415">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="2cd39-415">remove_PermissionRequested</span></span> 

<span data-ttu-id="2cd39-416">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2cd39-416">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="2cd39-417">общедоступные значения HRESULT [remove_PermissionRequested](#remove_permissionrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-417">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-418">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="2cd39-418">add_ProcessFailed</span></span> 

<span data-ttu-id="2cd39-419">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2cd39-419">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="2cd39-420">общедоступные значения HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-420">public HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-421">Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-421">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="2cd39-422">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="2cd39-422">remove_ProcessFailed</span></span> 

<span data-ttu-id="2cd39-423">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2cd39-423">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="2cd39-424">общедоступные значения HRESULT [remove_ProcessFailed](#remove_processfailed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-424">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-425">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="2cd39-425">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="2cd39-426">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="2cd39-426">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="2cd39-427">общедоступные значения HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="2cd39-427">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="2cd39-428">Вставленный сценарий будет применяться ко всем документам верхнего уровня и дочерним элементам навигации, пока они не будут удалены с помощью RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2cd39-428">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="2cd39-429">Это применяется асинхронно, и вы должны дождаться выполнения обработчика завершения, прежде чем можно будет убедиться, что сценарий готов к выполнению для навигации в будущем.</span><span class="sxs-lookup"><span data-stu-id="2cd39-429">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="2cd39-430">Обратите внимание, что если в HTML-документе есть изолированная [Среда с определенными свойствами или](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [заголовок HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , это повлияет на выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="2cd39-430">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="2cd39-431">Таким образом, например, если ключевое слово "Allow-Modal" не задано, вызовы `alert` функции будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="2cd39-431">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="2cd39-432">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="2cd39-432">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="2cd39-433">Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2cd39-433">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="2cd39-434">общедоступные значения HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2cd39-434">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="2cd39-435">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="2cd39-435">ExecuteScript</span></span> 

<span data-ttu-id="2cd39-436">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-436">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="2cd39-437">общедоступные значения HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="2cd39-437">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="2cd39-438">Это выполняется асинхронно и по завершении, если обработчик предоставлен в параметре ExecuteScriptCompletedHandler, вызывается его метод Invoke с результатом вычисления предоставленного JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2cd39-438">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="2cd39-439">Результирующее значение — это строка в кодировке JSON.</span><span class="sxs-lookup"><span data-stu-id="2cd39-439">The result value is a JSON encoded string.</span></span> <span data-ttu-id="2cd39-440">Если результат не определен, содержит цикл ссылки или не может быть закодирован в JSON, значение NULL JSON будет возвращено в виде строки null.</span><span class="sxs-lookup"><span data-stu-id="2cd39-440">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="2cd39-441">Обратите внимание, что функция без явного возвращаемого значения возвращает значение undefine.</span><span class="sxs-lookup"><span data-stu-id="2cd39-441">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="2cd39-442">Если выполняемый сценарий создает необработанное исключение, результат также равен null.</span><span class="sxs-lookup"><span data-stu-id="2cd39-442">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="2cd39-443">Этот метод применяется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="2cd39-443">This method is applied asynchronously.</span></span> <span data-ttu-id="2cd39-444">Если вызов выполняется, когда WebView находится на одном документе, а переход происходит после того, как вызов выполнен, но перед выполнением JavaScript, то сценарий не будет выполнен, а обработчик будет вызван с E_FAIL для параметра errorCode.</span><span class="sxs-lookup"><span data-stu-id="2cd39-444">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="2cd39-445">ExecuteScript будет работать даже в том случае, если IsScriptEnabled имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="2cd39-445">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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
            Callback<IWebView2ExecuteScriptCompletedHandler>(
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

#### <span data-ttu-id="2cd39-446">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="2cd39-446">CapturePreview</span></span> 

<span data-ttu-id="2cd39-447">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="2cd39-447">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="2cd39-448">Public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="2cd39-448">public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="2cd39-449">Укажите формат изображения с помощью параметра imageFormat.</span><span class="sxs-lookup"><span data-stu-id="2cd39-449">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="2cd39-450">Результирующие двоичные данные изображения записываются в указанный параметр imageStream.</span><span class="sxs-lookup"><span data-stu-id="2cd39-450">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="2cd39-451">Когда CapturePreview закончит запись в поток, вызывается метод Invoke в указанном параметре обработчика.</span><span class="sxs-lookup"><span data-stu-id="2cd39-451">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="2cd39-452">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="2cd39-452">Reload</span></span> 

<span data-ttu-id="2cd39-453">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="2cd39-453">Reload the current page.</span></span>

> <span data-ttu-id="2cd39-454">общедоступная [Перезагрузка](#reload)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="2cd39-454">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="2cd39-455">Это похоже на то, что переход к URI текущего документа верхнего уровня, включая все события навигации, которые обрабатывались, и учитывает любые записи в кэше HTTP.</span><span class="sxs-lookup"><span data-stu-id="2cd39-455">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="2cd39-456">Но история «назад» и «вперед» не будет изменена.</span><span class="sxs-lookup"><span data-stu-id="2cd39-456">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="2cd39-457">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="2cd39-457">get_Bounds</span></span> 

<span data-ttu-id="2cd39-458">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-458">The webview bounds.</span></span>

> <span data-ttu-id="2cd39-459">общедоступные значения HRESULT [get_Bounds](#get_bounds)(границы Rect \*)</span><span class="sxs-lookup"><span data-stu-id="2cd39-459">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="2cd39-460">Границы задаются относительно родительского дескриптора HWND.</span><span class="sxs-lookup"><span data-stu-id="2cd39-460">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="2cd39-461">Приложение может располагать WebView двумя способами:</span><span class="sxs-lookup"><span data-stu-id="2cd39-461">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="2cd39-462">Создание дочернего HWND, который является родительским дескриптором HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-462">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="2cd39-463">Расположите это окно в том месте, где должен быть WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-463">Position this window where the WebView should be.</span></span> <span data-ttu-id="2cd39-464">В этом случае используйте (0, 0) для левого верхнего угла WebView Bound's (сдвиг).</span><span class="sxs-lookup"><span data-stu-id="2cd39-464">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="2cd39-465">Используйте окно самого высокого приложения в качестве родительского HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-465">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="2cd39-466">Задайте Bound's левый верхний угол WebView, чтобы WebView правильно расположиться в приложении.</span><span class="sxs-lookup"><span data-stu-id="2cd39-466">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="2cd39-467">Значения границ находятся в пространстве координат основного приложения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-467">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="2cd39-468">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="2cd39-468">put_Bounds</span></span> 

<span data-ttu-id="2cd39-469">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="2cd39-469">Set the Bounds property.</span></span>

> <span data-ttu-id="2cd39-470">общедоступные значения HRESULT [put_Bounds](#put_bounds)(границы Rect)</span><span class="sxs-lookup"><span data-stu-id="2cd39-470">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### <span data-ttu-id="2cd39-471">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="2cd39-471">get_ZoomFactor</span></span> 

<span data-ttu-id="2cd39-472">Коэффициент увеличения для текущей страницы в WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-472">The zoom factor for the current page in the WebView.</span></span>

> <span data-ttu-id="2cd39-473">общедоступные значения HRESULT [get_ZoomFactor](#get_zoomfactor)(Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="2cd39-473">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="2cd39-474">Коэффициент масштабирования сохраняется на каждом сайте.</span><span class="sxs-lookup"><span data-stu-id="2cd39-474">The zoom factor is persisted per site.</span></span> <span data-ttu-id="2cd39-475">Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-475">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="2cd39-476">Когда WebView переходит на страницу с другого сайта, коэффициент масштабирования, заданный для предыдущей страницы, не будет применен.</span><span class="sxs-lookup"><span data-stu-id="2cd39-476">When WebView navigates to a page from a different site, the zoom factor set for the previous page will not be applied.</span></span> <span data-ttu-id="2cd39-477">Если приложение захочет задать коэффициент масштабирования для определенной страницы, самое раннее место — в обработчике событий DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-477">If the app wants to set the zoom factor for a certain page, the earliest place to do it is in the DocumentStateChanged event handler.</span></span> <span data-ttu-id="2cd39-478">Обратите внимание, что если это так, может возникнуть событие ZoomFactorChanged для коэффициента материализованных масштабов перед получением события ZoomFactorChanged для указанного коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2cd39-478">Note that if it does that, it might receive a ZoomFactorChanged event for the persisted zoom factor before receiving the ZoomFactorChanged event for the specified zoom factor.</span></span> <span data-ttu-id="2cd39-479">Указывать zoomFactor меньше или равно 0 не разрешается.</span><span class="sxs-lookup"><span data-stu-id="2cd39-479">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="2cd39-480">WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2cd39-480">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="2cd39-481">Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2cd39-481">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="2cd39-482">При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2cd39-482">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="2cd39-483">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="2cd39-483">put_ZoomFactor</span></span> 

<span data-ttu-id="2cd39-484">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="2cd39-484">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="2cd39-485">общедоступный [PUT_ZOOMFACTOR](#put_zoomfactor)HRESULT (двойной ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="2cd39-485">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="2cd39-486">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="2cd39-486">get_IsVisible</span></span> 

<span data-ttu-id="2cd39-487">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-487">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="2cd39-488">общедоступные значения HRESULT [get_IsVisible](#get_isvisible)(bool \* Visible)</span><span class="sxs-lookup"><span data-stu-id="2cd39-488">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="2cd39-489">Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="2cd39-489">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="2cd39-490">Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateWebView).</span><span class="sxs-lookup"><span data-stu-id="2cd39-490">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateWebView).</span></span> <span data-ttu-id="2cd39-491">Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible.</span><span class="sxs-lookup"><span data-stu-id="2cd39-491">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="2cd39-492">WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="2cd39-492">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="2cd39-493">Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-493">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="2cd39-494">Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-494">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="2cd39-495">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="2cd39-495">put_IsVisible</span></span> 

<span data-ttu-id="2cd39-496">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="2cd39-496">Set the IsVisible property.</span></span>

> <span data-ttu-id="2cd39-497">общедоступные значения HRESULT [put_IsVisible](#put_isvisible)(bool-Visible)</span><span class="sxs-lookup"><span data-stu-id="2cd39-497">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="2cd39-498">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="2cd39-498">PostWebMessageAsJson</span></span> 

<span data-ttu-id="2cd39-499">Опубликуйте указанное сообщение в документе верхнего уровня в этом [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="2cd39-499">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>

> <span data-ttu-id="2cd39-500">общедоступные значения HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="2cd39-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="2cd39-501">Срабатывает событие Window. Chrome. WebView для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="2cd39-501">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="2cd39-502">JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий:</span><span class="sxs-lookup"><span data-stu-id="2cd39-502">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="2cd39-503">Аргументы события представляют собой экземпляр `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="2cd39-503">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="2cd39-504">Параметр IWebView2Settings:: IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="2cd39-504">The IWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="2cd39-505">Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2cd39-505">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="2cd39-506">Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект.</span><span class="sxs-lookup"><span data-stu-id="2cd39-506">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="2cd39-507">Сведения о том, как отправлять сообщения из HTML-документа на WebView на узел, можно найти в SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="2cd39-507">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="2cd39-508">Это сообщение отправляется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="2cd39-508">This message is sent asynchronously.</span></span> <span data-ttu-id="2cd39-509">Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.</span><span class="sxs-lookup"><span data-stu-id="2cd39-509">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
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

#### <span data-ttu-id="2cd39-510">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="2cd39-510">PostWebMessageAsString</span></span> 

<span data-ttu-id="2cd39-511">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2cd39-511">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="2cd39-512">общедоступные значения HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="2cd39-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="2cd39-513">Это выполняется точно так же, как и PostWebMessageAsJson, но `window.chrome.webview` свойство Data события ARG имеет строковое значение с тем же значением, что и webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="2cd39-513">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="2cd39-514">Используйте это вместо PostWebMessageAsJson, если вы хотите общаться с помощью простых строк, а не объектов JSON.</span><span class="sxs-lookup"><span data-stu-id="2cd39-514">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="2cd39-515">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2cd39-515">add_WebMessageReceived</span></span> 

<span data-ttu-id="2cd39-516">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="2cd39-516">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="2cd39-517">общедоступные значения HRESULT [add_WebMessageReceived](#add_webmessagereceived)(обработчик[IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-517">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-518">Функция i, в `void postMessage(object)` которой объект — это любой объект, поддерживаемый преобразованием JSON.</span><span class="sxs-lookup"><span data-stu-id="2cd39-518">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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

 <span data-ttu-id="2cd39-519">При вызове [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) набор с помощью этого метода SetWebMessageReceivedEventHandler вызывается с помощью параметра объекта i, преобразованного в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="2cd39-519">When postMessage is called, the [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
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

#### <span data-ttu-id="2cd39-520">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2cd39-520">remove_WebMessageReceived</span></span> 

<span data-ttu-id="2cd39-521">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="2cd39-521">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="2cd39-522">общедоступные значения HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2cd39-522">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-523">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="2cd39-523">Close</span></span> 

<span data-ttu-id="2cd39-524">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="2cd39-524">Closes the webview and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="2cd39-525">общедоступное значение HRESULT [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="2cd39-525">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="2cd39-526">Очистка браузера instace освобождает ресурсы, переключающие WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-526">Cleaning up the browser instace will release the resources powering the webview.</span></span> <span data-ttu-id="2cd39-527">Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.</span><span class="sxs-lookup"><span data-stu-id="2cd39-527">The browser instance will be shut down if there are no other webviews using it.</span></span>

<span data-ttu-id="2cd39-528">После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся.</span><span class="sxs-lookup"><span data-stu-id="2cd39-528">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="2cd39-529">В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.</span><span class="sxs-lookup"><span data-stu-id="2cd39-529">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="2cd39-530">Метод Close вызывается неявно, когда WebView теряет свою конечную ссылку и является независимым.</span><span class="sxs-lookup"><span data-stu-id="2cd39-530">Close is implicitly called when the WebView loses its final reference and is destructed.</span></span> <span data-ttu-id="2cd39-531">Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-531">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="2cd39-532">В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="2cd39-532">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="2cd39-533">Закрыть, чтобы прервать этот цикл, освобождая все обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="2cd39-533">Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="2cd39-534">Но чтобы избежать такой ситуации, рекомендуется явно вызвать метод Close для WebView и не захватывать ссылку на WebView, чтобы убедиться в том, что WebView может быть корректно очищено.</span><span class="sxs-lookup"><span data-stu-id="2cd39-534">But to avoid this situation it is best practice to both explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### <span data-ttu-id="2cd39-535">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="2cd39-535">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="2cd39-536">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="2cd39-536">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="2cd39-537">общедоступные значения HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="2cd39-537">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="2cd39-538">Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="2cd39-538">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="2cd39-539">Параметр methodName — это полное имя метода в формате `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="2cd39-539">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="2cd39-540">Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода.</span><span class="sxs-lookup"><span data-stu-id="2cd39-540">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="2cd39-541">Метод Invoke обработчика вызывается, когда метод асинхронно завершается.</span><span class="sxs-lookup"><span data-stu-id="2cd39-541">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="2cd39-542">Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="2cd39-542">Invoke will be called with the method's return object as a JSON string.</span></span>

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
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="2cd39-543">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="2cd39-543">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="2cd39-544">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="2cd39-544">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="2cd39-545">общедоступные значения HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* обработчик, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-545">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2cd39-546">Список и описание доступных событий можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="2cd39-546">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available events.</span></span> <span data-ttu-id="2cd39-547">Параметр eventName — это полное имя события в формате `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="2cd39-547">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="2cd39-548">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="2cd39-548">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="2cd39-549">Вызов вызывается с использованием объекта аргументов события, содержащего объект Parameter события CDP, в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="2cd39-549">Invoke will be called with the an event args object containing the CDP event's parameter object as a JSON string.</span></span>

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
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="2cd39-550">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="2cd39-550">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="2cd39-551">Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="2cd39-551">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="2cd39-552">общедоступные значения HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR eventName, EventRegistrationToken token)</span><span class="sxs-lookup"><span data-stu-id="2cd39-552">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR eventName,EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2cd39-553">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="2cd39-553">get_BrowserProcessId</span></span> 

<span data-ttu-id="2cd39-554">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-554">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="2cd39-555">общедоступные значения HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="2cd39-555">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="2cd39-556">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="2cd39-556">get_CanGoBack</span></span> 

<span data-ttu-id="2cd39-557">Можно переходить по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-557">Can navigate the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="2cd39-558">общедоступные значения HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="2cd39-558">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="2cd39-559">get_CanGoBack изменить значение с помощью события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-559">get_CanGoBack change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="2cd39-560">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="2cd39-560">get_CanGoForward</span></span> 

<span data-ttu-id="2cd39-561">Можно переходить по WebView на следующую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-561">Can navigate the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="2cd39-562">общедоступные значения HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="2cd39-562">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="2cd39-563">get_CanGoForward изменить значение с помощью события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="2cd39-563">get_CanGoForward change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="2cd39-564">GoBack</span><span class="sxs-lookup"><span data-stu-id="2cd39-564">GoBack</span></span> 

<span data-ttu-id="2cd39-565">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-565">Navigates the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="2cd39-566">общедоступное значение HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="2cd39-566">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="2cd39-567">GoForward</span><span class="sxs-lookup"><span data-stu-id="2cd39-567">GoForward</span></span> 

<span data-ttu-id="2cd39-568">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="2cd39-568">Navigates the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="2cd39-569">общедоступные значения HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="2cd39-569">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="2cd39-570">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="2cd39-570">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="2cd39-571">Формат изображения, используемый в методе [IWebView2WebView:: CapturePreview](#capturepreview) .</span><span class="sxs-lookup"><span data-stu-id="2cd39-571">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>

> <span data-ttu-id="2cd39-572">[WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) перечисления</span><span class="sxs-lookup"><span data-stu-id="2cd39-572">enum [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="2cd39-573">Данные</span><span class="sxs-lookup"><span data-stu-id="2cd39-573">Values</span></span>                         | <span data-ttu-id="2cd39-574">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-574">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2cd39-575">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="2cd39-575">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="2cd39-576">Формат изображения PNG.</span><span class="sxs-lookup"><span data-stu-id="2cd39-576">PNG image format.</span></span>
<span data-ttu-id="2cd39-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="2cd39-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="2cd39-578">Формат изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="2cd39-578">JPEG image format.</span></span>

#### <span data-ttu-id="2cd39-579">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="2cd39-579">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="2cd39-580">Диалоговое окно вида JavaScript, используемое в интерфейсе [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd39-580">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>

> <span data-ttu-id="2cd39-581">[WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="2cd39-581">enum [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="2cd39-582">Данные</span><span class="sxs-lookup"><span data-stu-id="2cd39-582">Values</span></span>                         | <span data-ttu-id="2cd39-583">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-583">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2cd39-584">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="2cd39-584">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="2cd39-585">Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2cd39-585">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="2cd39-586">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="2cd39-586">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="2cd39-587">Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2cd39-587">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="2cd39-588">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="2cd39-588">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="2cd39-589">Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2cd39-589">A dialog invoked via the window.prompt JavaScript function.</span></span>

#### <span data-ttu-id="2cd39-590">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="2cd39-590">WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="2cd39-591">Состояние сбоя процесса, используемого в интерфейсе [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd39-591">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>

> <span data-ttu-id="2cd39-592">[WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="2cd39-592">enum [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)</span></span>

 <span data-ttu-id="2cd39-593">Данные</span><span class="sxs-lookup"><span data-stu-id="2cd39-593">Values</span></span>                         | <span data-ttu-id="2cd39-594">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-594">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2cd39-595">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="2cd39-595">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="2cd39-596">Указывает, что процесс браузера неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="2cd39-596">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="2cd39-597">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="2cd39-597">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="2cd39-598">Указывает, что процесс обработки неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="2cd39-598">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="2cd39-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="2cd39-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="2cd39-600">Указывает на то, что процесс рендеринга перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-600">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="2cd39-601">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="2cd39-601">WEBVIEW2_PERMISSION_TYPE</span></span> 

<span data-ttu-id="2cd39-602">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-602">The type of a permission request.</span></span>

> <span data-ttu-id="2cd39-603">[WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) перечисления</span><span class="sxs-lookup"><span data-stu-id="2cd39-603">enum [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)</span></span>

 <span data-ttu-id="2cd39-604">Данные</span><span class="sxs-lookup"><span data-stu-id="2cd39-604">Values</span></span>                         | <span data-ttu-id="2cd39-605">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-605">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2cd39-606">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="2cd39-606">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="2cd39-607">Неизвестное разрешение.</span><span class="sxs-lookup"><span data-stu-id="2cd39-607">Unknown permission.</span></span>
<span data-ttu-id="2cd39-608">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="2cd39-608">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span></span>            | <span data-ttu-id="2cd39-609">Разрешение на запись звука.</span><span class="sxs-lookup"><span data-stu-id="2cd39-609">Permission to capture audio.</span></span>
<span data-ttu-id="2cd39-610">WEBVIEW2_PERMISSION_TYPE_CAMERA</span><span class="sxs-lookup"><span data-stu-id="2cd39-610">WEBVIEW2_PERMISSION_TYPE_CAMERA</span></span>            | <span data-ttu-id="2cd39-611">Разрешение на захват видео.</span><span class="sxs-lookup"><span data-stu-id="2cd39-611">Permission to capture video.</span></span>
<span data-ttu-id="2cd39-612">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="2cd39-612">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span></span>            | <span data-ttu-id="2cd39-613">Разрешение на доступ к географической позиции.</span><span class="sxs-lookup"><span data-stu-id="2cd39-613">Permission to access geolocation.</span></span>
<span data-ttu-id="2cd39-614">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="2cd39-614">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span></span>            | <span data-ttu-id="2cd39-615">Разрешение на отправку веб-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2cd39-615">Permission to send web notifications.</span></span>
<span data-ttu-id="2cd39-616">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="2cd39-616">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span></span>            | <span data-ttu-id="2cd39-617">Разрешение на доступ к универсальному датчику.</span><span class="sxs-lookup"><span data-stu-id="2cd39-617">Permission to access generic sensor.</span></span>
<span data-ttu-id="2cd39-618">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="2cd39-618">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span></span>            | <span data-ttu-id="2cd39-619">Разрешение на чтение системного буфера обмена без жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="2cd39-619">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="2cd39-620">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="2cd39-620">WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="2cd39-621">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-621">Response to a permission request.</span></span>

> <span data-ttu-id="2cd39-622">[WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) перечисления</span><span class="sxs-lookup"><span data-stu-id="2cd39-622">enum [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)</span></span>

 <span data-ttu-id="2cd39-623">Данные</span><span class="sxs-lookup"><span data-stu-id="2cd39-623">Values</span></span>                         | <span data-ttu-id="2cd39-624">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-624">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2cd39-625">WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2cd39-625">WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="2cd39-626">Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.</span><span class="sxs-lookup"><span data-stu-id="2cd39-626">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="2cd39-627">WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="2cd39-627">WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="2cd39-628">Предоставьте разрешение на запрос.</span><span class="sxs-lookup"><span data-stu-id="2cd39-628">Grant the permission request.</span></span>
<span data-ttu-id="2cd39-629">WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="2cd39-629">WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="2cd39-630">Отказ от запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="2cd39-630">Deny the permission request.</span></span>

#### <span data-ttu-id="2cd39-631">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="2cd39-631">WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="2cd39-632">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="2cd39-632">Reason for moving focus.</span></span>

> <span data-ttu-id="2cd39-633">[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) перечисления</span><span class="sxs-lookup"><span data-stu-id="2cd39-633">enum [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)</span></span>

 <span data-ttu-id="2cd39-634">Данные</span><span class="sxs-lookup"><span data-stu-id="2cd39-634">Values</span></span>                         | <span data-ttu-id="2cd39-635">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-635">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2cd39-636">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="2cd39-636">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="2cd39-637">Настройка кода фокуса на WebView.</span><span class="sxs-lookup"><span data-stu-id="2cd39-637">Code setting focus into WebView.</span></span>
<span data-ttu-id="2cd39-638">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="2cd39-638">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="2cd39-639">Перемещение фокуса из-за прохождения вкладки вперед.</span><span class="sxs-lookup"><span data-stu-id="2cd39-639">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="2cd39-640">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="2cd39-640">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="2cd39-641">Перемещение фокуса из-за перемещения по табуляции назад.</span><span class="sxs-lookup"><span data-stu-id="2cd39-641">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="2cd39-642">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="2cd39-642">WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="2cd39-643">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="2cd39-643">Error status values for web navigations.</span></span>

> <span data-ttu-id="2cd39-644">[WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) перечисления</span><span class="sxs-lookup"><span data-stu-id="2cd39-644">enum [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)</span></span>

 <span data-ttu-id="2cd39-645">Данные</span><span class="sxs-lookup"><span data-stu-id="2cd39-645">Values</span></span>                         | <span data-ttu-id="2cd39-646">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-646">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2cd39-647">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="2cd39-647">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="2cd39-648">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2cd39-648">An unknown error occurred.</span></span>
<span data-ttu-id="2cd39-649">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="2cd39-649">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="2cd39-650">Общее имя сертификата SSL не совпадает с веб-адресом.</span><span class="sxs-lookup"><span data-stu-id="2cd39-650">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="2cd39-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="2cd39-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="2cd39-652">Срок действия сертификата SSL истек.</span><span class="sxs-lookup"><span data-stu-id="2cd39-652">The SSL certificate has expired.</span></span>
<span data-ttu-id="2cd39-653">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2cd39-653">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="2cd39-654">SSL-сертификат клиента включает ошибки.</span><span class="sxs-lookup"><span data-stu-id="2cd39-654">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="2cd39-655">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="2cd39-655">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="2cd39-656">SSL-сертификат отозван.</span><span class="sxs-lookup"><span data-stu-id="2cd39-656">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="2cd39-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="2cd39-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="2cd39-658">Недействительный сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="2cd39-658">The SSL certificate is invalid.</span></span>
<span data-ttu-id="2cd39-659">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="2cd39-659">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="2cd39-660">Узел недостижим.</span><span class="sxs-lookup"><span data-stu-id="2cd39-660">The host is unreachable.</span></span>
<span data-ttu-id="2cd39-661">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2cd39-661">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="2cd39-662">Время ожидания соединения истекло.</span><span class="sxs-lookup"><span data-stu-id="2cd39-662">The connection has timed out.</span></span>
<span data-ttu-id="2cd39-663">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="2cd39-663">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="2cd39-664">Сервер вернул недопустимый или нераспознанный ответ.</span><span class="sxs-lookup"><span data-stu-id="2cd39-664">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="2cd39-665">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="2cd39-665">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="2cd39-666">Соединение было прервано.</span><span class="sxs-lookup"><span data-stu-id="2cd39-666">The connection was aborted.</span></span>
<span data-ttu-id="2cd39-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="2cd39-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="2cd39-668">Подключение было сброшено.</span><span class="sxs-lookup"><span data-stu-id="2cd39-668">The connection was reset.</span></span>
<span data-ttu-id="2cd39-669">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="2cd39-669">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="2cd39-670">Соединение с Интернетом разорвано.</span><span class="sxs-lookup"><span data-stu-id="2cd39-670">The Internet connection has been lost.</span></span>
<span data-ttu-id="2cd39-671">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="2cd39-671">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="2cd39-672">Не удается подключиться к конечному объекту.</span><span class="sxs-lookup"><span data-stu-id="2cd39-672">Cannot connect to destination.</span></span>
<span data-ttu-id="2cd39-673">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="2cd39-673">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="2cd39-674">Не удалось разрешить указанное имя узла.</span><span class="sxs-lookup"><span data-stu-id="2cd39-674">Could not resolve provided host name.</span></span>
<span data-ttu-id="2cd39-675">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="2cd39-675">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="2cd39-676">Операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="2cd39-676">The operation was canceled.</span></span>
<span data-ttu-id="2cd39-677">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="2cd39-677">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="2cd39-678">Перенаправление запроса завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="2cd39-678">The request redirect failed.</span></span>
<span data-ttu-id="2cd39-679">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="2cd39-679">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="2cd39-680">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2cd39-680">An unexpected error occurred.</span></span>

#### <span data-ttu-id="2cd39-681">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="2cd39-681">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="2cd39-682">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cd39-682">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="2cd39-683">[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) перечисления</span><span class="sxs-lookup"><span data-stu-id="2cd39-683">enum [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)</span></span>

 <span data-ttu-id="2cd39-684">Данные</span><span class="sxs-lookup"><span data-stu-id="2cd39-684">Values</span></span>                         | <span data-ttu-id="2cd39-685">Описания</span><span class="sxs-lookup"><span data-stu-id="2cd39-685">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2cd39-686">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="2cd39-686">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="2cd39-687">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-687">All resources.</span></span>
<span data-ttu-id="2cd39-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="2cd39-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="2cd39-689">Ресурсы документов.</span><span class="sxs-lookup"><span data-stu-id="2cd39-689">Document resources.</span></span>
<span data-ttu-id="2cd39-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="2cd39-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="2cd39-691">Ресурсы CSS.</span><span class="sxs-lookup"><span data-stu-id="2cd39-691">CSS resources.</span></span>
<span data-ttu-id="2cd39-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="2cd39-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="2cd39-693">Графические ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-693">Image resources.</span></span>
<span data-ttu-id="2cd39-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="2cd39-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="2cd39-695">Другие мультимедийные ресурсы, например видео.</span><span class="sxs-lookup"><span data-stu-id="2cd39-695">Other media resources such as videos.</span></span>
<span data-ttu-id="2cd39-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="2cd39-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="2cd39-697">Ресурсы шрифта.</span><span class="sxs-lookup"><span data-stu-id="2cd39-697">Font resources.</span></span>
<span data-ttu-id="2cd39-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="2cd39-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="2cd39-699">Ресурсы сценария.</span><span class="sxs-lookup"><span data-stu-id="2cd39-699">Script resources.</span></span>
<span data-ttu-id="2cd39-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="2cd39-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="2cd39-701">HTTP-запросы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-701">XML HTTP requests.</span></span>
<span data-ttu-id="2cd39-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="2cd39-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="2cd39-703">Получение взаимодействия API.</span><span class="sxs-lookup"><span data-stu-id="2cd39-703">Fetch API communication.</span></span>
<span data-ttu-id="2cd39-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="2cd39-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="2cd39-705">TextTrack ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-705">TextTrack resources.</span></span>
<span data-ttu-id="2cd39-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="2cd39-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | 
<span data-ttu-id="2cd39-707">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="2cd39-707">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | 
<span data-ttu-id="2cd39-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="2cd39-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | 
<span data-ttu-id="2cd39-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="2cd39-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | 
<span data-ttu-id="2cd39-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="2cd39-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | 
<span data-ttu-id="2cd39-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="2cd39-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | 
<span data-ttu-id="2cd39-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="2cd39-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="2cd39-713">Другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2cd39-713">Other resources.</span></span>

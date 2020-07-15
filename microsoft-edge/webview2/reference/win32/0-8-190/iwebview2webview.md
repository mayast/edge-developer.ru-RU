---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 7ef58d19bc5284a3e71dc8be16f3865239047a10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878122"
---
# <span data-ttu-id="aeaa3-104">0.8.355-Interface IWebView2WebView</span><span class="sxs-lookup"><span data-stu-id="aeaa3-104">0.8.355 - interface IWebView2WebView</span></span> 

> [!NOTE]
> <span data-ttu-id="aeaa3-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="aeaa3-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView
  : public IUnknown
```

<span data-ttu-id="aeaa3-107">WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-107">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="aeaa3-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="aeaa3-108">Summary</span></span>

 <span data-ttu-id="aeaa3-109">Участников</span><span class="sxs-lookup"><span data-stu-id="aeaa3-109">Members</span></span>                        | <span data-ttu-id="aeaa3-110">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aeaa3-111">get_Settings</span><span class="sxs-lookup"><span data-stu-id="aeaa3-111">get_Settings</span></span>](#get_settings) | <span data-ttu-id="aeaa3-112">Объект [IWebView2Settings](IWebView2Settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-112">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="aeaa3-113">get_Source</span><span class="sxs-lookup"><span data-stu-id="aeaa3-113">get_Source</span></span>](#get_source) | <span data-ttu-id="aeaa3-114">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-114">The URI of the current top level document.</span></span>
[<span data-ttu-id="aeaa3-115">Которому</span><span class="sxs-lookup"><span data-stu-id="aeaa3-115">Navigate</span></span>](#navigate) | <span data-ttu-id="aeaa3-116">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="aeaa3-116">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="aeaa3-117">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-117">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="aeaa3-118">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-118">Move focus into WebView.</span></span>
[<span data-ttu-id="aeaa3-119">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="aeaa3-119">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="aeaa3-120">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-120">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="aeaa3-121">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="aeaa3-121">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="aeaa3-122">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-122">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="aeaa3-123">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="aeaa3-123">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="aeaa3-124">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-124">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="aeaa3-125">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="aeaa3-125">add_DocumentStateChanged</span></span>](#add_documentstatechanged) | <span data-ttu-id="aeaa3-126">Добавьте обработчик событий для события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-126">Add an event handler for the DocumentStateChanged event.</span></span>
[<span data-ttu-id="aeaa3-127">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="aeaa3-127">remove_DocumentStateChanged</span></span>](#remove_documentstatechanged) | <span data-ttu-id="aeaa3-128">Удалите обработчик событий, добавленный ранее add_DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-128">Remove an event handler previously added with add_DocumentStateChanged.</span></span>
[<span data-ttu-id="aeaa3-129">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="aeaa3-129">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="aeaa3-130">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-130">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="aeaa3-131">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="aeaa3-131">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="aeaa3-132">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-132">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="aeaa3-133">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="aeaa3-133">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="aeaa3-134">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-134">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="aeaa3-135">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="aeaa3-135">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="aeaa3-136">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-136">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="aeaa3-137">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-137">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="aeaa3-138">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-138">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="aeaa3-139">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-139">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="aeaa3-140">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-140">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="aeaa3-141">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-141">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="aeaa3-142">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-142">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="aeaa3-143">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-143">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="aeaa3-144">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-144">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="aeaa3-145">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-145">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="aeaa3-146">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-146">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="aeaa3-147">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-147">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="aeaa3-148">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-148">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="aeaa3-149">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="aeaa3-149">add_WebResourceRequested_deprecated</span></span>](#add_webresourcerequested_deprecated) | <span data-ttu-id="aeaa3-150">Этот API будет устаревшим, воспользуйтесь новым add_WebResourceRequested API.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-150">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>
[<span data-ttu-id="aeaa3-151">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-151">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="aeaa3-152">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-152">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="aeaa3-153">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="aeaa3-153">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="aeaa3-154">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-154">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="aeaa3-155">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="aeaa3-155">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="aeaa3-156">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-156">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="aeaa3-157">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="aeaa3-157">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="aeaa3-158">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-158">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="aeaa3-159">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="aeaa3-159">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="aeaa3-160">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-160">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="aeaa3-161">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-161">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="aeaa3-162">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-162">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="aeaa3-163">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-163">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="aeaa3-164">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-164">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="aeaa3-165">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="aeaa3-165">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="aeaa3-166">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-166">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="aeaa3-167">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="aeaa3-167">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="aeaa3-168">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-168">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="aeaa3-169">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="aeaa3-169">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="aeaa3-170">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-170">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="aeaa3-171">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="aeaa3-171">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="aeaa3-172">Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-172">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="aeaa3-173">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="aeaa3-173">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="aeaa3-174">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-174">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="aeaa3-175">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="aeaa3-175">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="aeaa3-176">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-176">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="aeaa3-177">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="aeaa3-177">Reload</span></span>](#reload) | <span data-ttu-id="aeaa3-178">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-178">Reload the current page.</span></span>
[<span data-ttu-id="aeaa3-179">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="aeaa3-179">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="aeaa3-180">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-180">The webview bounds.</span></span>
[<span data-ttu-id="aeaa3-181">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="aeaa3-181">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="aeaa3-182">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-182">Set the Bounds property.</span></span>
[<span data-ttu-id="aeaa3-183">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="aeaa3-183">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="aeaa3-184">Коэффициент увеличения для текущей страницы в WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-184">The zoom factor for the current page in the WebView.</span></span>
[<span data-ttu-id="aeaa3-185">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="aeaa3-185">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="aeaa3-186">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-186">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="aeaa3-187">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="aeaa3-187">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="aeaa3-188">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-188">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="aeaa3-189">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="aeaa3-189">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="aeaa3-190">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-190">Set the IsVisible property.</span></span>
[<span data-ttu-id="aeaa3-191">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="aeaa3-191">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="aeaa3-192">Опубликуйте указанное сообщение в документе верхнего уровня в этом [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="aeaa3-192">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>
[<span data-ttu-id="aeaa3-193">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="aeaa3-193">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="aeaa3-194">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-194">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="aeaa3-195">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="aeaa3-195">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="aeaa3-196">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-196">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="aeaa3-197">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="aeaa3-197">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="aeaa3-198">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-198">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="aeaa3-199">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-199">Close</span></span>](#close) | <span data-ttu-id="aeaa3-200">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-200">Closes the webview and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="aeaa3-201">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="aeaa3-201">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="aeaa3-202">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-202">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="aeaa3-203">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="aeaa3-203">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="aeaa3-204">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-204">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="aeaa3-205">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="aeaa3-205">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="aeaa3-206">Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-206">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>
[<span data-ttu-id="aeaa3-207">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="aeaa3-207">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="aeaa3-208">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-208">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="aeaa3-209">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="aeaa3-209">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="aeaa3-210">Можно переходить по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-210">Can navigate the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="aeaa3-211">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="aeaa3-211">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="aeaa3-212">Можно переходить по WebView на следующую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-212">Can navigate the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="aeaa3-213">GoBack</span><span class="sxs-lookup"><span data-stu-id="aeaa3-213">GoBack</span></span>](#goback) | <span data-ttu-id="aeaa3-214">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-214">Navigates the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="aeaa3-215">GoForward</span><span class="sxs-lookup"><span data-stu-id="aeaa3-215">GoForward</span></span>](#goforward) | <span data-ttu-id="aeaa3-216">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-216">Navigates the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="aeaa3-217">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-217">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#webview2_capture_preview_image_format) | <span data-ttu-id="aeaa3-218">Формат изображения, используемый в методе [IWebView2WebView:: CapturePreview](#capturepreview) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-218">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>
[<span data-ttu-id="aeaa3-219">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="aeaa3-219">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#webview2_script_dialog_kind) | <span data-ttu-id="aeaa3-220">Диалоговое окно вида JavaScript, используемое в интерфейсе [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-220">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>
[<span data-ttu-id="aeaa3-221">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="aeaa3-221">WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#webview2_process_failed_kind) | <span data-ttu-id="aeaa3-222">Состояние сбоя процесса, используемого в интерфейсе [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-222">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>
[<span data-ttu-id="aeaa3-223">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-223">WEBVIEW2_PERMISSION_TYPE</span></span>](#webview2_permission_type) | <span data-ttu-id="aeaa3-224">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-224">The type of a permission request.</span></span>
[<span data-ttu-id="aeaa3-225">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-225">WEBVIEW2_PERMISSION_STATE</span></span>](#webview2_permission_state) | <span data-ttu-id="aeaa3-226">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-226">Response to a permission request.</span></span>
[<span data-ttu-id="aeaa3-227">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="aeaa3-227">WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#webview2_move_focus_reason) | <span data-ttu-id="aeaa3-228">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-228">Reason for moving focus.</span></span>
[<span data-ttu-id="aeaa3-229">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="aeaa3-229">WEBVIEW2_WEB_ERROR_STATUS</span></span>](#webview2_web_error_status) | <span data-ttu-id="aeaa3-230">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-230">Error status values for web navigations.</span></span>
[<span data-ttu-id="aeaa3-231">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-231">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#webview2_web_resource_context) | <span data-ttu-id="aeaa3-232">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-232">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="aeaa3-233">События навигации</span><span class="sxs-lookup"><span data-stu-id="aeaa3-233">Navigation events</span></span>

<span data-ttu-id="aeaa3-234">Обычной последовательностью событий навигации является NavigationStarting, DocumentStateChanged и NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-234">The normal sequence of navigation events is NavigationStarting, DocumentStateChanged and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="aeaa3-236">Обратите внимание, что это для событий навигации с одинаковым событием NavigationId arg.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-236">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="aeaa3-237">События навигации с различными аргументы события NavigationId могут перекрывать друг друга.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-237">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="aeaa3-238">Например, если вы запускаете навигацию для события NavigationStarting, а затем запускаете другую навигацию, вы увидите NavigationStarting для первой навигации, за которой следует NavigationStarting второй переход, а затем — NavigationCompleted для первого перехода, а затем все оставшиеся события навигации для второй навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-238">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="aeaa3-239">В случае возникновения ошибок может возникнуть или не быть событием DocumentStateChanged в зависимости от того, проявляется ли переход на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-239">In error cases there may or may not be a DocumentStateChanged event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="aeaa3-240">В случае перенаправления HTTP в строке есть несколько событий NavigationStarting, для которых после первого будет задано значение параметра redirect.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-240">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="aeaa3-241">Для подразделов внутри WebView создается только событие NavigationStarting, которое дает узлу возможность блокировать навигацию по подфреймам.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-241">For subframes inside WebView, the only navigation event fired is the NavigationStarting event which gives host the ability to block subframe navigations.</span></span>

## <span data-ttu-id="aeaa3-242">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="aeaa3-242">Process model</span></span>

<span data-ttu-id="aeaa3-243">WebView2 использует ту же модель процессов, что и веб-браузер EDGE.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-243">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="aeaa3-244">В сеансе пользователя имеется один процесс браузера Edge для определенного каталога данных пользователя, который будет обрабатывать любой процесс вызова WebView2, указывающий на этот каталог данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-244">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="aeaa3-245">Это означает, что один процесс браузера Edge может обслуживать несколько процессов вызова и один процесс вызова может использовать несколько процессов браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-245">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="aeaa3-247">В процессе работы с браузером может быть некоторое количество процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-247">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="aeaa3-248">Они создаются по мере необходимости для того, чтобы обслуживать потенциально несколько кадров в разных представлениях.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-248">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="aeaa3-249">Количество процессов обработки может различаться в зависимости от функции браузера "изоляция сайта" и количества отдельных отключенных относящихся к отсоединенным источникам, отображаемым в соответствующих веб-представлениях.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-249">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="aeaa3-251">Вы можете реагировать на сбои и зависания в этих процессах браузера и отрисовки с помощью события ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-251">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="aeaa3-252">С помощью метода Close можно безопасно завершить работу связанных браузеров и процессов обработки.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-252">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="aeaa3-253">Потоковая модель</span><span class="sxs-lookup"><span data-stu-id="aeaa3-253">Threading model</span></span>

<span data-ttu-id="aeaa3-254">WebView2 должен создаваться в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-254">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="aeaa3-255">В частности, поток с конвейером сообщений.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-255">Specifically a thread with a message pump.</span></span> <span data-ttu-id="aeaa3-256">Все обратные вызовы будут происходить в этом потоке, и звонки в WebView должны выполняться в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-256">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="aeaa3-257">Небезопасно использовать WebView из другого потока.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-257">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="aeaa3-258">Обратные вызовы, включая обработчики событий и обработчики завершения выполняются последовательно.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-258">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="aeaa3-259">Это значит, что если у вас есть обработчик событий и начало цикла обработки сообщений, другие обработчики событий или обратные вызовы завершения будут запущены повторно.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-259">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="aeaa3-260">Безопасность</span><span class="sxs-lookup"><span data-stu-id="aeaa3-260">Security</span></span>

<span data-ttu-id="aeaa3-261">Всегда проверяйте свойство Source объекта WebView, прежде чем использовать ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString или любой другой метод для отправки данных в WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-261">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="aeaa3-262">WebView может перейти на другую страницу с помощью конечного пользователя, взаимодействующего со страницей или сценарием на странице, вызывающем навигацию.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-262">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="aeaa3-263">Также будьте внимательны с AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-263">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="aeaa3-264">Все будущие переходы запустят этот сценарий и предоставляют доступ к сведениям, предназначенным только для определенного происхождения, может быть предоставлен доступ к любому HTML-документу.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-264">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="aeaa3-265">При исследовании результата вызова метода ExecuteScript, события WebMessageReceived, всегда следует проверять источник отправителя или любой другой механизм получения данных из HTML-документа в WebView проверять URI HTML-документа, что вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-265">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="aeaa3-266">Когда вы создаете сообщение для отправки в WebView, предпочитать использование PostWebMessageAsJson и создавайте строковый параметр JSON с помощью библиотеки JSON.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-266">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="aeaa3-267">Это позволит избежать возможного ДТП данных в строку или сценарий JSON и убедиться, что злоумышленник, управляющий неуправляемым вводом, может изменить оставшуюся часть сообщения JSON или выполнить произвольный сценарий.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-267">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="aeaa3-268">Типы строк</span><span class="sxs-lookup"><span data-stu-id="aeaa3-268">String types</span></span>

<span data-ttu-id="aeaa3-269">Выход из параметров строки: LPWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-269">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="aeaa3-270">Вызываемый объект выделяет строку с помощью функции CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-270">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="aeaa3-271">Владение передается вызывающему абоненту и вызывающему абоненту, чтобы освободить память с помощью CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-271">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="aeaa3-272">Строка в параметрах — LPCWSTR строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-272">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="aeaa3-273">Вызывающий объект гарантирует допустимость строки в течение синхронного вызова функции.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-273">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="aeaa3-274">Если вызываемый объект должен сохранить это значение в некоторой точке после завершения вызова функции, вызываемый объект должен выделять собственную копию строкового значения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-274">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="aeaa3-275">Синтаксический анализ URI и JSON</span><span class="sxs-lookup"><span data-stu-id="aeaa3-275">URI and JSON parsing</span></span>

<span data-ttu-id="aeaa3-276">Различные методы предоставляют или допускают URI и JSON в виде строк.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-276">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="aeaa3-277">Для синтаксического анализа и создания этих строк используйте собственную библиотеку предпочтительных.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-277">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="aeaa3-278">Если приложение WinRT доступно для вашего приложения, вы можете использовать для `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` анализа или создания строк JSON либо `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` для синтаксического анализа и создания URI.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-278">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="aeaa3-279">Обе эти операции работают в приложениях Win32.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-279">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="aeaa3-280">Если вы используете IUri и CreateUri для синтаксического анализа URI, вы можете использовать следующие флаги создания URI, чтобы поведение CreateUri более точно соответствовало синтаксическому анализу URI в WebView:</span><span class="sxs-lookup"><span data-stu-id="aeaa3-280">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="aeaa3-281">Отладка</span><span class="sxs-lookup"><span data-stu-id="aeaa3-281">Debugging</span></span>

<span data-ttu-id="aeaa3-282">Откройте DevTools с помощью стандартных сочетаний клавиш: `F12` или `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-282">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="aeaa3-283">Вы можете использовать `--auto-open-devtools-for-tabs` параметр аргумента Command, чтобы окно DevTools было открыто немедленно при первом создании WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-283">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="aeaa3-284">Сведения о том, как предоставить дополнительные аргументы командной строки для процесса браузера, можно найти в документации CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-284">See CreateWebView documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="aeaa3-285">Изучите раздел реестра LoaderOverride для использования разных сборок WebView2 без изменения вашего приложения в документации CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-285">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateWebView documentation.</span></span>

## <span data-ttu-id="aeaa3-286">Управление версиями</span><span class="sxs-lookup"><span data-stu-id="aeaa3-286">Versioning</span></span>

<span data-ttu-id="aeaa3-287">После того как вы использовали определенную версию SDK для создания приложения, ваше приложение может завершить работу с более ранней или более поздней версией установленных двоичных файлов браузера.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-287">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="aeaa3-288">До версии 1.0.0.0 WebView2 на этапе обновления могут возрушиться изменения, которые не позволят пакету SDK работать с различными версиями установленных двоичных файлов браузера.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-288">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="aeaa3-289">После того как версия 1.0.0.0 может работать с различными версиями пакета SDK, следуйте приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-289">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="aeaa3-290">Для учета критических изменений в API убедитесь, что при вызове функции экспорта DLL CreateWebView2Environment и при вызове QueryInterface для любого объекта WebView2 возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-290">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateWebView2Environment and when calling QueryInterface on any WebView2 object.</span></span> <span data-ttu-id="aeaa3-291">Возвращаемое значение E_NOINTERFACE может указывать на то, что пакет SDK несовместим с двоичными файлами браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-291">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="aeaa3-292">Проверка сбоя из QueryInterface также учитывает ситуации, в которых пакет SDK более новый, чем версия браузера EDGE, и ваше приложение пытается использовать интерфейс, на котором нет браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-292">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="aeaa3-293">Если интерфейс недоступен, вы можете отключать связанный компонент, если это возможно, или иным образом информировать конечного пользователя о необходимости обновления браузера.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-293">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="aeaa3-294">Участников</span><span class="sxs-lookup"><span data-stu-id="aeaa3-294">Members</span></span>

#### <span data-ttu-id="aeaa3-295">get_Settings</span><span class="sxs-lookup"><span data-stu-id="aeaa3-295">get_Settings</span></span> 

<span data-ttu-id="aeaa3-296">Объект [IWebView2Settings](IWebView2Settings.md) , содержащий различные изменяемые параметры для запущенного WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-296">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="aeaa3-297">общедоступные значения HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \* \* параметры)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-297">public HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="aeaa3-298">get_Source</span><span class="sxs-lookup"><span data-stu-id="aeaa3-298">get_Source</span></span> 

<span data-ttu-id="aeaa3-299">Универсальный код ресурса (URI) текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-299">The URI of the current top level document.</span></span>

> <span data-ttu-id="aeaa3-300">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-300">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="aeaa3-301">Это значение может изменяться в рамках обработки события DocumentStateChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-301">This value potentially changes as a part of the DocumentStateChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="aeaa3-302">Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-302">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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

#### <span data-ttu-id="aeaa3-303">Которому</span><span class="sxs-lookup"><span data-stu-id="aeaa3-303">Navigate</span></span> 

<span data-ttu-id="aeaa3-304">Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="aeaa3-304">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="aeaa3-305">общедоступное значение HRESULT [навигации](#navigate)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-305">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="aeaa3-306">Дополнительные сведения приведены в разделе события навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-306">See the navigation events for more information.</span></span> <span data-ttu-id="aeaa3-307">Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-307">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### <span data-ttu-id="aeaa3-308">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-308">MoveFocus</span></span> 

<span data-ttu-id="aeaa3-309">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-309">Move focus into WebView.</span></span>

> <span data-ttu-id="aeaa3-310">общедоступные значения HRESULT [MoveFocus](#movefocus)(причина[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) )</span><span class="sxs-lookup"><span data-stu-id="aeaa3-310">public HRESULT [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="aeaa3-311">WebView получит фокус, и фокус будет установлен на элемент корреспондента на странице, которая размещена в WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-311">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="aeaa3-312">В целях программной причины фокус установлен на ранее сфокусированный элемент или элемент по умолчанию, если нет ранее фокусируемого элемента.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-312">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="aeaa3-313">В следующей причине фокус задается для первого элемента.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-313">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="aeaa3-314">По этой причине фокус установлен на последний элемент.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-314">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="aeaa3-315">WebView также может сосредоточиться на взаимодействии с пользователем, например, щелкнув на WebView или TAB.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-315">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="aeaa3-316">Для табуляции приложение может вызвать MoveFocus с помощью кнопки Далее или назад, чтобы выровнять элементы Tab и SHIFT + TAB, если это необходимо, если WebView является следующим элементом с вкладками.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-316">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="aeaa3-317">Кроме того, приложение может вызвать IsDialogMessage как часть цикла обработки сообщений, чтобы платформа автоматически обрабатывала табуляцию.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-317">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="aeaa3-318">Платформа будет повернута на все окна с помощью WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-318">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="aeaa3-319">Когда WebView получает фокус из IsDialogMessage, он будет внутренне размещать фокус на первом или последнем элементе Tab и Shift + Tab соответственно.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-319">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

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

#### <span data-ttu-id="aeaa3-320">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="aeaa3-320">NavigateToString</span></span> 

<span data-ttu-id="aeaa3-321">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-321">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="aeaa3-322">общедоступные значения HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-322">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="aeaa3-323">Параметр htmlContent не может быть больше 2 МБ символов.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-323">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="aeaa3-324">В качестве источника новой страницы будет указано пустое значение.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-324">The origin of the new page will be about:blank.</span></span>

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="aeaa3-325">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="aeaa3-325">add_NavigationStarting</span></span> 

<span data-ttu-id="aeaa3-326">Добавьте обработчик событий для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-326">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="aeaa3-327">общедоступные значения HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-327">public HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-328">NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-328">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="aeaa3-329">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-329">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="aeaa3-330">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="aeaa3-330">remove_NavigationStarting</span></span> 

<span data-ttu-id="aeaa3-331">Удалите обработчик событий, добавленный ранее add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-331">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="aeaa3-332">общедоступные значения HRESULT [remove_NavigationStarting](#remove_navigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-332">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-333">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="aeaa3-333">add_DocumentStateChanged</span></span> 

<span data-ttu-id="aeaa3-334">Добавьте обработчик событий для события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-334">Add an event handler for the DocumentStateChanged event.</span></span>

> <span data-ttu-id="aeaa3-335">общедоступные значения HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-335">public HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-336">DocumentStateChanged активируется, когда начнется загрузка нового содержимого в основной кадр WebView или происходит та же Навигация по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации).</span><span class="sxs-lookup"><span data-stu-id="aeaa3-336">DocumentStateChanged fires when new content has started loading on the webview's main frame or if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="aeaa3-337">Это следует за событием NavigationStarting и предшествует событию NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-337">This follows the NavigationStarting event and precedes the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="aeaa3-338">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="aeaa3-338">remove_DocumentStateChanged</span></span> 

<span data-ttu-id="aeaa3-339">Удалите обработчик событий, добавленный ранее add_DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-339">Remove an event handler previously added with add_DocumentStateChanged.</span></span>

> <span data-ttu-id="aeaa3-340">общедоступные значения HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-340">public HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-341">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="aeaa3-341">add_NavigationCompleted</span></span> 

<span data-ttu-id="aeaa3-342">Добавьте обработчик событий для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-342">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="aeaa3-343">общедоступные значения HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-343">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-344">Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-344">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="aeaa3-345">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="aeaa3-345">remove_NavigationCompleted</span></span> 

<span data-ttu-id="aeaa3-346">Удалите обработчик событий, добавленный ранее add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-346">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="aeaa3-347">общедоступные значения HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-347">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-348">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="aeaa3-348">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="aeaa3-349">Добавьте обработчик событий для события FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-349">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="aeaa3-350">общедоступные значения HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-350">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-351">FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-351">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="aeaa3-352">Это будет срабатывать и для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-352">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="aeaa3-353">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="aeaa3-353">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="aeaa3-354">Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-354">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="aeaa3-355">общедоступные значения HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-355">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-356">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-356">add_MoveFocusRequested</span></span> 

<span data-ttu-id="aeaa3-357">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-357">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="aeaa3-358">общедоступные значения HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-358">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-359">MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-359">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="aeaa3-360">При срабатывании этого события фокус WebView не изменился.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-360">The WebView's focus has not changed when this event is fired.</span></span>

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

#### <span data-ttu-id="aeaa3-361">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-361">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="aeaa3-362">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-362">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="aeaa3-363">общедоступные значения HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-363">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-364">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-364">add_GotFocus</span></span> 

<span data-ttu-id="aeaa3-365">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-365">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="aeaa3-366">общедоступные значения HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-366">public HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-367">Получение фокуса срабатывает, когда WebView получил фокусировку.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-367">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="aeaa3-368">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-368">remove_GotFocus</span></span> 

<span data-ttu-id="aeaa3-369">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-369">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="aeaa3-370">общедоступные значения HRESULT [remove_GotFocus](#remove_gotfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-370">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-371">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-371">add_LostFocus</span></span> 

<span data-ttu-id="aeaa3-372">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-372">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="aeaa3-373">общедоступные значения HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-373">public HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-374">LostFocus вызывается, когда WebView теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-374">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="aeaa3-375">В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-375">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="aeaa3-376">Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-376">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="aeaa3-377">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="aeaa3-377">remove_LostFocus</span></span> 

<span data-ttu-id="aeaa3-378">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-378">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="aeaa3-379">общедоступные значения HRESULT [remove_LostFocus](#remove_lostfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-379">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-380">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="aeaa3-380">add_WebResourceRequested_deprecated</span></span> 

<span data-ttu-id="aeaa3-381">Этот API будет устаревшим, воспользуйтесь новым add_WebResourceRequested API.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-381">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>

> <span data-ttu-id="aeaa3-382">открытые значения HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \* const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \* const resourceContextFilter, SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-382">public HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \*const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \*const resourceContextFilter,SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-383">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-383">Add an event handler for the WebResourceRequested event.</span></span> <span data-ttu-id="aeaa3-384">Активируется, когда WebView выполняет HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-384">Fires when the WebView has performs any HTTP request.</span></span> <span data-ttu-id="aeaa3-385">Используйте urlFilter для передачи списка с размером filterLength URL-адресов для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-385">Use urlFilter to pass in a list with size filterLength of urls to listen for.</span></span> <span data-ttu-id="aeaa3-386">Каждый элемент URL-адреса также поддерживает подстановочные знаки: "\*" соответствует нулю или нескольким символам, а "?" соответствует одному символу.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-386">Each url entry also supports wildcards: '\*' matches zero or more characters, and '?' matches exactly one character.</span></span> <span data-ttu-id="aeaa3-387">Для каждой записи urlFilter укажите соответствующие resourceContextFilter, представляющие типы ресурсов, которые должны срабатывать WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-387">For each urlFilter entry, provide a matching resourceContextFilter representing the types of resources for which WebResourceRequested should fire.</span></span> <span data-ttu-id="aeaa3-388">Если filterLength 0, то событие будет срабатывать для всех сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-388">If filterLength is 0, the event will fire for all network requests.</span></span> <span data-ttu-id="aeaa3-389">Поддерживаются следующие контексты ресурсов: документ, таблица стилей, изображение, мультимедиа, шрифт, сценарий, XHR, выборка.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-389">The supported resource contexts are: Document, Stylesheet, Image, Media, Font, Script, XHR, Fetch.</span></span>

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

#### <span data-ttu-id="aeaa3-390">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-390">remove_WebResourceRequested</span></span> 

<span data-ttu-id="aeaa3-391">Удалите обработчик событий, добавленный ранее add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-391">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="aeaa3-392">общедоступные значения HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-392">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-393">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="aeaa3-393">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="aeaa3-394">Добавьте обработчик событий для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-394">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="aeaa3-395">общедоступные значения HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-395">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-396">Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-396">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="aeaa3-397">Это событие срабатывает только в том случае, если свойству IWebView2Settings:: AreDefaultScriptDialogsEnabled задано значение false.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-397">This event only fires if the IWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span>

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

#### <span data-ttu-id="aeaa3-398">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="aeaa3-398">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="aeaa3-399">Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-399">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="aeaa3-400">общедоступные значения HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-400">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-401">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="aeaa3-401">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="aeaa3-402">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-402">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="aeaa3-403">общедоступные значения HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-403">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-404">Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-404">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="aeaa3-405">Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-405">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="aeaa3-406">При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-406">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="aeaa3-407">WebView связывает последний использованный коэффициент масштабирования для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-407">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="aeaa3-408">Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-408">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="aeaa3-409">При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-409">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the DocumentStateChanged event.</span></span>

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

#### <span data-ttu-id="aeaa3-410">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="aeaa3-410">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="aeaa3-411">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-411">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="aeaa3-412">общедоступные значения HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-412">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-413">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-413">add_PermissionRequested</span></span> 

<span data-ttu-id="aeaa3-414">Добавьте обработчик событий для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-414">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="aeaa3-415">общедоступные значения HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-415">public HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-416">Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-416">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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

#### <span data-ttu-id="aeaa3-417">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="aeaa3-417">remove_PermissionRequested</span></span> 

<span data-ttu-id="aeaa3-418">Удалите обработчик событий, добавленный ранее add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-418">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="aeaa3-419">общедоступные значения HRESULT [remove_PermissionRequested](#remove_permissionrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-419">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-420">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="aeaa3-420">add_ProcessFailed</span></span> 

<span data-ttu-id="aeaa3-421">Добавьте обработчик событий для события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-421">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="aeaa3-422">общедоступные значения HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-422">public HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-423">Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-423">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

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

#### <span data-ttu-id="aeaa3-424">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="aeaa3-424">remove_ProcessFailed</span></span> 

<span data-ttu-id="aeaa3-425">Удалите обработчик событий, добавленный ранее add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-425">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="aeaa3-426">общедоступные значения HRESULT [remove_ProcessFailed](#remove_processfailed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-426">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-427">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="aeaa3-427">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="aeaa3-428">Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-428">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="aeaa3-429">общедоступные значения HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-429">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="aeaa3-430">Вставленный сценарий будет применяться ко всем документам верхнего уровня и дочерним элементам навигации, пока они не будут удалены с помощью RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-430">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="aeaa3-431">Это применяется асинхронно, и вы должны дождаться выполнения обработчика завершения, прежде чем можно будет убедиться, что сценарий готов к выполнению для навигации в будущем.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-431">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="aeaa3-432">Обратите внимание, что если в HTML-документе есть изолированная [Среда с определенными свойствами или](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [заголовок HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , это повлияет на выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-432">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="aeaa3-433">Таким образом, например, если ключевое слово "Allow-Modal" не задано, вызовы `alert` функции будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-433">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="aeaa3-434">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="aeaa3-434">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="aeaa3-435">Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-435">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="aeaa3-436">общедоступные значения HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-436">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="aeaa3-437">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="aeaa3-437">ExecuteScript</span></span> 

<span data-ttu-id="aeaa3-438">Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-438">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="aeaa3-439">общедоступные значения HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-439">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="aeaa3-440">Это выполняется асинхронно и по завершении, если обработчик предоставлен в параметре ExecuteScriptCompletedHandler, вызывается его метод Invoke с результатом вычисления предоставленного JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-440">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="aeaa3-441">Результирующее значение — это строка в кодировке JSON.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-441">The result value is a JSON encoded string.</span></span> <span data-ttu-id="aeaa3-442">Если результат не определен, содержит цикл ссылки или не может быть закодирован в JSON, значение NULL JSON будет возвращено в виде строки null.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-442">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="aeaa3-443">Обратите внимание, что функция без явного возвращаемого значения возвращает значение undefine.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-443">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="aeaa3-444">Если выполняемый сценарий создает необработанное исключение, результат также равен null.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-444">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="aeaa3-445">Этот метод применяется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-445">This method is applied asynchronously.</span></span> <span data-ttu-id="aeaa3-446">Если вызов выполняется, когда WebView находится на одном документе, а переход происходит после того, как вызов выполнен, но перед выполнением JavaScript, то сценарий не будет выполнен, а обработчик будет вызван с E_FAIL для параметра errorCode.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-446">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="aeaa3-447">ExecuteScript будет работать даже в том случае, если IsScriptEnabled имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-447">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="aeaa3-448">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="aeaa3-448">CapturePreview</span></span> 

<span data-ttu-id="aeaa3-449">Запишите изображение того, что WebView на экране.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-449">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="aeaa3-450">Public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-450">public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="aeaa3-451">Укажите формат изображения с помощью параметра imageFormat.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-451">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="aeaa3-452">Результирующие двоичные данные изображения записываются в указанный параметр imageStream.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-452">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="aeaa3-453">Когда CapturePreview закончит запись в поток, вызывается метод Invoke в указанном параметре обработчика.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-453">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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

#### <span data-ttu-id="aeaa3-454">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="aeaa3-454">Reload</span></span> 

<span data-ttu-id="aeaa3-455">Перезагрузите текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-455">Reload the current page.</span></span>

> <span data-ttu-id="aeaa3-456">общедоступная [Перезагрузка](#reload)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="aeaa3-456">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="aeaa3-457">Это похоже на то, что переход к URI текущего документа верхнего уровня, включая все события навигации, которые обрабатывались, и учитывает любые записи в кэше HTTP.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-457">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="aeaa3-458">Но история «назад» и «вперед» не будет изменена.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-458">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="aeaa3-459">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="aeaa3-459">get_Bounds</span></span> 

<span data-ttu-id="aeaa3-460">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-460">The webview bounds.</span></span>

> <span data-ttu-id="aeaa3-461">общедоступные значения HRESULT [get_Bounds](#get_bounds)(границы Rect \*)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-461">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="aeaa3-462">Границы задаются относительно родительского дескриптора HWND.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-462">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="aeaa3-463">Приложение может располагать WebView двумя способами:</span><span class="sxs-lookup"><span data-stu-id="aeaa3-463">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="aeaa3-464">Создание дочернего HWND, который является родительским дескриптором HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-464">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="aeaa3-465">Расположите это окно в том месте, где должен быть WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-465">Position this window where the WebView should be.</span></span> <span data-ttu-id="aeaa3-466">В этом случае используйте (0, 0) для левого верхнего угла WebView Bound's (сдвиг).</span><span class="sxs-lookup"><span data-stu-id="aeaa3-466">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="aeaa3-467">Используйте окно самого высокого приложения в качестве родительского HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-467">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="aeaa3-468">Задайте Bound's левый верхний угол WebView, чтобы WebView правильно расположиться в приложении.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-468">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="aeaa3-469">Значения границ находятся в пространстве координат основного приложения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-469">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="aeaa3-470">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="aeaa3-470">put_Bounds</span></span> 

<span data-ttu-id="aeaa3-471">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-471">Set the Bounds property.</span></span>

> <span data-ttu-id="aeaa3-472">общедоступные значения HRESULT [put_Bounds](#put_bounds)(границы Rect)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-472">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

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

#### <span data-ttu-id="aeaa3-473">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="aeaa3-473">get_ZoomFactor</span></span> 

<span data-ttu-id="aeaa3-474">Коэффициент увеличения для текущей страницы в WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-474">The zoom factor for the current page in the WebView.</span></span>

> <span data-ttu-id="aeaa3-475">общедоступные значения HRESULT [get_ZoomFactor](#get_zoomfactor)(Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-475">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="aeaa3-476">Коэффициент масштабирования сохраняется на каждом сайте.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-476">The zoom factor is persisted per site.</span></span> <span data-ttu-id="aeaa3-477">Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-477">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="aeaa3-478">Когда WebView переходит на страницу с другого сайта, коэффициент масштабирования, заданный для предыдущей страницы, не будет применен.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-478">When WebView navigates to a page from a different site, the zoom factor set for the previous page will not be applied.</span></span> <span data-ttu-id="aeaa3-479">Если приложение захочет задать коэффициент масштабирования для определенной страницы, самое раннее место — в обработчике событий DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-479">If the app wants to set the zoom factor for a certain page, the earliest place to do it is in the DocumentStateChanged event handler.</span></span> <span data-ttu-id="aeaa3-480">Обратите внимание, что если это так, может возникнуть событие ZoomFactorChanged для коэффициента материализованных масштабов перед получением события ZoomFactorChanged для указанного коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-480">Note that if it does that, it might receive a ZoomFactorChanged event for the persisted zoom factor before receiving the ZoomFactorChanged event for the specified zoom factor.</span></span> <span data-ttu-id="aeaa3-481">Указывать zoomFactor меньше или равно 0 не разрешается.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-481">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="aeaa3-482">WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-482">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="aeaa3-483">Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-483">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="aeaa3-484">При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-484">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="aeaa3-485">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="aeaa3-485">put_ZoomFactor</span></span> 

<span data-ttu-id="aeaa3-486">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-486">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="aeaa3-487">общедоступный [PUT_ZOOMFACTOR](#put_zoomfactor)HRESULT (двойной ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-487">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="aeaa3-488">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="aeaa3-488">get_IsVisible</span></span> 

<span data-ttu-id="aeaa3-489">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-489">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="aeaa3-490">общедоступные значения HRESULT [get_IsVisible](#get_isvisible)(bool \* Visible)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-490">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="aeaa3-491">Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-491">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="aeaa3-492">Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateWebView).</span><span class="sxs-lookup"><span data-stu-id="aeaa3-492">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateWebView).</span></span> <span data-ttu-id="aeaa3-493">Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-493">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="aeaa3-494">WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-494">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="aeaa3-495">Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-495">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="aeaa3-496">Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-496">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="aeaa3-497">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="aeaa3-497">put_IsVisible</span></span> 

<span data-ttu-id="aeaa3-498">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-498">Set the IsVisible property.</span></span>

> <span data-ttu-id="aeaa3-499">общедоступные значения HRESULT [put_IsVisible](#put_isvisible)(bool-Visible)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-499">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

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

#### <span data-ttu-id="aeaa3-500">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="aeaa3-500">PostWebMessageAsJson</span></span> 

<span data-ttu-id="aeaa3-501">Опубликуйте указанное сообщение в документе верхнего уровня в этом [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="aeaa3-501">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>

> <span data-ttu-id="aeaa3-502">общедоступные значения HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-502">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="aeaa3-503">Срабатывает событие Window. Chrome. WebView для документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-503">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="aeaa3-504">JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий:</span><span class="sxs-lookup"><span data-stu-id="aeaa3-504">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="aeaa3-505">Аргументы события представляют собой экземпляр `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-505">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="aeaa3-506">Параметр IWebView2Settings:: IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-506">The IWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="aeaa3-507">Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-507">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="aeaa3-508">Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-508">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="aeaa3-509">Сведения о том, как отправлять сообщения из HTML-документа на WebView на узел, можно найти в SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-509">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="aeaa3-510">Это сообщение отправляется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-510">This message is sent asynchronously.</span></span> <span data-ttu-id="aeaa3-511">Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-511">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="aeaa3-512">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="aeaa3-512">PostWebMessageAsString</span></span> 

<span data-ttu-id="aeaa3-513">Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-513">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="aeaa3-514">общедоступные значения HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-514">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="aeaa3-515">Это выполняется точно так же, как и PostWebMessageAsJson, но `window.chrome.webview` свойство Data события ARG имеет строковое значение с тем же значением, что и webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-515">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="aeaa3-516">Используйте это вместо PostWebMessageAsJson, если вы хотите общаться с помощью простых строк, а не объектов JSON.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-516">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="aeaa3-517">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="aeaa3-517">add_WebMessageReceived</span></span> 

<span data-ttu-id="aeaa3-518">Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-518">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="aeaa3-519">общедоступные значения HRESULT [add_WebMessageReceived](#add_webmessagereceived)(обработчик[IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-519">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-520">Функция i, в `void postMessage(object)` которой объект — это любой объект, поддерживаемый преобразованием JSON.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-520">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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

 <span data-ttu-id="aeaa3-521">При вызове [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) набор с помощью этого метода SetWebMessageReceivedEventHandler вызывается с помощью параметра объекта i, преобразованного в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-521">When postMessage is called, the [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="aeaa3-522">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="aeaa3-522">remove_WebMessageReceived</span></span> 

<span data-ttu-id="aeaa3-523">Удалите обработчик событий, добавленный ранее add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-523">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="aeaa3-524">общедоступные значения HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-524">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-525">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-525">Close</span></span> 

<span data-ttu-id="aeaa3-526">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-526">Closes the webview and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="aeaa3-527">общедоступное значение HRESULT [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="aeaa3-527">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="aeaa3-528">Очистка браузера instace освобождает ресурсы, переключающие WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-528">Cleaning up the browser instace will release the resources powering the webview.</span></span> <span data-ttu-id="aeaa3-529">Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-529">The browser instance will be shut down if there are no other webviews using it.</span></span>

<span data-ttu-id="aeaa3-530">После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-530">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="aeaa3-531">В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-531">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="aeaa3-532">Метод Close вызывается неявно, когда WebView теряет свою конечную ссылку и является независимым.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-532">Close is implicitly called when the WebView loses its final reference and is destructed.</span></span> <span data-ttu-id="aeaa3-533">Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-533">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="aeaa3-534">В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-534">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="aeaa3-535">Закрыть, чтобы прервать этот цикл, освобождая все обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-535">Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="aeaa3-536">Но чтобы избежать такой ситуации, рекомендуется явно вызвать метод Close для WebView и не захватывать ссылку на WebView, чтобы убедиться в том, что WebView может быть корректно очищено.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-536">But to avoid this situation it is best practice to both explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

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

#### <span data-ttu-id="aeaa3-537">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="aeaa3-537">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="aeaa3-538">Вызовите асинхронный метод DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-538">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="aeaa3-539">общедоступные значения HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-539">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="aeaa3-540">Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-540">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="aeaa3-541">Параметр methodName — это полное имя метода в формате `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-541">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="aeaa3-542">Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-542">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="aeaa3-543">Метод Invoke обработчика вызывается, когда метод асинхронно завершается.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-543">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="aeaa3-544">Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-544">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="aeaa3-545">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="aeaa3-545">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="aeaa3-546">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-546">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="aeaa3-547">общедоступные значения HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* обработчик, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-547">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="aeaa3-548">Список и описание доступных событий можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-548">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available events.</span></span> <span data-ttu-id="aeaa3-549">Параметр eventName — это полное имя события в формате `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-549">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="aeaa3-550">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-550">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="aeaa3-551">Вызов вызывается с использованием объекта аргументов события, содержащего объект Parameter события CDP, в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-551">Invoke will be called with the an event args object containing the CDP event's parameter object as a JSON string.</span></span>

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

#### <span data-ttu-id="aeaa3-552">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="aeaa3-552">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="aeaa3-553">Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-553">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="aeaa3-554">общедоступные значения HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR eventName, EventRegistrationToken token)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-554">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR eventName,EventRegistrationToken token)</span></span>

#### <span data-ttu-id="aeaa3-555">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="aeaa3-555">get_BrowserProcessId</span></span> 

<span data-ttu-id="aeaa3-556">Идентификатор процесса браузера, на котором размещается WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-556">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="aeaa3-557">общедоступные значения HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-557">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="aeaa3-558">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="aeaa3-558">get_CanGoBack</span></span> 

<span data-ttu-id="aeaa3-559">Можно переходить по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-559">Can navigate the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="aeaa3-560">общедоступные значения HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-560">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="aeaa3-561">get_CanGoBack изменить значение с помощью события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-561">get_CanGoBack change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="aeaa3-562">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="aeaa3-562">get_CanGoForward</span></span> 

<span data-ttu-id="aeaa3-563">Можно переходить по WebView на следующую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-563">Can navigate the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="aeaa3-564">общедоступные значения HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="aeaa3-564">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="aeaa3-565">get_CanGoForward изменить значение с помощью события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-565">get_CanGoForward change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="aeaa3-566">GoBack</span><span class="sxs-lookup"><span data-stu-id="aeaa3-566">GoBack</span></span> 

<span data-ttu-id="aeaa3-567">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-567">Navigates the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="aeaa3-568">общедоступное значение HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="aeaa3-568">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="aeaa3-569">GoForward</span><span class="sxs-lookup"><span data-stu-id="aeaa3-569">GoForward</span></span> 

<span data-ttu-id="aeaa3-570">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-570">Navigates the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="aeaa3-571">общедоступные значения HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="aeaa3-571">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="aeaa3-572">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-572">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="aeaa3-573">Формат изображения, используемый в методе [IWebView2WebView:: CapturePreview](#capturepreview) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-573">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>

> <span data-ttu-id="aeaa3-574">[WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) перечисления</span><span class="sxs-lookup"><span data-stu-id="aeaa3-574">enum [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="aeaa3-575">Данные</span><span class="sxs-lookup"><span data-stu-id="aeaa3-575">Values</span></span>                         | <span data-ttu-id="aeaa3-576">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-576">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="aeaa3-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="aeaa3-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="aeaa3-578">Формат изображения PNG.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-578">PNG image format.</span></span>
<span data-ttu-id="aeaa3-579">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="aeaa3-579">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="aeaa3-580">Формат изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-580">JPEG image format.</span></span>

#### <span data-ttu-id="aeaa3-581">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="aeaa3-581">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="aeaa3-582">Диалоговое окно вида JavaScript, используемое в интерфейсе [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-582">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>

> <span data-ttu-id="aeaa3-583">[WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="aeaa3-583">enum [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="aeaa3-584">Данные</span><span class="sxs-lookup"><span data-stu-id="aeaa3-584">Values</span></span>                         | <span data-ttu-id="aeaa3-585">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-585">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="aeaa3-586">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-586">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="aeaa3-587">Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-587">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="aeaa3-588">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="aeaa3-588">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="aeaa3-589">Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-589">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="aeaa3-590">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-590">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="aeaa3-591">Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-591">A dialog invoked via the window.prompt JavaScript function.</span></span>

#### <span data-ttu-id="aeaa3-592">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="aeaa3-592">WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="aeaa3-593">Состояние сбоя процесса, используемого в интерфейсе [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-593">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>

> <span data-ttu-id="aeaa3-594">[WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="aeaa3-594">enum [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)</span></span>

 <span data-ttu-id="aeaa3-595">Данные</span><span class="sxs-lookup"><span data-stu-id="aeaa3-595">Values</span></span>                         | <span data-ttu-id="aeaa3-596">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-596">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="aeaa3-597">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-597">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="aeaa3-598">Указывает, что процесс браузера неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-598">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="aeaa3-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="aeaa3-600">Указывает, что процесс обработки неожиданно завершился.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-600">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="aeaa3-601">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-601">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="aeaa3-602">Указывает на то, что процесс рендеринга перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-602">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="aeaa3-603">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-603">WEBVIEW2_PERMISSION_TYPE</span></span> 

<span data-ttu-id="aeaa3-604">Тип запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-604">The type of a permission request.</span></span>

> <span data-ttu-id="aeaa3-605">[WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) перечисления</span><span class="sxs-lookup"><span data-stu-id="aeaa3-605">enum [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)</span></span>

 <span data-ttu-id="aeaa3-606">Данные</span><span class="sxs-lookup"><span data-stu-id="aeaa3-606">Values</span></span>                         | <span data-ttu-id="aeaa3-607">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-607">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="aeaa3-608">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="aeaa3-608">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="aeaa3-609">Неизвестное разрешение.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-609">Unknown permission.</span></span>
<span data-ttu-id="aeaa3-610">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-610">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span></span>            | <span data-ttu-id="aeaa3-611">Разрешение на запись звука.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-611">Permission to capture audio.</span></span>
<span data-ttu-id="aeaa3-612">WEBVIEW2_PERMISSION_TYPE_CAMERA</span><span class="sxs-lookup"><span data-stu-id="aeaa3-612">WEBVIEW2_PERMISSION_TYPE_CAMERA</span></span>            | <span data-ttu-id="aeaa3-613">Разрешение на захват видео.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-613">Permission to capture video.</span></span>
<span data-ttu-id="aeaa3-614">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="aeaa3-614">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span></span>            | <span data-ttu-id="aeaa3-615">Разрешение на доступ к географической позиции.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-615">Permission to access geolocation.</span></span>
<span data-ttu-id="aeaa3-616">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="aeaa3-616">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span></span>            | <span data-ttu-id="aeaa3-617">Разрешение на отправку веб-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-617">Permission to send web notifications.</span></span>
<span data-ttu-id="aeaa3-618">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="aeaa3-618">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span></span>            | <span data-ttu-id="aeaa3-619">Разрешение на доступ к универсальному датчику.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-619">Permission to access generic sensor.</span></span>
<span data-ttu-id="aeaa3-620">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="aeaa3-620">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span></span>            | <span data-ttu-id="aeaa3-621">Разрешение на чтение системного буфера обмена без жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-621">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="aeaa3-622">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-622">WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="aeaa3-623">Ответ на запрос разрешения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-623">Response to a permission request.</span></span>

> <span data-ttu-id="aeaa3-624">[WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) перечисления</span><span class="sxs-lookup"><span data-stu-id="aeaa3-624">enum [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)</span></span>

 <span data-ttu-id="aeaa3-625">Данные</span><span class="sxs-lookup"><span data-stu-id="aeaa3-625">Values</span></span>                         | <span data-ttu-id="aeaa3-626">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-626">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="aeaa3-627">WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-627">WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="aeaa3-628">Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-628">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="aeaa3-629">WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="aeaa3-629">WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="aeaa3-630">Предоставьте разрешение на запрос.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-630">Grant the permission request.</span></span>
<span data-ttu-id="aeaa3-631">WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="aeaa3-631">WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="aeaa3-632">Отказ от запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-632">Deny the permission request.</span></span>

#### <span data-ttu-id="aeaa3-633">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="aeaa3-633">WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="aeaa3-634">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-634">Reason for moving focus.</span></span>

> <span data-ttu-id="aeaa3-635">[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) перечисления</span><span class="sxs-lookup"><span data-stu-id="aeaa3-635">enum [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)</span></span>

 <span data-ttu-id="aeaa3-636">Данные</span><span class="sxs-lookup"><span data-stu-id="aeaa3-636">Values</span></span>                         | <span data-ttu-id="aeaa3-637">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-637">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="aeaa3-638">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="aeaa3-638">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="aeaa3-639">Настройка кода фокуса на WebView.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-639">Code setting focus into WebView.</span></span>
<span data-ttu-id="aeaa3-640">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-640">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="aeaa3-641">Перемещение фокуса из-за прохождения вкладки вперед.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-641">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="aeaa3-642">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="aeaa3-642">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="aeaa3-643">Перемещение фокуса из-за перемещения по табуляции назад.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-643">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="aeaa3-644">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="aeaa3-644">WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="aeaa3-645">Значения состояния ошибки для переходов по веб-страницам.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-645">Error status values for web navigations.</span></span>

> <span data-ttu-id="aeaa3-646">[WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) перечисления</span><span class="sxs-lookup"><span data-stu-id="aeaa3-646">enum [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)</span></span>

 <span data-ttu-id="aeaa3-647">Данные</span><span class="sxs-lookup"><span data-stu-id="aeaa3-647">Values</span></span>                         | <span data-ttu-id="aeaa3-648">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-648">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="aeaa3-649">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="aeaa3-649">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="aeaa3-650">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-650">An unknown error occurred.</span></span>
<span data-ttu-id="aeaa3-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="aeaa3-652">Общее имя сертификата SSL не совпадает с веб-адресом.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-652">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="aeaa3-653">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-653">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="aeaa3-654">Срок действия сертификата SSL истек.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-654">The SSL certificate has expired.</span></span>
<span data-ttu-id="aeaa3-655">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="aeaa3-655">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="aeaa3-656">SSL-сертификат клиента включает ошибки.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-656">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="aeaa3-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="aeaa3-658">SSL-сертификат отозван.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-658">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="aeaa3-659">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="aeaa3-659">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="aeaa3-660">Недействительный сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-660">The SSL certificate is invalid.</span></span>
<span data-ttu-id="aeaa3-661">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-661">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="aeaa3-662">Узел недостижим.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-662">The host is unreachable.</span></span>
<span data-ttu-id="aeaa3-663">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-663">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="aeaa3-664">Время ожидания соединения истекло.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-664">The connection has timed out.</span></span>
<span data-ttu-id="aeaa3-665">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-665">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="aeaa3-666">Сервер вернул недопустимый или нераспознанный ответ.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-666">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="aeaa3-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="aeaa3-668">Соединение было прервано.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-668">The connection was aborted.</span></span>
<span data-ttu-id="aeaa3-669">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="aeaa3-669">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="aeaa3-670">Подключение было сброшено.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-670">The connection was reset.</span></span>
<span data-ttu-id="aeaa3-671">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-671">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="aeaa3-672">Соединение с Интернетом разорвано.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-672">The Internet connection has been lost.</span></span>
<span data-ttu-id="aeaa3-673">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-673">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="aeaa3-674">Не удается подключиться к конечному объекту.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-674">Cannot connect to destination.</span></span>
<span data-ttu-id="aeaa3-675">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-675">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="aeaa3-676">Не удалось разрешить указанное имя узла.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-676">Could not resolve provided host name.</span></span>
<span data-ttu-id="aeaa3-677">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-677">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="aeaa3-678">Операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-678">The operation was canceled.</span></span>
<span data-ttu-id="aeaa3-679">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="aeaa3-679">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="aeaa3-680">Перенаправление запроса завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-680">The request redirect failed.</span></span>
<span data-ttu-id="aeaa3-681">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="aeaa3-681">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="aeaa3-682">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-682">An unexpected error occurred.</span></span>

#### <span data-ttu-id="aeaa3-683">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-683">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="aeaa3-684">Перечисление для контекстов запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-684">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="aeaa3-685">[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) перечисления</span><span class="sxs-lookup"><span data-stu-id="aeaa3-685">enum [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)</span></span>

 <span data-ttu-id="aeaa3-686">Данные</span><span class="sxs-lookup"><span data-stu-id="aeaa3-686">Values</span></span>                         | <span data-ttu-id="aeaa3-687">Описания</span><span class="sxs-lookup"><span data-stu-id="aeaa3-687">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="aeaa3-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="aeaa3-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="aeaa3-689">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-689">All resources.</span></span>
<span data-ttu-id="aeaa3-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="aeaa3-691">Ресурсы документов.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-691">Document resources.</span></span>
<span data-ttu-id="aeaa3-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="aeaa3-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="aeaa3-693">Ресурсы CSS.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-693">CSS resources.</span></span>
<span data-ttu-id="aeaa3-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="aeaa3-695">Графические ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-695">Image resources.</span></span>
<span data-ttu-id="aeaa3-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="aeaa3-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="aeaa3-697">Другие мультимедийные ресурсы, например видео.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-697">Other media resources such as videos.</span></span>
<span data-ttu-id="aeaa3-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="aeaa3-699">Ресурсы шрифта.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-699">Font resources.</span></span>
<span data-ttu-id="aeaa3-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="aeaa3-701">Ресурсы сценария.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-701">Script resources.</span></span>
<span data-ttu-id="aeaa3-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="aeaa3-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="aeaa3-703">HTTP-запросы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-703">XML HTTP requests.</span></span>
<span data-ttu-id="aeaa3-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="aeaa3-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="aeaa3-705">Получение взаимодействия API.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-705">Fetch API communication.</span></span>
<span data-ttu-id="aeaa3-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="aeaa3-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="aeaa3-707">TextTrack ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-707">TextTrack resources.</span></span>
<span data-ttu-id="aeaa3-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | 
<span data-ttu-id="aeaa3-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="aeaa3-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | 
<span data-ttu-id="aeaa3-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="aeaa3-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | 
<span data-ttu-id="aeaa3-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="aeaa3-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | 
<span data-ttu-id="aeaa3-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="aeaa3-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | 
<span data-ttu-id="aeaa3-713">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="aeaa3-713">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | 
<span data-ttu-id="aeaa3-714">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="aeaa3-714">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="aeaa3-715">Другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-715">Other resources.</span></span>

---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 94c6d6c424d715d3b6b57b366b71cf8e5fb8ec42
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878213"
---
# <span data-ttu-id="16dc7-104">0.8.355-Interface IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="16dc7-104">0.8.355 - interface IWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="16dc7-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="16dc7-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="16dc7-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="16dc7-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="16dc7-107">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="16dc7-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="16dc7-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="16dc7-108">Summary</span></span>

 <span data-ttu-id="16dc7-109">Участников</span><span class="sxs-lookup"><span data-stu-id="16dc7-109">Members</span></span>                        | <span data-ttu-id="16dc7-110">Описания</span><span class="sxs-lookup"><span data-stu-id="16dc7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="16dc7-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="16dc7-112">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="16dc7-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="16dc7-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="16dc7-114">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="16dc7-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="16dc7-116">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="16dc7-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="16dc7-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="16dc7-118">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="16dc7-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="16dc7-120">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="16dc7-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="16dc7-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="16dc7-122">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="16dc7-123">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="16dc7-123">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="16dc7-124">Этот параметр устарел и всегда будет возвращать значение false.</span><span class="sxs-lookup"><span data-stu-id="16dc7-124">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="16dc7-125">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="16dc7-125">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="16dc7-126">Этот параметр устарел и не действует.</span><span class="sxs-lookup"><span data-stu-id="16dc7-126">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="16dc7-127">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-127">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="16dc7-128">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="16dc7-128">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="16dc7-129">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-129">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="16dc7-130">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-130">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="16dc7-131">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-131">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="16dc7-132">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="16dc7-132">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="16dc7-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="16dc7-134">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-134">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="16dc7-135">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="16dc7-135">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="16dc7-136">Участников</span><span class="sxs-lookup"><span data-stu-id="16dc7-136">Members</span></span>

#### <span data-ttu-id="16dc7-137">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-137">get_IsScriptEnabled</span></span> 

<span data-ttu-id="16dc7-138">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="16dc7-138">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="16dc7-139">общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-139">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="16dc7-140">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="16dc7-140">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="16dc7-141">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16dc7-141">It is true by default.</span></span>

```cpp
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
```

#### <span data-ttu-id="16dc7-142">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-142">put_IsScriptEnabled</span></span> 

<span data-ttu-id="16dc7-143">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-143">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="16dc7-144">общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-144">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="16dc7-145">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-145">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="16dc7-146">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="16dc7-146">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="16dc7-147">общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-147">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="16dc7-148">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="16dc7-148">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="16dc7-149">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="16dc7-149">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="16dc7-150">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="16dc7-150">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="16dc7-151">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="16dc7-151">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="16dc7-152">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16dc7-152">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="16dc7-153">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-153">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="16dc7-154">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-154">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="16dc7-155">общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-155">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="16dc7-156">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-156">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="16dc7-157">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="16dc7-157">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="16dc7-158">общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-158">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="16dc7-159">Если задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются в функциях оповещения JavaScript, подтверждения и запросов).</span><span class="sxs-lookup"><span data-stu-id="16dc7-159">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="16dc7-160">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="16dc7-160">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="16dc7-161">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-161">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="16dc7-162">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-162">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="16dc7-163">общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-163">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="16dc7-164">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="16dc7-164">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="16dc7-165">Этот параметр устарел и всегда будет возвращать значение false.</span><span class="sxs-lookup"><span data-stu-id="16dc7-165">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="16dc7-166">общедоступные значения HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="16dc7-166">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="16dc7-167">Это означает, что элементы в WebView будут заполнять только границы WebView.</span><span class="sxs-lookup"><span data-stu-id="16dc7-167">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="16dc7-168">Это свойство будет удалено полностью.</span><span class="sxs-lookup"><span data-stu-id="16dc7-168">This property will then be completely removed.</span></span> <span data-ttu-id="16dc7-169">Вместо этого пожалуйста, прослушайте событие ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="16dc7-169">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="16dc7-170">Определяет, разрешено ли полноэкранное воспроизведение элементов в WebView.</span><span class="sxs-lookup"><span data-stu-id="16dc7-170">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="16dc7-171">Если это разрешено, веб-содержимое, например элемент видео в WebView, может быть отображено во весь экран.</span><span class="sxs-lookup"><span data-stu-id="16dc7-171">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="16dc7-172">Если это значение не разрешено, этот элемент будет заполнять границы WebView, когда элемент запрашивает весь экран.</span><span class="sxs-lookup"><span data-stu-id="16dc7-172">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="16dc7-173">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16dc7-173">It is true by default.</span></span>

#### <span data-ttu-id="16dc7-174">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="16dc7-174">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="16dc7-175">Этот параметр устарел и не действует.</span><span class="sxs-lookup"><span data-stu-id="16dc7-175">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="16dc7-176">общедоступные значения HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(bool IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="16dc7-176">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="16dc7-177">Вместо этого пожалуйста, прослушайте событие ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="16dc7-177">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="16dc7-178">Задайте свойство IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="16dc7-178">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="16dc7-179">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-179">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="16dc7-180">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="16dc7-180">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="16dc7-181">общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-181">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="16dc7-182">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="16dc7-182">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="16dc7-183">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16dc7-183">It is true by default.</span></span>

#### <span data-ttu-id="16dc7-184">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-184">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="16dc7-185">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-185">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="16dc7-186">общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-186">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="16dc7-187">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-187">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="16dc7-188">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="16dc7-188">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="16dc7-189">общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-189">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="16dc7-190">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16dc7-190">It is true by default.</span></span>

#### <span data-ttu-id="16dc7-191">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="16dc7-191">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="16dc7-192">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="16dc7-192">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="16dc7-193">общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="16dc7-193">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>


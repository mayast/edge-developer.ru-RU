---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 649506b28e0ecdbff33b44bbd8010ddb3d2a66b0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885802"
---
# <span data-ttu-id="2ae1a-104">0.8.355-Interface IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="2ae1a-104">0.8.355 - interface IWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="2ae1a-105">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="2ae1a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2ae1a-106">Summary</span></span>

 <span data-ttu-id="2ae1a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2ae1a-107">Members</span></span>                        | <span data-ttu-id="2ae1a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2ae1a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2ae1a-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="2ae1a-110">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="2ae1a-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="2ae1a-112">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="2ae1a-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="2ae1a-114">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="2ae1a-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="2ae1a-116">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="2ae1a-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="2ae1a-118">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="2ae1a-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="2ae1a-120">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="2ae1a-121">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="2ae1a-121">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="2ae1a-122">Этот параметр устарел и всегда будет возвращать значение false.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-122">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="2ae1a-123">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="2ae1a-123">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="2ae1a-124">Этот параметр устарел и не действует.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-124">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="2ae1a-125">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-125">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="2ae1a-126">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="2ae1a-127">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-127">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="2ae1a-128">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-128">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="2ae1a-129">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-129">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="2ae1a-130">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-130">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="2ae1a-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="2ae1a-132">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-132">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="2ae1a-133">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-133">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="2ae1a-134">Участников</span><span class="sxs-lookup"><span data-stu-id="2ae1a-134">Members</span></span>

#### <span data-ttu-id="2ae1a-135">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-135">get_IsScriptEnabled</span></span> 

<span data-ttu-id="2ae1a-136">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-136">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="2ae1a-137">общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-137">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="2ae1a-138">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-138">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="2ae1a-139">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-139">It is true by default.</span></span>

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

#### <span data-ttu-id="2ae1a-140">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-140">put_IsScriptEnabled</span></span> 

<span data-ttu-id="2ae1a-141">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-141">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="2ae1a-142">общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-142">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="2ae1a-143">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-143">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="2ae1a-144">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-144">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="2ae1a-145">общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-145">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="2ae1a-146">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-146">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="2ae1a-147">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-147">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="2ae1a-148">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-148">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="2ae1a-149">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-149">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="2ae1a-150">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-150">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="2ae1a-151">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-151">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="2ae1a-152">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-152">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="2ae1a-153">общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-153">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="2ae1a-154">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-154">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="2ae1a-155">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-155">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="2ae1a-156">общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-156">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="2ae1a-157">Если задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются в функциях оповещения JavaScript, подтверждения и запросов).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-157">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="2ae1a-158">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-158">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="2ae1a-159">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-159">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="2ae1a-160">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-160">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="2ae1a-161">общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-161">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="2ae1a-162">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="2ae1a-162">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="2ae1a-163">Этот параметр устарел и всегда будет возвращать значение false.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-163">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="2ae1a-164">общедоступные значения HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-164">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="2ae1a-165">Это означает, что элементы в WebView будут заполнять только границы WebView.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-165">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="2ae1a-166">Это свойство будет удалено полностью.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-166">This property will then be completely removed.</span></span> <span data-ttu-id="2ae1a-167">Вместо этого пожалуйста, прослушайте событие ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-167">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="2ae1a-168">Определяет, разрешено ли полноэкранное воспроизведение элементов в WebView.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-168">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="2ae1a-169">Если это разрешено, веб-содержимое, например элемент видео в WebView, может быть отображено во весь экран.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-169">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="2ae1a-170">Если это значение не разрешено, этот элемент будет заполнять границы WebView, когда элемент запрашивает весь экран.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-170">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="2ae1a-171">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-171">It is true by default.</span></span>

#### <span data-ttu-id="2ae1a-172">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="2ae1a-172">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="2ae1a-173">Этот параметр устарел и не действует.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-173">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="2ae1a-174">общедоступные значения HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(bool IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-174">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="2ae1a-175">Вместо этого пожалуйста, прослушайте событие ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-175">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="2ae1a-176">Задайте свойство IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-176">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="2ae1a-177">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-177">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="2ae1a-178">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-178">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="2ae1a-179">общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-179">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="2ae1a-180">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-180">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="2ae1a-181">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-181">It is true by default.</span></span>

#### <span data-ttu-id="2ae1a-182">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-182">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="2ae1a-183">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-183">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="2ae1a-184">общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-184">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="2ae1a-185">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-185">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="2ae1a-186">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-186">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="2ae1a-187">общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-187">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="2ae1a-188">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-188">It is true by default.</span></span>

#### <span data-ttu-id="2ae1a-189">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ae1a-189">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="2ae1a-190">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-190">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="2ae1a-191">общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="2ae1a-191">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>


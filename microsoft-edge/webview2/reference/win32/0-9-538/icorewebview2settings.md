---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2Settings
ms.openlocfilehash: 24a1e06be83fbb5c510c455e80c52b7165dabcde
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879592"
---
# <span data-ttu-id="c300d-104">интерфейс ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="c300d-104">interface ICoreWebView2Settings</span></span> 

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="c300d-105">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="c300d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c300d-106">Summary</span></span>

 <span data-ttu-id="c300d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c300d-107">Members</span></span>                        | <span data-ttu-id="c300d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c300d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c300d-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="c300d-110">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="c300d-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="c300d-112">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="c300d-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="c300d-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="c300d-114">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="c300d-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="c300d-115">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c300d-115">get_AreHostObjectsAllowed</span></span>](#get_arehostobjectsallowed) | <span data-ttu-id="c300d-116">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-116">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="c300d-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="c300d-118">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="c300d-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="c300d-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="c300d-120">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="c300d-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="c300d-122">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="c300d-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="c300d-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="c300d-124">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="c300d-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="c300d-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="c300d-126">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="c300d-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="c300d-128">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="c300d-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="c300d-130">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="c300d-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="c300d-132">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="c300d-133">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c300d-133">put_AreHostObjectsAllowed</span></span>](#put_arehostobjectsallowed) | <span data-ttu-id="c300d-134">Задайте свойство AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="c300d-134">Set the AreHostObjectsAllowed property.</span></span>
[<span data-ttu-id="c300d-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="c300d-136">Задайте свойство IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="c300d-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="c300d-138">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="c300d-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="c300d-140">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="c300d-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="c300d-142">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="c300d-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="c300d-144">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="c300d-145">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="c300d-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="c300d-146">Участников</span><span class="sxs-lookup"><span data-stu-id="c300d-146">Members</span></span>

#### <span data-ttu-id="c300d-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="c300d-148">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="c300d-149">общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="c300d-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="c300d-150">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c300d-150">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="c300d-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="c300d-152">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="c300d-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="c300d-153">общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="c300d-154">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="c300d-154">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="c300d-155">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c300d-155">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="c300d-156">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-156">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="c300d-157">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="c300d-157">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="c300d-158">общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-158">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="c300d-159">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c300d-159">It is true by default.</span></span>

#### <span data-ttu-id="c300d-160">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c300d-160">get_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="c300d-161">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-161">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="c300d-162">общедоступные значения HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(логический \* разрешено)</span><span class="sxs-lookup"><span data-stu-id="c300d-162">public HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="c300d-163">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c300d-163">Defaults to TRUE.</span></span>

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="c300d-164">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-164">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="c300d-165">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="c300d-165">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="c300d-166">общедоступные значения HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="c300d-166">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="c300d-167">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c300d-167">Defaults to TRUE.</span></span> <span data-ttu-id="c300d-168">Если эта ошибка отключена, при возникновении связанной ошибки будет отображаться пустая страница.</span><span class="sxs-lookup"><span data-stu-id="c300d-168">When disabled, blank page will be shown when related error happens.</span></span>

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="c300d-169">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-169">get_IsScriptEnabled</span></span> 

<span data-ttu-id="c300d-170">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-170">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="c300d-171">общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-171">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="c300d-172">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="c300d-172">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="c300d-173">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c300d-173">It is true by default.</span></span>

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

#### <span data-ttu-id="c300d-174">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-174">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="c300d-175">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="c300d-175">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="c300d-176">общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-176">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="c300d-177">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="c300d-177">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="c300d-178">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c300d-178">It is true by default.</span></span>

#### <span data-ttu-id="c300d-179">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-179">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="c300d-180">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="c300d-180">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="c300d-181">общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-181">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="c300d-182">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="c300d-182">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="c300d-183">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="c300d-183">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="c300d-184">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="c300d-184">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="c300d-185">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="c300d-185">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="c300d-186">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c300d-186">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="c300d-187">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-187">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="c300d-188">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="c300d-188">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="c300d-189">общедоступные значения HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="c300d-189">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="c300d-190">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c300d-190">Defaults to TRUE.</span></span> <span data-ttu-id="c300d-191">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать через API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="c300d-191">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="c300d-192">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-192">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="c300d-193">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-193">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="c300d-194">общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="c300d-194">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="c300d-195">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-195">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="c300d-196">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-196">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="c300d-197">общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-197">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="c300d-198">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-198">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="c300d-199">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-199">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="c300d-200">общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-200">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="c300d-201">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c300d-201">put_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="c300d-202">Задайте свойство AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="c300d-202">Set the AreHostObjectsAllowed property.</span></span>

> <span data-ttu-id="c300d-203">общедоступная [PUT_AREHOSTOBJECTSALLOWED](#put_arehostobjectsallowed)HRESULT (допустимая bool)</span><span class="sxs-lookup"><span data-stu-id="c300d-203">public HRESULT [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="c300d-204">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-204">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="c300d-205">Задайте свойство IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-205">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="c300d-206">общедоступные значения HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="c300d-206">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="c300d-207">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-207">put_IsScriptEnabled</span></span> 

<span data-ttu-id="c300d-208">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-208">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="c300d-209">общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-209">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="c300d-210">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-210">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="c300d-211">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-211">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="c300d-212">общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-212">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="c300d-213">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-213">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="c300d-214">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-214">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="c300d-215">общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="c300d-215">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="c300d-216">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c300d-216">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="c300d-217">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="c300d-217">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="c300d-218">общедоступные значения HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="c300d-218">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>


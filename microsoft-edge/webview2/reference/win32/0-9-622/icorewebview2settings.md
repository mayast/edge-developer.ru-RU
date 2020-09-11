---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2Settings
ms.openlocfilehash: 1ad6754d2ff59a92e107c66644e389582ff6053b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012513"
---
# <span data-ttu-id="4dd4f-104">интерфейс ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="4dd4f-104">interface ICoreWebView2Settings</span></span> 

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="4dd4f-105">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="4dd4f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4dd4f-106">Summary</span></span>

 <span data-ttu-id="4dd4f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="4dd4f-107">Members</span></span>                        | <span data-ttu-id="4dd4f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="4dd4f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4dd4f-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="4dd4f-110">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>
[<span data-ttu-id="4dd4f-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="4dd4f-112">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="4dd4f-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="4dd4f-114">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="4dd4f-115">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="4dd4f-115">get_AreHostObjectsAllowed</span></span>](#get_arehostobjectsallowed) | <span data-ttu-id="4dd4f-116">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-116">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>
[<span data-ttu-id="4dd4f-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="4dd4f-118">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="4dd4f-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="4dd4f-120">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="4dd4f-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="4dd4f-122">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="4dd4f-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="4dd4f-124">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="4dd4f-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="4dd4f-126">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="4dd4f-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="4dd4f-128">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="4dd4f-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="4dd4f-130">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="4dd4f-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="4dd4f-132">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="4dd4f-133">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="4dd4f-133">put_AreHostObjectsAllowed</span></span>](#put_arehostobjectsallowed) | <span data-ttu-id="4dd4f-134">Задайте свойство AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-134">Set the AreHostObjectsAllowed property.</span></span>
[<span data-ttu-id="4dd4f-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="4dd4f-136">Задайте свойство IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="4dd4f-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="4dd4f-138">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="4dd4f-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="4dd4f-140">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="4dd4f-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="4dd4f-142">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="4dd4f-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="4dd4f-144">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="4dd4f-145">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="4dd4f-146">Участников</span><span class="sxs-lookup"><span data-stu-id="4dd4f-146">Members</span></span>

#### <span data-ttu-id="4dd4f-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="4dd4f-148">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>

> <span data-ttu-id="4dd4f-149">общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="4dd4f-150">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-150">It is true by default.</span></span>

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

#### <span data-ttu-id="4dd4f-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="4dd4f-152">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="4dd4f-153">общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="4dd4f-154">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="4dd4f-154">If set to false, then WebView won't render the default JavaScript dialog box (Specifically those shown by the JavaScript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="4dd4f-155">Вместо этого, если обработчик событий задается посредством add_ScriptDialogOpening, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отображать собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-155">Instead, if an event handler is set via add_ScriptDialogOpening, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span> <span data-ttu-id="4dd4f-156">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-156">It is true by default.</span></span>

#### <span data-ttu-id="4dd4f-157">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-157">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="4dd4f-158">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-158">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="4dd4f-159">общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-159">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="4dd4f-160">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-160">It is true by default.</span></span>

#### <span data-ttu-id="4dd4f-161">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="4dd4f-161">get_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="4dd4f-162">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-162">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>

> <span data-ttu-id="4dd4f-163">общедоступные значения HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(логический \* разрешено)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-163">public HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="4dd4f-164">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-164">It is true by default.</span></span>

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

#### <span data-ttu-id="4dd4f-165">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-165">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="4dd4f-166">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-166">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="4dd4f-167">общедоступные значения HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-167">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="4dd4f-168">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-168">It is true by default.</span></span> <span data-ttu-id="4dd4f-169">Если эта ошибка отключена, при возникновении связанной ошибки будет отображаться пустая страница.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-169">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="4dd4f-170">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-170">get_IsScriptEnabled</span></span> 

<span data-ttu-id="4dd4f-171">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-171">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="4dd4f-172">общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-172">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="4dd4f-173">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-173">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="4dd4f-174">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-174">It is true by default.</span></span>

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

#### <span data-ttu-id="4dd4f-175">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-175">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="4dd4f-176">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-176">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="4dd4f-177">общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-177">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="4dd4f-178">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-178">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="4dd4f-179">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-179">It is true by default.</span></span>

#### <span data-ttu-id="4dd4f-180">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-180">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="4dd4f-181">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-181">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="4dd4f-182">общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-182">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="4dd4f-183">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="4dd4f-183">If set to true, communication from the host to the WebView's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="4dd4f-184">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции WebView и метода add_WebMessageReceived (Дополнительные сведения можно найти в add_WebMessageReceived документации).</span><span class="sxs-lookup"><span data-stu-id="4dd4f-184">Communication from the WebView's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and add_WebMessageReceived method (see add_WebMessageReceived documentation for details).</span></span> <span data-ttu-id="4dd4f-185">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-185">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="4dd4f-186">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-186">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="4dd4f-187">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-187">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="4dd4f-188">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-188">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="4dd4f-189">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-189">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="4dd4f-190">общедоступные значения HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-190">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="4dd4f-191">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-191">It is true by default.</span></span> <span data-ttu-id="4dd4f-192">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать через API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-192">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="4dd4f-193">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-193">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="4dd4f-194">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-194">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="4dd4f-195">общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-195">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="4dd4f-196">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-196">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="4dd4f-197">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-197">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="4dd4f-198">общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-198">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="4dd4f-199">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-199">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="4dd4f-200">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-200">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="4dd4f-201">общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-201">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="4dd4f-202">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="4dd4f-202">put_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="4dd4f-203">Задайте свойство AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-203">Set the AreHostObjectsAllowed property.</span></span>

> <span data-ttu-id="4dd4f-204">общедоступная [PUT_AREHOSTOBJECTSALLOWED](#put_arehostobjectsallowed)HRESULT (допустимая bool)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-204">public HRESULT [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="4dd4f-205">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-205">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="4dd4f-206">Задайте свойство IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-206">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="4dd4f-207">общедоступные значения HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-207">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="4dd4f-208">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-208">put_IsScriptEnabled</span></span> 

<span data-ttu-id="4dd4f-209">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-209">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="4dd4f-210">общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-210">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="4dd4f-211">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-211">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="4dd4f-212">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-212">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="4dd4f-213">общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-213">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="4dd4f-214">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-214">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="4dd4f-215">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-215">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="4dd4f-216">общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-216">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="4dd4f-217">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd4f-217">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="4dd4f-218">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-218">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="4dd4f-219">общедоступные значения HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-219">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>


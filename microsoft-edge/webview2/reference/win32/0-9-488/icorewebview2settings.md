---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a2ecd4bdb2d27a5e881f52791ae21290c748966a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886495"
---
# <span data-ttu-id="8d9d2-104">0.9.515-Interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="8d9d2-104">0.9.515 - interface ICoreWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="8d9d2-105">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="8d9d2-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8d9d2-106">Summary</span></span>

 <span data-ttu-id="8d9d2-107">Участников</span><span class="sxs-lookup"><span data-stu-id="8d9d2-107">Members</span></span>                        | <span data-ttu-id="8d9d2-108">Описания</span><span class="sxs-lookup"><span data-stu-id="8d9d2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8d9d2-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="8d9d2-110">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="8d9d2-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="8d9d2-112">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="8d9d2-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="8d9d2-114">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="8d9d2-115">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="8d9d2-115">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="8d9d2-116">Свойство AreRemoteObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-116">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="8d9d2-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="8d9d2-118">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="8d9d2-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="8d9d2-120">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="8d9d2-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="8d9d2-122">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="8d9d2-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="8d9d2-124">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="8d9d2-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="8d9d2-126">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="8d9d2-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="8d9d2-128">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="8d9d2-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="8d9d2-130">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="8d9d2-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="8d9d2-132">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="8d9d2-133">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="8d9d2-133">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="8d9d2-134">Задайте свойство AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-134">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="8d9d2-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="8d9d2-136">Задайте свойство IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="8d9d2-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="8d9d2-138">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="8d9d2-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="8d9d2-140">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="8d9d2-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="8d9d2-142">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="8d9d2-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="8d9d2-144">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="8d9d2-145">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="8d9d2-146">Участников</span><span class="sxs-lookup"><span data-stu-id="8d9d2-146">Members</span></span>

#### <span data-ttu-id="8d9d2-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="8d9d2-148">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="8d9d2-149">общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="8d9d2-150">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-150">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="8d9d2-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="8d9d2-152">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="8d9d2-153">общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="8d9d2-154">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="8d9d2-154">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="8d9d2-155">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-155">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="8d9d2-156">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-156">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="8d9d2-157">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-157">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="8d9d2-158">общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-158">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="8d9d2-159">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-159">It is true by default.</span></span>

#### <span data-ttu-id="8d9d2-160">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="8d9d2-160">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="8d9d2-161">Свойство AreRemoteObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-161">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="8d9d2-162">общедоступные значения HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(логический \* разрешено)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-162">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="8d9d2-163">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-163">Defaults to TRUE.</span></span>

```cpp
            BOOL allowRemoteObjects;
            CHECK_FAILURE(m_settings->get_AreRemoteObjectsAllowed(&allowRemoteObjects));
            if (allowRemoteObjects)
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to remote objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to remote objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="8d9d2-164">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-164">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="8d9d2-165">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-165">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="8d9d2-166">общедоступные значения HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-166">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="8d9d2-167">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-167">Defaults to TRUE.</span></span> <span data-ttu-id="8d9d2-168">Если эта ошибка отключена, при возникновении связанной ошибки будет отображаться пустая страница.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-168">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="8d9d2-169">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-169">get_IsScriptEnabled</span></span> 

<span data-ttu-id="8d9d2-170">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-170">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="8d9d2-171">общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-171">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="8d9d2-172">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-172">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="8d9d2-173">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-173">It is true by default.</span></span>

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

#### <span data-ttu-id="8d9d2-174">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-174">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="8d9d2-175">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-175">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="8d9d2-176">общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-176">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="8d9d2-177">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-177">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="8d9d2-178">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-178">It is true by default.</span></span>

#### <span data-ttu-id="8d9d2-179">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-179">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="8d9d2-180">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-180">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="8d9d2-181">общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-181">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="8d9d2-182">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="8d9d2-182">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="8d9d2-183">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="8d9d2-183">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="8d9d2-184">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-184">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="8d9d2-185">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-185">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="8d9d2-186">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-186">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="8d9d2-187">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-187">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="8d9d2-188">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-188">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="8d9d2-189">общедоступные значения HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-189">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="8d9d2-190">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-190">Defaults to TRUE.</span></span> <span data-ttu-id="8d9d2-191">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать через API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-191">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="8d9d2-192">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-192">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="8d9d2-193">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-193">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="8d9d2-194">общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-194">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="8d9d2-195">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-195">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="8d9d2-196">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-196">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="8d9d2-197">общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-197">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="8d9d2-198">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-198">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="8d9d2-199">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-199">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="8d9d2-200">общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-200">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="8d9d2-201">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="8d9d2-201">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="8d9d2-202">Задайте свойство AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-202">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="8d9d2-203">общедоступная [PUT_AREREMOTEOBJECTSALLOWED](#put_areremoteobjectsallowed)HRESULT (допустимая bool)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-203">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="8d9d2-204">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-204">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="8d9d2-205">Задайте свойство IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-205">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="8d9d2-206">общедоступные значения HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-206">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="8d9d2-207">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-207">put_IsScriptEnabled</span></span> 

<span data-ttu-id="8d9d2-208">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-208">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="8d9d2-209">общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-209">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="8d9d2-210">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-210">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="8d9d2-211">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-211">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="8d9d2-212">общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-212">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="8d9d2-213">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-213">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="8d9d2-214">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-214">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="8d9d2-215">общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-215">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="8d9d2-216">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="8d9d2-216">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="8d9d2-217">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-217">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="8d9d2-218">общедоступные значения HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-218">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>


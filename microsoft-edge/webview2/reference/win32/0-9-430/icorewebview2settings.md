---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2596b2352f36dce6773de2e60e0442ff5fa3b6d5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880222"
---
# <span data-ttu-id="feaad-104">0.9.430-Interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="feaad-104">0.9.430 - interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="feaad-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="feaad-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="feaad-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="feaad-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="feaad-107">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="feaad-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="feaad-108">Summary</span></span>

 <span data-ttu-id="feaad-109">Участников</span><span class="sxs-lookup"><span data-stu-id="feaad-109">Members</span></span>                        | <span data-ttu-id="feaad-110">Описания</span><span class="sxs-lookup"><span data-stu-id="feaad-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="feaad-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="feaad-112">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="feaad-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="feaad-114">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="feaad-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="feaad-116">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="feaad-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="feaad-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="feaad-118">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="feaad-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="feaad-120">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="feaad-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="feaad-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="feaad-122">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="feaad-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="feaad-124">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="feaad-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="feaad-125">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-125">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="feaad-126">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-126">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="feaad-127">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-127">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="feaad-128">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="feaad-128">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="feaad-129">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-129">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="feaad-130">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-130">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="feaad-131">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-131">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="feaad-132">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="feaad-133">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-133">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="feaad-134">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-134">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="feaad-135">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="feaad-135">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="feaad-136">Свойство AreRemoteObjectsAllowed используется для управления доступом к удаленным объектам на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-136">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="feaad-137">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="feaad-137">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="feaad-138">Задайте свойство AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="feaad-138">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="feaad-139">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-139">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="feaad-140">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-140">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="feaad-141">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-141">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="feaad-142">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-142">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="feaad-143">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="feaad-143">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="feaad-144">Участников</span><span class="sxs-lookup"><span data-stu-id="feaad-144">Members</span></span>

#### <span data-ttu-id="feaad-145">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-145">get_IsScriptEnabled</span></span> 

<span data-ttu-id="feaad-146">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-146">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="feaad-147">общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-147">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="feaad-148">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="feaad-148">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="feaad-149">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="feaad-149">It is true by default.</span></span>

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

#### <span data-ttu-id="feaad-150">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-150">put_IsScriptEnabled</span></span> 

<span data-ttu-id="feaad-151">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-151">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="feaad-152">общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-152">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="feaad-153">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-153">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="feaad-154">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="feaad-154">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="feaad-155">общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-155">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="feaad-156">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="feaad-156">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="feaad-157">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="feaad-157">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="feaad-158">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="feaad-158">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="feaad-159">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="feaad-159">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="feaad-160">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="feaad-160">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="feaad-161">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-161">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="feaad-162">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-162">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="feaad-163">общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-163">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="feaad-164">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-164">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="feaad-165">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="feaad-165">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="feaad-166">общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-166">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="feaad-167">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="feaad-167">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="feaad-168">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="feaad-168">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="feaad-169">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-169">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="feaad-170">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-170">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="feaad-171">общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-171">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="feaad-172">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-172">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="feaad-173">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="feaad-173">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="feaad-174">общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-174">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="feaad-175">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="feaad-175">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="feaad-176">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="feaad-176">It is true by default.</span></span>

#### <span data-ttu-id="feaad-177">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-177">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="feaad-178">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-178">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="feaad-179">общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-179">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="feaad-180">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-180">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="feaad-181">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="feaad-181">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="feaad-182">общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-182">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="feaad-183">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="feaad-183">It is true by default.</span></span>

#### <span data-ttu-id="feaad-184">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-184">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="feaad-185">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-185">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="feaad-186">общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="feaad-186">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="feaad-187">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-187">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="feaad-188">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-188">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="feaad-189">общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="feaad-189">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="feaad-190">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="feaad-190">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="feaad-191">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-191">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="feaad-192">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-192">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="feaad-193">общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="feaad-193">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="feaad-194">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="feaad-194">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="feaad-195">Свойство AreRemoteObjectsAllowed используется для управления доступом к удаленным объектам на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-195">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="feaad-196">общедоступные значения HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(логический \* разрешено)</span><span class="sxs-lookup"><span data-stu-id="feaad-196">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="feaad-197">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="feaad-197">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="feaad-198">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="feaad-198">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="feaad-199">Задайте свойство AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="feaad-199">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="feaad-200">общедоступная [PUT_AREREMOTEOBJECTSALLOWED](#put_areremoteobjectsallowed)HRESULT (допустимая bool)</span><span class="sxs-lookup"><span data-stu-id="feaad-200">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="feaad-201">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-201">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="feaad-202">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="feaad-202">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="feaad-203">общедоступные значения HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="feaad-203">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="feaad-204">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="feaad-204">Defaults to TRUE.</span></span> <span data-ttu-id="feaad-205">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать с помощью put_ZoomFactor API.</span><span class="sxs-lookup"><span data-stu-id="feaad-205">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control is disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control is enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="feaad-206">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="feaad-206">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="feaad-207">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="feaad-207">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="feaad-208">общедоступные значения HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="feaad-208">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>


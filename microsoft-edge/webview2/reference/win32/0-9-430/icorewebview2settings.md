---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 70ccef9e99b3649ceca49b736570ba416cf73ebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883989"
---
# <span data-ttu-id="c2a27-104">0.9.430-Interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="c2a27-104">0.9.430 - interface ICoreWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="c2a27-105">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="c2a27-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c2a27-106">Summary</span></span>

 <span data-ttu-id="c2a27-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c2a27-107">Members</span></span>                        | <span data-ttu-id="c2a27-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c2a27-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c2a27-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="c2a27-110">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="c2a27-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="c2a27-112">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="c2a27-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="c2a27-114">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="c2a27-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="c2a27-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="c2a27-116">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="c2a27-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="c2a27-118">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="c2a27-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="c2a27-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="c2a27-120">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="c2a27-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="c2a27-122">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="c2a27-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="c2a27-123">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-123">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="c2a27-124">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-124">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="c2a27-125">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-125">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="c2a27-126">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="c2a27-126">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="c2a27-127">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-127">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="c2a27-128">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-128">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="c2a27-129">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-129">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="c2a27-130">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-130">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="c2a27-131">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-131">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="c2a27-132">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-132">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="c2a27-133">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c2a27-133">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="c2a27-134">Свойство AreRemoteObjectsAllowed используется для управления доступом к удаленным объектам на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-134">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="c2a27-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c2a27-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="c2a27-136">Задайте свойство AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="c2a27-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="c2a27-137">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-137">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="c2a27-138">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-138">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="c2a27-139">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-139">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="c2a27-140">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-140">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="c2a27-141">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="c2a27-141">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="c2a27-142">Участников</span><span class="sxs-lookup"><span data-stu-id="c2a27-142">Members</span></span>

#### <span data-ttu-id="c2a27-143">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-143">get_IsScriptEnabled</span></span> 

<span data-ttu-id="c2a27-144">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-144">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="c2a27-145">общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-145">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="c2a27-146">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="c2a27-146">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="c2a27-147">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2a27-147">It is true by default.</span></span>

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

#### <span data-ttu-id="c2a27-148">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-148">put_IsScriptEnabled</span></span> 

<span data-ttu-id="c2a27-149">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-149">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="c2a27-150">общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-150">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="c2a27-151">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-151">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="c2a27-152">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="c2a27-152">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="c2a27-153">общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-153">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="c2a27-154">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="c2a27-154">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="c2a27-155">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="c2a27-155">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="c2a27-156">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="c2a27-156">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="c2a27-157">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="c2a27-157">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="c2a27-158">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2a27-158">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="c2a27-159">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-159">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="c2a27-160">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-160">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="c2a27-161">общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-161">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="c2a27-162">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-162">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="c2a27-163">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="c2a27-163">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="c2a27-164">общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-164">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="c2a27-165">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="c2a27-165">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="c2a27-166">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c2a27-166">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="c2a27-167">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-167">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="c2a27-168">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-168">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="c2a27-169">общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-169">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="c2a27-170">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-170">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="c2a27-171">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="c2a27-171">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="c2a27-172">общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-172">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="c2a27-173">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="c2a27-173">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="c2a27-174">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2a27-174">It is true by default.</span></span>

#### <span data-ttu-id="c2a27-175">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-175">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="c2a27-176">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-176">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="c2a27-177">общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-177">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="c2a27-178">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-178">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="c2a27-179">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="c2a27-179">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="c2a27-180">общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-180">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="c2a27-181">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2a27-181">It is true by default.</span></span>

#### <span data-ttu-id="c2a27-182">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-182">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="c2a27-183">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-183">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="c2a27-184">общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="c2a27-184">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="c2a27-185">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-185">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="c2a27-186">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-186">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="c2a27-187">общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="c2a27-187">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="c2a27-188">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c2a27-188">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="c2a27-189">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-189">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="c2a27-190">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-190">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="c2a27-191">общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="c2a27-191">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="c2a27-192">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c2a27-192">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="c2a27-193">Свойство AreRemoteObjectsAllowed используется для управления доступом к удаленным объектам на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-193">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="c2a27-194">общедоступные значения HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(логический \* разрешено)</span><span class="sxs-lookup"><span data-stu-id="c2a27-194">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="c2a27-195">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c2a27-195">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="c2a27-196">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="c2a27-196">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="c2a27-197">Задайте свойство AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="c2a27-197">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="c2a27-198">общедоступная [PUT_AREREMOTEOBJECTSALLOWED](#put_areremoteobjectsallowed)HRESULT (допустимая bool)</span><span class="sxs-lookup"><span data-stu-id="c2a27-198">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="c2a27-199">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-199">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="c2a27-200">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="c2a27-200">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="c2a27-201">общедоступные значения HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="c2a27-201">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="c2a27-202">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c2a27-202">Defaults to TRUE.</span></span> <span data-ttu-id="c2a27-203">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать с помощью put_ZoomFactor API.</span><span class="sxs-lookup"><span data-stu-id="c2a27-203">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

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

#### <span data-ttu-id="c2a27-204">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="c2a27-204">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="c2a27-205">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="c2a27-205">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="c2a27-206">общедоступные значения HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="c2a27-206">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>


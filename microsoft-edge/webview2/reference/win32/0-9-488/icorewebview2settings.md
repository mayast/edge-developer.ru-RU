---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a996660bb667ca0e556326e0bf2b71c15b9344c2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880334"
---
# <span data-ttu-id="6c2c9-104">0.9.515-Interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="6c2c9-104">0.9.515 - interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="6c2c9-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6c2c9-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="6c2c9-107">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="6c2c9-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6c2c9-108">Summary</span></span>

 <span data-ttu-id="6c2c9-109">Участников</span><span class="sxs-lookup"><span data-stu-id="6c2c9-109">Members</span></span>                        | <span data-ttu-id="6c2c9-110">Описания</span><span class="sxs-lookup"><span data-stu-id="6c2c9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c2c9-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="6c2c9-112">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="6c2c9-113">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-113">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="6c2c9-114">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="6c2c9-115">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-115">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="6c2c9-116">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="6c2c9-117">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="6c2c9-117">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="6c2c9-118">Свойство AreRemoteObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-118">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="6c2c9-119">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-119">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="6c2c9-120">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="6c2c9-121">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-121">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="6c2c9-122">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="6c2c9-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="6c2c9-124">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="6c2c9-125">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-125">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="6c2c9-126">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="6c2c9-127">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-127">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="6c2c9-128">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="6c2c9-129">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-129">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="6c2c9-130">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-130">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="6c2c9-131">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-131">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="6c2c9-132">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-132">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="6c2c9-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="6c2c9-134">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-134">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="6c2c9-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="6c2c9-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="6c2c9-136">Задайте свойство AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="6c2c9-137">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-137">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="6c2c9-138">Задайте свойство IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-138">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="6c2c9-139">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-139">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="6c2c9-140">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-140">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="6c2c9-141">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-141">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="6c2c9-142">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-142">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="6c2c9-143">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-143">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="6c2c9-144">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-144">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="6c2c9-145">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-145">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="6c2c9-146">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-146">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="6c2c9-147">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-147">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="6c2c9-148">Участников</span><span class="sxs-lookup"><span data-stu-id="6c2c9-148">Members</span></span>

#### <span data-ttu-id="6c2c9-149">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-149">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="6c2c9-150">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-150">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="6c2c9-151">общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-151">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="6c2c9-152">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-152">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="6c2c9-153">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-153">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="6c2c9-154">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-154">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="6c2c9-155">общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-155">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="6c2c9-156">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="6c2c9-156">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="6c2c9-157">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-157">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="6c2c9-158">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-158">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="6c2c9-159">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-159">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="6c2c9-160">общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-160">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="6c2c9-161">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-161">It is true by default.</span></span>

#### <span data-ttu-id="6c2c9-162">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="6c2c9-162">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="6c2c9-163">Свойство AreRemoteObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-163">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="6c2c9-164">общедоступные значения HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(логический \* разрешено)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-164">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="6c2c9-165">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-165">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="6c2c9-166">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-166">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="6c2c9-167">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-167">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="6c2c9-168">общедоступные значения HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-168">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="6c2c9-169">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-169">Defaults to TRUE.</span></span> <span data-ttu-id="6c2c9-170">Если эта ошибка отключена, при возникновении связанной ошибки будет отображаться пустая страница.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-170">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="6c2c9-171">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-171">get_IsScriptEnabled</span></span> 

<span data-ttu-id="6c2c9-172">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-172">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="6c2c9-173">общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-173">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="6c2c9-174">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-174">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="6c2c9-175">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-175">It is true by default.</span></span>

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

#### <span data-ttu-id="6c2c9-176">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-176">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="6c2c9-177">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-177">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="6c2c9-178">общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-178">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="6c2c9-179">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-179">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="6c2c9-180">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-180">It is true by default.</span></span>

#### <span data-ttu-id="6c2c9-181">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-181">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="6c2c9-182">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-182">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="6c2c9-183">общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-183">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="6c2c9-184">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="6c2c9-184">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="6c2c9-185">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="6c2c9-185">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="6c2c9-186">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-186">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="6c2c9-187">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-187">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="6c2c9-188">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-188">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="6c2c9-189">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-189">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="6c2c9-190">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-190">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="6c2c9-191">общедоступные значения HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-191">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="6c2c9-192">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-192">Defaults to TRUE.</span></span> <span data-ttu-id="6c2c9-193">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать через API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-193">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="6c2c9-194">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-194">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="6c2c9-195">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-195">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="6c2c9-196">общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-196">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="6c2c9-197">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-197">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="6c2c9-198">Задайте свойство AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-198">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="6c2c9-199">общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-199">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="6c2c9-200">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-200">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="6c2c9-201">Задайте свойство AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-201">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="6c2c9-202">общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-202">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="6c2c9-203">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="6c2c9-203">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="6c2c9-204">Задайте свойство AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-204">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="6c2c9-205">общедоступная [PUT_AREREMOTEOBJECTSALLOWED](#put_areremoteobjectsallowed)HRESULT (допустимая bool)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-205">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="6c2c9-206">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-206">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="6c2c9-207">Задайте свойство IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-207">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="6c2c9-208">общедоступные значения HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-208">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="6c2c9-209">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-209">put_IsScriptEnabled</span></span> 

<span data-ttu-id="6c2c9-210">Задайте свойство IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-210">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="6c2c9-211">общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-211">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="6c2c9-212">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-212">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="6c2c9-213">Задайте свойство IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-213">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="6c2c9-214">общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-214">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="6c2c9-215">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-215">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="6c2c9-216">Задайте свойство IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-216">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="6c2c9-217">общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-217">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="6c2c9-218">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="6c2c9-218">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="6c2c9-219">Задайте свойство IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c2c9-219">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="6c2c9-220">общедоступные значения HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="6c2c9-220">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>


---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 6b512bcb5e8962b09d3a98c567465a488ef4038d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879676"
---
# <span data-ttu-id="f03c5-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="f03c5-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="f03c5-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f03c5-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f03c5-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f03c5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f03c5-107">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="f03c5-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f03c5-108">Summary</span></span>

 <span data-ttu-id="f03c5-109">Участников</span><span class="sxs-lookup"><span data-stu-id="f03c5-109">Members</span></span>                        | <span data-ttu-id="f03c5-110">Описания</span><span class="sxs-lookup"><span data-stu-id="f03c5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f03c5-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="f03c5-112">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="f03c5-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="f03c5-114">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="f03c5-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="f03c5-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="f03c5-116">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="f03c5-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="f03c5-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="f03c5-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="f03c5-118">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="f03c5-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="f03c5-120">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f03c5-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="f03c5-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="f03c5-122">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="f03c5-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="f03c5-124">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="f03c5-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="f03c5-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="f03c5-126">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="f03c5-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="f03c5-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="f03c5-128">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="f03c5-129">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f03c5-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="f03c5-130">Участников</span><span class="sxs-lookup"><span data-stu-id="f03c5-130">Members</span></span>

#### <span data-ttu-id="f03c5-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="f03c5-132">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="f03c5-133">Открытый логический [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="f03c5-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="f03c5-134">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="f03c5-134">Defaults to TRUE.</span></span>

#### <span data-ttu-id="f03c5-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="f03c5-136">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="f03c5-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="f03c5-137">Открытый логический [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="f03c5-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="f03c5-138">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="f03c5-138">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="f03c5-139">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f03c5-139">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="f03c5-140">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-140">AreDevToolsEnabled</span></span> 

<span data-ttu-id="f03c5-141">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="f03c5-141">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="f03c5-142">Открытый логический [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="f03c5-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="f03c5-143">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f03c5-143">It is true by default.</span></span>

#### <span data-ttu-id="f03c5-144">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="f03c5-144">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="f03c5-145">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-145">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="f03c5-146">Открытый логический [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="f03c5-146">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="f03c5-147">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="f03c5-147">Defaults to TRUE.</span></span>

#### <span data-ttu-id="f03c5-148">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-148">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="f03c5-149">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f03c5-149">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="f03c5-150">Открытый логический [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="f03c5-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="f03c5-151">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="f03c5-151">Defaults to TRUE.</span></span> <span data-ttu-id="f03c5-152">Если эта ошибка отключена, при возникновении связанной ошибки будет отображаться пустая страница.</span><span class="sxs-lookup"><span data-stu-id="f03c5-152">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="f03c5-153">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-153">IsScriptEnabled</span></span> 

<span data-ttu-id="f03c5-154">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-154">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="f03c5-155">Открытый логический [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="f03c5-155">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="f03c5-156">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="f03c5-156">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="f03c5-157">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f03c5-157">It is true by default.</span></span>

#### <span data-ttu-id="f03c5-158">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-158">IsStatusBarEnabled</span></span> 

<span data-ttu-id="f03c5-159">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="f03c5-159">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="f03c5-160">Открытый логический [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="f03c5-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="f03c5-161">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="f03c5-161">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="f03c5-162">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f03c5-162">It is true by default.</span></span>

#### <span data-ttu-id="f03c5-163">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-163">IsWebMessageEnabled</span></span> 

<span data-ttu-id="f03c5-164">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="f03c5-164">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="f03c5-165">Открытый логический [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="f03c5-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="f03c5-166">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="f03c5-166">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="f03c5-167">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="f03c5-167">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="f03c5-168">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="f03c5-168">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="f03c5-169">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="f03c5-169">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="f03c5-170">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f03c5-170">It is true by default.</span></span>

#### <span data-ttu-id="f03c5-171">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="f03c5-171">IsZoomControlEnabled</span></span> 

<span data-ttu-id="f03c5-172">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="f03c5-172">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="f03c5-173">Открытый логический [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="f03c5-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="f03c5-174">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="f03c5-174">Defaults to TRUE.</span></span> <span data-ttu-id="f03c5-175">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать через API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="f03c5-175">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>


---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 87b78956c29dac74bd023556a8c495222d248e9f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012439"
---
# <span data-ttu-id="d8ac7-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="d8ac7-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="d8ac7-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d8ac7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d8ac7-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d8ac7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d8ac7-107">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="d8ac7-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d8ac7-108">Summary</span></span>

 <span data-ttu-id="d8ac7-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d8ac7-109">Members</span></span>                        | <span data-ttu-id="d8ac7-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d8ac7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d8ac7-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="d8ac7-112">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>
[<span data-ttu-id="d8ac7-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="d8ac7-114">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="d8ac7-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="d8ac7-116">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="d8ac7-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="d8ac7-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="d8ac7-118">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>
[<span data-ttu-id="d8ac7-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="d8ac7-120">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="d8ac7-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="d8ac7-122">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="d8ac7-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="d8ac7-124">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="d8ac7-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="d8ac7-126">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="d8ac7-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="d8ac7-128">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="d8ac7-129">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="d8ac7-130">Участников</span><span class="sxs-lookup"><span data-stu-id="d8ac7-130">Members</span></span>

#### <span data-ttu-id="d8ac7-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="d8ac7-132">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>

> <span data-ttu-id="d8ac7-133">Открытый логический [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="d8ac7-134">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-134">It is true by default.</span></span>

#### <span data-ttu-id="d8ac7-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="d8ac7-136">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="d8ac7-137">Открытый логический [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="d8ac7-138">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="d8ac7-138">If set to false, then WebView won't render the default JavaScript dialog box (Specifically those shown by the JavaScript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="d8ac7-139">Если установлено значение true, то можно также подписаться на событие ScriptDialogOpening, которое будет содержать все сведения о диалоговом окне, и разрешить ведущему приложению показывать собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-139">If set to true, one can also subscribe to ScriptDialogOpening event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span> <span data-ttu-id="d8ac7-140">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-140">It is true by default.</span></span>

#### <span data-ttu-id="d8ac7-141">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-141">AreDevToolsEnabled</span></span> 

<span data-ttu-id="d8ac7-142">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-142">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="d8ac7-143">Открытый логический [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-143">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="d8ac7-144">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-144">It is true by default.</span></span>

#### <span data-ttu-id="d8ac7-145">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="d8ac7-145">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="d8ac7-146">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-146">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>

> <span data-ttu-id="d8ac7-147">Открытый логический [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-147">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="d8ac7-148">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-148">It is true by default.</span></span>

#### <span data-ttu-id="d8ac7-149">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-149">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="d8ac7-150">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-150">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="d8ac7-151">Открытый логический [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-151">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="d8ac7-152">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-152">It is true by default.</span></span> <span data-ttu-id="d8ac7-153">Если эта ошибка отключена, при возникновении связанной ошибки будет отображаться пустая страница.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-153">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="d8ac7-154">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-154">IsScriptEnabled</span></span> 

<span data-ttu-id="d8ac7-155">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-155">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="d8ac7-156">Открытый логический [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-156">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="d8ac7-157">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-157">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="d8ac7-158">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-158">It is true by default.</span></span>

#### <span data-ttu-id="d8ac7-159">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-159">IsStatusBarEnabled</span></span> 

<span data-ttu-id="d8ac7-160">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-160">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="d8ac7-161">Открытый логический [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-161">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="d8ac7-162">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-162">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="d8ac7-163">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-163">It is true by default.</span></span>

#### <span data-ttu-id="d8ac7-164">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-164">IsWebMessageEnabled</span></span> 

<span data-ttu-id="d8ac7-165">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-165">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="d8ac7-166">Открытый логический [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-166">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="d8ac7-167">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="d8ac7-167">If set to true, communication from the host to the WebView's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="d8ac7-168">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и события WebMessageReceived (Дополнительные сведения можно найти в WebMessageReceived документации).</span><span class="sxs-lookup"><span data-stu-id="d8ac7-168">Communication from the WebView's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the WebMessageReceived event (see WebMessageReceived documentation for details).</span></span> <span data-ttu-id="d8ac7-169">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-169">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="d8ac7-170">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-170">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="d8ac7-171">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-171">It is true by default.</span></span>

#### <span data-ttu-id="d8ac7-172">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ac7-172">IsZoomControlEnabled</span></span> 

<span data-ttu-id="d8ac7-173">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-173">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="d8ac7-174">Открытый логический [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="d8ac7-174">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="d8ac7-175">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-175">It is true by default.</span></span> <span data-ttu-id="d8ac7-176">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать через API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="d8ac7-176">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>


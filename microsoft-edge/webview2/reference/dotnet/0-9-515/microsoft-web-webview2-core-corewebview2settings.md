---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f0ac0bf7ae3b237bca45b22ed97ec16513666922
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697555"
---
# <span data-ttu-id="5f7b0-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="5f7b0-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

> [!NOTE]
> <span data-ttu-id="5f7b0-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="5f7b0-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="5f7b0-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="5f7b0-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="5f7b0-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="5f7b0-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="5f7b0-109">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-109">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="5f7b0-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5f7b0-110">Summary</span></span>

 <span data-ttu-id="5f7b0-111">Участников</span><span class="sxs-lookup"><span data-stu-id="5f7b0-111">Members</span></span>                        | <span data-ttu-id="5f7b0-112">Описания</span><span class="sxs-lookup"><span data-stu-id="5f7b0-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5f7b0-113">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-113">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="5f7b0-114">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-114">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="5f7b0-115">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-115">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="5f7b0-116">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-116">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="5f7b0-117">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-117">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="5f7b0-118">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-118">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="5f7b0-119">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="5f7b0-119">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="5f7b0-120">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-120">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="5f7b0-121">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-121">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="5f7b0-122">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-122">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="5f7b0-123">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-123">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="5f7b0-124">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-124">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="5f7b0-125">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-125">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="5f7b0-126">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="5f7b0-127">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-127">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="5f7b0-128">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-128">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="5f7b0-129">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-129">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="5f7b0-130">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-130">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="5f7b0-131">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-131">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="5f7b0-132">Участников</span><span class="sxs-lookup"><span data-stu-id="5f7b0-132">Members</span></span>

#### <span data-ttu-id="5f7b0-133">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-133">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="5f7b0-134">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-134">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="5f7b0-135">Открытый логический [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-135">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="5f7b0-136">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-136">Defaults to TRUE.</span></span>

#### <span data-ttu-id="5f7b0-137">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-137">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="5f7b0-138">AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-138">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="5f7b0-139">Открытый логический [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-139">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="5f7b0-140">Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload).</span><span class="sxs-lookup"><span data-stu-id="5f7b0-140">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="5f7b0-141">Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-141">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="5f7b0-142">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-142">AreDevToolsEnabled</span></span> 

<span data-ttu-id="5f7b0-143">AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-143">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="5f7b0-144">Открытый логический [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-144">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="5f7b0-145">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-145">It is true by default.</span></span>

#### <span data-ttu-id="5f7b0-146">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="5f7b0-146">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="5f7b0-147">Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-147">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="5f7b0-148">Открытый логический [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-148">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="5f7b0-149">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-149">Defaults to TRUE.</span></span>

#### <span data-ttu-id="5f7b0-150">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-150">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="5f7b0-151">Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-151">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="5f7b0-152">Открытый логический [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-152">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="5f7b0-153">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-153">Defaults to TRUE.</span></span> <span data-ttu-id="5f7b0-154">Если эта ошибка отключена, при возникновении связанной ошибки будет отображаться пустая страница.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-154">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="5f7b0-155">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-155">IsScriptEnabled</span></span> 

<span data-ttu-id="5f7b0-156">Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-156">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="5f7b0-157">Открытый логический [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-157">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="5f7b0-158">Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-158">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="5f7b0-159">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-159">It is true by default.</span></span>

#### <span data-ttu-id="5f7b0-160">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-160">IsStatusBarEnabled</span></span> 

<span data-ttu-id="5f7b0-161">IsStatusBarEnabled определяет, будет ли отображаться строка состояния.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-161">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="5f7b0-162">Открытый логический [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-162">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="5f7b0-163">Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-163">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="5f7b0-164">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-164">It is true by default.</span></span>

#### <span data-ttu-id="5f7b0-165">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-165">IsWebMessageEnabled</span></span> 

<span data-ttu-id="5f7b0-166">Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-166">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="5f7b0-167">Открытый логический [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-167">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="5f7b0-168">Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson).</span><span class="sxs-lookup"><span data-stu-id="5f7b0-168">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="5f7b0-169">Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler).</span><span class="sxs-lookup"><span data-stu-id="5f7b0-169">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="5f7b0-170">Если задано значение false, связь не разрешена.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-170">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="5f7b0-171">PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-171">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="5f7b0-172">Это значение верно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-172">It is true by default.</span></span>

#### <span data-ttu-id="5f7b0-173">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="5f7b0-173">IsZoomControlEnabled</span></span> 

<span data-ttu-id="5f7b0-174">Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-174">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="5f7b0-175">Открытый логический [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="5f7b0-175">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="5f7b0-176">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-176">Defaults to TRUE.</span></span> <span data-ttu-id="5f7b0-177">Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать через API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="5f7b0-177">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>


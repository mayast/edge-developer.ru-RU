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
# Класс Microsoft. Web. WebView2. Core. CoreWebView2Settings 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Определяет свойства, которые включают, отключают или изменяют функции WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled) | Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.
[AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.
[AreDevToolsEnabled](#aredevtoolsenabled) | AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.
[AreHostObjectsAllowed](#arehostobjectsallowed) | Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.
[IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled) | Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.
[IsScriptEnabled](#isscriptenabled) | Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.
[IsStatusBarEnabled](#isstatusbarenabled) | IsStatusBarEnabled определяет, будет ли отображаться строка состояния.
[IsWebMessageEnabled](#iswebmessageenabled) | Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.
[IsZoomControlEnabled](#iszoomcontrolenabled) | Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.

Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.

## Участников

#### AreDefaultContextMenusEnabled 

Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.

> Открытый логический [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)

По умолчанию используется значение TRUE.

#### AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.

> Открытый логический [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)

Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload). Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.

#### AreDevToolsEnabled 

AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.

> Открытый логический [AreDevToolsEnabled](#aredevtoolsenabled)

Это значение верно по умолчанию.

#### AreHostObjectsAllowed 

Свойство AreHostObjectsAllowed используется для управления тем, какие объекты узла доступны на странице в WebView.

> Открытый логический [AreHostObjectsAllowed](#arehostobjectsallowed)

По умолчанию используется значение TRUE.

#### IsBuiltInErrorPageEnabled 

Свойство IsBuiltInErrorPageEnabled используется для того, чтобы отключить встроенную страницу ошибки для сбоя навигации и обработки сбоя процесса рендеринга.

> Открытый логический [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)

По умолчанию используется значение TRUE. Если эта ошибка отключена, при возникновении связанной ошибки будет отображаться пустая страница.

#### IsScriptEnabled 

Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.

> Открытый логический [IsScriptEnabled](#isscriptenabled)

Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен. Это значение верно по умолчанию.

#### IsStatusBarEnabled 

IsStatusBarEnabled определяет, будет ли отображаться строка состояния.

> Открытый логический [IsStatusBarEnabled](#isstatusbarenabled)

Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения. Это значение верно по умолчанию.

#### IsWebMessageEnabled 

Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.

> Открытый логический [IsWebMessageEnabled](#iswebmessageenabled)

Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson). Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler). Если задано значение false, связь не разрешена. PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error. Это значение верно по умолчанию.

#### IsZoomControlEnabled 

Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.

> Открытый логический [IsZoomControlEnabled](#iszoomcontrolenabled)

По умолчанию используется значение TRUE. Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать через API ZoomFactor.


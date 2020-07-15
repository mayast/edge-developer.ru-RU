---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 94c6d6c424d715d3b6b57b366b71cf8e5fb8ec42
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878213"
---
# 0.8.355-Interface IWebView2Settings 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2Settings
  : public IUnknown
```

Определяет свойства, которые включают, отключают или изменяют функции WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_IsScriptEnabled](#get_isscriptenabled) | Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.
[put_IsScriptEnabled](#put_isscriptenabled) | Задайте свойство IsScriptEnabled.
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Задайте свойство IsWebMessageEnabled.
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Задайте свойство AreDefaultScriptDialogsEnabled.
[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated) | Этот параметр устарел и всегда будет возвращать значение false.
[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated) | Этот параметр устарел и не действует.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled определяет, будет ли отображаться строка состояния.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Задайте свойство IsStatusBarEnabled.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Задайте свойство AreDevToolsEnabled.

Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.

## Участников

#### get_IsScriptEnabled 

Определяет, включено ли выполнение JavaScript во всех последующих навигации в WebView.

> общедоступные значения HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool * IsScriptEnabled)

Это относится только к сценариям в документе; сценарии, добавленные с помощью ExecuteScript, будут выполняться даже в том случае, если сценарий отключен. Это значение верно по умолчанию.

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

#### put_IsScriptEnabled 

Задайте свойство IsScriptEnabled.

> общедоступные значения HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)

#### get_IsWebMessageEnabled 

Свойство IsWebMessageEnabled используется при загрузке нового HTML-документа.

> общедоступные значения HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool * IsWebMessageEnabled)

Если установлено значение true, связь между узлом и HTML-документом верхнего уровня WebView разрешается с помощью события Message PostWebMessageAsJson, PostWebMessageAsString и Window. Chrome. WebView (Дополнительные сведения можно найти в документации PostWebMessageAsJson). Связь между HTML-документом верхнего уровня WebView разрешается с помощью функции. Chrome. WebView и метода SetWebMessageReceivedEventHandler (подробности можно найти в документации SetWebMessageReceivedEventHandler). Если задано значение false, связь не разрешена. PostWebMessageAsJson и PostWebMessageAsString завершатся сбоем с E_ACCESSDENIED и Window. Chrome. WebView. i, вызывая экземпляр объекта Error. Это значение верно по умолчанию.

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### put_IsWebMessageEnabled 

Задайте свойство IsWebMessageEnabled.

> общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.

> общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool * AreDefaultScriptDialogsEnabled)

Если задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются в функциях оповещения JavaScript, подтверждения и запросов). Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.

#### put_AreDefaultScriptDialogsEnabled 

Задайте свойство AreDefaultScriptDialogsEnabled.

> общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)

#### get_IsFullscreenAllowed_deprecated 

Этот параметр устарел и всегда будет возвращать значение false.

> общедоступные значения HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool * IsFullscreenAllowed)

Это означает, что элементы в WebView будут заполнять только границы WebView. Это свойство будет удалено полностью. Вместо этого пожалуйста, прослушайте событие ContainsFullScreenElementChanged.

Определяет, разрешено ли полноэкранное воспроизведение элементов в WebView. Если это разрешено, веб-содержимое, например элемент видео в WebView, может быть отображено во весь экран. Если это значение не разрешено, этот элемент будет заполнять границы WebView, когда элемент запрашивает весь экран. Это значение верно по умолчанию.

#### put_IsFullscreenAllowed_deprecated 

Этот параметр устарел и не действует.

> общедоступные значения HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(bool IsFullscreenAllowed)

Вместо этого пожалуйста, прослушайте событие ContainsFullScreenElementChanged.

Задайте свойство IsFullscreenAllowed.

#### get_IsStatusBarEnabled 

IsStatusBarEnabled определяет, будет ли отображаться строка состояния.

> общедоступные значения HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool * IsStatusBarEnabled)

Строка состояния обычно отображается в левом левом углу WebView и отображает такие элементы, как URI ссылки, когда пользователь наводит на него указатель мыши и другие сведения. Это значение верно по умолчанию.

#### put_IsStatusBarEnabled 

Задайте свойство IsStatusBarEnabled.

> общедоступные значения HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)

#### get_AreDevToolsEnabled 

AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.

> общедоступные значения HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool * AreDevToolsEnabled)

Это значение верно по умолчанию.

#### put_AreDevToolsEnabled 

Задайте свойство AreDevToolsEnabled.

> общедоступные значения HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)


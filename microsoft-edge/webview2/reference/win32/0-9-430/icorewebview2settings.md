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
# 0.9.430-Interface ICoreWebView2Settings 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2Settings
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
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled определяет, будет ли отображаться строка состояния.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Задайте свойство IsStatusBarEnabled.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled определяет, может ли пользователь использовать контекстное меню или сочетания клавиш для открытия окна DevTools.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Задайте свойство AreDevToolsEnabled.
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Задайте свойство AreDefaultContextMenusEnabled.
[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed) | Свойство AreRemoteObjectsAllowed используется для управления доступом к удаленным объектам на странице в WebView.
[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed) | Задайте свойство AreRemoteObjectsAllowed.
[get_IsZoomControlEnabled](#get_iszoomcontrolenabled) | Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.
[put_IsZoomControlEnabled](#put_iszoomcontrolenabled) | Задайте свойство IsZoomControlEnabled.

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
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### put_IsWebMessageEnabled 

Задайте свойство IsWebMessageEnabled.

> общедоступные значения HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled используется при загрузке нового документа HTML.

> общедоступные значения HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool * AreDefaultScriptDialogsEnabled)

Если для этого свойства задано значение false, WebView не будет отображать диалоговое окно JavaScript по умолчанию (в том числе те, которые отображаются предупреждением JavaScript, Confirm, функции Prompt и событие beforeunload). Вместо этого, если обработчик событий установлен с помощью SetScriptDialogOpeningEventHandler, WebView отправляет событие, которое будет содержать все сведения о диалоговом окне, и позволяет ведущему приложению отобразить собственный пользовательский интерфейс.

#### put_AreDefaultScriptDialogsEnabled 

Задайте свойство AreDefaultScriptDialogsEnabled.

> общедоступные значения HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)

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

#### get_AreDefaultContextMenusEnabled 

Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.

> общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический * включен)

По умолчанию используется значение TRUE.

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

#### put_AreDefaultContextMenusEnabled 

Задайте свойство AreDefaultContextMenusEnabled.

> общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)

#### get_AreRemoteObjectsAllowed 

Свойство AreRemoteObjectsAllowed используется для управления доступом к удаленным объектам на странице в WebView.

> общедоступные значения HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(логический * разрешено)

По умолчанию используется значение TRUE.

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

#### put_AreRemoteObjectsAllowed 

Задайте свойство AreRemoteObjectsAllowed.

> общедоступная [PUT_AREREMOTEOBJECTSALLOWED](#put_areremoteobjectsallowed)HRESULT (допустимая bool)

#### get_IsZoomControlEnabled 

Свойство IsZoomControlEnabled используется, чтобы не допустить воздействия пользователя на масштаб WebView.

> общедоступные значения HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(логический * включен)

По умолчанию используется значение TRUE. Если эта функция отключена, пользователь не сможет изменять масштаб с помощью клавиш CTRL +/-или CTRL + колесика мыши, но масштаб можно задать с помощью put_ZoomFactor API.

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

#### put_IsZoomControlEnabled 

Задайте свойство IsZoomControlEnabled.

> общедоступные значения HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(логический параметр включен)


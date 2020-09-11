---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalEnvironmentOptions
ms.openlocfilehash: ba91056fa6d2e6cf9e7da18202fb3c74d7deb827
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010245"
---
# 0.9.579-Interface ICoreWebView2ExperimentalEnvironmentOptions 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

Экспериментальные параметры, которые используются для создания среды WebView2.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled) | Свойство IsSingleSignOnUsingOSPrimaryAccountEnabled используется для включения единого входа с помощью ресурсов Azure Active Directory (AAD) в WebView с помощью учетной записи Windows и единого входа с веб-сайтов с помощью учетной записи Майкрософт, связанной с входом в учетную запись Windows.
[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled) | Задайте свойство IsSingleSignOnUsingOSPrimaryAccountEnabled.

Реализация по умолчанию предоставляется в WebView2ExperimentalEnvironmentOptions. h.

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2ExperimentalEnvironmentOptions>();
    CHECK_FAILURE(options->put_IsSingleSignOnUsingOSPrimaryAccountEnabled(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## Участников

#### get_IsSingleSignOnUsingOSPrimaryAccountEnabled 

Свойство IsSingleSignOnUsingOSPrimaryAccountEnabled используется для включения единого входа с помощью ресурсов Azure Active Directory (AAD) в WebView с помощью учетной записи Windows и единого входа с веб-сайтов с помощью учетной записи Майкрософт, связанной с входом в учетную запись Windows.

> общедоступные значения HRESULT [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(логический * включен)

По умолчанию отключено. Приложения универсальной платформы Windows также должны объявлять enterpriseCloudSSO [ограниченную возможность](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) для работы единого входа.

#### put_IsSingleSignOnUsingOSPrimaryAccountEnabled 

Задайте свойство IsSingleSignOnUsingOSPrimaryAccountEnabled.

> общедоступные значения HRESULT [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(логический параметр включен)


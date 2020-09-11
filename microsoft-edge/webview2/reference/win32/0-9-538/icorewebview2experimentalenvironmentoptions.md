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
# <span data-ttu-id="dde8a-104">0.9.579-Interface ICoreWebView2ExperimentalEnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="dde8a-104">0.9.579 - interface ICoreWebView2ExperimentalEnvironmentOptions</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="dde8a-105">Экспериментальные параметры, которые используются для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="dde8a-105">Experimental options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="dde8a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="dde8a-106">Summary</span></span>

 <span data-ttu-id="dde8a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="dde8a-107">Members</span></span>                        | <span data-ttu-id="dde8a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="dde8a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dde8a-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="dde8a-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#get_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="dde8a-110">Свойство IsSingleSignOnUsingOSPrimaryAccountEnabled используется для включения единого входа с помощью ресурсов Azure Active Directory (AAD) в WebView с помощью учетной записи Windows и единого входа с веб-сайтов с помощью учетной записи Майкрософт, связанной с входом в учетную запись Windows.</span><span class="sxs-lookup"><span data-stu-id="dde8a-110">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="dde8a-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="dde8a-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#put_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="dde8a-112">Задайте свойство IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="dde8a-112">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

<span data-ttu-id="dde8a-113">Реализация по умолчанию предоставляется в WebView2ExperimentalEnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="dde8a-113">A default implementation is provided in WebView2ExperimentalEnvironmentOptions.h.</span></span>

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

## <span data-ttu-id="dde8a-114">Участников</span><span class="sxs-lookup"><span data-stu-id="dde8a-114">Members</span></span>

#### <span data-ttu-id="dde8a-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="dde8a-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="dde8a-116">Свойство IsSingleSignOnUsingOSPrimaryAccountEnabled используется для включения единого входа с помощью ресурсов Azure Active Directory (AAD) в WebView с помощью учетной записи Windows и единого входа с веб-сайтов с помощью учетной записи Майкрософт, связанной с входом в учетную запись Windows.</span><span class="sxs-lookup"><span data-stu-id="dde8a-116">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="dde8a-117">общедоступные значения HRESULT [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="dde8a-117">public HRESULT [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="dde8a-118">По умолчанию отключено.</span><span class="sxs-lookup"><span data-stu-id="dde8a-118">Default is disabled.</span></span> <span data-ttu-id="dde8a-119">Приложения универсальной платформы Windows также должны объявлять enterpriseCloudSSO [ограниченную возможность](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) для работы единого входа.</span><span class="sxs-lookup"><span data-stu-id="dde8a-119">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="dde8a-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="dde8a-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="dde8a-121">Задайте свойство IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="dde8a-121">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

> <span data-ttu-id="dde8a-122">общедоступные значения HRESULT [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="dde8a-122">public HRESULT [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(BOOL enabled)</span></span>


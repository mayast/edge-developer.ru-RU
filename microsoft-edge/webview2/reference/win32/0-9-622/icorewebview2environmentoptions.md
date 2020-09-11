---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2EnvironmentOptions
ms.openlocfilehash: a4e51dc08e2c31664cb77e4e6ee0136bab2f261d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012565"
---
# <span data-ttu-id="97e6d-104">интерфейс ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="97e6d-104">interface ICoreWebView2EnvironmentOptions</span></span> 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="97e6d-105">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="97e6d-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="97e6d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="97e6d-106">Summary</span></span>

 <span data-ttu-id="97e6d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="97e6d-107">Members</span></span>                        | <span data-ttu-id="97e6d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="97e6d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97e6d-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="97e6d-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="97e6d-110">AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.</span><span class="sxs-lookup"><span data-stu-id="97e6d-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="97e6d-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="97e6d-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#get_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="97e6d-112">Свойство AllowSingleSignOnUsingOSPrimaryAccount используется для включения единого входа с помощью ресурсов Azure Active Directory (AAD) в WebView с помощью учетной записи Windows и единого входа с веб-сайтов с помощью учетной записи Майкрософт, связанной с входом в учетную запись Windows.</span><span class="sxs-lookup"><span data-stu-id="97e6d-112">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="97e6d-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="97e6d-113">get_Language</span></span>](#get_language) | <span data-ttu-id="97e6d-114">Язык по умолчанию, с которым будет выполняться WebView.</span><span class="sxs-lookup"><span data-stu-id="97e6d-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="97e6d-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="97e6d-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="97e6d-116">Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="97e6d-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="97e6d-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="97e6d-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="97e6d-118">Задайте свойство AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="97e6d-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="97e6d-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="97e6d-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#put_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="97e6d-120">Задайте свойство AllowSingleSignOnUsingOSPrimaryAccount.</span><span class="sxs-lookup"><span data-stu-id="97e6d-120">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>
[<span data-ttu-id="97e6d-121">put_Language</span><span class="sxs-lookup"><span data-stu-id="97e6d-121">put_Language</span></span>](#put_language) | <span data-ttu-id="97e6d-122">Задайте свойство Language.</span><span class="sxs-lookup"><span data-stu-id="97e6d-122">Set the Language property.</span></span>
[<span data-ttu-id="97e6d-123">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="97e6d-123">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="97e6d-124">Задайте свойство TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="97e6d-124">Set the TargetCompatibleBrowserVersion property.</span></span>

<span data-ttu-id="97e6d-125">Реализация по умолчанию предоставляется в WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="97e6d-125">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    CHECK_FAILURE(options->put_AllowSingleSignOnUsingOSPrimaryAccount(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="97e6d-126">Участников</span><span class="sxs-lookup"><span data-stu-id="97e6d-126">Members</span></span>

#### <span data-ttu-id="97e6d-127">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="97e6d-127">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="97e6d-128">AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.</span><span class="sxs-lookup"><span data-stu-id="97e6d-128">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="97e6d-129">общедоступные значения HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="97e6d-129">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="97e6d-130">Они будут переданы в процесс браузера как часть командной строки.</span><span class="sxs-lookup"><span data-stu-id="97e6d-130">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="97e6d-131">Дополнительные сведения о параметрах командной строки для процесса браузера можно найти [в разделе Run Chromium with flags](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="97e6d-131">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="97e6d-132">Если приложение запускается с переключателем командной строки, `--edge-webview-switches=xxx` значение этого переключателя (XXX в приведенном выше примере) также будет добавлено в командную строку процесса браузера.</span><span class="sxs-lookup"><span data-stu-id="97e6d-132">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="97e6d-133">Некоторые переключатели `--user-data-dir` , такие как внутренние и важные для WebView.</span><span class="sxs-lookup"><span data-stu-id="97e6d-133">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="97e6d-134">Эти переключатели будут игнорироваться, даже если они указаны.</span><span class="sxs-lookup"><span data-stu-id="97e6d-134">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="97e6d-135">Если один и тот же параметр указан несколько раз, последний — один.</span><span class="sxs-lookup"><span data-stu-id="97e6d-135">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="97e6d-136">Вы не пытаетесь объединять различные значения одного переключателя, кроме отключенных и включенных функций.</span><span class="sxs-lookup"><span data-stu-id="97e6d-136">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="97e6d-137">Функции, указанные в параметре `--enable-features` и `--disable-features` объединяемые с простой логикой: функции будут объединены с указанными функциями и встроенными функциями, а если функция отключена, она будет удалена из списка включенные компоненты.</span><span class="sxs-lookup"><span data-stu-id="97e6d-137">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="97e6d-138">Значения командной строки процесса приложения `--edge-webview-switches` обрабатываются после обработки параметра additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="97e6d-138">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="97e6d-139">Некоторые функции отключены для внутреннего использования и не могут быть включены.</span><span class="sxs-lookup"><span data-stu-id="97e6d-139">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="97e6d-140">Если синтаксический анализ для указанных переключателей не удался, они будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="97e6d-140">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="97e6d-141">По умолчанию выполняется процесс браузера без дополнительных флагов.</span><span class="sxs-lookup"><span data-stu-id="97e6d-141">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="97e6d-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="97e6d-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="97e6d-143">Свойство AllowSingleSignOnUsingOSPrimaryAccount используется для включения единого входа с помощью ресурсов Azure Active Directory (AAD) в WebView с помощью учетной записи Windows и единого входа с веб-сайтов с помощью учетной записи Майкрософт, связанной с входом в учетную запись Windows.</span><span class="sxs-lookup"><span data-stu-id="97e6d-143">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="97e6d-144">общедоступные значения HRESULT [get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)(bool \* Allow)</span><span class="sxs-lookup"><span data-stu-id="97e6d-144">public HRESULT [get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)(BOOL \* allow)</span></span>

<span data-ttu-id="97e6d-145">По умолчанию отключено.</span><span class="sxs-lookup"><span data-stu-id="97e6d-145">Default is disabled.</span></span> <span data-ttu-id="97e6d-146">Приложения универсальной платформы Windows также должны объявлять enterpriseCloudSSO [ограниченную возможность](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) для работы единого входа.</span><span class="sxs-lookup"><span data-stu-id="97e6d-146">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="97e6d-147">get_Language</span><span class="sxs-lookup"><span data-stu-id="97e6d-147">get_Language</span></span> 

<span data-ttu-id="97e6d-148">Язык по умолчанию, с которым будет выполняться WebView.</span><span class="sxs-lookup"><span data-stu-id="97e6d-148">The default language that WebView will run with.</span></span>

> <span data-ttu-id="97e6d-149">общедоступные значения HRESULT [get_Language](#get_language)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="97e6d-149">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="97e6d-150">Это относится к UI браузера, таким как контекстное меню и диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="97e6d-150">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="97e6d-151">Она также применяется к HTTP-заголовку "принимаемые языки", WebView отправляется на веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="97e6d-151">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="97e6d-152">Оно представлено в формате, `language[-country]` который `language` является буквенным кодом из ISO 639 и `country` является буквенным кодом из ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="97e6d-152">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="97e6d-153">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="97e6d-153">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="97e6d-154">Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="97e6d-154">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="97e6d-155">общедоступные значения HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="97e6d-155">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="97e6d-156">Это значение по умолчанию соответствует версии среды выполнения Edge WebView2, соответствующей версии SDK, используемой приложением.</span><span class="sxs-lookup"><span data-stu-id="97e6d-156">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="97e6d-157">Формат этого значения совпадает с форматом свойства BrowserVersionString и другими BrowserVersion значениями.</span><span class="sxs-lookup"><span data-stu-id="97e6d-157">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="97e6d-158">Учитывается только часть версии значения BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="97e6d-158">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="97e6d-159">Суффикс канала, если он существует, пропускается.</span><span class="sxs-lookup"><span data-stu-id="97e6d-159">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="97e6d-160">Используемая версия двоичных файлов среды выполнения WebView2 может отличаться от указанной TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="97e6d-160">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="97e6d-161">Они гарантированно совместимы.</span><span class="sxs-lookup"><span data-stu-id="97e6d-161">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="97e6d-162">Вы можете проверить фактическую версию в свойстве BrowserVersionString на ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="97e6d-162">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="97e6d-163">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="97e6d-163">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="97e6d-164">Задайте свойство AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="97e6d-164">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="97e6d-165">общедоступные значения HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="97e6d-165">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="97e6d-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="97e6d-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="97e6d-167">Задайте свойство AllowSingleSignOnUsingOSPrimaryAccount.</span><span class="sxs-lookup"><span data-stu-id="97e6d-167">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>

> <span data-ttu-id="97e6d-168">общедоступные значения HRESULT [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(разрешено логическое)</span><span class="sxs-lookup"><span data-stu-id="97e6d-168">public HRESULT [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(BOOL allow)</span></span>

#### <span data-ttu-id="97e6d-169">put_Language</span><span class="sxs-lookup"><span data-stu-id="97e6d-169">put_Language</span></span> 

<span data-ttu-id="97e6d-170">Задайте свойство Language.</span><span class="sxs-lookup"><span data-stu-id="97e6d-170">Set the Language property.</span></span>

> <span data-ttu-id="97e6d-171">общедоступные значения HRESULT [put_Language](#put_language)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="97e6d-171">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="97e6d-172">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="97e6d-172">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="97e6d-173">Задайте свойство TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="97e6d-173">Set the TargetCompatibleBrowserVersion property.</span></span>

> <span data-ttu-id="97e6d-174">общедоступные значения HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="97e6d-174">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1cac030b27164222bd1c11240cf4a92aee91ff01
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880677"
---
# <span data-ttu-id="94263-104">0.9.515-Interface ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="94263-104">0.9.515 - interface ICoreWebView2EnvironmentOptions</span></span> 

> [!NOTE]
> <span data-ttu-id="94263-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="94263-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="94263-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="94263-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="94263-107">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="94263-107">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="94263-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="94263-108">Summary</span></span>

 <span data-ttu-id="94263-109">Участников</span><span class="sxs-lookup"><span data-stu-id="94263-109">Members</span></span>                        | <span data-ttu-id="94263-110">Описания</span><span class="sxs-lookup"><span data-stu-id="94263-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="94263-111">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="94263-111">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="94263-112">AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.</span><span class="sxs-lookup"><span data-stu-id="94263-112">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="94263-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="94263-113">get_Language</span></span>](#get_language) | <span data-ttu-id="94263-114">Язык по умолчанию, с которым будет выполняться WebView.</span><span class="sxs-lookup"><span data-stu-id="94263-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="94263-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="94263-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="94263-116">Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="94263-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="94263-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="94263-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="94263-118">Задайте свойство AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="94263-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="94263-119">put_Language</span><span class="sxs-lookup"><span data-stu-id="94263-119">put_Language</span></span>](#put_language) | <span data-ttu-id="94263-120">Задайте свойство Language.</span><span class="sxs-lookup"><span data-stu-id="94263-120">Set the Language property.</span></span>
[<span data-ttu-id="94263-121">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="94263-121">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="94263-122">Установите TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="94263-122">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="94263-123">Реализация по умолчанию предоставляется в WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="94263-123">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="94263-124">Участников</span><span class="sxs-lookup"><span data-stu-id="94263-124">Members</span></span>

#### <span data-ttu-id="94263-125">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="94263-125">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="94263-126">AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.</span><span class="sxs-lookup"><span data-stu-id="94263-126">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="94263-127">общедоступные значения HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="94263-127">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="94263-128">Они будут переданы в процесс браузера как часть командной строки.</span><span class="sxs-lookup"><span data-stu-id="94263-128">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="94263-129">Дополнительные сведения о параметрах командной строки для процесса браузера можно найти [в разделе Run Chromium with flags](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="94263-129">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="94263-130">Если приложение запускается с переключателем командной строки, `--edge-webview-switches=xxx` значение этого переключателя (XXX в приведенном выше примере) также будет добавлено в командную строку процесса браузера.</span><span class="sxs-lookup"><span data-stu-id="94263-130">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="94263-131">Некоторые переключатели `--user-data-dir` , такие как внутренние и важные для WebView.</span><span class="sxs-lookup"><span data-stu-id="94263-131">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="94263-132">Эти переключатели будут игнорироваться, даже если они указаны.</span><span class="sxs-lookup"><span data-stu-id="94263-132">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="94263-133">Если один и тот же параметр указан несколько раз, последний — один.</span><span class="sxs-lookup"><span data-stu-id="94263-133">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="94263-134">Вы не пытаетесь объединять различные значения одного переключателя, кроме отключенных и включенных функций.</span><span class="sxs-lookup"><span data-stu-id="94263-134">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="94263-135">Функции, указанные в параметре `--enable-features` и `--disable-features` объединяемые с простой логикой: функции будут объединены с указанными функциями и встроенными функциями, а если функция отключена, она будет удалена из списка включенные компоненты.</span><span class="sxs-lookup"><span data-stu-id="94263-135">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="94263-136">Значения командной строки процесса приложения `--edge-webview-switches` обрабатываются после обработки параметра additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="94263-136">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="94263-137">Некоторые функции отключены для внутреннего использования и не могут быть включены.</span><span class="sxs-lookup"><span data-stu-id="94263-137">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="94263-138">Если синтаксический анализ для указанных переключателей не удался, они будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="94263-138">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="94263-139">По умолчанию выполняется процесс браузера без дополнительных флагов.</span><span class="sxs-lookup"><span data-stu-id="94263-139">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="94263-140">get_Language</span><span class="sxs-lookup"><span data-stu-id="94263-140">get_Language</span></span> 

<span data-ttu-id="94263-141">Язык по умолчанию, с которым будет выполняться WebView.</span><span class="sxs-lookup"><span data-stu-id="94263-141">The default language that WebView will run with.</span></span>

> <span data-ttu-id="94263-142">общедоступные значения HRESULT [get_Language](#get_language)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="94263-142">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="94263-143">Это относится к UI браузера, таким как контекстное меню и диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="94263-143">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="94263-144">Она также применяется к HTTP-заголовку "принимаемые языки", WebView отправляется на веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="94263-144">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="94263-145">Оно представлено в формате, `language[-country]` который `language` является буквенным кодом из ISO 639 и `country` является буквенным кодом из ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="94263-145">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="94263-146">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="94263-146">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="94263-147">Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="94263-147">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="94263-148">общедоступные значения HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="94263-148">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="94263-149">Это значение по умолчанию соответствует версии среды выполнения Edge WebView2, соответствующей версии SDK, используемой приложением.</span><span class="sxs-lookup"><span data-stu-id="94263-149">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="94263-150">Формат этого значения совпадает с форматом свойства BrowserVersionString и другими BrowserVersion значениями.</span><span class="sxs-lookup"><span data-stu-id="94263-150">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="94263-151">Учитывается только часть версии значения BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="94263-151">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="94263-152">Суффикс канала, если он существует, пропускается.</span><span class="sxs-lookup"><span data-stu-id="94263-152">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="94263-153">Используемая версия двоичных файлов среды выполнения WebView2 может отличаться от указанной TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="94263-153">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="94263-154">Они гарантированно совместимы.</span><span class="sxs-lookup"><span data-stu-id="94263-154">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="94263-155">Вы можете проверить фактическую версию в свойстве BrowserVersionString на ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="94263-155">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="94263-156">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="94263-156">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="94263-157">Задайте свойство AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="94263-157">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="94263-158">общедоступные значения HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="94263-158">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="94263-159">put_Language</span><span class="sxs-lookup"><span data-stu-id="94263-159">put_Language</span></span> 

<span data-ttu-id="94263-160">Задайте свойство Language.</span><span class="sxs-lookup"><span data-stu-id="94263-160">Set the Language property.</span></span>

> <span data-ttu-id="94263-161">общедоступные значения HRESULT [put_Language](#put_language)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="94263-161">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="94263-162">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="94263-162">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="94263-163">Установите TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="94263-163">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="94263-164">общедоступные значения HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="94263-164">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>


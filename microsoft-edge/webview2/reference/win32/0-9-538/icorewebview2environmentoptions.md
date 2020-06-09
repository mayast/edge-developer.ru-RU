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
ms.openlocfilehash: 3de9cd454f693179a0d1dc63e6ccb1332f80c875
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699175"
---
# <span data-ttu-id="9e775-104">интерфейс ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="9e775-104">interface ICoreWebView2EnvironmentOptions</span></span> 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="9e775-105">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="9e775-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="9e775-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9e775-106">Summary</span></span>

 <span data-ttu-id="9e775-107">Участников</span><span class="sxs-lookup"><span data-stu-id="9e775-107">Members</span></span>                        | <span data-ttu-id="9e775-108">Описания</span><span class="sxs-lookup"><span data-stu-id="9e775-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e775-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="9e775-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="9e775-110">AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.</span><span class="sxs-lookup"><span data-stu-id="9e775-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="9e775-111">get_Language</span><span class="sxs-lookup"><span data-stu-id="9e775-111">get_Language</span></span>](#get_language) | <span data-ttu-id="9e775-112">Язык по умолчанию, с которым будет выполняться WebView.</span><span class="sxs-lookup"><span data-stu-id="9e775-112">The default language that WebView will run with.</span></span>
[<span data-ttu-id="9e775-113">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="9e775-113">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="9e775-114">Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="9e775-114">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="9e775-115">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="9e775-115">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="9e775-116">Задайте свойство AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="9e775-116">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="9e775-117">put_Language</span><span class="sxs-lookup"><span data-stu-id="9e775-117">put_Language</span></span>](#put_language) | <span data-ttu-id="9e775-118">Задайте свойство Language.</span><span class="sxs-lookup"><span data-stu-id="9e775-118">Set the Language property.</span></span>
[<span data-ttu-id="9e775-119">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="9e775-119">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="9e775-120">Установите TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="9e775-120">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="9e775-121">Реализация по умолчанию предоставляется в WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="9e775-121">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

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

## <span data-ttu-id="9e775-122">Участников</span><span class="sxs-lookup"><span data-stu-id="9e775-122">Members</span></span>

#### <span data-ttu-id="9e775-123">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="9e775-123">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="9e775-124">AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.</span><span class="sxs-lookup"><span data-stu-id="9e775-124">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="9e775-125">общедоступные значения HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="9e775-125">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="9e775-126">Они будут переданы в процесс браузера как часть командной строки.</span><span class="sxs-lookup"><span data-stu-id="9e775-126">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="9e775-127">Дополнительные сведения о параметрах командной строки для процесса браузера можно найти [в разделе Run Chromium with flags](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="9e775-127">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="9e775-128">Если приложение запускается с переключателем командной строки, `--edge-webview-switches=xxx` значение этого переключателя (XXX в приведенном выше примере) также будет добавлено в командную строку процесса браузера.</span><span class="sxs-lookup"><span data-stu-id="9e775-128">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="9e775-129">Некоторые переключатели `--user-data-dir` , такие как внутренние и важные для WebView.</span><span class="sxs-lookup"><span data-stu-id="9e775-129">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="9e775-130">Эти переключатели будут игнорироваться, даже если они указаны.</span><span class="sxs-lookup"><span data-stu-id="9e775-130">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="9e775-131">Если один и тот же параметр указан несколько раз, последний — один.</span><span class="sxs-lookup"><span data-stu-id="9e775-131">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="9e775-132">Вы не пытаетесь объединять различные значения одного переключателя, кроме отключенных и включенных функций.</span><span class="sxs-lookup"><span data-stu-id="9e775-132">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="9e775-133">Функции, указанные в параметре `--enable-features` и `--disable-features` объединяемые с простой логикой: функции будут объединены с указанными функциями и встроенными функциями, а если функция отключена, она будет удалена из списка включенные компоненты.</span><span class="sxs-lookup"><span data-stu-id="9e775-133">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="9e775-134">Значения командной строки процесса приложения `--edge-webview-switches` обрабатываются после обработки параметра additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="9e775-134">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="9e775-135">Некоторые функции отключены для внутреннего использования и не могут быть включены.</span><span class="sxs-lookup"><span data-stu-id="9e775-135">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="9e775-136">Если синтаксический анализ для указанных переключателей не удался, они будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="9e775-136">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="9e775-137">По умолчанию выполняется процесс браузера без дополнительных флагов.</span><span class="sxs-lookup"><span data-stu-id="9e775-137">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="9e775-138">get_Language</span><span class="sxs-lookup"><span data-stu-id="9e775-138">get_Language</span></span> 

<span data-ttu-id="9e775-139">Язык по умолчанию, с которым будет выполняться WebView.</span><span class="sxs-lookup"><span data-stu-id="9e775-139">The default language that WebView will run with.</span></span>

> <span data-ttu-id="9e775-140">общедоступные значения HRESULT [get_Language](#get_language)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="9e775-140">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="9e775-141">Это относится к UI браузера, таким как контекстное меню и диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="9e775-141">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="9e775-142">Она также применяется к HTTP-заголовку "принимаемые языки", WebView отправляется на веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="9e775-142">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="9e775-143">Оно представлено в формате, `language[-country]` который `language` является буквенным кодом из ISO 639 и `country` является буквенным кодом из ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="9e775-143">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="9e775-144">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="9e775-144">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="9e775-145">Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="9e775-145">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="9e775-146">общедоступные значения HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="9e775-146">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="9e775-147">Это значение по умолчанию соответствует версии среды выполнения Edge WebView2, соответствующей версии SDK, используемой приложением.</span><span class="sxs-lookup"><span data-stu-id="9e775-147">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="9e775-148">Формат этого значения совпадает с форматом свойства BrowserVersionString и другими BrowserVersion значениями.</span><span class="sxs-lookup"><span data-stu-id="9e775-148">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="9e775-149">Учитывается только часть версии значения BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="9e775-149">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="9e775-150">Суффикс канала, если он существует, пропускается.</span><span class="sxs-lookup"><span data-stu-id="9e775-150">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="9e775-151">Используемая версия двоичных файлов среды выполнения WebView2 может отличаться от указанной TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="9e775-151">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="9e775-152">Они гарантированно совместимы.</span><span class="sxs-lookup"><span data-stu-id="9e775-152">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="9e775-153">Вы можете проверить фактическую версию в свойстве BrowserVersionString на ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="9e775-153">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="9e775-154">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="9e775-154">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="9e775-155">Задайте свойство AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="9e775-155">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="9e775-156">общедоступные значения HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="9e775-156">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="9e775-157">put_Language</span><span class="sxs-lookup"><span data-stu-id="9e775-157">put_Language</span></span> 

<span data-ttu-id="9e775-158">Задайте свойство Language.</span><span class="sxs-lookup"><span data-stu-id="9e775-158">Set the Language property.</span></span>

> <span data-ttu-id="9e775-159">общедоступные значения HRESULT [put_Language](#put_language)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="9e775-159">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="9e775-160">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="9e775-160">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="9e775-161">Установите TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="9e775-161">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="9e775-162">общедоступные значения HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="9e775-162">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>


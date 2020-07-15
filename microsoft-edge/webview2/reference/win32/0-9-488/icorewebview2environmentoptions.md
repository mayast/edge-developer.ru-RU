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
# 0.9.515-Interface ICoreWebView2EnvironmentOptions 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

Параметры, используемые для создания среды WebView2.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_AdditionalBrowserArguments](#get_additionalbrowserarguments) | AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.
[get_Language](#get_language) | Язык по умолчанию, с которым будет выполняться WebView.
[get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion) | Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.
[put_AdditionalBrowserArguments](#put_additionalbrowserarguments) | Задайте свойство AdditionalBrowserArguments.
[put_Language](#put_language) | Задайте свойство Language.
[put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion) | Установите TargetCompatibleBrowserVersion.

Реализация по умолчанию предоставляется в WebView2EnvironmentOptions. h.

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

## Участников

#### get_AdditionalBrowserArguments 

AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.

> общедоступные значения HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR * Value)

Они будут переданы в процесс браузера как часть командной строки. Дополнительные сведения о параметрах командной строки для процесса браузера можно найти [в разделе Run Chromium with flags](https://aka.ms/RunChromiumWithFlags) . Если приложение запускается с переключателем командной строки, `--edge-webview-switches=xxx` значение этого переключателя (XXX в приведенном выше примере) также будет добавлено в командную строку процесса браузера. Некоторые переключатели `--user-data-dir` , такие как внутренние и важные для WebView. Эти переключатели будут игнорироваться, даже если они указаны. Если один и тот же параметр указан несколько раз, последний — один. Вы не пытаетесь объединять различные значения одного переключателя, кроме отключенных и включенных функций. Функции, указанные в параметре `--enable-features` и `--disable-features` объединяемые с простой логикой: функции будут объединены с указанными функциями и встроенными функциями, а если функция отключена, она будет удалена из списка включенные компоненты. Значения командной строки процесса приложения `--edge-webview-switches` обрабатываются после обработки параметра additionalBrowserArguments. Некоторые функции отключены для внутреннего использования и не могут быть включены. Если синтаксический анализ для указанных переключателей не удался, они будут пропущены. По умолчанию выполняется процесс браузера без дополнительных флагов.

#### get_Language 

Язык по умолчанию, с которым будет выполняться WebView.

> общедоступные значения HRESULT [get_Language](#get_language)(LPWSTR * Value)

Это относится к UI браузера, таким как контекстное меню и диалоговые окна. Она также применяется к HTTP-заголовку "принимаемые языки", WebView отправляется на веб-сайты. Оно представлено в формате, `language[-country]` который `language` является буквенным кодом из ISO 639 и `country` является буквенным кодом из ISO 3166.

#### get_TargetCompatibleBrowserVersion 

Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.

> общедоступные значения HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR * Value)

Это значение по умолчанию соответствует версии среды выполнения Edge WebView2, соответствующей версии SDK, используемой приложением. Формат этого значения совпадает с форматом свойства BrowserVersionString и другими BrowserVersion значениями. Учитывается только часть версии значения BrowserVersion. Суффикс канала, если он существует, пропускается. Используемая версия двоичных файлов среды выполнения WebView2 может отличаться от указанной TargetCompatibleBrowserVersion. Они гарантированно совместимы. Вы можете проверить фактическую версию в свойстве BrowserVersionString на ICoreWebView2Environment.

#### put_AdditionalBrowserArguments 

Задайте свойство AdditionalBrowserArguments.

> общедоступные значения HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(значение LPCWSTR)

#### put_Language 

Задайте свойство Language.

> общедоступные значения HRESULT [put_Language](#put_language)(значение LPCWSTR)

#### put_TargetCompatibleBrowserVersion 

Установите TargetCompatibleBrowserVersion.

> общедоступные значения HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(значение LPCWSTR)


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8378c6388f0bc7cda26ef4a34b8ef5e8d5c95f4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885046"
---
# класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Параметры, используемые для создания среды WebView2.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[AdditionalBrowserArguments](#additionalbrowserarguments) | AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.
[Язык](#language) | Язык по умолчанию, с которым будет выполняться WebView.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.
[CoreWebView2EnvironmentOptions](#corewebview2environmentoptions) | Инициализирует новый экземпляр класса CoreWebView2EnvironmentOptions.

Реализация по умолчанию предоставляется в WebView2EnvironmentOptions. h.

## Участников

#### AdditionalBrowserArguments 

AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView.

> общедоступная строка [AdditionalBrowserArguments](#additionalbrowserarguments)

Они будут переданы в процесс браузера как часть командной строки. Дополнительные сведения о параметрах командной строки для процесса браузера можно найти [в разделе Run Chromium with flags](https://aka.ms/RunChromiumWithFlags) . Если приложение запускается с переключателем командной строки, `--edge-webview-switches=xxx` значение этого переключателя (XXX в приведенном выше примере) также будет добавлено в командную строку процесса браузера. Некоторые переключатели `--user-data-dir` , такие как внутренние и важные для WebView. Эти переключатели будут игнорироваться, даже если они указаны. Если один и тот же параметр указан несколько раз, последний — один. Вы не пытаетесь объединять различные значения одного переключателя, кроме отключенных и включенных функций. Функции, указанные в параметре `--enable-features` и `--disable-features` объединяемые с простой логикой: функции будут объединены с указанными функциями и встроенными функциями, а если функция отключена, она будет удалена из списка включенные компоненты. Значения командной строки процесса приложения `--edge-webview-switches` обрабатываются после обработки параметра additionalBrowserArguments. Некоторые функции отключены для внутреннего использования и не могут быть включены. Если синтаксический анализ для указанных переключателей не удался, они будут пропущены. По умолчанию выполняется процесс браузера без дополнительных флагов.

#### Язык 

Язык по умолчанию, с которым будет выполняться WebView.

> [язык](#language) общедоступной строки

Это относится к UI браузера, таким как контекстное меню и диалоговые окна. Она также применяется к HTTP-заголовку "принимаемые языки", WebView отправляется на веб-сайты. Оно представлено в формате, `language[-country]` который `language` является буквенным кодом из ISO 639 и `country` является буквенным кодом из ISO 3166.

#### TargetCompatibleBrowserVersion 

Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.

> общедоступная строка [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)

Это значение по умолчанию соответствует версии среды выполнения Edge WebView2, соответствующей версии SDK, используемой приложением. Формат этого значения совпадает с форматом свойства BrowserVersionString и другими BrowserVersion значениями. Учитывается только часть версии значения BrowserVersion. Суффикс канала, если он существует, пропускается. Используемая версия двоичных файлов среды выполнения WebView2 может отличаться от указанной TargetCompatibleBrowserVersion. Они гарантированно совместимы. Вы можете проверить фактическую версию в свойстве BrowserVersionString на CoreWebView2Environment.

#### CoreWebView2EnvironmentOptions 

Инициализирует новый экземпляр класса CoreWebView2EnvironmentOptions.

> общедоступный [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(строковый additionalBrowserArguments, язык строк, строка targetCompatibleBrowserVersion)

##### Параметры
* `additionalBrowserArguments` AdditionalBrowserArguments можно указать, чтобы изменить поведение WebView. 

* `language` Язык по умолчанию, с которым будет выполняться WebView. 

* `targetCompatibleBrowserVersion` Версия двоичных файлов среды выполнения WebView2, которые должны быть совместимы с вызывающим приложением.


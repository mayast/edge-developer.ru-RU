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
ms.openlocfilehash: 93e662088ae1561b5dcb33390f46a41c19ca0aaf
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699132"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Аргументы события для события ScriptDialogOpening.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[DefaultText](#defaulttext) | Второй параметр, передаваемый диалоговому окну запроса JavaScript.
[Любые](#kind) | Диалоговое окно "вида JavaScript".
[Сообщение](#message) | Сообщение в диалоговом окне.
[ResultText](#resulttext) | Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".
[Универсальный код ресурса (URI)](#uri) | URI страницы, запросившего диалоговое окно.
[Принять](#accept) | Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.
[GetDeferral](#getdeferral) | Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.

## Участников

#### DefaultText 

Второй параметр, передаваемый диалоговому окну запроса JavaScript.

> общедоступная строка [DefaultText](#defaulttext)

Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".

#### Любые 

Диалоговое окно "вида JavaScript".

> общедоступный [CoreWebView2ScriptDialogKind](#kind)

Приняв, подтвердите, запросите или beforeunload.

#### Сообщение 

Сообщение в диалоговом окне.

> [сообщение](#message) общедоступной строки

Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.

#### ResultText 

Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".

> общедоступная строка [ResultText](#resulttext)

Этот тип игнорируется, если диалоговое окно не является запросом. Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".

#### Универсальный код ресурса (URI) 

URI страницы, запросившего диалоговое окно.

> [URI](#uri) общедоступной строки

#### Принять 

Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.

> общедоступная отмена [приема](#accept)()

Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии. И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.

#### GetDeferral 

Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.

> общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()

Вы можете использовать этот параметр, чтобы выполнить событие позже.


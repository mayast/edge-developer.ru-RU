---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885795"
---
# 0.8.355-Interface IWebView2ScriptDialogOpeningEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Аргументы события для события [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | URI страницы, запросившего диалоговое окно.
[get_Kind](#get_kind) | Диалоговое окно "вида JavaScript".
[get_Message](#get_message) | Сообщение в диалоговом окне.
[Принять](#accept) | Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК", чтобы подтвердить и запросить диалоговые окна, или не вызывайте этот способ для обозначения отмены.
[get_DefaultText](#get_defaulttext) | Второй параметр, передаваемый диалоговому окну запроса JavaScript.
[get_ResultText](#get_resulttext) | Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".
[put_ResultText](#put_resulttext) | Задайте свойство ResultText.
[GetDeferral](#getdeferral) | Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.

## Участников

#### get_Uri 

URI страницы, запросившего диалоговое окно.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### get_Kind 

Диалоговое окно "вида JavaScript".

> общедоступные значения HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND * видам)

#### get_Message 

Сообщение в диалоговом окне.

> общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR * сообщение)

Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt.

#### Принять 

Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК", чтобы подтвердить и запросить диалоговые окна, или не вызывайте этот способ для обозначения отмены.

> общедоступное значение HRESULT [принято](#accept)()

Из JavaScript это означает, что функция Confirm возвращает значение истина, если вызывается метод принятии. И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.

#### get_DefaultText 

Второй параметр, передаваемый диалоговому окну запроса JavaScript.

> общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR * DefaultText)

Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".

#### get_ResultText 

Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".

> общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR * ResultText)

Этот тип игнорируется, если диалоговое окно не является запросом. Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".

#### put_ResultText 

Задайте свойство ResultText.

> общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)

#### GetDeferral 

Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.

> общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * РБП)

Вы можете использовать этот параметр, чтобы выполнить событие позже.


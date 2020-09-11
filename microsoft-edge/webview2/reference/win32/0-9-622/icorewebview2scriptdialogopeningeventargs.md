---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: 442bd26caeb78804ceb202b302123b0ee1127f09
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012524"
---
# интерфейс ICoreWebView2ScriptDialogOpeningEventArgs 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Аргументы события для события ScriptDialogOpening.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Принять](#accept) | Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.
[get_DefaultText](#get_defaulttext) | Второй параметр, передаваемый диалоговому окну запроса JavaScript.
[get_Kind](#get_kind) | Диалоговое окно "вида JavaScript".
[get_Message](#get_message) | Сообщение в диалоговом окне.
[get_ResultText](#get_resulttext) | Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".
[get_Uri](#get_uri) | URI страницы, запросившего диалоговое окно.
[GetDeferral](#getdeferral) | Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.
[put_ResultText](#put_resulttext) | Задайте свойство ResultText.

## Участников

#### Принять 

Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.

> общедоступное значение HRESULT [принято](#accept)()

Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии. И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.

#### get_DefaultText 

Второй параметр, передаваемый диалоговому окну запроса JavaScript.

> общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR * DefaultText)

Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".

#### get_Kind 

Диалоговое окно "вида JavaScript".

> общедоступные значения HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND * видам)

Приняв, подтвердите, запросите или beforeunload.

#### get_Message 

Сообщение в диалоговом окне.

> общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR * сообщение)

Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.

#### get_ResultText 

Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".

> общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR * ResultText)

Этот тип игнорируется, если диалоговое окно не является запросом. Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".

#### get_Uri 

URI страницы, запросившего диалоговое окно.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### GetDeferral 

Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.

> общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * РБП)

Вы можете использовать этот параметр, чтобы выполнить событие позже.

#### put_ResultText 

Задайте свойство ResultText.

> общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)


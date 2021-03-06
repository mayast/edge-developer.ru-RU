---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: 8de2eaf6046b41df46b516694162471d22cafac3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012456"
---
# интерфейс ICoreWebView2MoveFocusRequestedEventArgs 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

Аргументы события для события MoveFocusRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Указывает, было ли событие обработано приложением.
[get_Reason](#get_reason) | Причина, по которой WebView запускает событие "MoveFocus".
[put_Handled](#put_handled) | Задайте свойство Handled.

## Участников

#### get_Handled 

Указывает, было ли событие обработано приложением.

> общедоступные значения HRESULT [get_Handled](#get_handled)(bool * Value)

Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE. Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию. Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно. Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.

#### get_Reason 

Причина, по которой WebView запускает событие "MoveFocus".

> общедоступные значения HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON * причина)

#### put_Handled 

Задайте свойство Handled.

> общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)


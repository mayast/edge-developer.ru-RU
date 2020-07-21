---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 5d8d447bced6bbbb51ae33220e74ebcf47f11ce5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885929"
---
# 0.8.355-Interface IWebView2MoveFocusRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

Аргументы события для события MoveFocusRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Reason](#get_reason) | Причина, по которой WebView запускает событие "MoveFocus".
[get_Handled](#get_handled) | Указывает, было ли событие обработано приложением.
[put_Handled](#put_handled) | Задайте свойство Handled.

## Участников

#### get_Reason 

Причина, по которой WebView запускает событие "MoveFocus".

> общедоступное значение HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON * значение)

#### get_Handled 

Указывает, было ли событие обработано приложением.

> общедоступные значения HRESULT [get_Handled](#get_handled)(bool * Value)

Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE. Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию. Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно. Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.

#### put_Handled 

Задайте свойство Handled.

> общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)


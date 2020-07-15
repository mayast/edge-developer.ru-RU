---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: fe0c0fae0ec33cbc5ba50ca163b3f4fc8baa61b9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880957"
---
# 0.9.430-Interface ICoreWebView2MoveFocusRequestedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2MoveFocusRequestedEventArgs
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

> общедоступное значение HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON * значение)

#### get_Handled 

Указывает, было ли событие обработано приложением.

> общедоступные значения HRESULT [get_Handled](#get_handled)(bool * Value)

Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE. Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию. Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно. Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.

#### put_Handled 

Задайте свойство Handled.

> общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)


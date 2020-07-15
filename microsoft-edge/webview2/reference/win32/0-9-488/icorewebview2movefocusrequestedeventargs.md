---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: dc6c904150605dc05b2fef00600785b9840f0eb8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880530"
---
# 0.9.515-Interface ICoreWebView2MoveFocusRequestedEventArgs 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

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

> общедоступное значение HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON * значение)

#### put_Handled 

Задайте свойство Handled.

> общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)


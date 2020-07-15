---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1a5330a9217430595acd708d565f38ca88f879f0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880943"
---
# 0.9.515-Interface ICoreWebView2AcceleratorKeyPressedEventArgs 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Аргументы события для события AcceleratorKeyPressed.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.
[get_KeyEventKind](#get_keyeventkind) | Тип события key, который привел к инициированию события.
[get_KeyEventLParam](#get_keyeventlparam) | Значение LPARAM, сопровождающее сообщение в окне.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.
[get_VirtualKey](#get_virtualkey) | Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.
[put_Handled](#put_handled) | Задает свойство Handled.

## Участников

#### get_Handled 

Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.

> общедоступные значения HRESULT [get_Handled](#get_handled)(логический * обработанный)

Если для свойства Handled установлено значение TRUE, это не позволит WebView выполнить действие по умолчанию для этого ключа ускорителя. В противном случае WebView выполнит действие по умолчанию для сочетания клавиш.

#### get_KeyEventKind 

Тип события key, который привел к инициированию события.

> общедоступные значения HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND * KeyEventKind)

#### get_KeyEventLParam 

Значение LPARAM, сопровождающее сообщение в окне.

> общедоступное значение HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int * lParam)

Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.

#### get_PhysicalKeyStatus 

Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.

> общедоступные значения HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### get_VirtualKey 

Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.

> общедоступные значения HRESULT [get_VirtualKey](#get_virtualkey)(uint * VirtualKey)

Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A". Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).

#### put_Handled 

Задает свойство Handled.

> общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)


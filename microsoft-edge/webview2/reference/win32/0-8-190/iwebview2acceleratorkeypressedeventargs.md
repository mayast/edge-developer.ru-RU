---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 5b15d6205306e558d1d8709cceed8b7a68a77bce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654823"
---
# интерфейс IWebView2AcceleratorKeyPressedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Аргументы события для события AcceleratorKeyPressed.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_KeyEventType](#get_keyeventtype) | Тип события key, который привел к инициированию события.
[get_VirtualKey](#get_virtualkey) | Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.
[get_KeyEventLParam](#get_keyeventlparam) | Значение LPARAM, сопровождающее сообщение в окне.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.
[Рабатывайте](#handle) | Вызов этого действия позволит продолжить процесс браузера.

## Участников

#### get_KeyEventType 

Тип события key, который привел к инициированию события.

> общедоступные значения HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE * KeyEventType)

Это один из WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN или WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.

#### get_VirtualKey 

Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.

> общедоступные значения HRESULT [get_VirtualKey](#get_virtualkey)(uint * VirtualKey)

Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A". Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).

#### get_KeyEventLParam 

Значение LPARAM, сопровождающее сообщение в окне.

> общедоступное значение HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int * lParam)

Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.

#### get_PhysicalKeyStatus 

Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.

> общедоступные значения HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### Рабатывайте 

Вызов этого действия позволит продолжить процесс браузера.

> общедоступный [дескриптор](#handle)HRESULT (обработанные логические значения)

Передача значения TRUE не позволит браузеру выполнить действие по умолчанию для этого ключа ускорителя. Если обработчик событий возвращается без [дескриптора вызова ()](#handle), то он эквивалентен дескриптору вызова (false). Вызов [дескриптора ()](#handle) после того, как он уже был вызван, или возвращенный обработчик событий не выполняет никаких действий.


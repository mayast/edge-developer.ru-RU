---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: aeefa0257a273f0eecd99d3f666adc03be709d9a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880495"
---
# 0.9.515-Interface ICoreWebView2NewWindowRequestedEventArgs 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

Аргументы события для события NewWindowRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.
[get_IsUserInitiated](#get_isuserinitiated) | IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.
[get_NewWindow](#get_newwindow) | Получает новое окно.
[get_Uri](#get_uri) | Целевой URI для NewWindowRequest.
[GetDeferral](#getdeferral) | Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.
[put_Handled](#put_handled) | Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.
[put_NewWindow](#put_newwindow) | Задает WebView в качестве результата NewWindowRequest.

Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).

## Участников

#### get_Handled 

Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.

> общедоступные значения HRESULT [get_Handled](#get_handled)(логический * обработанный)

#### get_IsUserInitiated 

IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.

> общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### get_NewWindow 

Получает новое окно.

> общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) * * NewWindow)

#### get_Uri 

Целевой URI для NewWindowRequest.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### GetDeferral 

Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.

> общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * РБП)

Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) , чтобы завершить запрос на открытие окна позже. Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.

#### put_Handled 

Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.

> общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)

Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy. Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет. Значение по умолчанию — false.

#### put_NewWindow 

Задает WebView в качестве результата NewWindowRequest.

> общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) * NewWindow)

Не следует перемещаться по целевому WebView. Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.


---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2ea3500c5e230b543f75241c47c58163276942da
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654855"
---
# интерфейс ICoreWebView2NewWindowRequestedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

Аргументы события для события NewWindowRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Целевой URI для NewWindowRequest.
[put_NewWindow](#put_newwindow) | Задает WebView в качестве результата NewWindowRequest.
[get_NewWindow](#get_newwindow) | Получает новое окно.
[put_Handled](#put_handled) | Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.
[get_Handled](#get_handled) | Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.
[get_IsUserInitiated](#get_isuserinitiated) | IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.
[GetDeferral](#getdeferral) | Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.

Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (через Window. Open () и т. д.)

## Участников

#### get_Uri 

Целевой URI для NewWindowRequest.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### put_NewWindow 

Задает WebView в качестве результата NewWindowRequest.

> общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) * NewWindow)

Не следует перемещаться по целевому WebView. Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.

#### get_NewWindow 

Получает новое окно.

> общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) * * NewWindow)

#### put_Handled 

Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.

> общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)

Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy. Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет. Значение по умолчанию — false.

#### get_Handled 

Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.

> общедоступные значения HRESULT [get_Handled](#get_handled)(логический * обработанный)

#### get_IsUserInitiated 

IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.

> общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### GetDeferral 

Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.

> общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * РБП)

Вы можете использовать объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) , чтобы завершить запрос на открытие окна позже. Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.


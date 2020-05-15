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
ms.openlocfilehash: e1917a4383e6e5d8aaf79464c4607d8f2d4f0cdc
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654654"
---
# интерфейс IWebView2NewWindowRequestedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2NewWindowRequestedEventArgs
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
[GetDeferral](#getdeferral) | Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.

Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (через Window. Open () и т. д.)

## Участников

#### get_Uri 

Целевой URI для NewWindowRequest.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### put_NewWindow 

Задает WebView в качестве результата NewWindowRequest.

> общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) * NewWindow)

Не следует перемещаться по целевому WebView. Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.

#### get_NewWindow 

Получает новое окно.

> общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) * * NewWindow)

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

Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.

> общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * РБП)

Вы можете использовать объект [IWebView2Deferral](IWebView2Deferral.md) , чтобы завершить запрос на открытие окна позже. Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.


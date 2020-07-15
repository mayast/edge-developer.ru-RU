---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d10154fbaeb8dca0247dc721a2144899feba38df
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880012"
---
# класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Аргументы события для события NewWindowRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Handled](#handled) | Обрабатываются ли NewWindowRequestedEvent с помощью Host.
[IsUserInitiated](#isuserinitiated) | IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.
[NewWindow](#newwindow) | Получает новое окно.
[Универсальный код ресурса (URI)](#uri) | Целевой URI для NewWindowRequest.
[GetDeferral](#getdeferral) | Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.

Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).

## Участников

#### Handled 

Обрабатываются ли NewWindowRequestedEvent с помощью Host.

> общедоступный логический том [обработан](#handled)

Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy. Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет. Значение по умолчанию — false.

#### IsUserInitiated 

IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.

> Открытый логический [IsUserInitiated](#isuserinitiated)

#### NewWindow 

Получает новое окно.

> общедоступная CoreWebView2 [NewWindow](#newwindow)

#### Универсальный код ресурса (URI) 

Целевой URI для NewWindowRequest.

> [URI](#uri) общедоступной строки

Не следует перемещаться по целевому WebView. Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.

#### GetDeferral 

Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.

> общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()

Вы можете использовать объект CoreWebView2Deferral, чтобы завершить запрос на открытие окна позже. Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.


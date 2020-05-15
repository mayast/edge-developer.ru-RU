---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 3c88108f0e1df89c62c8713ff37f35d0c759cf6c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654994"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Аргументы события для события MoveFocusRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Handled](#handled) | Указывает, было ли событие обработано приложением.
[Причина](#reason) | Причина, по которой WebView запускает событие "MoveFocus".

## Участников

#### Handled 

Указывает, было ли событие обработано приложением.

> общедоступный логический том [обработан](#handled)

Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE. Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию. Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно. Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.

#### Причина 

Причина, по которой WebView запускает событие "MoveFocus".

> [Причина](#reason) общедоступной CoreWebView2MoveFocusReason


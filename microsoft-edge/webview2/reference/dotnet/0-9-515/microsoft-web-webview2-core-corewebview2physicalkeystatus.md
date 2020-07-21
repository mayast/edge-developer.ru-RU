---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: eecf4dd59d12c30667defd4e078e8624718bde26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884591"
---
# Структура 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[IsExtendedKey](#isextendedkey) | Указывает на то, является ли ключ дополнительным ключом.
[IsKeyReleased](#iskeyreleased) | Состояние перехода.
[IsMenuKeyDown](#ismenukeydown) | Код контекста.
[RepeatCount](#repeatcount) | Число повторов для текущего сообщения.
[ScanCode](#scancode) | Код сканирования.
[WasKeyDown](#waskeydown) | Предыдущее состояние ключа.

Подробные сведения о WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .

## Участников

#### IsExtendedKey 

Указывает на то, является ли ключ дополнительным ключом.

> public int [IsExtendedKey](#isextendedkey)

#### IsKeyReleased 

Состояние перехода.

> public int [IsKeyReleased](#iskeyreleased)

#### IsMenuKeyDown 

Код контекста.

> public int [IsMenuKeyDown](#ismenukeydown)

#### RepeatCount 

Число повторов для текущего сообщения.

> Открытый uint [repeatCount](#repeatcount)

#### ScanCode 

Код сканирования.

> Открытый uint [ScanCode](#scancode)

#### WasKeyDown 

Предыдущее состояние ключа.

> public int [WasKeyDown](#waskeydown)


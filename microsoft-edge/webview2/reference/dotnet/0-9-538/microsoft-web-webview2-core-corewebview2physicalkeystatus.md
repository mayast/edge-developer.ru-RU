---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 280fe2d970d78bf1ea7a79b21f5081510ee27053
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878773"
---
# Структура Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

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


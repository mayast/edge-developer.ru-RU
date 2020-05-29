---
description: Ссылка на домен DOMDebugger. Отладка DOM позволяет задавать точки останова для определенных операций и событий DOM. Выполнение JavaScript будет остановлено на этих операциях так, как если бы была установлена обычная точка останова.
title: Протокол DOMDebugger Domain-DevTools версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571667"
---
# DOMDebugger
Отладка DOM позволяет задавать точки останова для определенных операций и событий DOM. Выполнение JavaScript будет остановлено на этих операциях так, как если бы была установлена обычная точка останова.

| | |
|-|-|
| [**Методы**](#methods) | [setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint) |
## Методы

### setInstrumentationBreakpoint
<span><b>Проб. </b></span>Задает точку останова для определенного собственного события.

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>eventName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя инструментирования, на котором нужно остановиться. Допустимые значения: "scriptFirstStatement".</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeInstrumentationBreakpoint
<span><b>Проб. </b></span>Удаляет точку останова в определенном собственном событии.

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>eventName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя инструментирования, на котором нужно остановиться. Допустимые значения: "scriptFirstStatement".</td>
        </tr>
    </tbody>
</table>
</p>

---

---
description: Ссылка на домен оверлея. Перекрытие доменов обеспечивает взаимодействие визуальных элементов оформления и выделения узлов
title: Overlay Domain-DevTools Protocol версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: a7657e2abc99e45894f19f6557f12f78f8ee9c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571666"
---
# Наложение
Перекрытие доменов обеспечивает взаимодействие визуальных элементов оформления и выделения узлов

| | |
|-|-|
| [**Методы**](#methods) | [Включение](#enable), [Отключение](#disable), [setInspectMode](#setinspectmode) |
| [**События**](#events) | [inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested) |
| [**Зависимости**](#dependencies) | [DOM](dom.md) |
## Методы

### "Включить"
Включение отчетов о <code>nodeHighlightRequested</code> <code>inspectElementRequested</code> событиях и событий

</p>

---

### "Отключить" 
Отключает отчетность о событиях домена оверлея

</p>

---

### setInspectMode
Задает режим выделения элементов для клиента.

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
            <td>mode</td>
            <td><code class="flyout">string</code></td>
            <td>Режим проверки.  Допустимые значения: "searchForNode" и "нет".</td>
        </tr>
        <tr>
            <td>highlightConfig <br/> <i>необязательные</i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td>Конфигурация подсветки, которую необходимо использовать при проверке</td>
        </tr>
    </tbody>
</table>
</p>

---

## События

### inspectNodeRequested
Уведомляет клиента о том, что пользователь запросит проверить конкретный узел.

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
            <td>backendNodeId</td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td>Запрошенный код узла внутреннего узла</td>
        </tr>
    </tbody>
</table>
</p>

---

### nodeHighlightRequested
Показывает, что пользователь наводит указатель мыши на узел и может проверить узел

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
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td>Идентификатор узла для рассматриваемого узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Зависимости

[DOM](dom.md)
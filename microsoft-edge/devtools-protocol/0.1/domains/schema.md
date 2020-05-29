---
description: Ссылка на домен схемы. Предоставляет сведения о схеме протоколов.
title: Schema Domain-DevTools Protocol версии 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 83d7019d18ccce1c81b67aafdcafe1a8566694ea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571686"
---
# Схема
Предоставляет сведения о схеме протоколов.

| | |
|-|-|
| [**Методы**](#methods) | ["домены"](#getdomains) |
| [**Типы**](#types) | [Домен](#domain) |
## Методы

### "домены"
Возвращает поддерживаемые домены.

<table>
    <thead>
        <tr>
            <th>Дает</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>имена</td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td>Список поддерживаемых доменов.</td>
        </tr>
    </tbody>
</table>

---

## Типы

### <a name="domain"></a> Домен `object`

Описание домена протоколов.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Доменное имя.</td>
        </tr>
        <tr>
            <td>version</td>
            <td><code class="flyout">string</code></td>
            <td>Версия домена.</td>
        </tr>
    </tbody>
</table>

---

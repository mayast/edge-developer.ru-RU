---
description: Ссылка на домен схемы. Предоставляет сведения о схеме протоколов.
title: Domain Schema-DevTools Protocol версии 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a2f679f6f4bf8e82dc7298d96f798507b1338062
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882928"
---
# Domain Schema-DevTools Protocol версии 0,1 (EdgeHTML)  

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

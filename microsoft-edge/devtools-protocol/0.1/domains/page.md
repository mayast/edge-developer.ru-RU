---
description: Ссылка на домен страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools версии 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 1602673eae1c04f60046a898dbadeab1b59f9ce5
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882942"
---
# Домен страницы — Протокол DevTools версии 0,1 (EdgeHTML)  

Действия и события, связанные с проверенной страницей, относятся к домену страницы.

| | |
|-|-|
| [**Методы**](#methods) | [Включение](#enable), [Отключение](#disable), [Навигация](#navigate) |
| [**Типы**](#types) | [FrameId](#frameid) |
## Методы

### "Включить"
Включение уведомлений домена на странице.


---

### "Отключить" 
Отключение уведомлений домена на странице.


---

### переход
Переход на текущую страницу по указанному URL-адресу.

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
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес для перемещения по странице.</td>
        </tr>
    </tbody>
</table>
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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b>Проб. </b></span>Код кадра, который будет использоваться для навигации.</td>
        </tr>
    </tbody>
</table>

---

## Типы

### <a name="frameid"></a> FrameId `string`

Уникальный идентификатор кадра.


---

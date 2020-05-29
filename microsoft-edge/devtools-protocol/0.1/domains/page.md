---
description: Ссылка на домен страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools версии 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a1cd094baef4571240881a86ecccfdb319fef61b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571692"
---
# Page
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

---
description: Ссылка на домен страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools версии 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 864515eefbcb809e280f2ab1d81015018272c398
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882844"
---
# Домен страницы — Протокол DevTools версии 0,2 (EdgeHTML)  

Действия и события, связанные с проверенной страницей, относятся к домену страницы.

| | |
|-|-|
| [**Методы**](#methods) | [Включение](#enable), [Отключение](#disable), [Навигация](#navigate), [getFrameTree](#getframetree) |
| [**Мероприятия**](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |
| [**Типы**](#types) | [FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree) |
## Методы

### "Включить"
Включение уведомлений домена на странице.

</p>

---

### "Отключить" 
Отключение уведомлений домена на странице.

</p>

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
        <tr>
            <td>frameId <br/> <i>необязательные</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Код кадра для навигации. Если он не указан, переходим к верхней странице.</td>
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
            <td>Код кадра, который будет использоваться для навигации.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getFrameTree
Возвращает структуру дерева кадров.

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
            <td>frameTree</td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td>Показать древовидную структуру фреймов.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Мероприятия

### frameAttached
Срабатывает, если кадр присоединен к родительскому элементу.

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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Идентификатор присоединенного кадра.</td>
        </tr>
        <tr>
            <td>parentFrameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Идентификатор родительского фрейма.</td>
        </tr>
        <tr>
            <td>стека <br/> <i>необязательные</i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td>Трассировка стека JavaScript для вложенного кадра задается только в том случае, если кадр инициирован из сценария.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameDetached
Срабатывает, если кадр отсоединен от родительского элемента.

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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Идентификатор отсоединенного кадра.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameNavigated
Срабатывает после завершения навигации кадра.

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
            <td>интервал</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Объект Frame.</td>
        </tr>
    </tbody>
</table>
</p>

---

### loadEventFired
Соответствует событию Window. OnLoad.

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
            <td>штамп</td>
            <td><code class="flyout">number</code></td>
            <td>Количество миллисекунд, прошедшее с момента создания эпохи.</td>
        </tr>
    </tbody>
</table>
</p>

---

### domContentEventFired
Соответствует событию Document. onDOMContentLoaded.

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
            <td>штамп</td>
            <td><code class="flyout">number</code></td>
            <td>Количество миллисекунд, прошедшее с момента создания эпохи.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Типы

### <a name="frameid"></a> FrameId `string`

Уникальный идентификатор кадра.

</p>

---

### <a name="frame"></a> Кадр `object`

Сведения о кадре на странице.

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
            <td>id</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Уникальный идентификатор кадра.</td>
        </tr>
        <tr>
            <td>parentId <br/> <i>необязательные</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Уникальный идентификатор родительского фрейма.</td>
        </tr>
        <tr>
            <td>name <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Имя кадра, указанное в теге.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес документа в рамке.</td>
        </tr>
        <tr>
            <td>securityOrigin</td>
            <td><code class="flyout">string</code></td>
            <td>Источник защиты документа фрейма.</td>
        </tr>
        <tr>
            <td>Успешности</td>
            <td><code class="flyout">string</code></td>
            <td>Тип MIME документа Frame определяется браузером.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> FrameTree `object`

Сведения о иерархии рамок.

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
            <td>интервал</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Сведения о кадре для этого элемента дерева.</td>
        </tr>
        <tr>
            <td>childFrames <br/> <i>необязательные</i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td>Дочерние кадры.</td>
        </tr>
    </tbody>
</table>
</p>

---

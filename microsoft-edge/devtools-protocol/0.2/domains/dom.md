---
description: Ссылка на домен DOM. Этот домен предоставляет DOM-операции чтения и записи. Каждый узел DOM представлен с помощью зеркального объекта `id` . Это `id` можно использовать для получения дополнительных сведений на узле, разрешения их в обертку объекта JavaScript и т. д. Важно, чтобы клиент получал события DOM только для тех узлов, которые известны клиенту. Внутренний сервер отслеживает узлы, отправленные клиенту, и никогда не отправляет один и тот же узел дважды. Ответственность за сбор сведений о узлах, отправленных клиенту, лежит на клиенте.<p>Обратите внимание, что `iframe` элементы Owner будут возвращать соответствующие элементы документа в качестве дочерних узлов.</p>
title: Домен DOM — протокол DevTools версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 9ebe5ff709ac2981cb2359b7279c5d4e5d375426
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571673"
---
# DOM
Этот домен предоставляет DOM-операции чтения и записи. Каждый узел DOM представлен с помощью зеркального объекта `id` . Это `id` можно использовать для получения дополнительных сведений на узле, разрешения их в обертку объекта JavaScript и т. д. Важно, чтобы клиент получал события DOM только для тех узлов, которые известны клиенту. Внутренний сервер отслеживает узлы, отправленные клиенту, и никогда не отправляет один и тот же узел дважды. Ответственность за сбор сведений о узлах, отправленных клиенту, лежит на клиенте.<p>Обратите внимание, что `iframe` элементы Owner будут возвращать соответствующие элементы документа в качестве дочерних узлов.</p>

| | |
|-|-|
| [**Методы**](#methods) | [Включение](#enable), [Отключение](#disable), [getDocument](#getdocument) [highlightNode](#highlightnode), [hideHighlight](#hidehighlight) [setInspectedNode](#setinspectednode) , [requestChildNodes](#requestchildnodes), [InAttribute](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector) [, querySelectorAll](#queryselectorall) [requestNode](#requestnode) [. requestNode](#resolvenode) |
| [**События**](#events) | [setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated) |
| [**Типы**](#types) | [RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype) |
| [**Зависимости**](#dependencies) | [Язык](runtime.md) |
## Методы

### "Включить"
Включает агент DOM для указанной страницы.

</p>

---

### "Отключить" 
Отключает агент DOM для указанной страницы. Отключение DOM сделает все ранее действительные nodeIds недействительными.

</p>

---

### "документ"
Возвращает корневой узел DOM (и, при необходимости, поддерево) вызывающему объекту. При вызове `getDocument` будут аннулированы все ранее действительные nodeIds

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
            <td>одной</td>
            <td><code class="flyout">integer</code></td>
            <td>Максимальная глубина, при которой должны извлекаться дочерние элементы, значение по умолчанию — 2. Используйте-1 для всего поддерева.</td>
        </tr>
        <tr>
            <td>pierce</td>
            <td><code class="flyout">boolean</code></td>
            <td>Следует ли прослеживать элементы iframe при возврате поддерева (значение по умолчанию — ложь).</td>
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
            <td>узла</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Конечный узел.</td>
        </tr>
    </tbody>
</table>
</p>

---

### highlightNode
Higlights узел DOM с заданным идентификатором или оберткой объекта. nodeId, backendNodeId или objectId должны быть указаны.

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
            <td>nodeId <br/> <i>необязательные</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор выделяемого узла.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>необязательные</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Идентификатор узла внутреннего элемента, который нужно выделиь.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>Код объекта JavaScript для выделенного узла.</td>
        </tr>
        <tr>
            <td>higlightConfig</td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td>Описательный вид подсветки.</td>
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
            <td>узла</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Конечный узел.</td>
        </tr>
    </tbody>
</table>
</p>

---

### hideHighlight
Скрывает любой текущий выделенный фрагмент DOM-узла.

</p>

---

### requestChildNodes
Запросы, которые дочерние элементы узла с указанным идентификатором, возвращаются в GHE вызывающего кода в форме `setChildNodes` событий. `setChildNodes` будет инициировано для каждого узла, который ранее не возвращал дочерние элементы, начиная с запрашиваемого узла и до указанной глубины.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, из которого нужно получить дочерние элементы.</td>
        </tr>
        <tr>
            <td>одной</td>
            <td><code class="flyout">integer</code></td>
            <td>Максимальная глубина, при которой должны извлекаться дочерние элементы, по умолчанию равной 1. Используйте-1 для всего поддерева.</td>
        </tr>
        <tr>
            <td>pierce</td>
            <td><code class="flyout">boolean</code></td>
            <td>Следует ли прослеживать элементы iframe при возврате поддерева (значение по умолчанию — ложь).</td>
        </tr>
    </tbody>
</table>
</p>

---

### Атрибуты.
Возвращает атрибуты для указанного узла.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, для которого требуется извлечь attibutes.</td>
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
            <td>атрибуты</td>
            <td><code class="flyout">string[]</code></td>
            <td>Массив с чередованием имен и значений атрибутов узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getOuterHTML
Возвращает разметку HTML узла.

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
            <td>nodeId <br/> <i>необязательные</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>необязательные</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Идентификатор узла внутреннего сервера.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>Идентификатор объекта JavaScript обертки узла.</td>
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
            <td>outerHTML</td>
            <td><code class="flyout">string</code></td>
            <td>Внешняя разметка HTML.</td>
        </tr>
    </tbody>
</table>
</p>

---

### pushNodesByBackendIdsToFrontend
Поиск идентификаторов узлов и разрешение всех родительских элементов для указанных кодов внутренних узлов

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
            <td>backendNodeIds</td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td>Идентификаторы узлов внутренних узлов, которые нужно разрешить</td>
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
            <td>nodeIds</td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Идентификаторы узлов разрешенных узлов</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelector
Выполняется `querySelector` на указанном узле.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла для запроса.</td>
        </tr>
        <tr>
            <td>выбора</td>
            <td><code class="flyout">string</code></td>
            <td>Строка выбора.</td>
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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Результат выбора запроса.</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelectorAll
Выполняется `querySelectorAll` на указанном узле.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла для запроса.</td>
        </tr>
        <tr>
            <td>выбора</td>
            <td><code class="flyout">string</code></td>
            <td>Строка выбора.</td>
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
            <td>nodeIds</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Результаты выбора запроса.</td>
        </tr>
    </tbody>
</table>
</p>

---

### requestNode
Запросы, которые отправляются вызывающему объекту для узла с указанным идентификатором удаленного объекта. Все узлы, которые формируют путь из узла к корню, также отправляются клиенту в виде серии `setChildNodes` уведомлений. Возвращает значение 0, если документ, содержащий запрошенный узел, ранее не запрашивался клиентом.

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
            <td>objectId</td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>Идентификатор объекта JavaScript, который нужно преобразовать в узел.</td>
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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла для заданного объекта.</td>
        </tr>
    </tbody>
</table>
</p>

---

### resolveNode
Выполняет разрешение объекта узла JavaScript для данного NodeId или BackendNodeId.

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
            <td>nodeId <br/> <i>необязательные</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор разрешаемого узла.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>необязательные</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Код внутреннего узла для разрешаемого узла.</td>
        </tr>
        <tr>
            <td>objectGroup</td>
            <td><code class="flyout">string</code></td>
            <td>Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</td>
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
            <td>объект</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Обертка объекта JavaScript для данного узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setInspectedNode
<span><b>Проб. </b></span>Позволяет консоли ссылаться на предыдущий проверенный узел с указанным ID через $0-$ 4.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла DOM, доступ к которому осуществляется с помощью $0-$ 4 в интерфейсе API командной строки.</td>
        </tr>
    </tbody>
</table>
</p>

---

## События

### setChildNodes
Возникает, когда серверный внутренний объект хочет предоставить клиенту отсутствующую структуру DOM. Это происходит при большинстве звонков, запрашивающих nodeIds

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
            <td>parentId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Родительский узел для poplate с дочерними элементами.</td>
        </tr>
        <tr>
            <td>кластер</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Массив дочерних узлов.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeModified
Срабатывает при `Element` изменении атрибута.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, который изменился.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Имя атрибута.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Значение атрибута.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeRemoved
Срабатывает при `Element` удалении атрибута.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, который изменился.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Имя атрибута.</td>
        </tr>
    </tbody>
</table>
</p>

---

### characterDataModified
Событие «зеркала `DOMCharacterDataModified` ».

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, который изменился.</td>
        </tr>
        <tr>
            <td>charcterData</td>
            <td><code class="flyout">string</code></td>
            <td>Новое текстовое значение.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeInserted
Событие «зеркала `DOMNodeInserted` ».

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, который изменился.</td>
        </tr>
        <tr>
            <td>previousNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор предыдущего одноуровневого элемента вставленного узла.</td>
        </tr>
        <tr>
            <td>узлы</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Вставленные данные узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeRemoved
Событие «зеркала `DOMNodeRemoved` ».

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, который изменился.</td>
        </tr>
        <tr>
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, который был удален.</td>
        </tr>
    </tbody>
</table>
</p>

---

### documentUpdated
Срабатывает `Document` , если обновление выполнено полностью. Идентификаторы узлов больше не действительны.

</p>

---

## Типы

### <a name="rgba"></a> RGBA `object`

Структура, содержащая цвет RGBA.

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
            <td>&</td>
            <td><code class="flyout">integer</code></td>
            <td>Красный компонент в диапазоне [0-255].</td>
        </tr>
        <tr>
            <td>финансовой</td>
            <td><code class="flyout">integer</code></td>
            <td>Зеленый компонент в диапазоне [0-255].</td>
        </tr>
        <tr>
            <td>байт</td>
            <td><code class="flyout">integer</code></td>
            <td>Синий компонент в диапазоне [0-255].</td>
        </tr>
        <tr>
            <td>а <br/> <i>необязательные</i></td>
            <td><code class="flyout">number</code></td>
            <td>Альфа-компонент в диапазоне [0-1]. Значение по умолчанию — 1.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> HighlightConfig `object`

Данные конфигурации для выделяют элементы страницы.

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
            <td>contentColor <br/> <i>необязательные</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Цвет заливки, выделяя рамку содержимого. Значение по умолчанию — прозрачный.</td>
        </tr>
        <tr>
            <td>paddingColor <br/> <i>необязательные</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Цвет заливки с выделением полей. Значение по умолчанию — прозрачный.</td>
        </tr>
        <tr>
            <td>Границы <br/> <i>необязательные</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Цвет заливки выделения границ. Значение по умолчанию — прозрачный.</td>
        </tr>
        <tr>
            <td>marginColor <br/> <i>необязательные</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Цвет заливки полей. Значение по умолчанию — прозрачный.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> NodeId `integer`

Уникальный идентификатор узла DOM

</p>

---

### <a name="node"></a> Узлы `object`

Зеркальный объект, представляющий фактические узлы DOM.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, используемый для ссылки на этот узел. Внутренний сервер будет срабатывать события DOM для узлов, которые имеют nodeId, известный клиенту.</td>
        </tr>
        <tr>
            <td>parentId <br/> <i>необязательные</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла родительского узла, если таковой имеется.</td>
        </tr>
        <tr>
            <td>backendNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор внутреннего узла узла. BackendNodeIds узлы ссылок, которые могут быть известны клиенту, но не отменяют события DOM для этого узла.</td>
        </tr>
        <tr>
            <td>Узла</td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`nodeType.</td>
        </tr>
        <tr>
            <td>nodeName</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`nodeName.</td>
        </tr>
        <tr>
            <td>Локально</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`localName</td>
        </tr>
        <tr>
            <td>nodeValue</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`nodeValue</td>
        </tr>
        <tr>
            <td>childNodeCount <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Число дочерних элементов для `Container` узлов.</td>
        </tr>
        <tr>
            <td>дети <br/> <i>необязательные</i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Дочерние узлы этого узла, запрашиваемые дочерними элементами.</td>
        </tr>
        <tr>
            <td>атрибуты <br/> <i>необязательные</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Атрибуты `Element` узлов в форме плоского массива [файл1, value1, имя2, значение2]</td>
        </tr>
        <tr>
            <td>documentURL <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес документа, `Document` на который указывает узел.</td>
        </tr>
        <tr>
            <td>baseURL <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес документа, который `Document` используются узлами для завершения URL-адреса.</td>
        </tr>
        <tr>
            <td>publicId <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` PublicId узла.</td>
        </tr>
        <tr>
            <td>systemId <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` SystemId узла.</td>
        </tr>
        <tr>
            <td>internalSubset <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` InternalSubset узла.</td>
        </tr>
        <tr>
            <td>xmlVersion <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` Версия XML узла в случае XML-документов.</td>
        </tr>
        <tr>
            <td>name <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Имя узла.</td>
        </tr>
        <tr>
            <td>value <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Значение узла.</td>
        </tr>
        <tr>
            <td>frameId <br/> <i>необязательные</i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td>ИДЕНТИФИКАТОР кадра для элементов владельца кадра.</td>
        </tr>
        <tr>
            <td>contentDocument <br/> <i>необязательные</i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Документ содержимого для элементов владельца фрейма.</td>
        </tr>
        <tr>
            <td>isSVG <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Значение true, если узел является SVG.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> BackendNodeId `integer`

Уникальный идентификатор узла DOM, который используется для ссылки на узел, который может не быть передан на сервер переднего плана.

</p>

---

### <a name="pseudotype"></a> PseudoType `string`

Тип псевдослучайных элементов.

##### Допустимые значения
Первая строка, первая буква, до, после, выделение
</p>

---

## Зависимости

[Язык](runtime.md)
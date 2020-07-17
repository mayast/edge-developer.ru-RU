---
description: Справочник по домену среды выполнения. Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов. Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не были явно освобождены.
title: Домен среды выполнения — протокол DevTools версии 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 710b3b3e0383f1f6feb7947e0468730d2e0b0e66
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882865"
---
# Домен среды выполнения — протокол DevTools версии 0,2 (EdgeHTML)  

Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов. Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не были явно освобождены.

| | |
|-|-|
| [**Методы**](#methods) | [Включение](#enable), [Отключение](#disable), [Оценка](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [Свойства](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries) |
| [**Мероприятия**](#events) | [executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled) |
| [**Типы**](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription) [timestamp](#timestamp), [ExecutionContextDescription,](#exceptiondetails) [StackTrace](#stacktrace) [CallFrame](#callframe) |
## Методы

### "Включить"
Позволяет создавать отчеты об ошибках <code>executionContextCreated</code> <code>executionContextDestroyed</code> и <code>executionContextsCleared</code> событиях. При включении отчетов <code>executionContextCreated</code> событие будет отправлено немедленно для каждого существующего контекста выполнения.

</p>

---

### "Отключить" 
Отключает отчетность о <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> событиях.

</p>

---

### Проверьте
Вычисляет выражение для глобального объекта.

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
            <td>выражение</td>
            <td><code class="flyout">string</code></td>
            <td>Выражение для вычисления.</td>
        </tr>
        <tr>
            <td>includeCommandLineAPI <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Определяет, будет ли интерфейс API командной строки доступен во время оценки.</td>
        </tr>
        <tr>
            <td>objectGroup <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение. Переопределение <code>setPauseOnException</code> состояния.</td>
        </tr>
        <tr>
            <td>contextId <br/> <i>необязательные</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Указывает, в каком контексте выполнения выполнить оценку. Если параметр опущен, то оценка будет выполнена в контексте страницы проверки.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Может ли результат быть объектом JSON, который должен отправляться по значению.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</td>
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
            <td>завершил</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Результат вычисления.</td>
        </tr>
    </tbody>
</table>
</p>

---

### callFunctionOn
Вызывает функцию с заданным объявлением для заданного объекта. Группа объектов результата наследуется от целевого объекта.

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
            <td>functionDeclaration</td>
            <td><code class="flyout">string</code></td>
            <td>Объявление вызываемой функции.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Идентификатор объекта, для которого вызывается функция. Следует указать значение objectId или executionContextId.  objectId должен быть из функции Runtime. Evaluate ().</td>
        </tr>
        <tr>
            <td>arguments <br/> <i>необязательные</i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td>Аргументы вызова. Все аргументы вызова должны принадлежать тому же миру JavaScript, что и целевой объект.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>В режиме молчания исключения, созданные во время оценки, не включаются в отчеты и не приостанавливают выполнение. Переопределение <code>setPauseOnException</code> состояния.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Должен ли результат быть объектом JSON, который будет отправляться по значению.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><code>await</code>Разрешено ли выполнение для получающегося и возвращаемого значения после того, как ожидается обещание.</td>
        </tr>
        <tr>
            <td>executionContextId <br/> <i>необязательные</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Задает контекст выполнения, для которого будет использоваться глобальный объект для вызова функции. Следует указать значение executionContextId или objectId.</td>
        </tr>
        <tr>
            <td>objectGroup <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Символьное имя группы, которое можно использовать для освобождения нескольких объектов. Если objectGroup не указан, а objectId — objectGroup будет унаследован от Object.</td>
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
            <td>завершил</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Результат звонка.</td>
        </tr>
    </tbody>
</table>
</p>

---

### awaitPromise
Добавьте обработчик в Promise с заданным идентификатором объекта Promise.

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
            <td>promiseObjectId</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Идентификатор обещания.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Может ли результат быть объектом JSON, который должен отправляться по значению.</td>
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
            <td>завершил</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Результат обещания.  Будет содержать отклоненное значение, если обещание отклонено.</td>
        </tr>
    </tbody>
</table>
</p>

---

### Свойства.
Возвращает свойства заданного объекта. Группа объектов результата наследуется от целевого объекта.

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
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Идентификатор объекта, свойства которого нужно вернуть. objectId должен быть из функции Debugger. evaluateOnCallFrame ().</td>
        </tr>
        <tr>
            <td>ownProperties <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Если значение равно true, возвращает свойства только для самого элемента, а не для цепочки прототипов.</td>
        </tr>
        <tr>
            <td>accessorPropertiesOnly <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Проб. </b></span>Если значение равно true, возвращает свойства метода доступа (только с методами Get и Set). внутренние свойства не возвращаются ни одному из них.</td>
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
            <td>завершил</td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td>Свойства объекта.</td>
        </tr>
    </tbody>
</table>
</p>

---

### globalLexicalScopeNames
Возвращает все переменные let, const и Class из глобальной области консоли.

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
            <td>названия</td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### releaseObject
Освобождает удаленный объект с заданным идентификатором.

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
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Идентификатор объекта для освобождения. </td>
        </tr>
    </tbody>
</table>
</p>

---

### releaseObjectGroup
Освобождает все удаленные объекты, которые принадлежат данной группе.

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
            <td>objectGroup</td>
            <td><code class="flyout">string</code></td>
            <td>Имя группы символьных объектов. </td>
        </tr>
    </tbody>
</table>
</p>

---

### discardConsoleEntries
Отмена собранных исключений и вызовов API консоли.

</p>

---

## Мероприятия

### executionContextCreated
Выдается при создании нового контекста выполнения.

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
            <td>context</td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td>Вновь созданный контекст выполнения.</td>
        </tr>
    </tbody>
</table>
</p>

---

### executionContextDestroyed
Выдается при удалении контекста выполнения.

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
            <td>executionContextId</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Идентификатор разрушенного контекста</td>
        </tr>
    </tbody>
</table>
</p>

---

### executionContextsCleared
Выдается, когда все executionContexts были очищены в браузере

</p>

---

### exceptionThrown
Выдается, когда возникло исключение и оно не обрабатывается.

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
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Метка времени исключения.</td>
        </tr>
        <tr>
            <td>exceptionDetails</td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### consoleAPICalled


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
            <td>Тип</td>
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: log, info, предупреждение, ошибка, отладка, тип, таблица, трассировка, dir, DirXML, Clear, выбор, подсчет, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</i></td>
            <td>Тип звонка. Сюда входят журналы, сведения, предупреждение, ошибка, отладка, подсказка, таблица, трассировка, dir, DirXML, очистить, выбрать, счёт, countReset, timeEnd, исключение, метка времени, группа, сообщение, отметку и groupEnd.</td>
        </tr>
        <tr>
            <td>аргументы</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td>Аргументы вызова.</td>
        </tr>
        <tr>
            <td>executionContextId</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Идентификатор контекста, в котором сделан вызов консоли</td>
        </tr>
        <tr>
            <td>штамп <br/> <i>необязательные</i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Отметка времени вызова.</td>
        </tr>
        <tr>
            <td>Стек <br/> <i>необязательные</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Трассировка стека, записанная, если она доступна</td>
        </tr>
    </tbody>
</table>
</p>

---

## Типы

### <a name="scriptid"></a> ScriptId `string`

Уникальный идентификатор сценария.

</p>

---

### <a name="remoteobjectid"></a> RemoteObjectId `string`

Уникальный идентификатор объекта.

</p>

---

### <a name="unserializablevalue"></a> UnserializableValue `string`

Примитивное значение, которое не может быть JSON-stringified.

##### Допустимые значения
Бесконечность, NaN,-Infinity,-0
</p>

---

### <a name="remoteobject"></a> RemoteObject `object`

Зеркальный объект, который ссылается на исходный объект JavaScript.

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
            <td>Тип</td>
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: Object, Function, undefine, String, число, логический, символ</i></td>
            <td>Тип объекта.</td>
        </tr>
        <tr>
            <td>Подтип <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: NULL, Error, Promise, Node</i></td>
            <td>Подсказка подтипа объекта. Задается <code>object</code> только для значений типа.</td>
        </tr>
        <tr>
            <td>className <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Имя класса объекта (конструктор). Задается <code>object</code> только для значений типа.</td>
        </tr>
        <tr>
            <td>value <br/> <i>необязательные</i></td>
            <td><code class="flyout">any</code></td>
            <td>Значение удаленного объекта в случае примитивных значений или значений JSON (если оно было запрошено).</td>
        </tr>
        <tr>
            <td>unserializableValue <br/> <i>необязательные</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Примитивное значение, которое не может быть JSON-stringified, не имеет <code>value</code>, но получает это свойство.</td>
        </tr>
        <tr>
            <td>description <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Строковое представление объекта.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Уникальный идентификатор объекта (для значений, не являющихся примитивами).</td>
        </tr>
        <tr>
            <td>msDebuggerPropertyId <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Проб. </b></span>Microsoft: соответствующий идентификатор свойства отладчика для этого объекта.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> PropertyDescriptor `object`

Дескриптор свойства объекта.

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
            <td>Описание свойства или символа.</td>
        </tr>
        <tr>
            <td>value <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Значение, связанное со свойством.</td>
        </tr>
        <tr>
            <td>доступных <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Значение true, если значение, связанное со свойством, может быть изменено (только дескрипторы данных).</td>
        </tr>
        <tr>
            <td>получить <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Функция, которая служит в качестве метода доступа к свойству или не <code>undefined</code> содержит дескрипторов методов доступа get ().</td>
        </tr>
        <tr>
            <td>set <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Функция, которая используется в качестве Setter для свойства, или если отсутствует <code>undefined</code> Метод Setter (только дескрипторы методов доступа).</td>
        </tr>
        <tr>
            <td>настраиваемые</td>
            <td><code class="flyout">boolean</code></td>
            <td>Значение true, если тип дескриптора свойства может изменяться, и если свойство может быть удалено из соответствующего объекта.</td>
        </tr>
        <tr>
            <td>Перечислим</td>
            <td><code class="flyout">boolean</code></td>
            <td>Значение true, если это свойство появляется при перечислении свойств соответствующего объекта.</td>
        </tr>
        <tr>
            <td>wasThrown <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Значение true, если результат был сгенерирован во время оценки.</td>
        </tr>
        <tr>
            <td>isOwn <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Значение true, если свойство принадлежит объекту.</td>
        </tr>
        <tr>
            <td>msReturnValue <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Проб. </b></span>Microsoft: значение true, если свойство является возвращаемым значением.</td>
        </tr>
        <tr>
            <td>Символ <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Объект символа свойства, если свойство имеет `symbol` тип. </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> CallArgument `object`

Представляет аргумент вызова функции. Идентификатор удаленного объекта <code>objectId</code> , примитивный <code>value</code> , несериализуемый примитивный или ни один из них (для неопределенного значения).

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
            <td>value <br/> <i>необязательные</i></td>
            <td><code class="flyout">any</code></td>
            <td>Примитивное значение или сериализуемый объект JavaScript.</td>
        </tr>
        <tr>
            <td>unserializableValue <br/> <i>необязательные</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Примитивное значение, которое не может быть JSON-stringified.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Удаленный объектный обработчик.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> ExecutionContextId `integer`

Идентификатор контекста выполнения.

</p>

---

### <a name="executioncontextdescription"></a> ExecutionContextDescription `object`

Описание изолированного мира.

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
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Уникальный идентификатор контекста выполнения. Его можно использовать, чтобы указать, в какой контекст выполнения следует выполнять оценку сценария.</td>
        </tr>
        <tr>
            <td>исходных</td>
            <td><code class="flyout">string</code></td>
            <td>Источник контекста выполнения.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Понятное имя, описывающее данный контекст.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> ExceptionDetails `object`

Подробные сведения об исключении (или ошибке), выброшенных при компиляции или выполнении сценария.

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
            <td>exceptionId</td>
            <td><code class="flyout">integer</code></td>
            <td>Идентификатор исключения.</td>
        </tr>
        <tr>
            <td>текст</td>
            <td><code class="flyout">string</code></td>
            <td>Текст исключения, который должен использоваться вместе с объектом Exception, если он доступен.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки в местоположении исключения (на основе 0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер столбца в расположении исключения (на основе 0).</td>
        </tr>
        <tr>
            <td>scriptId <br/> <i>необязательные</i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>Идентификатор сценария расположения исключения.</td>
        </tr>
        <tr>
            <td>url <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес расположения исключения, которое будет использоваться, когда сценарий не был передан.</td>
        </tr>
        <tr>
            <td>Стек <br/> <i>необязательные</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Трассировка стека JavaScript (если она доступна).</td>
        </tr>
        <tr>
            <td>Ошибка <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Объект Exception, если он доступен.</td>
        </tr>
        <tr>
            <td>executionContextId <br/> <i>необязательные</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Идентификатор контекста, в котором произошло исключение.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> Метка времени `integer`

Количество миллисекунд, прошедшее с момента создания эпохи.

</p>

---

### <a name="callframe"></a> CallFrame `object`

Запись в стек для ошибок и утверждений во время выполнения.

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
            <td>functionName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя функции JavaScript.</td>
        </tr>
        <tr>
            <td>scriptId</td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>Идентификатор сценария JavaScript. Если отладчик не включен, ScriptId будет пустым.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Имя сценария JavaScript или URL-адрес.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки сценария JavaScript (на основе 0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер столбца сценария JavaScript (на основе 0).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> Стек `object`

Вызывайте кадры для утверждений и сообщений об ошибках.

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
            <td>description <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Метка строки для этой трассировки стека. Для асинхронных трассировок это может быть название функции, которая инициировала асинхронный вызов.</td>
        </tr>
        <tr>
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Имя функции JavaScript.</td>
        </tr>
        <tr>
            <td>родитель <br/> <i>необязательные</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Асинхронная трассировка стека JavaScript, предшествующая данному стеку (если она доступна).</td>
        </tr>
    </tbody>
</table>
</p>

---

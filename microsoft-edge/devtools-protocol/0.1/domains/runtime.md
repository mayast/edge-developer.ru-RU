---
description: Справочник по домену среды выполнения. Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов. Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не были явно освобождены.
title: Домен среды выполнения — протокол DevTools версии 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 33bc98b272aaa8831e908207b97ea7d3d0842976
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571689"
---
# Язык
Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов. Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не были явно освобождены.

| | |
|-|-|
| [**Методы**](#methods) | [Включение](#enable), [Отключение](#disable), [Оценка](#evaluate), [callFunctionOn](#callfunctionon), [Свойства](#getproperties) |
| [**События**](#events) | [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown) |
| [**Типы**](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Метка времени](#timestamp) [, CallFrame,](#callframe) [StackTrace](#stacktrace) |
## Методы

### "Включить"
Включает создание отчетов о <code>executionContextsCleared</code> событии.


---

### "Отключить" 
Отключение отчета о <code>executionContextsCleared</code> событии.


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
            <td>Идентификатор объекта, свойства которого нужно вернуть.  objectId должен быть из функции Debugger. evaluateOnCallFrame ().</td>
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

---

## События

### executionContextsCleared
Выдается, когда все executionContexts были очищены в браузере


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

---

## Типы

### <a name="scriptid"></a> ScriptId `string`

Уникальный идентификатор сценария.


---

### <a name="remoteobjectid"></a> RemoteObjectId `string`

Уникальный идентификатор объекта.


---

### <a name="unserializablevalue"></a> UnserializableValue `string`

Примитивное значение, которое не может быть JSON-stringified.

##### Допустимые значения
Бесконечность, NaN,-Infinity,-0

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
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: NULL, ошибка, обещание</i></td>
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

---

### <a name="executioncontextid"></a> ExecutionContextId `integer`

Идентификатор контекста выполнения.


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

---

### <a name="timestamp"></a> Метка времени `integer`

Количество миллисекунд, прошедшее с момента создания эпохи.


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
            <td>Идентификатор сценария JavaScript.</td>
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

---

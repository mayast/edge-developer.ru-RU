---
description: Ссылка на домен отладчика. Домен отладчика предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки останова, пошаговое выполнение, изменяя трассировку стека и т. д.
title: Debugger Domain-DevTools Protocol версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: de967b0e067bf43ea07f8975eac7ee7c5a4dfd83
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571678"
---
# Отладчика
Домен отладчика предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки останова, пошаговое выполнение, изменяя трассировку стека и т. д.

| | |
|-|-|
| [**Методы**](#methods) | [включить](#enable), [Отключить](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [steping](#stepout), [Pause](#pause), [Resume](#resume), [getScriptSource, setPauseOnExceptions](#getscriptsource) [, evaluateOnCallFrame](#setpauseonexceptions), [setVariableValue](#setvariablevalue) [setVariableValue](#evaluateoncallframe) [setBlackboxPatterns](#setblackboxpatterns) [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |
| [**События**](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [приостановлено](#paused), [возобновлено](#resumed) |
| [**Типы**](#types) | [BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [область](#scope) |
| [**Зависимости**](#dependencies) | [Язык](runtime.md) |
## Методы

### "Включить"
Включает отладчик для заданной страницы. Клиенты не должны предполагать, что отладка включена, пока не будет получен результат этой команды.

</p>

---

### "Отключить" 
Отключает отладчик для данной страницы.

</p>

---

### getPossibleBreakpoints
Возвращает возможные расположения для точки останова. scriptId в начальном и конечном диапазонах должны быть одинаковыми.

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
            <td>start</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Начало диапазона для поиска возможных местоположений точки останова в.</td>
        </tr>
        <tr>
            <td>завершить</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Конец диапазона для поиска возможных местоположений точки останова в (исключая). Если не указано, конец сценариев используется как конец диапазона.</td>
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
            <td>ячейк</td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td>Список возможных местоположений точки останова.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpointsActive
Активирует и деактивирует все точки останова на странице.

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
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Новое значение для точек останова в активном состоянии.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpointByUrl
Задает точку останова JavaScript в указанном расположении с помощью URL-адреса или регулярного URL-адреса. После того как вы выпустили эту команду, для всех существующих проанализированных сценариев будут заданы точки останова и они возвращаются в <code>locations</code> свойство. После синтаксического анализа сценария сопоставления будут <code>breakpointResolved</code> выданы последующие события. Эта логическая точка останова будет содержаться в повторной загрузке страницы.

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
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки, в которой нужно установить точку останова.</td>
        </tr>
        <tr>
            <td>url <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес ресурсов, для которых нужно установить точку останова.</td>
        </tr>
        <tr>
            <td>urlRegex <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Шаблон Regex для URL-адресов ресурсов, для которых нужно установить точки останова. Либо <code>url</code> <code>urlRegex</code> должен быть указан.</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Смещение в строке для задания точки останова в.</td>
        </tr>
        <tr>
            <td>постусловия <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Выражение, используемое в качестве условия для точки останова. Если указан, отладчик будет остановлен только в точке останова, если это выражение имеет значение true.</td>
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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Идентификатор созданной точки останова для дальнейшей ссылки.</td>
        </tr>
        <tr>
            <td>ячейк</td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td>Список местоположений, разрешенных этой точкой останова, на момент добавления.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpoint
Задает точку останова JavaScript в указанном месте.

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
            <td>поиска</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Расположение, в котором нужно установить точку останова.</td>
        </tr>
        <tr>
            <td>постусловия <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Выражение, используемое в качестве условия для точки останова. Если указан, отладчик будет остановлен только в точке останова, если это выражение имеет значение true.</td>
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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Идентификатор созданной точки останова для дальнейшей ссылки.</td>
        </tr>
        <tr>
            <td>actualLocation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Расположение, в которое разрешена точка останова.</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeBreakpoint
Удаляет точку останова JavaScript.

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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### stepOver
Пошаговые инструкции.

</p>

---

### stepInto
Пошаговые инструкции в вызов функции.

</p>

---

### Пошаговое руководство
Пошаговые инструкции по вызову функции.

</p>

---

### pause
Останавливается на следующей инструкции JavaScript.

</p>

---

### resume
Возобновляет выполнение JavaScript.

</p>

---

### getScriptSource
Возвращает источник для сценария с заданным идентификатором.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Идентификатор сценария, для которого требуется получить источник.</td>
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
            <td>scriptSource</td>
            <td><code class="flyout">string</code></td>
            <td>Источник сценария.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setPauseOnExceptions
Определяет состояние Pause on Exceptions. Может быть настроено на остановку для всех исключений, неперехваченных исключений или исключений. Состояние начальной паузы в состоянии исключений <code>none</code> .

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
            <td>состояни</td>
            <td><code class="flyout">string</code> <br/> <i>Разрешенные значения: нет, не перехвачено, все</i></td>
            <td>Пауза в режиме исключений.</td>
        </tr>
    </tbody>
</table>
</p>

---

### evaluateOnCallFrame
Вычисляет выражение для данного кадра вызова.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Идентификатор кадра звонка, который нужно вычислить.</td>
        </tr>
        <tr>
            <td>выражение</td>
            <td><code class="flyout">string</code></td>
            <td>Выражение для вычисления.</td>
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
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Обертка объекта для результата вычисления.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setVariableValue
Изменяет значение переменной в callframe. Области, основанные на объектах, не поддерживаются и должны изменяться вручную.

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
            <td>scopeNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>число областей на основе 0, указанное в цепочке диапазонов. Разрешены только типы областей "локальный", "замыкание" и "Catch". Другие области можно манипулировать вручную.</td>
        </tr>
        <tr>
            <td>variableName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя переменной.</td>
        </tr>
        <tr>
            <td>newValue</td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td>Новое значение переменной.</td>
        </tr>
        <tr>
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Идентификатор callframe, который содержит переменную.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBlackboxPatterns
<span><b>Проб. </b></span>Замена предыдущих шаблонов BlackBox на прошедшие. Заставляет сервер пропускать пошаговое выполнение или приостановку в сценариях с URL-адресом, совпадающим с одним из шаблонов. Отладчик попытается покинуть сценарий blackboxed, выполнив несколько раз подряд, и, наконец, перейдет к элементу "шаг с выходом", если неудачно.

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
            <td>структуру</td>
            <td><code class="flyout">string[]</code></td>
            <td>Массив regexps, который будет использоваться для проверки URL-адреса сценария для состояния BlackBox.</td>
        </tr>
    </tbody>
</table>
</p>

---

### msSetDebuggerPropertyValue
<span><b>Проб. </b></span>Microsoft: задает для указанного свойства отладчика указанное значение.

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
            <td>debuggerPropertyId</td>
            <td><code class="flyout">string</code></td>
            <td>Microsoft: заданный идентификатор свойства (например, msDebuggerPropertyId).</td>
        </tr>
        <tr>
            <td>newValue</td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

## События

### scriptParsed
Возникает при синтаксическом анализе сценария. Это событие также срабатывает для всех известных и несобранных сценариев при включенном отладчике.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Идентификатор синтаксического анализа сценария.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес или имя синтаксического анализа сценария (если есть).</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Смещение строки сценария в ресурсе с указанным URL-адресом (для тегов сценария).</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Смещение столбца сценария в ресурсе с указанным URL-адресом.</td>
        </tr>
        <tr>
            <td>endLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Последняя строка сценария.</td>
        </tr>
        <tr>
            <td>endColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Длина последней строки сценария.</td>
        </tr>
        <tr>
            <td>executionContextId</td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td>Задает контекст создания сценария.</td>
        </tr>
        <tr>
            <td>sourceMapURL <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес карты источника, связанной со сценарием (если есть).</td>
        </tr>
        <tr>
            <td>Длина <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Проб. </b></span>Длина сценария.</td>
        </tr>
        <tr>
            <td>msParentId <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Проб. </b></span>Это идентификатор родительского документа.</td>
        </tr>
        <tr>
            <td>msMimeType <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Проб. </b></span>Это тип MIME.</td>
        </tr>
        <tr>
            <td>msIsDynamicCode <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Проб. </b></span>Это указывает на то, является ли этот динамический код.</td>
        </tr>
        <tr>
            <td>msLongDocumentId <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Проб. </b></span>Это длинный идентификатор документа.</td>
        </tr>
    </tbody>
</table>
</p>

---

### breakpointResolved
Срабатывает при разрешении точки останова для фактического сценария и местоположения.

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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Уникальный идентификатор точки останова.</td>
        </tr>
        <tr>
            <td>поиска</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Место фактического местоположения точки останова.</td>
        </tr>
        <tr>
            <td>msLength <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Проб. </b></span>Microsoft: длина кода (например, число знаков) в месте точки останова.</td>
        </tr>
    </tbody>
</table>
</p>

---

### пауза
Возникает, когда отладчикы прерываются для точки останова или исключения.

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
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Стек вызовов, для которого остановлен отладчик.</td>
        </tr>
        <tr>
            <td>оправдан</td>
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: точка останова, шаг, исключение, другое, EventListener</i></td>
            <td>Причина приостановки.</td>
        </tr>
        <tr>
            <td>data <br/> <i>необязательные</i></td>
            <td><code class="flyout">object</code></td>
            <td>Объект, содержащий специфичные для разрыва дополнительные свойства.</td>
        </tr>
        <tr>
            <td>hitBreakpoints <br/> <i>необязательные</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Идентификаторы точек останова</td>
        </tr>
        <tr>
            <td>asyncStackTrace <br/> <i>необязательные</i></td>
            <td><!--  <a href="#stacktrace">  --><code class="flyout">StackTrace</code><!--  </a>  --></td>
            <td>Асинхронная трассировка стека JavaScript.</td>
        </tr>
    </tbody>
</table>
</p>

---

### возобновляется
Возникает, когда отладчик возобновляет выполнение.

</p>

---

## Типы

### <a name="breakpointid"></a> BreakpointId `string`

Идентификатор точки останова.

</p>

---

### <a name="callframeid"></a> CallFrameId `string`

Идентификатор кадра звонка.

</p>

---

### <a name="location"></a> Местоположение `object`

Расположение в исходном коде.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Идентификатор сценария, указанный в <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки в сценарии (от 0 до 1).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Номер столбца в сценарии (от 0 до 1).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: длина кода (например, число символов) в этом кадре звонка.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="breaklocation"></a> BreakLocation `object`

Разрыв места в исходном коде.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Идентификатор сценария, указанный в <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки в сценарии (от 0 до 1).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Номер столбца в сценарии (от 0 до 1).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: длина кода (например, число символов) в этом кадре звонка.</td>
        </tr>
        <tr>
            <td>Тип <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Допустимые значения: debuggerStatement, Call, Return.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callframe"></a> CallFrame `object`

Кадр звонка JavaScript. Массив кадров звонка, вызываемый из стека вызовов.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Идентификатор кадра звонка. Этот идентификатор действителен только в том случае, если отладчик приостановлен.</td>
        </tr>
        <tr>
            <td>functionName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя функции JavaScript, вызываемой в этом кадре звонка.</td>
        </tr>
        <tr>
            <td>functionLocation <br/> <i>необязательные</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b>Проб. </b></span>Расположение в исходном коде.</td>
        </tr>
        <tr>
            <td>поиска</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Расположение в исходном коде.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Имя сценария JavaScript или URL-адрес.</td>
        </tr>
        <tr>
            <td>scopeChain</td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td>Цепочка диапазонов для этого кадра звонка.</td>
        </tr>
        <tr>
            <td>этой</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> объект для этого кадра звонка.</td>
        </tr>
        <tr>
            <td>Возвращен <br/> <i>необязательные</i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Возвращаемое значение, если функция находится на точке возврата.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="scope"></a> Область применения `object`

Описание области.

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
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: Global, Local, with, замыкание, catch, Block, Script, eval, Module, Return</i></td>
            <td>Тип области.</td>
        </tr>
        <tr>
            <td>объект</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Объект, представляющий область. Для <code>global</code> и <code>with</code> областей представляет фактический объект; для остальных областей это искусственный несохраняемый объект, перечисление переменных области в качестве свойств.</td>
        </tr>
        <tr>
            <td>name <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td>startLocation <br/> <i>необязательные</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Место в исходном коде, с которого начинается область</td>
        </tr>
        <tr>
            <td>endLocation <br/> <i>необязательные</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Место в исходном коде, где заканчивается область</td>
        </tr>
    </tbody>
</table>
</p>

---

## Зависимости

[Язык](runtime.md)

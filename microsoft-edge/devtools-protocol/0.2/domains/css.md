---
description: Ссылка на домен CSS. Этот домен предоставляет доступ к операциям чтения и записи в CSS. Все объекты CSS (таблицы стилей, правила и стили) связаны с помощью `id` последующих операций связанного объекта. Каждый тип объекта имеет определенную `id` структуру, и они не взаимозаменяемы между объектами разных типов. Объекты CSS можно загрузить с помощью `get*ForNode()` вызовов (которые допускают идентификатор узла DOM). Кроме того, клиент может следить за таблицами стилей с помощью `styleSheetAdded` / `styleSheetRemoved` событий, а затем загружать нужное содержимое таблицы стилей, используя эти `getStyleSheet[Text]()` методы.
title: Домен CSS — протокол DevTools версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 939eda0ae2f5228657d35899ab75b39493eff917
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571679"
---
# CSS
Этот домен предоставляет доступ к операциям чтения и записи в CSS. Все объекты CSS (таблицы стилей, правила и стили) связаны с помощью `id` последующих операций связанного объекта. Каждый тип объекта имеет определенную `id` структуру, и они не взаимозаменяемы между объектами разных типов. Объекты CSS можно загрузить с помощью `get*ForNode()` вызовов (которые допускают идентификатор узла DOM). Кроме того, клиент может следить за таблицами стилей с помощью `styleSheetAdded` / `styleSheetRemoved` событий, а затем загружать нужное содержимое таблицы стилей, используя эти `getStyleSheet[Text]()` методы.

| | |
|-|-|
| [**Методы**](#methods) | [Включение](#enable), [Отключение](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode) |
| [**События**](#events) | [styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved) |
| [**Типы**](#types) | [StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry, CSSStyle](#shorthandentry) [,](#cssmedia) [,](#cssstyle) [, CSSProperty](#cssproperty)CSSMedia [MediaQueryExpression](#mediaqueryexpression), MediaQuery [PlatformFontUsage](#platformfontusage), MediaQueryExpression [CSSKeyframesRule](#csskeyframesrule) [MediaQuery](#mediaquery) [CSSKeyframeRule](#csskeyframerule) [CSSComputedStyleProperty](#csscomputedstyleproperty) [CSSStyleSheetHeader](#cssstylesheetheader) |
| [**Зависимости**](#dependencies) | [DOM](dom.md) |
## Методы

### "Включить"
Включает агент CSS для указанной страницы. Клиентам не следует предполагать, что агент CSS был активирован до тех пор, пока не будет получен результат этой команды.

</p>

---

### "Отключить" 
Отключение агента CSS для заданной страницы.

</p>

---

### getInlineStylesForNode
Возвращает стили, определенные в тексте (явно в атрибуте Style, и неявно, с помощью атрибутов DOM) для узла DOM, идентифицированного `nodeId` .

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
            <td></td>
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
            <td>inlineStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Встроенный стиль для указанного узла DOM.</td>
        </tr>
        <tr>
            <td>attributesStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Стиль элемента, определяемый атрибутом (например, в результате "ширина = 20 высота = 100%").</td>
        </tr>
    </tbody>
</table>
</p>

---

### getMatchedStylesForNode
Возвращает запрашиваемые стили для узла DOM, указанного в `nodeId` .

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
            <td></td>
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
            <td>inlineStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Встроенный стиль для указанного узла DOM.</td>
        </tr>
        <tr>
            <td>attributesStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Стиль элемента, определяемый атрибутом (например, в результате "ширина = 20 высота = 100%").</td>
        </tr>
        <tr>
            <td>matchedCSSRules <br /> <i>необязательные</i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Правила CSS, соответствующие этому узлу, из всех применимых стилей.</td>
        </tr>
        <tr>
            <td>pseudoElements <br /> <i>необязательные</i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td>Соответствия псевдо-стиля для этого узла.</td>
        </tr>
        <tr>
            <td>наследуются <br /> <i>необязательные</i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td>Цепочка унаследованных стилей (от родительского узла непосредственно до корневого элемента дерева DOM).</td>
        </tr>
        <tr>
            <td>cssKeyframesRules <br /> <i>необязательные</i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td>Список анимаций с ключевыми кадрами CSS, соответствующих данному узлу.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getPlatformFontsForNode
Запрашивает сведения о шрифтах платформы, которые мы использовали для отрисовки дочерних TextNodes в данном узле.

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
            <td></td>
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
            <td>выбранные</td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td>Статистика использования для каждого используемого шрифта платформы.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getComputedStyleForNode
Возвращает вычисленный стиль для узла DOM, определенного `nodeId` .

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
            <td></td>
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
            <td>computedStyle</td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td>Вычисляемый стиль для указанного узла DOM.</td>
        </tr>
    </tbody>
</table>
</p>

---

## События

### styleSheetAdded
Срабатывает каждый раз, когда добавляется активная таблица стилей документов.

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
            <td>header</td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td>Добавлены метаданные таблицы стилей.</td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetChanged
Возникает при изменении таблицы стилей в результате операции клиента.

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
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetRemoved
Срабатывает каждый раз, когда удаляется активная таблица стилей документов.

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
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор удаленной таблицы стилей.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Типы

### <a name="stylesheetid"></a> StyleSheetId `string`



</p>

---

### <a name="pseudoelementmatches"></a> PseudoElementMatches `object`

Коллекция правил CSS для одного псевдо-стиля.

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
            <td>pseudoType</td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td>Тип псевдослучайных элементов.</td>
        </tr>
        <tr>
            <td>соответствует</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Соответствующие правила CSS, применимые к псевдо.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> InheritedStyleEntry `object`

Наследуемая коллекция правил CSS из узла-предка.

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
            <td>inlineStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Встроенный стиль родительского узла (если таковой имеется) в цепочке наследования стилей.</td>
        </tr>
        <tr>
            <td>matchedCSSRules</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Соответствие правил CSS, соответствующих узлу-предку в цепочке наследования стилей.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> RuleMatch `object`

Сопоставление данных для правила CSS.

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
            <td>условия</td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td>Правило CSS в сопоставлении.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> Значение `object`

Данные для простого селектора (они разделяются запятыми в списке Selector).

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
            <td>текст</td>
            <td><code class="flyout">string</code></td>
            <td>Текст значения.</td>
        </tr>
        <tr>
            <td>действия <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Диапазон значений в основном ресурсе (если он доступен).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> SelectorList `object`

Данные списка Selector.

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
            <td>селекторов</td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td>Выберите элемент в списке.</td>
        </tr>
        <tr>
            <td>текст</td>
            <td><code class="flyout">string</code></td>
            <td>Текст селектора правил.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> CSSRule `object`

Представление правила CSS.

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
            <td>styleSheetId <br /> <i>необязательные</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей CSS (отсутствует для таблицы пользовательского агента и правил для таблиц, указанных пользователем) это правило получено.</td>
        </tr>
        <tr>
            <td>selectorList <br /> <i>необязательные</i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td>Данные селектора правила.</td>
        </tr>
        <tr>
            <td>исходных <br /> <i>необязательные</i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Источник родительской таблицы.</td>
        </tr>
        <tr>
            <td>стиль</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Связанное объявление стиля.</td>
        </tr>
        <tr>
            <td>мультимедиа <br /> <i>необязательные</i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td>Массив списка мультимедиа (для правил, включающих мультимедийные запросы). Массив перечисление запросов мультимедиа, начиная с самого внутреннего, и заканчивая его.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> SourceRange `object`

Диапазон текста в ресурсе. Все номера отсчитываются от нуля.

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
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Начало строки диапазона.</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Начальный столбец диапазона (включительно).</td>
        </tr>
        <tr>
            <td>endLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Конец строки диапазона</td>
        </tr>
        <tr>
            <td>endColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Конечный столбец диапазона (за исключением).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> ShorthandEntry `object`



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
            <td>Сокращенное имя.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Сокращенное значение.</td>
        </tr>
        <tr>
            <td>роли <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Имеет ли свойство заметку "! важно" (подразумевается `false` , что она отсутствует).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> CSSStyle `object`

Представление стиля CSS.

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
            <td>styleSheetId <br /> <i>необязательные</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей CSS (отсутствует для таблицы пользовательского агента и правил для таблиц, указанных пользователем) это правило получено.</td>
        </tr>
        <tr>
            <td>cssProperties</td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td>Свойства CSS в стиле.</td>
        </tr>
        <tr>
            <td>shorthandEntries</td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td>Вычисляемые значения для всех сокращений, обнаруженных в стиле.</td>
        </tr>
        <tr>
            <td>cssText <br /> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Текст объявления стиля (если он доступен).</td>
        </tr>
        <tr>
            <td>действия <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Диапазон объявлений стиля во вложенной таблице стилей (если она доступна).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> CSSProperty `object`

Данные объявления свойств CSS.

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
            <td>Имя свойства.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Значение свойства.</td>
        </tr>
        <tr>
            <td>роли <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Имеет ли свойство заметку "! важно" (подразумевается `false` , что она отсутствует).</td>
        </tr>
        <tr>
            <td>согласия <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Является ли свойство неявным (подразумевается, `false` если оно отсутствует).</td>
        </tr>
        <tr>
            <td>текст <br /> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Полный текст свойства, указанный в стиле.</td>
        </tr>
        <tr>
            <td>parsedOk <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Понимается ли свойство браузером (подразумевается, `true` если оно отсутствует).</td>
        </tr>
        <tr>
            <td>отключает <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Отключено ли свойство пользователем (доступно только для свойств на основе исходного кода).</td>
        </tr>
        <tr>
            <td>действия <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Весь диапазон свойств во вложенном объявлении стиля (если он доступен).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> CSSMedia `object`

Дескриптор правила мультимедиа CSS.

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
            <td>текст</td>
            <td><code class="flyout">string</code></td>
            <td>Текст запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>исходный</td>
            <td><code class="flyout">string</code> <br /> <i>Разрешенные значения: mediaRule, importRule, linkedSheet, inlineSheet</i></td>
            <td>Источник запроса мультимедиа: "mediaRule", если он указан в правиле @media, "importRule", если задано правилом @import, "linkedSheet", если он указан с помощью атрибута "Media" в теге ссылки связанной таблицы стилей, "inlineSheet", если он указан с помощью атрибута "мультимедиа", заданное атрибутом "медиа" в теге стиля встроенной таблицы стилей.</td>
        </tr>
        <tr>
            <td>sourceURL <br /> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес документа, содержащего описание запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>действия <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Диапазон заголовков связанного правила (@media или @import) во вложенной таблице стилей (если она доступна).</td>
        </tr>
        <tr>
            <td>styleSheetId <br /> <i>необязательные</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей, содержащей этот объект (если существует).</td>
        </tr>
        <tr>
            <td>mediaList <br /> <i>необязательные</i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td>Массив мультимедийных запросов.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> MediaQuery `object`

Дескриптор запроса мультимедиа.

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
            <td>многомер</td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td>Массив выражений с запросом мультимедиа.</td>
        </tr>
        <tr>
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Удовлетворено ли условие запроса мультимедиа.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> MediaQueryExpression `object`

Дескриптор выражения для запроса мультимедиа.

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
            <td>value</td>
            <td><code class="flyout">number</code></td>
            <td>Значение выражения для запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>единич</td>
            <td><code class="flyout">string</code></td>
            <td>Единицы выражения запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>функция</td>
            <td><code class="flyout">string</code></td>
            <td>Функция выражения для запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>valueRange <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Связанный диапазон текста значения в включающей таблице стилей (если она доступна).</td>
        </tr>
        <tr>
            <td>computedLength <br /> <i>необязательные</i></td>
            <td><code class="flyout">number</code></td>
            <td>Вычисленная длина выражения запроса мультимедиа (если применимо).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> PlatformFontUsage `object`

Сведения о количестве глифов, отображаемых с использованием заданного шрифта.

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
            <td>familyName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя семейства шрифтов, указанное платформой.</td>
        </tr>
        <tr>
            <td>isCustomFont</td>
            <td><code class="flyout">boolean</code></td>
            <td>Указывает, был ли этот шрифт скачан или разрешается локально.</td>
        </tr>
        <tr>
            <td>glyphCount</td>
            <td><code class="flyout">number</code></td>
            <td>Количество глифов, обработанных с помощью этого шрифта.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> CSSKeyframesRule `object`

Представление правила "ключевые кадры CSS".

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
            <td>animationName</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Имя анимации.</td>
        </tr>
        <tr>
            <td>Ключевые кадры</td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td>Список ключевых кадров.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> CSSKeyframeRule `object`

Представление правила для ключевого кадра CSS.

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
            <td>styleSheetId <br /> <i>необязательные</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей CSS (отсутствует для таблицы пользовательского агента и правил для таблиц, указанных пользователем) это правило получено.</td>
        </tr>
        <tr>
            <td>исходных</td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Источник родительской таблицы.</td>
        </tr>
        <tr>
            <td>keyText</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Текст соответствующего ключа.</td>
        </tr>
        <tr>
            <td>стиль</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Связанное объявление стиля.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> CSSComputedStyleProperty `object`



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
            <td>Имя свойства вычисляемого стиля.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Значение свойства "вычисляемый стиль".</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> CSSStyleSheetHeader `object`

Таблица стилей CSS Metainformation.

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
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей.</td>
        </tr>
        <tr>
            <td>sourceURL</td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес ресурса таблицы стилей.</td>
        </tr>
        <tr>
            <td>отключает</td>
            <td><code class="flyout">boolean</code></td>
            <td>Указывает, отключена ли таблица стилей.</td>
        </tr>
        <tr>
            <td>isInline</td>
            <td><code class="flyout">boolean</code></td>
            <td>Создана ли эта таблица стилей для тега STYLE с помощью средства синтаксического анализа. Этот флаг не установлен для тегов Document. письменного стиля.</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">number</code></td>
            <td>Смещение строки таблицы стилей в пределах ресурса (с отсчетом от нуля).</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">number</code></td>
            <td>Смещение столбца в таблице стилей в рамках ресурса (с отсчетом от нуля).</td>
        </tr>
        <tr>
            <td>Длина</td>
            <td><code class="flyout">number</code></td>
            <td>Размер содержимого (в символах).</td>
        </tr>
    </tbody>
</table>
</p>

---

## Зависимости

[DOM](dom.md)

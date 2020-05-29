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
# <span data-ttu-id="fea8c-108">CSS</span><span class="sxs-lookup"><span data-stu-id="fea8c-108">CSS</span></span>
<span data-ttu-id="fea8c-109">Этот домен предоставляет доступ к операциям чтения и записи в CSS.</span><span class="sxs-lookup"><span data-stu-id="fea8c-109">This domain exposes CSS read/write operations.</span></span> <span data-ttu-id="fea8c-110">Все объекты CSS (таблицы стилей, правила и стили) связаны с помощью `id` последующих операций связанного объекта.</span><span class="sxs-lookup"><span data-stu-id="fea8c-110">All CSS objects (stylesheets, rules, and styles) have an associated `id` used in subsequent operations on the related object.</span></span> <span data-ttu-id="fea8c-111">Каждый тип объекта имеет определенную `id` структуру, и они не взаимозаменяемы между объектами разных типов.</span><span class="sxs-lookup"><span data-stu-id="fea8c-111">Each object type has a specific `id` structure, and those are not interchangeable between objects of different kinds.</span></span> <span data-ttu-id="fea8c-112">Объекты CSS можно загрузить с помощью `get*ForNode()` вызовов (которые допускают идентификатор узла DOM).</span><span class="sxs-lookup"><span data-stu-id="fea8c-112">CSS objects can be loaded using the `get*ForNode()` calls (which accept a DOM node id).</span></span> <span data-ttu-id="fea8c-113">Кроме того, клиент может следить за таблицами стилей с помощью `styleSheetAdded` / `styleSheetRemoved` событий, а затем загружать нужное содержимое таблицы стилей, используя эти `getStyleSheet[Text]()` методы.</span><span class="sxs-lookup"><span data-stu-id="fea8c-113">A client can also keep track of stylesheets via the `styleSheetAdded`/`styleSheetRemoved` events and subsequently load the required stylesheet contents using the `getStyleSheet[Text]()` methods.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="fea8c-114">Методы</span><span class="sxs-lookup"><span data-stu-id="fea8c-114">Methods</span></span>**](#methods) | <span data-ttu-id="fea8c-115">[Включение](#enable), [Отключение](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span><span class="sxs-lookup"><span data-stu-id="fea8c-115">[enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span></span> |
| [**<span data-ttu-id="fea8c-116">События</span><span class="sxs-lookup"><span data-stu-id="fea8c-116">Events</span></span>**](#events) | <span data-ttu-id="fea8c-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span><span class="sxs-lookup"><span data-stu-id="fea8c-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span></span> |
| [**<span data-ttu-id="fea8c-118">Типы</span><span class="sxs-lookup"><span data-stu-id="fea8c-118">Types</span></span>**](#types) | <span data-ttu-id="fea8c-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry, CSSStyle](#shorthandentry) [,](#cssmedia) [,](#cssstyle) [, CSSProperty](#cssproperty)CSSMedia [MediaQueryExpression](#mediaqueryexpression), MediaQuery [PlatformFontUsage](#platformfontusage), MediaQueryExpression [CSSKeyframesRule](#csskeyframesrule) [MediaQuery](#mediaquery) [CSSKeyframeRule](#csskeyframerule) [CSSComputedStyleProperty](#csscomputedstyleproperty) [CSSStyleSheetHeader](#cssstylesheetheader)</span><span class="sxs-lookup"><span data-stu-id="fea8c-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span></span> |
| [**<span data-ttu-id="fea8c-120">Зависимости</span><span class="sxs-lookup"><span data-stu-id="fea8c-120">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="fea8c-121">DOM</span><span class="sxs-lookup"><span data-stu-id="fea8c-121">DOM</span></span>](dom.md) |
## <span data-ttu-id="fea8c-122">Методы</span><span class="sxs-lookup"><span data-stu-id="fea8c-122">Methods</span></span>

### <span data-ttu-id="fea8c-123">"Включить"</span><span class="sxs-lookup"><span data-stu-id="fea8c-123">enable</span></span>
<span data-ttu-id="fea8c-124">Включает агент CSS для указанной страницы.</span><span class="sxs-lookup"><span data-stu-id="fea8c-124">Enables the CSS agent for the given page.</span></span> <span data-ttu-id="fea8c-125">Клиентам не следует предполагать, что агент CSS был активирован до тех пор, пока не будет получен результат этой команды.</span><span class="sxs-lookup"><span data-stu-id="fea8c-125">Clients should not assume that the CSS agent has been enabled until the result of this command is received.</span></span>

</p>

---

### <span data-ttu-id="fea8c-126">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="fea8c-126">disable</span></span>
<span data-ttu-id="fea8c-127">Отключение агента CSS для заданной страницы.</span><span class="sxs-lookup"><span data-stu-id="fea8c-127">Disables the CSS agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="fea8c-128">getInlineStylesForNode</span><span class="sxs-lookup"><span data-stu-id="fea8c-128">getInlineStylesForNode</span></span>
<span data-ttu-id="fea8c-129">Возвращает стили, определенные в тексте (явно в атрибуте Style, и неявно, с помощью атрибутов DOM) для узла DOM, идентифицированного `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="fea8c-129">Returns the styles defined inline (explicitly in the "style" attribute and implicitly, using DOM attributes) for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-130">Параметры</span><span class="sxs-lookup"><span data-stu-id="fea8c-130">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-131">nodeId</span><span class="sxs-lookup"><span data-stu-id="fea8c-131">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-132">Дает</span><span class="sxs-lookup"><span data-stu-id="fea8c-132">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-133">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="fea8c-133">inlineStyle</span></span> <br /> <i><span data-ttu-id="fea8c-134">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-134">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="fea8c-135">Встроенный стиль для указанного узла DOM.</span><span class="sxs-lookup"><span data-stu-id="fea8c-135">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-136">attributesStyle</span><span class="sxs-lookup"><span data-stu-id="fea8c-136">attributesStyle</span></span> <br /> <i><span data-ttu-id="fea8c-137">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-137">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="fea8c-138">Стиль элемента, определяемый атрибутом (например, в результате "ширина = 20 высота = 100%").</span><span class="sxs-lookup"><span data-stu-id="fea8c-138">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="fea8c-139">getMatchedStylesForNode</span><span class="sxs-lookup"><span data-stu-id="fea8c-139">getMatchedStylesForNode</span></span>
<span data-ttu-id="fea8c-140">Возвращает запрашиваемые стили для узла DOM, указанного в `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="fea8c-140">Returns requested styles for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-141">Параметры</span><span class="sxs-lookup"><span data-stu-id="fea8c-141">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-142">nodeId</span><span class="sxs-lookup"><span data-stu-id="fea8c-142">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-143">Дает</span><span class="sxs-lookup"><span data-stu-id="fea8c-143">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-144">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="fea8c-144">inlineStyle</span></span> <br /> <i><span data-ttu-id="fea8c-145">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-145">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="fea8c-146">Встроенный стиль для указанного узла DOM.</span><span class="sxs-lookup"><span data-stu-id="fea8c-146">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-147">attributesStyle</span><span class="sxs-lookup"><span data-stu-id="fea8c-147">attributesStyle</span></span> <br /> <i><span data-ttu-id="fea8c-148">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-148">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="fea8c-149">Стиль элемента, определяемый атрибутом (например, в результате "ширина = 20 высота = 100%").</span><span class="sxs-lookup"><span data-stu-id="fea8c-149">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-150">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="fea8c-150">matchedCSSRules</span></span> <br /> <i><span data-ttu-id="fea8c-151">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-151">optional</span></span></i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="fea8c-152">Правила CSS, соответствующие этому узлу, из всех применимых стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-152">CSS rules matching this node, from all applicable stylesheets.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-153">pseudoElements</span><span class="sxs-lookup"><span data-stu-id="fea8c-153">pseudoElements</span></span> <br /> <i><span data-ttu-id="fea8c-154">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-154">optional</span></span></i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td><span data-ttu-id="fea8c-155">Соответствия псевдо-стиля для этого узла.</span><span class="sxs-lookup"><span data-stu-id="fea8c-155">Pseudo style matches for this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-156">наследуются</span><span class="sxs-lookup"><span data-stu-id="fea8c-156">inherited</span></span> <br /> <i><span data-ttu-id="fea8c-157">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-157">optional</span></span></i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td><span data-ttu-id="fea8c-158">Цепочка унаследованных стилей (от родительского узла непосредственно до корневого элемента дерева DOM).</span><span class="sxs-lookup"><span data-stu-id="fea8c-158">A chain of inherited styles (from the immediate node parent up to the DOM tree root).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-159">cssKeyframesRules</span><span class="sxs-lookup"><span data-stu-id="fea8c-159">cssKeyframesRules</span></span> <br /> <i><span data-ttu-id="fea8c-160">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-160">optional</span></span></i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td><span data-ttu-id="fea8c-161">Список анимаций с ключевыми кадрами CSS, соответствующих данному узлу.</span><span class="sxs-lookup"><span data-stu-id="fea8c-161">A list of CSS keyframed animations matching this node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="fea8c-162">getPlatformFontsForNode</span><span class="sxs-lookup"><span data-stu-id="fea8c-162">getPlatformFontsForNode</span></span>
<span data-ttu-id="fea8c-163">Запрашивает сведения о шрифтах платформы, которые мы использовали для отрисовки дочерних TextNodes в данном узле.</span><span class="sxs-lookup"><span data-stu-id="fea8c-163">Requests information about platform fonts which we used to render child TextNodes in the given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-164">Параметры</span><span class="sxs-lookup"><span data-stu-id="fea8c-164">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-165">nodeId</span><span class="sxs-lookup"><span data-stu-id="fea8c-165">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-166">Дает</span><span class="sxs-lookup"><span data-stu-id="fea8c-166">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-167">выбранные</span><span class="sxs-lookup"><span data-stu-id="fea8c-167">fonts</span></span></td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td><span data-ttu-id="fea8c-168">Статистика использования для каждого используемого шрифта платформы.</span><span class="sxs-lookup"><span data-stu-id="fea8c-168">Usage statistics for every employed platform font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="fea8c-169">getComputedStyleForNode</span><span class="sxs-lookup"><span data-stu-id="fea8c-169">getComputedStyleForNode</span></span>
<span data-ttu-id="fea8c-170">Возвращает вычисленный стиль для узла DOM, определенного `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="fea8c-170">Returns the computed style for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-171">Параметры</span><span class="sxs-lookup"><span data-stu-id="fea8c-171">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-172">nodeId</span><span class="sxs-lookup"><span data-stu-id="fea8c-172">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-173">Дает</span><span class="sxs-lookup"><span data-stu-id="fea8c-173">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-174">computedStyle</span><span class="sxs-lookup"><span data-stu-id="fea8c-174">computedStyle</span></span></td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td><span data-ttu-id="fea8c-175">Вычисляемый стиль для указанного узла DOM.</span><span class="sxs-lookup"><span data-stu-id="fea8c-175">Computed style for the specified DOM node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="fea8c-176">События</span><span class="sxs-lookup"><span data-stu-id="fea8c-176">Events</span></span>

### <span data-ttu-id="fea8c-177">styleSheetAdded</span><span class="sxs-lookup"><span data-stu-id="fea8c-177">styleSheetAdded</span></span>
<span data-ttu-id="fea8c-178">Срабатывает каждый раз, когда добавляется активная таблица стилей документов.</span><span class="sxs-lookup"><span data-stu-id="fea8c-178">Fired whenever an active document stylesheet is added.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-179">Параметры</span><span class="sxs-lookup"><span data-stu-id="fea8c-179">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-180">header</span><span class="sxs-lookup"><span data-stu-id="fea8c-180">header</span></span></td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td><span data-ttu-id="fea8c-181">Добавлены метаданные таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-181">Added stylesheet metainfo.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="fea8c-182">styleSheetChanged</span><span class="sxs-lookup"><span data-stu-id="fea8c-182">styleSheetChanged</span></span>
<span data-ttu-id="fea8c-183">Возникает при изменении таблицы стилей в результате операции клиента.</span><span class="sxs-lookup"><span data-stu-id="fea8c-183">Fired whenever a stylesheet is changed as a result of the client operation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-184">Параметры</span><span class="sxs-lookup"><span data-stu-id="fea8c-184">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-185">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="fea8c-185">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="fea8c-186">styleSheetRemoved</span><span class="sxs-lookup"><span data-stu-id="fea8c-186">styleSheetRemoved</span></span>
<span data-ttu-id="fea8c-187">Срабатывает каждый раз, когда удаляется активная таблица стилей документов.</span><span class="sxs-lookup"><span data-stu-id="fea8c-187">Fired whenever an active document stylesheet is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-188">Параметры</span><span class="sxs-lookup"><span data-stu-id="fea8c-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-189">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="fea8c-189">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="fea8c-190">Идентификатор удаленной таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-190">Identifier of the removed stylesheet.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="fea8c-191">Типы</span><span class="sxs-lookup"><span data-stu-id="fea8c-191">Types</span></span>

### <a name="stylesheetid"></a> <span data-ttu-id="fea8c-192">StyleSheetId</span><span class="sxs-lookup"><span data-stu-id="fea8c-192">StyleSheetId</span></span> `string`



</p>

---

### <a name="pseudoelementmatches"></a> <span data-ttu-id="fea8c-193">PseudoElementMatches</span><span class="sxs-lookup"><span data-stu-id="fea8c-193">PseudoElementMatches</span></span> `object`

<span data-ttu-id="fea8c-194">Коллекция правил CSS для одного псевдо-стиля.</span><span class="sxs-lookup"><span data-stu-id="fea8c-194">CSS rule collection for a single pseudo style.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-195">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-195">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-196">pseudoType</span><span class="sxs-lookup"><span data-stu-id="fea8c-196">pseudoType</span></span></td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td><span data-ttu-id="fea8c-197">Тип псевдослучайных элементов.</span><span class="sxs-lookup"><span data-stu-id="fea8c-197">Pseudo element type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-198">соответствует</span><span class="sxs-lookup"><span data-stu-id="fea8c-198">matches</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="fea8c-199">Соответствующие правила CSS, применимые к псевдо.</span><span class="sxs-lookup"><span data-stu-id="fea8c-199">Matches of CSS rules applicable to the pseudo style.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> <span data-ttu-id="fea8c-200">InheritedStyleEntry</span><span class="sxs-lookup"><span data-stu-id="fea8c-200">InheritedStyleEntry</span></span> `object`

<span data-ttu-id="fea8c-201">Наследуемая коллекция правил CSS из узла-предка.</span><span class="sxs-lookup"><span data-stu-id="fea8c-201">Inherited CSS rule collection from ancestor node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-202">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-202">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-203">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="fea8c-203">inlineStyle</span></span> <br /> <i><span data-ttu-id="fea8c-204">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-204">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="fea8c-205">Встроенный стиль родительского узла (если таковой имеется) в цепочке наследования стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-205">The ancestor node's inline style, if any, in the style inheritance chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-206">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="fea8c-206">matchedCSSRules</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="fea8c-207">Соответствие правил CSS, соответствующих узлу-предку в цепочке наследования стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-207">Matches of CSS rules matching the ancestor node in the style inheritance chain.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> <span data-ttu-id="fea8c-208">RuleMatch</span><span class="sxs-lookup"><span data-stu-id="fea8c-208">RuleMatch</span></span> `object`

<span data-ttu-id="fea8c-209">Сопоставление данных для правила CSS.</span><span class="sxs-lookup"><span data-stu-id="fea8c-209">Match data for a CSS rule.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-210">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-210">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-211">условия</span><span class="sxs-lookup"><span data-stu-id="fea8c-211">rule</span></span></td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td><span data-ttu-id="fea8c-212">Правило CSS в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="fea8c-212">CSS rule in the match.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> <span data-ttu-id="fea8c-213">Значение</span><span class="sxs-lookup"><span data-stu-id="fea8c-213">Value</span></span> `object`

<span data-ttu-id="fea8c-214">Данные для простого селектора (они разделяются запятыми в списке Selector).</span><span class="sxs-lookup"><span data-stu-id="fea8c-214">Data for a simple selector (these are delimited by commas in a selector list).</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-215">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-215">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-216">текст</span><span class="sxs-lookup"><span data-stu-id="fea8c-216">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-217">Текст значения.</span><span class="sxs-lookup"><span data-stu-id="fea8c-217">Value text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-218">действия</span><span class="sxs-lookup"><span data-stu-id="fea8c-218">range</span></span> <br /> <i><span data-ttu-id="fea8c-219">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-219">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="fea8c-220">Диапазон значений в основном ресурсе (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="fea8c-220">Value range in the underlying resource (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> <span data-ttu-id="fea8c-221">SelectorList</span><span class="sxs-lookup"><span data-stu-id="fea8c-221">SelectorList</span></span> `object`

<span data-ttu-id="fea8c-222">Данные списка Selector.</span><span class="sxs-lookup"><span data-stu-id="fea8c-222">Selector list data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-223">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-223">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-224">селекторов</span><span class="sxs-lookup"><span data-stu-id="fea8c-224">selectors</span></span></td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td><span data-ttu-id="fea8c-225">Выберите элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="fea8c-225">Selectors in the list.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-226">текст</span><span class="sxs-lookup"><span data-stu-id="fea8c-226">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-227">Текст селектора правил.</span><span class="sxs-lookup"><span data-stu-id="fea8c-227">Rule selector text.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> <span data-ttu-id="fea8c-228">CSSRule</span><span class="sxs-lookup"><span data-stu-id="fea8c-228">CSSRule</span></span> `object`

<span data-ttu-id="fea8c-229">Представление правила CSS.</span><span class="sxs-lookup"><span data-stu-id="fea8c-229">CSS rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-230">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-230">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-231">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="fea8c-231">styleSheetId</span></span> <br /> <i><span data-ttu-id="fea8c-232">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-232">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="fea8c-233">Идентификатор таблицы стилей CSS (отсутствует для таблицы пользовательского агента и правил для таблиц, указанных пользователем) это правило получено.</span><span class="sxs-lookup"><span data-stu-id="fea8c-233">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-234">selectorList</span><span class="sxs-lookup"><span data-stu-id="fea8c-234">selectorList</span></span> <br /> <i><span data-ttu-id="fea8c-235">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-235">optional</span></span></i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td><span data-ttu-id="fea8c-236">Данные селектора правила.</span><span class="sxs-lookup"><span data-stu-id="fea8c-236">Rule selector data.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-237">исходных</span><span class="sxs-lookup"><span data-stu-id="fea8c-237">origin</span></span> <br /> <i><span data-ttu-id="fea8c-238">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-238">optional</span></span></i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="fea8c-239">Источник родительской таблицы.</span><span class="sxs-lookup"><span data-stu-id="fea8c-239">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-240">стиль</span><span class="sxs-lookup"><span data-stu-id="fea8c-240">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="fea8c-241">Связанное объявление стиля.</span><span class="sxs-lookup"><span data-stu-id="fea8c-241">Associated style declaration.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-242">мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fea8c-242">media</span></span> <br /> <i><span data-ttu-id="fea8c-243">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-243">optional</span></span></i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td><span data-ttu-id="fea8c-244">Массив списка мультимедиа (для правил, включающих мультимедийные запросы).</span><span class="sxs-lookup"><span data-stu-id="fea8c-244">Media list array (for rules involving media queries).</span></span> <span data-ttu-id="fea8c-245">Массив перечисление запросов мультимедиа, начиная с самого внутреннего, и заканчивая его.</span><span class="sxs-lookup"><span data-stu-id="fea8c-245">The array enumerates media queries starting with the innermost one, going outwards.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> <span data-ttu-id="fea8c-246">SourceRange</span><span class="sxs-lookup"><span data-stu-id="fea8c-246">SourceRange</span></span> `object`

<span data-ttu-id="fea8c-247">Диапазон текста в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="fea8c-247">Text range within a resource.</span></span> <span data-ttu-id="fea8c-248">Все номера отсчитываются от нуля.</span><span class="sxs-lookup"><span data-stu-id="fea8c-248">All numbers are zero-based.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-249">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-249">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-250">startLine</span><span class="sxs-lookup"><span data-stu-id="fea8c-250">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fea8c-251">Начало строки диапазона.</span><span class="sxs-lookup"><span data-stu-id="fea8c-251">Start line of range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-252">startColumn</span><span class="sxs-lookup"><span data-stu-id="fea8c-252">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fea8c-253">Начальный столбец диапазона (включительно).</span><span class="sxs-lookup"><span data-stu-id="fea8c-253">Start column of range (inclusive).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-254">endLine</span><span class="sxs-lookup"><span data-stu-id="fea8c-254">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fea8c-255">Конец строки диапазона</span><span class="sxs-lookup"><span data-stu-id="fea8c-255">End line of range</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-256">endColumn</span><span class="sxs-lookup"><span data-stu-id="fea8c-256">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="fea8c-257">Конечный столбец диапазона (за исключением).</span><span class="sxs-lookup"><span data-stu-id="fea8c-257">End column of range (exclusive).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> <span data-ttu-id="fea8c-258">ShorthandEntry</span><span class="sxs-lookup"><span data-stu-id="fea8c-258">ShorthandEntry</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-259">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-259">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-260">name</span><span class="sxs-lookup"><span data-stu-id="fea8c-260">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-261">Сокращенное имя.</span><span class="sxs-lookup"><span data-stu-id="fea8c-261">Shorthand name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-262">value</span><span class="sxs-lookup"><span data-stu-id="fea8c-262">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-263">Сокращенное значение.</span><span class="sxs-lookup"><span data-stu-id="fea8c-263">Shorthand value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-264">роли</span><span class="sxs-lookup"><span data-stu-id="fea8c-264">important</span></span> <br /> <i><span data-ttu-id="fea8c-265">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-265">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-266">Имеет ли свойство заметку "! важно" (подразумевается `false` , что она отсутствует).</span><span class="sxs-lookup"><span data-stu-id="fea8c-266">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> <span data-ttu-id="fea8c-267">CSSStyle</span><span class="sxs-lookup"><span data-stu-id="fea8c-267">CSSStyle</span></span> `object`

<span data-ttu-id="fea8c-268">Представление стиля CSS.</span><span class="sxs-lookup"><span data-stu-id="fea8c-268">CSS style representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-269">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-269">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-270">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="fea8c-270">styleSheetId</span></span> <br /> <i><span data-ttu-id="fea8c-271">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-271">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="fea8c-272">Идентификатор таблицы стилей CSS (отсутствует для таблицы пользовательского агента и правил для таблиц, указанных пользователем) это правило получено.</span><span class="sxs-lookup"><span data-stu-id="fea8c-272">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-273">cssProperties</span><span class="sxs-lookup"><span data-stu-id="fea8c-273">cssProperties</span></span></td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td><span data-ttu-id="fea8c-274">Свойства CSS в стиле.</span><span class="sxs-lookup"><span data-stu-id="fea8c-274">CSS properties in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-275">shorthandEntries</span><span class="sxs-lookup"><span data-stu-id="fea8c-275">shorthandEntries</span></span></td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td><span data-ttu-id="fea8c-276">Вычисляемые значения для всех сокращений, обнаруженных в стиле.</span><span class="sxs-lookup"><span data-stu-id="fea8c-276">Computed values for all shorthands found in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-277">cssText</span><span class="sxs-lookup"><span data-stu-id="fea8c-277">cssText</span></span> <br /> <i><span data-ttu-id="fea8c-278">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-278">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-279">Текст объявления стиля (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="fea8c-279">Style declaration text (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-280">действия</span><span class="sxs-lookup"><span data-stu-id="fea8c-280">range</span></span> <br /> <i><span data-ttu-id="fea8c-281">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-281">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="fea8c-282">Диапазон объявлений стиля во вложенной таблице стилей (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="fea8c-282">Style declaration range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> <span data-ttu-id="fea8c-283">CSSProperty</span><span class="sxs-lookup"><span data-stu-id="fea8c-283">CSSProperty</span></span> `object`

<span data-ttu-id="fea8c-284">Данные объявления свойств CSS.</span><span class="sxs-lookup"><span data-stu-id="fea8c-284">CSS property declaration data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-285">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-285">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-286">name</span><span class="sxs-lookup"><span data-stu-id="fea8c-286">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-287">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="fea8c-287">The property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-288">value</span><span class="sxs-lookup"><span data-stu-id="fea8c-288">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-289">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="fea8c-289">The property value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-290">роли</span><span class="sxs-lookup"><span data-stu-id="fea8c-290">important</span></span> <br /> <i><span data-ttu-id="fea8c-291">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-291">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-292">Имеет ли свойство заметку "! важно" (подразумевается `false` , что она отсутствует).</span><span class="sxs-lookup"><span data-stu-id="fea8c-292">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-293">согласия</span><span class="sxs-lookup"><span data-stu-id="fea8c-293">implicit</span></span> <br /> <i><span data-ttu-id="fea8c-294">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-294">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-295">Является ли свойство неявным (подразумевается, `false` если оно отсутствует).</span><span class="sxs-lookup"><span data-stu-id="fea8c-295">Whether the property is implicit (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-296">текст</span><span class="sxs-lookup"><span data-stu-id="fea8c-296">text</span></span> <br /> <i><span data-ttu-id="fea8c-297">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-297">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-298">Полный текст свойства, указанный в стиле.</span><span class="sxs-lookup"><span data-stu-id="fea8c-298">The full property text as specified in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-299">parsedOk</span><span class="sxs-lookup"><span data-stu-id="fea8c-299">parsedOk</span></span> <br /> <i><span data-ttu-id="fea8c-300">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-300">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-301">Понимается ли свойство браузером (подразумевается, `true` если оно отсутствует).</span><span class="sxs-lookup"><span data-stu-id="fea8c-301">Whether the property is understood by the browser (implies `true` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-302">отключает</span><span class="sxs-lookup"><span data-stu-id="fea8c-302">disabled</span></span> <br /> <i><span data-ttu-id="fea8c-303">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-303">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-304">Отключено ли свойство пользователем (доступно только для свойств на основе исходного кода).</span><span class="sxs-lookup"><span data-stu-id="fea8c-304">Whether the property is disabled by the user (present for source-based properties only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-305">действия</span><span class="sxs-lookup"><span data-stu-id="fea8c-305">range</span></span> <br /> <i><span data-ttu-id="fea8c-306">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-306">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="fea8c-307">Весь диапазон свойств во вложенном объявлении стиля (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="fea8c-307">The entire property range in the enclosing style declaration (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> <span data-ttu-id="fea8c-308">CSSMedia</span><span class="sxs-lookup"><span data-stu-id="fea8c-308">CSSMedia</span></span> `object`

<span data-ttu-id="fea8c-309">Дескриптор правила мультимедиа CSS.</span><span class="sxs-lookup"><span data-stu-id="fea8c-309">CSS media rule descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-310">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-310">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-311">текст</span><span class="sxs-lookup"><span data-stu-id="fea8c-311">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-312">Текст запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-312">Media query text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-313">исходный</span><span class="sxs-lookup"><span data-stu-id="fea8c-313">source</span></span></td>
            <td><code class="flyout">string</code> <br /> <i><span data-ttu-id="fea8c-314">Разрешенные значения: mediaRule, importRule, linkedSheet, inlineSheet</span><span class="sxs-lookup"><span data-stu-id="fea8c-314">Allowed values: mediaRule, importRule, linkedSheet, inlineSheet</span></span></i></td>
            <td><span data-ttu-id="fea8c-315">Источник запроса мультимедиа: "mediaRule", если он указан в правиле @media, "importRule", если задано правилом @import, "linkedSheet", если он указан с помощью атрибута "Media" в теге ссылки связанной таблицы стилей, "inlineSheet", если он указан с помощью атрибута "мультимедиа", заданное атрибутом "медиа" в теге стиля встроенной таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-315">Source of the media query: "mediaRule" if specified by a @media rule, "importRule" if specified by an @import rule, "linkedSheet" if specified by a "media" attribute in a linked stylesheet's LINK tag, "inlineSheet" if specified by a "media" attribute in an inline stylesheet's STYLE tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-316">sourceURL</span><span class="sxs-lookup"><span data-stu-id="fea8c-316">sourceURL</span></span> <br /> <i><span data-ttu-id="fea8c-317">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-317">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-318">URL-адрес документа, содержащего описание запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-318">URL of the document containing the media query description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-319">действия</span><span class="sxs-lookup"><span data-stu-id="fea8c-319">range</span></span> <br /> <i><span data-ttu-id="fea8c-320">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-320">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="fea8c-321">Диапазон заголовков связанного правила (@media или @import) во вложенной таблице стилей (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="fea8c-321">The associated rule (@media or @import) header range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-322">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="fea8c-322">styleSheetId</span></span> <br /> <i><span data-ttu-id="fea8c-323">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-323">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="fea8c-324">Идентификатор таблицы стилей, содержащей этот объект (если существует).</span><span class="sxs-lookup"><span data-stu-id="fea8c-324">Identifier of the stylesheet containing this object (if exists).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-325">mediaList</span><span class="sxs-lookup"><span data-stu-id="fea8c-325">mediaList</span></span> <br /> <i><span data-ttu-id="fea8c-326">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-326">optional</span></span></i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td><span data-ttu-id="fea8c-327">Массив мультимедийных запросов.</span><span class="sxs-lookup"><span data-stu-id="fea8c-327">Array of media queries.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> <span data-ttu-id="fea8c-328">MediaQuery</span><span class="sxs-lookup"><span data-stu-id="fea8c-328">MediaQuery</span></span> `object`

<span data-ttu-id="fea8c-329">Дескриптор запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-329">Media query descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-330">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-331">многомер</span><span class="sxs-lookup"><span data-stu-id="fea8c-331">expressions</span></span></td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td><span data-ttu-id="fea8c-332">Массив выражений с запросом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-332">Array of media query expressions.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-333">active</span><span class="sxs-lookup"><span data-stu-id="fea8c-333">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-334">Удовлетворено ли условие запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-334">Whether the media query condition is satisfied.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> <span data-ttu-id="fea8c-335">MediaQueryExpression</span><span class="sxs-lookup"><span data-stu-id="fea8c-335">MediaQueryExpression</span></span> `object`

<span data-ttu-id="fea8c-336">Дескриптор выражения для запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-336">Media query expression descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-337">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-338">value</span><span class="sxs-lookup"><span data-stu-id="fea8c-338">value</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="fea8c-339">Значение выражения для запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-339">Media query expression value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-340">единич</span><span class="sxs-lookup"><span data-stu-id="fea8c-340">unit</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-341">Единицы выражения запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-341">Media query expression units.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-342">функция</span><span class="sxs-lookup"><span data-stu-id="fea8c-342">feature</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-343">Функция выражения для запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-343">Media query expression feature.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-344">valueRange</span><span class="sxs-lookup"><span data-stu-id="fea8c-344">valueRange</span></span> <br /> <i><span data-ttu-id="fea8c-345">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-345">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="fea8c-346">Связанный диапазон текста значения в включающей таблице стилей (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="fea8c-346">The associated range of the value text in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-347">computedLength</span><span class="sxs-lookup"><span data-stu-id="fea8c-347">computedLength</span></span> <br /> <i><span data-ttu-id="fea8c-348">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-348">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="fea8c-349">Вычисленная длина выражения запроса мультимедиа (если применимо).</span><span class="sxs-lookup"><span data-stu-id="fea8c-349">Computed length of media query expression (if applicable).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> <span data-ttu-id="fea8c-350">PlatformFontUsage</span><span class="sxs-lookup"><span data-stu-id="fea8c-350">PlatformFontUsage</span></span> `object`

<span data-ttu-id="fea8c-351">Сведения о количестве глифов, отображаемых с использованием заданного шрифта.</span><span class="sxs-lookup"><span data-stu-id="fea8c-351">Information about amount of glyphs that were rendered with given font.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-352">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-352">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-353">familyName</span><span class="sxs-lookup"><span data-stu-id="fea8c-353">familyName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-354">Имя семейства шрифтов, указанное платформой.</span><span class="sxs-lookup"><span data-stu-id="fea8c-354">Font's family name reported by platform.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-355">isCustomFont</span><span class="sxs-lookup"><span data-stu-id="fea8c-355">isCustomFont</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-356">Указывает, был ли этот шрифт скачан или разрешается локально.</span><span class="sxs-lookup"><span data-stu-id="fea8c-356">Indicates if the font was downloaded or resolved locally.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-357">glyphCount</span><span class="sxs-lookup"><span data-stu-id="fea8c-357">glyphCount</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="fea8c-358">Количество глифов, обработанных с помощью этого шрифта.</span><span class="sxs-lookup"><span data-stu-id="fea8c-358">Amount of glyphs that were rendered with this font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> <span data-ttu-id="fea8c-359">CSSKeyframesRule</span><span class="sxs-lookup"><span data-stu-id="fea8c-359">CSSKeyframesRule</span></span> `object`

<span data-ttu-id="fea8c-360">Представление правила "ключевые кадры CSS".</span><span class="sxs-lookup"><span data-stu-id="fea8c-360">CSS keyframes rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-361">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-361">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-362">animationName</span><span class="sxs-lookup"><span data-stu-id="fea8c-362">animationName</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="fea8c-363">Имя анимации.</span><span class="sxs-lookup"><span data-stu-id="fea8c-363">Animation name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-364">Ключевые кадры</span><span class="sxs-lookup"><span data-stu-id="fea8c-364">keyframes</span></span></td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td><span data-ttu-id="fea8c-365">Список ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="fea8c-365">List of keyframes.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> <span data-ttu-id="fea8c-366">CSSKeyframeRule</span><span class="sxs-lookup"><span data-stu-id="fea8c-366">CSSKeyframeRule</span></span> `object`

<span data-ttu-id="fea8c-367">Представление правила для ключевого кадра CSS.</span><span class="sxs-lookup"><span data-stu-id="fea8c-367">CSS keyframe rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-368">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-369">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="fea8c-369">styleSheetId</span></span> <br /> <i><span data-ttu-id="fea8c-370">необязательные</span><span class="sxs-lookup"><span data-stu-id="fea8c-370">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="fea8c-371">Идентификатор таблицы стилей CSS (отсутствует для таблицы пользовательского агента и правил для таблиц, указанных пользователем) это правило получено.</span><span class="sxs-lookup"><span data-stu-id="fea8c-371">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-372">исходных</span><span class="sxs-lookup"><span data-stu-id="fea8c-372">origin</span></span></td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="fea8c-373">Источник родительской таблицы.</span><span class="sxs-lookup"><span data-stu-id="fea8c-373">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-374">keyText</span><span class="sxs-lookup"><span data-stu-id="fea8c-374">keyText</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="fea8c-375">Текст соответствующего ключа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-375">Associated key text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-376">стиль</span><span class="sxs-lookup"><span data-stu-id="fea8c-376">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="fea8c-377">Связанное объявление стиля.</span><span class="sxs-lookup"><span data-stu-id="fea8c-377">Associated style declaration.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> <span data-ttu-id="fea8c-378">CSSComputedStyleProperty</span><span class="sxs-lookup"><span data-stu-id="fea8c-378">CSSComputedStyleProperty</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-379">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-380">name</span><span class="sxs-lookup"><span data-stu-id="fea8c-380">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-381">Имя свойства вычисляемого стиля.</span><span class="sxs-lookup"><span data-stu-id="fea8c-381">Computed style property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-382">value</span><span class="sxs-lookup"><span data-stu-id="fea8c-382">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-383">Значение свойства "вычисляемый стиль".</span><span class="sxs-lookup"><span data-stu-id="fea8c-383">Computed style property value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> <span data-ttu-id="fea8c-384">CSSStyleSheetHeader</span><span class="sxs-lookup"><span data-stu-id="fea8c-384">CSSStyleSheetHeader</span></span> `object`

<span data-ttu-id="fea8c-385">Таблица стилей CSS Metainformation.</span><span class="sxs-lookup"><span data-stu-id="fea8c-385">CSS stylesheet metainformation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fea8c-386">Свойства</span><span class="sxs-lookup"><span data-stu-id="fea8c-386">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fea8c-387">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="fea8c-387">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="fea8c-388">Идентификатор таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-388">The stylesheet identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-389">sourceURL</span><span class="sxs-lookup"><span data-stu-id="fea8c-389">sourceURL</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fea8c-390">URL-адрес ресурса таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-390">Stylesheet resource URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-391">отключает</span><span class="sxs-lookup"><span data-stu-id="fea8c-391">disabled</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-392">Указывает, отключена ли таблица стилей.</span><span class="sxs-lookup"><span data-stu-id="fea8c-392">Denotes whether the stylesheet is disabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-393">isInline</span><span class="sxs-lookup"><span data-stu-id="fea8c-393">isInline</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="fea8c-394">Создана ли эта таблица стилей для тега STYLE с помощью средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="fea8c-394">Whether this stylesheet is created for STYLE tag by parser.</span></span> <span data-ttu-id="fea8c-395">Этот флаг не установлен для тегов Document. письменного стиля.</span><span class="sxs-lookup"><span data-stu-id="fea8c-395">This flag is not set for document.written STYLE tags.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-396">startLine</span><span class="sxs-lookup"><span data-stu-id="fea8c-396">startLine</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="fea8c-397">Смещение строки таблицы стилей в пределах ресурса (с отсчетом от нуля).</span><span class="sxs-lookup"><span data-stu-id="fea8c-397">Line offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-398">startColumn</span><span class="sxs-lookup"><span data-stu-id="fea8c-398">startColumn</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="fea8c-399">Смещение столбца в таблице стилей в рамках ресурса (с отсчетом от нуля).</span><span class="sxs-lookup"><span data-stu-id="fea8c-399">Column offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fea8c-400">Длина</span><span class="sxs-lookup"><span data-stu-id="fea8c-400">length</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="fea8c-401">Размер содержимого (в символах).</span><span class="sxs-lookup"><span data-stu-id="fea8c-401">Size of the content (in characters).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="fea8c-402">Зависимости</span><span class="sxs-lookup"><span data-stu-id="fea8c-402">Dependencies</span></span>

[<span data-ttu-id="fea8c-403">DOM</span><span class="sxs-lookup"><span data-stu-id="fea8c-403">DOM</span></span>](dom.md)

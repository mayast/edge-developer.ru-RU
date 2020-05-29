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
# <span data-ttu-id="f8718-109">DOM</span><span class="sxs-lookup"><span data-stu-id="f8718-109">DOM</span></span>
<span data-ttu-id="f8718-110">Этот домен предоставляет DOM-операции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f8718-110">This domain exposes DOM read/write operations.</span></span> <span data-ttu-id="f8718-111">Каждый узел DOM представлен с помощью зеркального объекта `id` .</span><span class="sxs-lookup"><span data-stu-id="f8718-111">Each DOM Node is represented with its mirror object that has an `id`.</span></span> <span data-ttu-id="f8718-112">Это `id` можно использовать для получения дополнительных сведений на узле, разрешения их в обертку объекта JavaScript и т. д. Важно, чтобы клиент получал события DOM только для тех узлов, которые известны клиенту.</span><span class="sxs-lookup"><span data-stu-id="f8718-112">This `id` can be used to get additional information on the Node, resolve it into the JavaScript object wrapper, etc. It is important that client receives DOM events only for the nodes that are known to the client.</span></span> <span data-ttu-id="f8718-113">Внутренний сервер отслеживает узлы, отправленные клиенту, и никогда не отправляет один и тот же узел дважды.</span><span class="sxs-lookup"><span data-stu-id="f8718-113">Backend keeps track of the nodes that were sent to the client and never sends the same node twice.</span></span> <span data-ttu-id="f8718-114">Ответственность за сбор сведений о узлах, отправленных клиенту, лежит на клиенте.</span><span class="sxs-lookup"><span data-stu-id="f8718-114">It is client's responsibility to collect information about the nodes that were sent to the client.</span></span><p><span data-ttu-id="f8718-115">Обратите внимание, что `iframe` элементы Owner будут возвращать соответствующие элементы документа в качестве дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="f8718-115">Note that `iframe` owner elements will return corresponding document elements as their child nodes.</span></span></p>

| | |
|-|-|
| [**<span data-ttu-id="f8718-116">Методы</span><span class="sxs-lookup"><span data-stu-id="f8718-116">Methods</span></span>**](#methods) | <span data-ttu-id="f8718-117">[Включение](#enable), [Отключение](#disable), [getDocument](#getdocument) [highlightNode](#highlightnode), [hideHighlight](#hidehighlight) [setInspectedNode](#setinspectednode) , [requestChildNodes](#requestchildnodes), [InAttribute](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector) [, querySelectorAll](#queryselectorall) [requestNode](#requestnode) [. requestNode](#resolvenode)</span><span class="sxs-lookup"><span data-stu-id="f8718-117">[enable](#enable), [disable](#disable), [getDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span></span> |
| [**<span data-ttu-id="f8718-118">События</span><span class="sxs-lookup"><span data-stu-id="f8718-118">Events</span></span>**](#events) | <span data-ttu-id="f8718-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span><span class="sxs-lookup"><span data-stu-id="f8718-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span></span> |
| [**<span data-ttu-id="f8718-120">Типы</span><span class="sxs-lookup"><span data-stu-id="f8718-120">Types</span></span>**](#types) | <span data-ttu-id="f8718-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span><span class="sxs-lookup"><span data-stu-id="f8718-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [Node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span></span> |
| [**<span data-ttu-id="f8718-122">Зависимости</span><span class="sxs-lookup"><span data-stu-id="f8718-122">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="f8718-123">Язык</span><span class="sxs-lookup"><span data-stu-id="f8718-123">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="f8718-124">Методы</span><span class="sxs-lookup"><span data-stu-id="f8718-124">Methods</span></span>

### <span data-ttu-id="f8718-125">"Включить"</span><span class="sxs-lookup"><span data-stu-id="f8718-125">enable</span></span>
<span data-ttu-id="f8718-126">Включает агент DOM для указанной страницы.</span><span class="sxs-lookup"><span data-stu-id="f8718-126">Enables DOM agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="f8718-127">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="f8718-127">disable</span></span>
<span data-ttu-id="f8718-128">Отключает агент DOM для указанной страницы.</span><span class="sxs-lookup"><span data-stu-id="f8718-128">Disables DOM agent for the given page.</span></span> <span data-ttu-id="f8718-129">Отключение DOM сделает все ранее действительные nodeIds недействительными.</span><span class="sxs-lookup"><span data-stu-id="f8718-129">Disabling the DOM will invalidate any previously valid nodeIds.</span></span>

</p>

---

### <span data-ttu-id="f8718-130">"документ"</span><span class="sxs-lookup"><span data-stu-id="f8718-130">getDocument</span></span>
<span data-ttu-id="f8718-131">Возвращает корневой узел DOM (и, при необходимости, поддерево) вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="f8718-131">Returns the root DOM node (and optionally the subtree) to the caller.</span></span> <span data-ttu-id="f8718-132">При вызове `getDocument` будут аннулированы все ранее действительные nodeIds</span><span class="sxs-lookup"><span data-stu-id="f8718-132">Calling `getDocument` will invalidate any previously valid nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-133">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-133">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-134">одной</span><span class="sxs-lookup"><span data-stu-id="f8718-134">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f8718-135">Максимальная глубина, при которой должны извлекаться дочерние элементы, значение по умолчанию — 2.</span><span class="sxs-lookup"><span data-stu-id="f8718-135">The maximum depth at which children should be retrieved, defaults to 2.</span></span> <span data-ttu-id="f8718-136">Используйте-1 для всего поддерева.</span><span class="sxs-lookup"><span data-stu-id="f8718-136">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-137">pierce</span><span class="sxs-lookup"><span data-stu-id="f8718-137">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f8718-138">Следует ли прослеживать элементы iframe при возврате поддерева (значение по умолчанию — ложь).</span><span class="sxs-lookup"><span data-stu-id="f8718-138">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-139">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-139">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-140">узла</span><span class="sxs-lookup"><span data-stu-id="f8718-140">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="f8718-141">Конечный узел.</span><span class="sxs-lookup"><span data-stu-id="f8718-141">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-142">highlightNode</span><span class="sxs-lookup"><span data-stu-id="f8718-142">highlightNode</span></span>
<span data-ttu-id="f8718-143">Higlights узел DOM с заданным идентификатором или оберткой объекта.</span><span class="sxs-lookup"><span data-stu-id="f8718-143">Higlights DOM node with given id or object wrapper.</span></span> <span data-ttu-id="f8718-144">nodeId, backendNodeId или objectId должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="f8718-144">nodeId, backendNodeId, or objectId must be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-145">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-145">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-146">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-146">nodeId</span></span> <br/> <i><span data-ttu-id="f8718-147">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-147">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-148">Идентификатор выделяемого узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-148">Identifier of the node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-149">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-149">backendNodeId</span></span> <br/> <i><span data-ttu-id="f8718-150">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-150">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="f8718-151">Идентификатор узла внутреннего элемента, который нужно выделиь.</span><span class="sxs-lookup"><span data-stu-id="f8718-151">Identifier of the backend node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-152">objectId</span><span class="sxs-lookup"><span data-stu-id="f8718-152">objectId</span></span> <br/> <i><span data-ttu-id="f8718-153">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-153">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="f8718-154">Код объекта JavaScript для выделенного узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-154">JavaScript object id of the node to be highlighted.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-155">higlightConfig</span><span class="sxs-lookup"><span data-stu-id="f8718-155">higlightConfig</span></span></td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td><span data-ttu-id="f8718-156">Описательный вид подсветки.</span><span class="sxs-lookup"><span data-stu-id="f8718-156">Descriptor of the highlight appearance.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-157">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-157">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-158">узла</span><span class="sxs-lookup"><span data-stu-id="f8718-158">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="f8718-159">Конечный узел.</span><span class="sxs-lookup"><span data-stu-id="f8718-159">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-160">hideHighlight</span><span class="sxs-lookup"><span data-stu-id="f8718-160">hideHighlight</span></span>
<span data-ttu-id="f8718-161">Скрывает любой текущий выделенный фрагмент DOM-узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-161">Hides any current DOM node highlight.</span></span>

</p>

---

### <span data-ttu-id="f8718-162">requestChildNodes</span><span class="sxs-lookup"><span data-stu-id="f8718-162">requestChildNodes</span></span>
<span data-ttu-id="f8718-163">Запросы, которые дочерние элементы узла с указанным идентификатором, возвращаются в GHE вызывающего кода в форме `setChildNodes` событий.</span><span class="sxs-lookup"><span data-stu-id="f8718-163">Requests that children of the node with given id are returned to ghe caller in the form of `setChildNodes` events.</span></span> `setChildNodes` <span data-ttu-id="f8718-164">будет инициировано для каждого узла, который ранее не возвращал дочерние элементы, начиная с запрашиваемого узла и до указанной глубины.</span><span class="sxs-lookup"><span data-stu-id="f8718-164">will be fired for each node that has not previously returned it's children, starting from the requested node down to the specified depth.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-165">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-165">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-166">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-166">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-167">Идентификатор узла, из которого нужно получить дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="f8718-167">Id of the node to get children from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-168">одной</span><span class="sxs-lookup"><span data-stu-id="f8718-168">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f8718-169">Максимальная глубина, при которой должны извлекаться дочерние элементы, по умолчанию равной 1.</span><span class="sxs-lookup"><span data-stu-id="f8718-169">The maximum depth at which children should be retrieved, defaults to 1.</span></span> <span data-ttu-id="f8718-170">Используйте-1 для всего поддерева.</span><span class="sxs-lookup"><span data-stu-id="f8718-170">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-171">pierce</span><span class="sxs-lookup"><span data-stu-id="f8718-171">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f8718-172">Следует ли прослеживать элементы iframe при возврате поддерева (значение по умолчанию — ложь).</span><span class="sxs-lookup"><span data-stu-id="f8718-172">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-173">Атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f8718-173">getAttributes</span></span>
<span data-ttu-id="f8718-174">Возвращает атрибуты для указанного узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-174">Returns attributes for the specified node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-175">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-175">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-176">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-176">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-177">Идентификатор узла, для которого требуется извлечь attibutes.</span><span class="sxs-lookup"><span data-stu-id="f8718-177">Id of the node to retrieve attibutes for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-178">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-178">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-179">атрибуты</span><span class="sxs-lookup"><span data-stu-id="f8718-179">attributes</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="f8718-180">Массив с чередованием имен и значений атрибутов узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-180">An interleaved array of node attribute names and values.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-181">getOuterHTML</span><span class="sxs-lookup"><span data-stu-id="f8718-181">getOuterHTML</span></span>
<span data-ttu-id="f8718-182">Возвращает разметку HTML узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-182">Returns node's HTML markup.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-183">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-183">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-184">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-184">nodeId</span></span> <br/> <i><span data-ttu-id="f8718-185">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-185">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-186">Идентификатор узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-186">Identifier of the node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-187">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-187">backendNodeId</span></span> <br/> <i><span data-ttu-id="f8718-188">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-188">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="f8718-189">Идентификатор узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="f8718-189">Identifier of the backend node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-190">objectId</span><span class="sxs-lookup"><span data-stu-id="f8718-190">objectId</span></span> <br/> <i><span data-ttu-id="f8718-191">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-191">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="f8718-192">Идентификатор объекта JavaScript обертки узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-192">JavaScript object id of the node wrapper.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-193">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-193">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-194">outerHTML</span><span class="sxs-lookup"><span data-stu-id="f8718-194">outerHTML</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-195">Внешняя разметка HTML.</span><span class="sxs-lookup"><span data-stu-id="f8718-195">Outer HTML markup.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-196">pushNodesByBackendIdsToFrontend</span><span class="sxs-lookup"><span data-stu-id="f8718-196">pushNodesByBackendIdsToFrontend</span></span>
<span data-ttu-id="f8718-197">Поиск идентификаторов узлов и разрешение всех родительских элементов для указанных кодов внутренних узлов</span><span class="sxs-lookup"><span data-stu-id="f8718-197">Looks up Node Ids and resolves all parents for the specified Backend Node Ids</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-198">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-198">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-199">backendNodeIds</span><span class="sxs-lookup"><span data-stu-id="f8718-199">backendNodeIds</span></span></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td><span data-ttu-id="f8718-200">Идентификаторы узлов внутренних узлов, которые нужно разрешить</span><span class="sxs-lookup"><span data-stu-id="f8718-200">Backend Node IDs of the nodes to resolve</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-201">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-201">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-202">nodeIds</span><span class="sxs-lookup"><span data-stu-id="f8718-202">nodeIds</span></span></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="f8718-203">Идентификаторы узлов разрешенных узлов</span><span class="sxs-lookup"><span data-stu-id="f8718-203">Node Ids of the resolved nodes</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-204">querySelector</span><span class="sxs-lookup"><span data-stu-id="f8718-204">querySelector</span></span>
<span data-ttu-id="f8718-205">Выполняется `querySelector` на указанном узле.</span><span class="sxs-lookup"><span data-stu-id="f8718-205">Executes `querySelector` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-206">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-207">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-207">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-208">Идентификатор узла для запроса.</span><span class="sxs-lookup"><span data-stu-id="f8718-208">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-209">выбора</span><span class="sxs-lookup"><span data-stu-id="f8718-209">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-210">Строка выбора.</span><span class="sxs-lookup"><span data-stu-id="f8718-210">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-211">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-211">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-212">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-212">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-213">Результат выбора запроса.</span><span class="sxs-lookup"><span data-stu-id="f8718-213">Query selector result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-214">querySelectorAll</span><span class="sxs-lookup"><span data-stu-id="f8718-214">querySelectorAll</span></span>
<span data-ttu-id="f8718-215">Выполняется `querySelectorAll` на указанном узле.</span><span class="sxs-lookup"><span data-stu-id="f8718-215">Executes `querySelectorAll` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-216">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-216">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-217">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-217">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-218">Идентификатор узла для запроса.</span><span class="sxs-lookup"><span data-stu-id="f8718-218">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-219">выбора</span><span class="sxs-lookup"><span data-stu-id="f8718-219">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-220">Строка выбора.</span><span class="sxs-lookup"><span data-stu-id="f8718-220">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-221">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-221">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-222">nodeIds</span><span class="sxs-lookup"><span data-stu-id="f8718-222">nodeIds</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="f8718-223">Результаты выбора запроса.</span><span class="sxs-lookup"><span data-stu-id="f8718-223">Query selector results.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-224">requestNode</span><span class="sxs-lookup"><span data-stu-id="f8718-224">requestNode</span></span>
<span data-ttu-id="f8718-225">Запросы, которые отправляются вызывающему объекту для узла с указанным идентификатором удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="f8718-225">Requests that the node with given remote object Id is sent to caller.</span></span> <span data-ttu-id="f8718-226">Все узлы, которые формируют путь из узла к корню, также отправляются клиенту в виде серии `setChildNodes` уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f8718-226">All nodes that form the path from the node to the root are also sent to the client as a series of `setChildNodes` notifications.</span></span> <span data-ttu-id="f8718-227">Возвращает значение 0, если документ, содержащий запрошенный узел, ранее не запрашивался клиентом.</span><span class="sxs-lookup"><span data-stu-id="f8718-227">returns 0 if the document containing the requested node has not previously been requested by the client.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-228">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-228">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-229">objectId</span><span class="sxs-lookup"><span data-stu-id="f8718-229">objectId</span></span></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="f8718-230">Идентификатор объекта JavaScript, который нужно преобразовать в узел.</span><span class="sxs-lookup"><span data-stu-id="f8718-230">JavaScript object Id to convert into node.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-231">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-231">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-232">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-232">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-233">Идентификатор узла для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="f8718-233">Node Id for given object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-234">resolveNode</span><span class="sxs-lookup"><span data-stu-id="f8718-234">resolveNode</span></span>
<span data-ttu-id="f8718-235">Выполняет разрешение объекта узла JavaScript для данного NodeId или BackendNodeId.</span><span class="sxs-lookup"><span data-stu-id="f8718-235">Resolves the JavaScript node object for a given NodeId or BackendNodeId.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-236">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-236">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-237">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-237">nodeId</span></span> <br/> <i><span data-ttu-id="f8718-238">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-238">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-239">Идентификатор разрешаемого узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-239">Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-240">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-240">backendNodeId</span></span> <br/> <i><span data-ttu-id="f8718-241">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-241">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="f8718-242">Код внутреннего узла для разрешаемого узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-242">Backend Node Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-243">objectGroup</span><span class="sxs-lookup"><span data-stu-id="f8718-243">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-244">Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="f8718-244">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-245">Дает</span><span class="sxs-lookup"><span data-stu-id="f8718-245">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-246">объект</span><span class="sxs-lookup"><span data-stu-id="f8718-246">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="f8718-247">Обертка объекта JavaScript для данного узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-247">JavaScript object wrapper for given node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-248">setInspectedNode</span><span class="sxs-lookup"><span data-stu-id="f8718-248">setInspectedNode</span></span>
<span><b><span data-ttu-id="f8718-249">Проб.</span><span class="sxs-lookup"><span data-stu-id="f8718-249">Experimental.</span></span> </b></span><span data-ttu-id="f8718-250">Позволяет консоли ссылаться на предыдущий проверенный узел с указанным ID через $0-$ 4.</span><span class="sxs-lookup"><span data-stu-id="f8718-250">Enables console to refer to the previous inspected node with given id via $0-$4.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-251">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-252">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-252">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-253">Идентификатор узла DOM, доступ к которому осуществляется с помощью $0-$ 4 в интерфейсе API командной строки.</span><span class="sxs-lookup"><span data-stu-id="f8718-253">DOM node id to be accessible by means of $0-$4 in command line API.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="f8718-254">События</span><span class="sxs-lookup"><span data-stu-id="f8718-254">Events</span></span>

### <span data-ttu-id="f8718-255">setChildNodes</span><span class="sxs-lookup"><span data-stu-id="f8718-255">setChildNodes</span></span>
<span data-ttu-id="f8718-256">Возникает, когда серверный внутренний объект хочет предоставить клиенту отсутствующую структуру DOM.</span><span class="sxs-lookup"><span data-stu-id="f8718-256">Fired when the backend wishes to provide client with missing DOM structure.</span></span> <span data-ttu-id="f8718-257">Это происходит при большинстве звонков, запрашивающих nodeIds</span><span class="sxs-lookup"><span data-stu-id="f8718-257">This happens upon most calls requesting nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-258">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-258">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-259">parentId</span><span class="sxs-lookup"><span data-stu-id="f8718-259">parentId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-260">Родительский узел для poplate с дочерними элементами.</span><span class="sxs-lookup"><span data-stu-id="f8718-260">Parent node to poplate with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-261">кластер</span><span class="sxs-lookup"><span data-stu-id="f8718-261">nodes</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="f8718-262">Массив дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="f8718-262">Child nodes array.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-263">attributeModified</span><span class="sxs-lookup"><span data-stu-id="f8718-263">attributeModified</span></span>
<span data-ttu-id="f8718-264">Срабатывает при `Element` изменении атрибута.</span><span class="sxs-lookup"><span data-stu-id="f8718-264">Fired when `Element`'s attribute is modified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-265">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-265">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-266">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-266">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-267">Идентификатор узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="f8718-267">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-268">name</span><span class="sxs-lookup"><span data-stu-id="f8718-268">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-269">Имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="f8718-269">Attribute name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-270">value</span><span class="sxs-lookup"><span data-stu-id="f8718-270">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-271">Значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="f8718-271">Attribute value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-272">attributeRemoved</span><span class="sxs-lookup"><span data-stu-id="f8718-272">attributeRemoved</span></span>
<span data-ttu-id="f8718-273">Срабатывает при `Element` удалении атрибута.</span><span class="sxs-lookup"><span data-stu-id="f8718-273">Fired when `Element`'s attribute is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-274">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-274">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-275">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-275">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-276">Идентификатор узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="f8718-276">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-277">name</span><span class="sxs-lookup"><span data-stu-id="f8718-277">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-278">Имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="f8718-278">Attribute name.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-279">characterDataModified</span><span class="sxs-lookup"><span data-stu-id="f8718-279">characterDataModified</span></span>
<span data-ttu-id="f8718-280">Событие «зеркала `DOMCharacterDataModified` ».</span><span class="sxs-lookup"><span data-stu-id="f8718-280">Mirrors `DOMCharacterDataModified` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-281">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-281">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-282">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-282">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-283">Идентификатор узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="f8718-283">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-284">charcterData</span><span class="sxs-lookup"><span data-stu-id="f8718-284">charcterData</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-285">Новое текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="f8718-285">New text value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-286">childNodeInserted</span><span class="sxs-lookup"><span data-stu-id="f8718-286">childNodeInserted</span></span>
<span data-ttu-id="f8718-287">Событие «зеркала `DOMNodeInserted` ».</span><span class="sxs-lookup"><span data-stu-id="f8718-287">Mirrors `DOMNodeInserted` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-288">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-288">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-289">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-289">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-290">Идентификатор узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="f8718-290">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-291">previousNodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-291">previousNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-292">Идентификатор предыдущего одноуровневого элемента вставленного узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-292">Id of the inserted node's previous sibling.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-293">узлы</span><span class="sxs-lookup"><span data-stu-id="f8718-293">node</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="f8718-294">Вставленные данные узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-294">Inserted node data.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-295">childNodeRemoved</span><span class="sxs-lookup"><span data-stu-id="f8718-295">childNodeRemoved</span></span>
<span data-ttu-id="f8718-296">Событие «зеркала `DOMNodeRemoved` ».</span><span class="sxs-lookup"><span data-stu-id="f8718-296">Mirrors `DOMNodeRemoved` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-297">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8718-297">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-298">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-298">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-299">Идентификатор узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="f8718-299">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-300">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-300">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-301">Идентификатор узла, который был удален.</span><span class="sxs-lookup"><span data-stu-id="f8718-301">Id of the node that has been removed.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f8718-302">documentUpdated</span><span class="sxs-lookup"><span data-stu-id="f8718-302">documentUpdated</span></span>
<span data-ttu-id="f8718-303">Срабатывает `Document` , если обновление выполнено полностью.</span><span class="sxs-lookup"><span data-stu-id="f8718-303">Fired when `Document` has been totally updated.</span></span> <span data-ttu-id="f8718-304">Идентификаторы узлов больше не действительны.</span><span class="sxs-lookup"><span data-stu-id="f8718-304">Node ids are no longer valid.</span></span>

</p>

---

## <span data-ttu-id="f8718-305">Типы</span><span class="sxs-lookup"><span data-stu-id="f8718-305">Types</span></span>

### <a name="rgba"></a> <span data-ttu-id="f8718-306">RGBA</span><span class="sxs-lookup"><span data-stu-id="f8718-306">RGBA</span></span> `object`

<span data-ttu-id="f8718-307">Структура, содержащая цвет RGBA.</span><span class="sxs-lookup"><span data-stu-id="f8718-307">A Structure holding an RGBA color.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-308">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8718-308">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-309">&</span><span class="sxs-lookup"><span data-stu-id="f8718-309">r</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f8718-310">Красный компонент в диапазоне [0-255].</span><span class="sxs-lookup"><span data-stu-id="f8718-310">The red component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-311">финансовой</span><span class="sxs-lookup"><span data-stu-id="f8718-311">g</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f8718-312">Зеленый компонент в диапазоне [0-255].</span><span class="sxs-lookup"><span data-stu-id="f8718-312">The green component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-313">байт</span><span class="sxs-lookup"><span data-stu-id="f8718-313">b</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f8718-314">Синий компонент в диапазоне [0-255].</span><span class="sxs-lookup"><span data-stu-id="f8718-314">The blue component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-315">а</span><span class="sxs-lookup"><span data-stu-id="f8718-315">a</span></span> <br/> <i><span data-ttu-id="f8718-316">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-316">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="f8718-317">Альфа-компонент в диапазоне [0-1].</span><span class="sxs-lookup"><span data-stu-id="f8718-317">The alpha component, in the [0-1] range.</span></span> <span data-ttu-id="f8718-318">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="f8718-318">Default is 1.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> <span data-ttu-id="f8718-319">HighlightConfig</span><span class="sxs-lookup"><span data-stu-id="f8718-319">HighlightConfig</span></span> `object`

<span data-ttu-id="f8718-320">Данные конфигурации для выделяют элементы страницы.</span><span class="sxs-lookup"><span data-stu-id="f8718-320">Configuration data for highlighting of page elements.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-321">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8718-321">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-322">contentColor</span><span class="sxs-lookup"><span data-stu-id="f8718-322">contentColor</span></span> <br/> <i><span data-ttu-id="f8718-323">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-323">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="f8718-324">Цвет заливки, выделяя рамку содержимого.</span><span class="sxs-lookup"><span data-stu-id="f8718-324">The content box highlight fill color.</span></span> <span data-ttu-id="f8718-325">Значение по умолчанию — прозрачный.</span><span class="sxs-lookup"><span data-stu-id="f8718-325">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-326">paddingColor</span><span class="sxs-lookup"><span data-stu-id="f8718-326">paddingColor</span></span> <br/> <i><span data-ttu-id="f8718-327">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-327">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="f8718-328">Цвет заливки с выделением полей.</span><span class="sxs-lookup"><span data-stu-id="f8718-328">The padding highlight fill color.</span></span> <span data-ttu-id="f8718-329">Значение по умолчанию — прозрачный.</span><span class="sxs-lookup"><span data-stu-id="f8718-329">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-330">Границы</span><span class="sxs-lookup"><span data-stu-id="f8718-330">borderColor</span></span> <br/> <i><span data-ttu-id="f8718-331">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-331">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="f8718-332">Цвет заливки выделения границ.</span><span class="sxs-lookup"><span data-stu-id="f8718-332">The border highlight fill color.</span></span> <span data-ttu-id="f8718-333">Значение по умолчанию — прозрачный.</span><span class="sxs-lookup"><span data-stu-id="f8718-333">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-334">marginColor</span><span class="sxs-lookup"><span data-stu-id="f8718-334">marginColor</span></span> <br/> <i><span data-ttu-id="f8718-335">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-335">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="f8718-336">Цвет заливки полей.</span><span class="sxs-lookup"><span data-stu-id="f8718-336">The margin highlight fill color.</span></span> <span data-ttu-id="f8718-337">Значение по умолчанию — прозрачный.</span><span class="sxs-lookup"><span data-stu-id="f8718-337">Default is transparent.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> <span data-ttu-id="f8718-338">NodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-338">NodeId</span></span> `integer`

<span data-ttu-id="f8718-339">Уникальный идентификатор узла DOM</span><span class="sxs-lookup"><span data-stu-id="f8718-339">Unique DOM node identifier</span></span>

</p>

---

### <a name="node"></a> <span data-ttu-id="f8718-340">Узлы</span><span class="sxs-lookup"><span data-stu-id="f8718-340">Node</span></span> `object`

<span data-ttu-id="f8718-341">Зеркальный объект, представляющий фактические узлы DOM.</span><span class="sxs-lookup"><span data-stu-id="f8718-341">Mirror object that represents the actual DOM nodes.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f8718-342">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8718-342">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f8718-343">nodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-343">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-344">Идентификатор узла, используемый для ссылки на этот узел.</span><span class="sxs-lookup"><span data-stu-id="f8718-344">Node Identifier used to reference this node.</span></span> <span data-ttu-id="f8718-345">Внутренний сервер будет срабатывать события DOM для узлов, которые имеют nodeId, известный клиенту.</span><span class="sxs-lookup"><span data-stu-id="f8718-345">Backend will fire DOM events for nodes that have a nodeId that is known to the client</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-346">parentId</span><span class="sxs-lookup"><span data-stu-id="f8718-346">parentId</span></span> <br/> <i><span data-ttu-id="f8718-347">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-347">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-348">Идентификатор узла родительского узла, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="f8718-348">Node Identifier of the parent Node, if any.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-349">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-349">backendNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="f8718-350">Идентификатор внутреннего узла узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-350">Backend Node identifier of the node.</span></span> <span data-ttu-id="f8718-351">BackendNodeIds узлы ссылок, которые могут быть известны клиенту, но не отменяют события DOM для этого узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-351">BackendNodeIds reference Nodes that can be known to the client, but do not push DOM events about this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-352">Узла</span><span class="sxs-lookup"><span data-stu-id="f8718-352">nodeType</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`<span data-ttu-id="f8718-353">nodeType.</span><span class="sxs-lookup"><span data-stu-id="f8718-353">'s nodeType.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-354">nodeName</span><span class="sxs-lookup"><span data-stu-id="f8718-354">nodeName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="f8718-355">nodeName.</span><span class="sxs-lookup"><span data-stu-id="f8718-355">'s nodeName.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-356">Локально</span><span class="sxs-lookup"><span data-stu-id="f8718-356">localName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="f8718-357">localName</span><span class="sxs-lookup"><span data-stu-id="f8718-357">'s localName</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-358">nodeValue</span><span class="sxs-lookup"><span data-stu-id="f8718-358">nodeValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="f8718-359">nodeValue</span><span class="sxs-lookup"><span data-stu-id="f8718-359">'s nodeValue</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-360">childNodeCount</span><span class="sxs-lookup"><span data-stu-id="f8718-360">childNodeCount</span></span> <br/> <i><span data-ttu-id="f8718-361">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-361">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f8718-362">Число дочерних элементов для `Container` узлов.</span><span class="sxs-lookup"><span data-stu-id="f8718-362">Child count for `Container` nodes.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-363">дети</span><span class="sxs-lookup"><span data-stu-id="f8718-363">children</span></span> <br/> <i><span data-ttu-id="f8718-364">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-364">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="f8718-365">Дочерние узлы этого узла, запрашиваемые дочерними элементами.</span><span class="sxs-lookup"><span data-stu-id="f8718-365">Child nodes of this node when requested with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-366">атрибуты</span><span class="sxs-lookup"><span data-stu-id="f8718-366">attributes</span></span> <br/> <i><span data-ttu-id="f8718-367">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-367">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="f8718-368">Атрибуты `Element` узлов в форме плоского массива [файл1, value1, имя2, значение2]</span><span class="sxs-lookup"><span data-stu-id="f8718-368">Attributes of `Element` nodes in the form of a flat array \`[name1, value1, name2, value2]</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-369">documentURL</span><span class="sxs-lookup"><span data-stu-id="f8718-369">documentURL</span></span> <br/> <i><span data-ttu-id="f8718-370">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-370">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-371">URL-адрес документа, `Document` на который указывает узел.</span><span class="sxs-lookup"><span data-stu-id="f8718-371">Document URL that `Document` nodes point to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-372">baseURL</span><span class="sxs-lookup"><span data-stu-id="f8718-372">baseURL</span></span> <br/> <i><span data-ttu-id="f8718-373">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-373">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f8718-374">URL-адрес документа, который `Document` используются узлами для завершения URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f8718-374">Document URL that `Document` nodes use for URL completion.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-375">publicId</span><span class="sxs-lookup"><span data-stu-id="f8718-375">publicId</span></span> <br/> <i><span data-ttu-id="f8718-376">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-376">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="f8718-377">PublicId узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-377">Node's publicId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-378">systemId</span><span class="sxs-lookup"><span data-stu-id="f8718-378">systemId</span></span> <br/> <i><span data-ttu-id="f8718-379">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-379">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="f8718-380">SystemId узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-380">Node's systemId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-381">internalSubset</span><span class="sxs-lookup"><span data-stu-id="f8718-381">internalSubset</span></span> <br/> <i><span data-ttu-id="f8718-382">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-382">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="f8718-383">InternalSubset узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-383">Node's internalSubset.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-384">xmlVersion</span><span class="sxs-lookup"><span data-stu-id="f8718-384">xmlVersion</span></span> <br/> <i><span data-ttu-id="f8718-385">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-385">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` <span data-ttu-id="f8718-386">Версия XML узла в случае XML-документов.</span><span class="sxs-lookup"><span data-stu-id="f8718-386">Node's xml version in the case of XML documents.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-387">name</span><span class="sxs-lookup"><span data-stu-id="f8718-387">name</span></span> <br/> <i><span data-ttu-id="f8718-388">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-388">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="f8718-389">Имя узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-389">Node's name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-390">value</span><span class="sxs-lookup"><span data-stu-id="f8718-390">value</span></span> <br/> <i><span data-ttu-id="f8718-391">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-391">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="f8718-392">Значение узла.</span><span class="sxs-lookup"><span data-stu-id="f8718-392">Node's value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-393">frameId</span><span class="sxs-lookup"><span data-stu-id="f8718-393">frameId</span></span> <br/> <i><span data-ttu-id="f8718-394">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-394">optional</span></span></i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td><span data-ttu-id="f8718-395">ИДЕНТИФИКАТОР кадра для элементов владельца кадра.</span><span class="sxs-lookup"><span data-stu-id="f8718-395">Frame ID for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-396">contentDocument</span><span class="sxs-lookup"><span data-stu-id="f8718-396">contentDocument</span></span> <br/> <i><span data-ttu-id="f8718-397">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-397">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="f8718-398">Документ содержимого для элементов владельца фрейма.</span><span class="sxs-lookup"><span data-stu-id="f8718-398">Content document for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f8718-399">isSVG</span><span class="sxs-lookup"><span data-stu-id="f8718-399">isSVG</span></span> <br/> <i><span data-ttu-id="f8718-400">необязательные</span><span class="sxs-lookup"><span data-stu-id="f8718-400">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f8718-401">Значение true, если узел является SVG.</span><span class="sxs-lookup"><span data-stu-id="f8718-401">True if the node is SVG.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> <span data-ttu-id="f8718-402">BackendNodeId</span><span class="sxs-lookup"><span data-stu-id="f8718-402">BackendNodeId</span></span> `integer`

<span data-ttu-id="f8718-403">Уникальный идентификатор узла DOM, который используется для ссылки на узел, который может не быть передан на сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="f8718-403">Unique DOM node identifier used to reference a node that may not have been pushed to the front-end.</span></span>

</p>

---

### <a name="pseudotype"></a> <span data-ttu-id="f8718-404">PseudoType</span><span class="sxs-lookup"><span data-stu-id="f8718-404">PseudoType</span></span> `string`

<span data-ttu-id="f8718-405">Тип псевдослучайных элементов.</span><span class="sxs-lookup"><span data-stu-id="f8718-405">Pseudo element type.</span></span>

##### <span data-ttu-id="f8718-406">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="f8718-406">Allowed Values</span></span>
<span data-ttu-id="f8718-407">Первая строка, первая буква, до, после, выделение</span><span class="sxs-lookup"><span data-stu-id="f8718-407">first-line, first-letter, before, after, selection</span></span>
</p>

---

## <span data-ttu-id="f8718-408">Зависимости</span><span class="sxs-lookup"><span data-stu-id="f8718-408">Dependencies</span></span>

[<span data-ttu-id="f8718-409">Язык</span><span class="sxs-lookup"><span data-stu-id="f8718-409">Runtime</span></span>](runtime.md)
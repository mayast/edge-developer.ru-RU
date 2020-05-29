---
description: Ссылка на домен оверлея. Перекрытие доменов обеспечивает взаимодействие визуальных элементов оформления и выделения узлов
title: Overlay Domain-DevTools Protocol версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: a7657e2abc99e45894f19f6557f12f78f8ee9c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571666"
---
# <span data-ttu-id="710ef-104">Наложение</span><span class="sxs-lookup"><span data-stu-id="710ef-104">Overlay</span></span>
<span data-ttu-id="710ef-105">Перекрытие доменов обеспечивает взаимодействие визуальных элементов оформления и выделения узлов</span><span class="sxs-lookup"><span data-stu-id="710ef-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="710ef-106">Методы</span><span class="sxs-lookup"><span data-stu-id="710ef-106">Methods</span></span>**](#methods) | <span data-ttu-id="710ef-107">[Включение](#enable), [Отключение](#disable), [setInspectMode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="710ef-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="710ef-108">События</span><span class="sxs-lookup"><span data-stu-id="710ef-108">Events</span></span>**](#events) | <span data-ttu-id="710ef-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="710ef-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="710ef-110">Зависимости</span><span class="sxs-lookup"><span data-stu-id="710ef-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="710ef-111">DOM</span><span class="sxs-lookup"><span data-stu-id="710ef-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="710ef-112">Методы</span><span class="sxs-lookup"><span data-stu-id="710ef-112">Methods</span></span>

### <span data-ttu-id="710ef-113">"Включить"</span><span class="sxs-lookup"><span data-stu-id="710ef-113">enable</span></span>
<span data-ttu-id="710ef-114">Включение отчетов о <code>nodeHighlightRequested</code> <code>inspectElementRequested</code> событиях и событий</span><span class="sxs-lookup"><span data-stu-id="710ef-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="710ef-115">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="710ef-115">disable</span></span>
<span data-ttu-id="710ef-116">Отключает отчетность о событиях домена оверлея</span><span class="sxs-lookup"><span data-stu-id="710ef-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="710ef-117">setInspectMode</span><span class="sxs-lookup"><span data-stu-id="710ef-117">setInspectMode</span></span>
<span data-ttu-id="710ef-118">Задает режим выделения элементов для клиента.</span><span class="sxs-lookup"><span data-stu-id="710ef-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="710ef-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="710ef-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="710ef-120">mode</span><span class="sxs-lookup"><span data-stu-id="710ef-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="710ef-121">Режим проверки.</span><span class="sxs-lookup"><span data-stu-id="710ef-121">The inspection mode.</span></span>  <span data-ttu-id="710ef-122">Допустимые значения: "searchForNode" и "нет".</span><span class="sxs-lookup"><span data-stu-id="710ef-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="710ef-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="710ef-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="710ef-124">необязательные</span><span class="sxs-lookup"><span data-stu-id="710ef-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="710ef-125">Конфигурация подсветки, которую необходимо использовать при проверке</span><span class="sxs-lookup"><span data-stu-id="710ef-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="710ef-126">События</span><span class="sxs-lookup"><span data-stu-id="710ef-126">Events</span></span>

### <span data-ttu-id="710ef-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="710ef-127">inspectNodeRequested</span></span>
<span data-ttu-id="710ef-128">Уведомляет клиента о том, что пользователь запросит проверить конкретный узел.</span><span class="sxs-lookup"><span data-stu-id="710ef-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="710ef-129">Параметры</span><span class="sxs-lookup"><span data-stu-id="710ef-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="710ef-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="710ef-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="710ef-131">Запрошенный код узла внутреннего узла</span><span class="sxs-lookup"><span data-stu-id="710ef-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="710ef-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="710ef-132">nodeHighlightRequested</span></span>
<span data-ttu-id="710ef-133">Показывает, что пользователь наводит указатель мыши на узел и может проверить узел</span><span class="sxs-lookup"><span data-stu-id="710ef-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="710ef-134">Параметры</span><span class="sxs-lookup"><span data-stu-id="710ef-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="710ef-135">nodeId</span><span class="sxs-lookup"><span data-stu-id="710ef-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="710ef-136">Идентификатор узла для рассматриваемого узла.</span><span class="sxs-lookup"><span data-stu-id="710ef-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="710ef-137">Зависимости</span><span class="sxs-lookup"><span data-stu-id="710ef-137">Dependencies</span></span>

[<span data-ttu-id="710ef-138">DOM</span><span class="sxs-lookup"><span data-stu-id="710ef-138">DOM</span></span>](dom.md)
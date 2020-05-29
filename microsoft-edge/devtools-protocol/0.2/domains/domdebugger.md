---
description: Ссылка на домен DOMDebugger. Отладка DOM позволяет задавать точки останова для определенных операций и событий DOM. Выполнение JavaScript будет остановлено на этих операциях так, как если бы была установлена обычная точка останова.
title: Протокол DOMDebugger Domain-DevTools версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571667"
---
# <span data-ttu-id="d3490-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="d3490-105">DOMDebugger</span></span>
<span data-ttu-id="d3490-106">Отладка DOM позволяет задавать точки останова для определенных операций и событий DOM.</span><span class="sxs-lookup"><span data-stu-id="d3490-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="d3490-107">Выполнение JavaScript будет остановлено на этих операциях так, как если бы была установлена обычная точка останова.</span><span class="sxs-lookup"><span data-stu-id="d3490-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="d3490-108">Методы</span><span class="sxs-lookup"><span data-stu-id="d3490-108">Methods</span></span>**](#methods) | <span data-ttu-id="d3490-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="d3490-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="d3490-110">Методы</span><span class="sxs-lookup"><span data-stu-id="d3490-110">Methods</span></span>

### <span data-ttu-id="d3490-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="d3490-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="d3490-112">Проб.</span><span class="sxs-lookup"><span data-stu-id="d3490-112">Experimental.</span></span> </b></span><span data-ttu-id="d3490-113">Задает точку останова для определенного собственного события.</span><span class="sxs-lookup"><span data-stu-id="d3490-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d3490-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3490-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d3490-115">eventName</span><span class="sxs-lookup"><span data-stu-id="d3490-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d3490-116">Имя инструментирования, на котором нужно остановиться.</span><span class="sxs-lookup"><span data-stu-id="d3490-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="d3490-117">Допустимые значения: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="d3490-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d3490-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="d3490-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="d3490-119">Проб.</span><span class="sxs-lookup"><span data-stu-id="d3490-119">Experimental.</span></span> </b></span><span data-ttu-id="d3490-120">Удаляет точку останова в определенном собственном событии.</span><span class="sxs-lookup"><span data-stu-id="d3490-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d3490-121">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3490-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d3490-122">eventName</span><span class="sxs-lookup"><span data-stu-id="d3490-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d3490-123">Имя инструментирования, на котором нужно остановиться.</span><span class="sxs-lookup"><span data-stu-id="d3490-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="d3490-124">Допустимые значения: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="d3490-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

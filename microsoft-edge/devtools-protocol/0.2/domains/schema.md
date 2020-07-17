---
description: Ссылка на домен схемы. Предоставляет сведения о схеме протоколов.
title: Domain Schema-DevTools Protocol версии 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: d0fbe9cde742d255797a2460b940732ffa5b8f27
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882879"
---
# <span data-ttu-id="f49c0-104">Domain Schema-DevTools Protocol версии 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f49c0-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="f49c0-105">Предоставляет сведения о схеме протоколов.</span><span class="sxs-lookup"><span data-stu-id="f49c0-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="f49c0-106">Методы</span><span class="sxs-lookup"><span data-stu-id="f49c0-106">Methods</span></span>**](#methods) | [<span data-ttu-id="f49c0-107">"домены"</span><span class="sxs-lookup"><span data-stu-id="f49c0-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="f49c0-108">Типы</span><span class="sxs-lookup"><span data-stu-id="f49c0-108">Types</span></span>**](#types) | [<span data-ttu-id="f49c0-109">Домен</span><span class="sxs-lookup"><span data-stu-id="f49c0-109">Domain</span></span>](#domain) |
## <span data-ttu-id="f49c0-110">Методы</span><span class="sxs-lookup"><span data-stu-id="f49c0-110">Methods</span></span>

### <span data-ttu-id="f49c0-111">"домены"</span><span class="sxs-lookup"><span data-stu-id="f49c0-111">getDomains</span></span>
<span data-ttu-id="f49c0-112">Возвращает поддерживаемые домены.</span><span class="sxs-lookup"><span data-stu-id="f49c0-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f49c0-113">Дает</span><span class="sxs-lookup"><span data-stu-id="f49c0-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f49c0-114">имена</span><span class="sxs-lookup"><span data-stu-id="f49c0-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="f49c0-115">Список поддерживаемых доменов.</span><span class="sxs-lookup"><span data-stu-id="f49c0-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="f49c0-116">Типы</span><span class="sxs-lookup"><span data-stu-id="f49c0-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="f49c0-117">Домен</span><span class="sxs-lookup"><span data-stu-id="f49c0-117">Domain</span></span> `object`

<span data-ttu-id="f49c0-118">Описание домена протоколов.</span><span class="sxs-lookup"><span data-stu-id="f49c0-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f49c0-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="f49c0-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f49c0-120">name</span><span class="sxs-lookup"><span data-stu-id="f49c0-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f49c0-121">Доменное имя.</span><span class="sxs-lookup"><span data-stu-id="f49c0-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f49c0-122">version</span><span class="sxs-lookup"><span data-stu-id="f49c0-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f49c0-123">Версия домена.</span><span class="sxs-lookup"><span data-stu-id="f49c0-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

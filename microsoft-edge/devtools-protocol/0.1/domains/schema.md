---
description: Ссылка на домен схемы. Предоставляет сведения о схеме протоколов.
title: Domain Schema-DevTools Protocol версии 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a2f679f6f4bf8e82dc7298d96f798507b1338062
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882928"
---
# <span data-ttu-id="b7c39-104">Domain Schema-DevTools Protocol версии 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="b7c39-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="b7c39-105">Предоставляет сведения о схеме протоколов.</span><span class="sxs-lookup"><span data-stu-id="b7c39-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="b7c39-106">Методы</span><span class="sxs-lookup"><span data-stu-id="b7c39-106">Methods</span></span>**](#methods) | [<span data-ttu-id="b7c39-107">"домены"</span><span class="sxs-lookup"><span data-stu-id="b7c39-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="b7c39-108">Типы</span><span class="sxs-lookup"><span data-stu-id="b7c39-108">Types</span></span>**](#types) | [<span data-ttu-id="b7c39-109">Домен</span><span class="sxs-lookup"><span data-stu-id="b7c39-109">Domain</span></span>](#domain) |
## <span data-ttu-id="b7c39-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b7c39-110">Methods</span></span>

### <span data-ttu-id="b7c39-111">"домены"</span><span class="sxs-lookup"><span data-stu-id="b7c39-111">getDomains</span></span>
<span data-ttu-id="b7c39-112">Возвращает поддерживаемые домены.</span><span class="sxs-lookup"><span data-stu-id="b7c39-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b7c39-113">Дает</span><span class="sxs-lookup"><span data-stu-id="b7c39-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b7c39-114">имена</span><span class="sxs-lookup"><span data-stu-id="b7c39-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="b7c39-115">Список поддерживаемых доменов.</span><span class="sxs-lookup"><span data-stu-id="b7c39-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="b7c39-116">Типы</span><span class="sxs-lookup"><span data-stu-id="b7c39-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="b7c39-117">Домен</span><span class="sxs-lookup"><span data-stu-id="b7c39-117">Domain</span></span> `object`

<span data-ttu-id="b7c39-118">Описание домена протоколов.</span><span class="sxs-lookup"><span data-stu-id="b7c39-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b7c39-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7c39-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b7c39-120">name</span><span class="sxs-lookup"><span data-stu-id="b7c39-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b7c39-121">Доменное имя.</span><span class="sxs-lookup"><span data-stu-id="b7c39-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b7c39-122">version</span><span class="sxs-lookup"><span data-stu-id="b7c39-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b7c39-123">Версия домена.</span><span class="sxs-lookup"><span data-stu-id="b7c39-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---

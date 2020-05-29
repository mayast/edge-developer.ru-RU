---
description: Ссылка на домен схемы. Предоставляет сведения о схеме протоколов.
title: Schema Domain-DevTools Protocol версии 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 83d7019d18ccce1c81b67aafdcafe1a8566694ea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571686"
---
# <span data-ttu-id="5cf66-104">Схема</span><span class="sxs-lookup"><span data-stu-id="5cf66-104">Schema</span></span>
<span data-ttu-id="5cf66-105">Предоставляет сведения о схеме протоколов.</span><span class="sxs-lookup"><span data-stu-id="5cf66-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="5cf66-106">Методы</span><span class="sxs-lookup"><span data-stu-id="5cf66-106">Methods</span></span>**](#methods) | [<span data-ttu-id="5cf66-107">"домены"</span><span class="sxs-lookup"><span data-stu-id="5cf66-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="5cf66-108">Типы</span><span class="sxs-lookup"><span data-stu-id="5cf66-108">Types</span></span>**](#types) | [<span data-ttu-id="5cf66-109">Домен</span><span class="sxs-lookup"><span data-stu-id="5cf66-109">Domain</span></span>](#domain) |
## <span data-ttu-id="5cf66-110">Методы</span><span class="sxs-lookup"><span data-stu-id="5cf66-110">Methods</span></span>

### <span data-ttu-id="5cf66-111">"домены"</span><span class="sxs-lookup"><span data-stu-id="5cf66-111">getDomains</span></span>
<span data-ttu-id="5cf66-112">Возвращает поддерживаемые домены.</span><span class="sxs-lookup"><span data-stu-id="5cf66-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5cf66-113">Дает</span><span class="sxs-lookup"><span data-stu-id="5cf66-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5cf66-114">имена</span><span class="sxs-lookup"><span data-stu-id="5cf66-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="5cf66-115">Список поддерживаемых доменов.</span><span class="sxs-lookup"><span data-stu-id="5cf66-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="5cf66-116">Типы</span><span class="sxs-lookup"><span data-stu-id="5cf66-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="5cf66-117">Домен</span><span class="sxs-lookup"><span data-stu-id="5cf66-117">Domain</span></span> `object`

<span data-ttu-id="5cf66-118">Описание домена протоколов.</span><span class="sxs-lookup"><span data-stu-id="5cf66-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5cf66-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="5cf66-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5cf66-120">name</span><span class="sxs-lookup"><span data-stu-id="5cf66-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5cf66-121">Доменное имя.</span><span class="sxs-lookup"><span data-stu-id="5cf66-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5cf66-122">version</span><span class="sxs-lookup"><span data-stu-id="5cf66-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5cf66-123">Версия домена.</span><span class="sxs-lookup"><span data-stu-id="5cf66-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---

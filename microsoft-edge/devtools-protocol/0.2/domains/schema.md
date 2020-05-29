---
description: Ссылка на домен схемы. Предоставляет сведения о схеме протоколов.
title: Schema Domain-DevTools Protocol версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: df86e6669956c14b7c905514fc44376f71eaa993
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571661"
---
# <span data-ttu-id="2e325-104">Схема</span><span class="sxs-lookup"><span data-stu-id="2e325-104">Schema</span></span>
<span data-ttu-id="2e325-105">Предоставляет сведения о схеме протоколов.</span><span class="sxs-lookup"><span data-stu-id="2e325-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="2e325-106">Методы</span><span class="sxs-lookup"><span data-stu-id="2e325-106">Methods</span></span>**](#methods) | [<span data-ttu-id="2e325-107">"домены"</span><span class="sxs-lookup"><span data-stu-id="2e325-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="2e325-108">Типы</span><span class="sxs-lookup"><span data-stu-id="2e325-108">Types</span></span>**](#types) | [<span data-ttu-id="2e325-109">Домен</span><span class="sxs-lookup"><span data-stu-id="2e325-109">Domain</span></span>](#domain) |
## <span data-ttu-id="2e325-110">Методы</span><span class="sxs-lookup"><span data-stu-id="2e325-110">Methods</span></span>

### <span data-ttu-id="2e325-111">"домены"</span><span class="sxs-lookup"><span data-stu-id="2e325-111">getDomains</span></span>
<span data-ttu-id="2e325-112">Возвращает поддерживаемые домены.</span><span class="sxs-lookup"><span data-stu-id="2e325-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2e325-113">Дает</span><span class="sxs-lookup"><span data-stu-id="2e325-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2e325-114">имена</span><span class="sxs-lookup"><span data-stu-id="2e325-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="2e325-115">Список поддерживаемых доменов.</span><span class="sxs-lookup"><span data-stu-id="2e325-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="2e325-116">Типы</span><span class="sxs-lookup"><span data-stu-id="2e325-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="2e325-117">Домен</span><span class="sxs-lookup"><span data-stu-id="2e325-117">Domain</span></span> `object`

<span data-ttu-id="2e325-118">Описание домена протоколов.</span><span class="sxs-lookup"><span data-stu-id="2e325-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2e325-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e325-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2e325-120">name</span><span class="sxs-lookup"><span data-stu-id="2e325-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2e325-121">Доменное имя.</span><span class="sxs-lookup"><span data-stu-id="2e325-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2e325-122">version</span><span class="sxs-lookup"><span data-stu-id="2e325-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2e325-123">Версия домена.</span><span class="sxs-lookup"><span data-stu-id="2e325-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

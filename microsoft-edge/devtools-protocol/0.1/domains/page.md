---
description: Ссылка на домен страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools версии 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 1602673eae1c04f60046a898dbadeab1b59f9ce5
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882942"
---
# <span data-ttu-id="f69e4-104">Домен страницы — Протокол DevTools версии 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f69e4-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="f69e4-105">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="f69e4-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="f69e4-106">Методы</span><span class="sxs-lookup"><span data-stu-id="f69e4-106">Methods</span></span>**](#methods) | <span data-ttu-id="f69e4-107">[Включение](#enable), [Отключение](#disable), [Навигация](#navigate)</span><span class="sxs-lookup"><span data-stu-id="f69e4-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="f69e4-108">Типы</span><span class="sxs-lookup"><span data-stu-id="f69e4-108">Types</span></span>**](#types) | [<span data-ttu-id="f69e4-109">FrameId</span><span class="sxs-lookup"><span data-stu-id="f69e4-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="f69e4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="f69e4-110">Methods</span></span>

### <span data-ttu-id="f69e4-111">"Включить"</span><span class="sxs-lookup"><span data-stu-id="f69e4-111">enable</span></span>
<span data-ttu-id="f69e4-112">Включение уведомлений домена на странице.</span><span class="sxs-lookup"><span data-stu-id="f69e4-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="f69e4-113">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="f69e4-113">disable</span></span>
<span data-ttu-id="f69e4-114">Отключение уведомлений домена на странице.</span><span class="sxs-lookup"><span data-stu-id="f69e4-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="f69e4-115">переход</span><span class="sxs-lookup"><span data-stu-id="f69e4-115">navigate</span></span>
<span data-ttu-id="f69e4-116">Переход на текущую страницу по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="f69e4-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f69e4-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="f69e4-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f69e4-118">url</span><span class="sxs-lookup"><span data-stu-id="f69e4-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f69e4-119">URL-адрес для перемещения по странице.</span><span class="sxs-lookup"><span data-stu-id="f69e4-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f69e4-120">Дает</span><span class="sxs-lookup"><span data-stu-id="f69e4-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f69e4-121">frameId</span><span class="sxs-lookup"><span data-stu-id="f69e4-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="f69e4-122">Проб.</span><span class="sxs-lookup"><span data-stu-id="f69e4-122">Experimental.</span></span> </b></span><span data-ttu-id="f69e4-123">Код кадра, который будет использоваться для навигации.</span><span class="sxs-lookup"><span data-stu-id="f69e4-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="f69e4-124">Типы</span><span class="sxs-lookup"><span data-stu-id="f69e4-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="f69e4-125">FrameId</span><span class="sxs-lookup"><span data-stu-id="f69e4-125">FrameId</span></span> `string`

<span data-ttu-id="f69e4-126">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="f69e4-126">Unique frame identifier.</span></span>


---

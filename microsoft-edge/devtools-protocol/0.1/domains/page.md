---
description: Ссылка на домен страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools версии 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a1cd094baef4571240881a86ecccfdb319fef61b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571692"
---
# <span data-ttu-id="adcb5-104">Page</span><span class="sxs-lookup"><span data-stu-id="adcb5-104">Page</span></span>
<span data-ttu-id="adcb5-105">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="adcb5-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="adcb5-106">Методы</span><span class="sxs-lookup"><span data-stu-id="adcb5-106">Methods</span></span>**](#methods) | <span data-ttu-id="adcb5-107">[Включение](#enable), [Отключение](#disable), [Навигация](#navigate)</span><span class="sxs-lookup"><span data-stu-id="adcb5-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="adcb5-108">Типы</span><span class="sxs-lookup"><span data-stu-id="adcb5-108">Types</span></span>**](#types) | [<span data-ttu-id="adcb5-109">FrameId</span><span class="sxs-lookup"><span data-stu-id="adcb5-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="adcb5-110">Методы</span><span class="sxs-lookup"><span data-stu-id="adcb5-110">Methods</span></span>

### <span data-ttu-id="adcb5-111">"Включить"</span><span class="sxs-lookup"><span data-stu-id="adcb5-111">enable</span></span>
<span data-ttu-id="adcb5-112">Включение уведомлений домена на странице.</span><span class="sxs-lookup"><span data-stu-id="adcb5-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="adcb5-113">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="adcb5-113">disable</span></span>
<span data-ttu-id="adcb5-114">Отключение уведомлений домена на странице.</span><span class="sxs-lookup"><span data-stu-id="adcb5-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="adcb5-115">переход</span><span class="sxs-lookup"><span data-stu-id="adcb5-115">navigate</span></span>
<span data-ttu-id="adcb5-116">Переход на текущую страницу по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="adcb5-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="adcb5-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="adcb5-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="adcb5-118">url</span><span class="sxs-lookup"><span data-stu-id="adcb5-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="adcb5-119">URL-адрес для перемещения по странице.</span><span class="sxs-lookup"><span data-stu-id="adcb5-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="adcb5-120">Дает</span><span class="sxs-lookup"><span data-stu-id="adcb5-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="adcb5-121">frameId</span><span class="sxs-lookup"><span data-stu-id="adcb5-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="adcb5-122">Проб.</span><span class="sxs-lookup"><span data-stu-id="adcb5-122">Experimental.</span></span> </b></span><span data-ttu-id="adcb5-123">Код кадра, который будет использоваться для навигации.</span><span class="sxs-lookup"><span data-stu-id="adcb5-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="adcb5-124">Типы</span><span class="sxs-lookup"><span data-stu-id="adcb5-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="adcb5-125">FrameId</span><span class="sxs-lookup"><span data-stu-id="adcb5-125">FrameId</span></span> `string`

<span data-ttu-id="adcb5-126">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="adcb5-126">Unique frame identifier.</span></span>


---

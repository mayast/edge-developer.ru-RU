---
description: Ссылка на домен страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools версии 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 864515eefbcb809e280f2ab1d81015018272c398
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882844"
---
# <span data-ttu-id="5562a-104">Домен страницы — Протокол DevTools версии 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="5562a-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="5562a-105">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="5562a-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="5562a-106">Методы</span><span class="sxs-lookup"><span data-stu-id="5562a-106">Methods</span></span>**](#methods) | <span data-ttu-id="5562a-107">[Включение](#enable), [Отключение](#disable), [Навигация](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="5562a-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="5562a-108">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="5562a-108">Events</span></span>**](#events) | <span data-ttu-id="5562a-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="5562a-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="5562a-110">Типы</span><span class="sxs-lookup"><span data-stu-id="5562a-110">Types</span></span>**](#types) | <span data-ttu-id="5562a-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="5562a-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="5562a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5562a-112">Methods</span></span>

### <span data-ttu-id="5562a-113">"Включить"</span><span class="sxs-lookup"><span data-stu-id="5562a-113">enable</span></span>
<span data-ttu-id="5562a-114">Включение уведомлений домена на странице.</span><span class="sxs-lookup"><span data-stu-id="5562a-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="5562a-115">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="5562a-115">disable</span></span>
<span data-ttu-id="5562a-116">Отключение уведомлений домена на странице.</span><span class="sxs-lookup"><span data-stu-id="5562a-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="5562a-117">переход</span><span class="sxs-lookup"><span data-stu-id="5562a-117">navigate</span></span>
<span data-ttu-id="5562a-118">Переход на текущую страницу по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="5562a-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="5562a-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-120">url</span><span class="sxs-lookup"><span data-stu-id="5562a-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5562a-121">URL-адрес для перемещения по странице.</span><span class="sxs-lookup"><span data-stu-id="5562a-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-122">frameId</span><span class="sxs-lookup"><span data-stu-id="5562a-122">frameId</span></span> <br/> <i><span data-ttu-id="5562a-123">необязательные</span><span class="sxs-lookup"><span data-stu-id="5562a-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="5562a-124">Код кадра для навигации.</span><span class="sxs-lookup"><span data-stu-id="5562a-124">Frame id to navigate.</span></span> <span data-ttu-id="5562a-125">Если он не указан, переходим к верхней странице.</span><span class="sxs-lookup"><span data-stu-id="5562a-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-126">Дает</span><span class="sxs-lookup"><span data-stu-id="5562a-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-127">frameId</span><span class="sxs-lookup"><span data-stu-id="5562a-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="5562a-128">Код кадра, который будет использоваться для навигации.</span><span class="sxs-lookup"><span data-stu-id="5562a-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5562a-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="5562a-129">getFrameTree</span></span>
<span data-ttu-id="5562a-130">Возвращает структуру дерева кадров.</span><span class="sxs-lookup"><span data-stu-id="5562a-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-131">Дает</span><span class="sxs-lookup"><span data-stu-id="5562a-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="5562a-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="5562a-133">Показать древовидную структуру фреймов.</span><span class="sxs-lookup"><span data-stu-id="5562a-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="5562a-134">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="5562a-134">Events</span></span>

### <span data-ttu-id="5562a-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="5562a-135">frameAttached</span></span>
<span data-ttu-id="5562a-136">Срабатывает, если кадр присоединен к родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="5562a-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-137">Параметры</span><span class="sxs-lookup"><span data-stu-id="5562a-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-138">frameId</span><span class="sxs-lookup"><span data-stu-id="5562a-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="5562a-139">Идентификатор присоединенного кадра.</span><span class="sxs-lookup"><span data-stu-id="5562a-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="5562a-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="5562a-141">Идентификатор родительского фрейма.</span><span class="sxs-lookup"><span data-stu-id="5562a-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-142">стека</span><span class="sxs-lookup"><span data-stu-id="5562a-142">stack</span></span> <br/> <i><span data-ttu-id="5562a-143">необязательные</span><span class="sxs-lookup"><span data-stu-id="5562a-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="5562a-144">Трассировка стека JavaScript для вложенного кадра задается только в том случае, если кадр инициирован из сценария.</span><span class="sxs-lookup"><span data-stu-id="5562a-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5562a-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="5562a-145">frameDetached</span></span>
<span data-ttu-id="5562a-146">Срабатывает, если кадр отсоединен от родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="5562a-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-147">Параметры</span><span class="sxs-lookup"><span data-stu-id="5562a-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-148">frameId</span><span class="sxs-lookup"><span data-stu-id="5562a-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="5562a-149">Идентификатор отсоединенного кадра.</span><span class="sxs-lookup"><span data-stu-id="5562a-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5562a-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="5562a-150">frameNavigated</span></span>
<span data-ttu-id="5562a-151">Срабатывает после завершения навигации кадра.</span><span class="sxs-lookup"><span data-stu-id="5562a-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-152">Параметры</span><span class="sxs-lookup"><span data-stu-id="5562a-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-153">интервал</span><span class="sxs-lookup"><span data-stu-id="5562a-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="5562a-154">Объект Frame.</span><span class="sxs-lookup"><span data-stu-id="5562a-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5562a-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="5562a-155">loadEventFired</span></span>
<span data-ttu-id="5562a-156">Соответствует событию Window. OnLoad.</span><span class="sxs-lookup"><span data-stu-id="5562a-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-157">Параметры</span><span class="sxs-lookup"><span data-stu-id="5562a-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-158">штамп</span><span class="sxs-lookup"><span data-stu-id="5562a-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="5562a-159">Количество миллисекунд, прошедшее с момента создания эпохи.</span><span class="sxs-lookup"><span data-stu-id="5562a-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5562a-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="5562a-160">domContentEventFired</span></span>
<span data-ttu-id="5562a-161">Соответствует событию Document. onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="5562a-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="5562a-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-163">штамп</span><span class="sxs-lookup"><span data-stu-id="5562a-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="5562a-164">Количество миллисекунд, прошедшее с момента создания эпохи.</span><span class="sxs-lookup"><span data-stu-id="5562a-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="5562a-165">Типы</span><span class="sxs-lookup"><span data-stu-id="5562a-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="5562a-166">FrameId</span><span class="sxs-lookup"><span data-stu-id="5562a-166">FrameId</span></span> `string`

<span data-ttu-id="5562a-167">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="5562a-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="5562a-168">Кадр</span><span class="sxs-lookup"><span data-stu-id="5562a-168">Frame</span></span> `object`

<span data-ttu-id="5562a-169">Сведения о кадре на странице.</span><span class="sxs-lookup"><span data-stu-id="5562a-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-170">Свойства</span><span class="sxs-lookup"><span data-stu-id="5562a-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-171">id</span><span class="sxs-lookup"><span data-stu-id="5562a-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="5562a-172">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="5562a-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-173">parentId</span><span class="sxs-lookup"><span data-stu-id="5562a-173">parentId</span></span> <br/> <i><span data-ttu-id="5562a-174">необязательные</span><span class="sxs-lookup"><span data-stu-id="5562a-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="5562a-175">Уникальный идентификатор родительского фрейма.</span><span class="sxs-lookup"><span data-stu-id="5562a-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-176">name</span><span class="sxs-lookup"><span data-stu-id="5562a-176">name</span></span> <br/> <i><span data-ttu-id="5562a-177">необязательные</span><span class="sxs-lookup"><span data-stu-id="5562a-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5562a-178">Имя кадра, указанное в теге.</span><span class="sxs-lookup"><span data-stu-id="5562a-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-179">url</span><span class="sxs-lookup"><span data-stu-id="5562a-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5562a-180">URL-адрес документа в рамке.</span><span class="sxs-lookup"><span data-stu-id="5562a-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="5562a-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5562a-182">Источник защиты документа фрейма.</span><span class="sxs-lookup"><span data-stu-id="5562a-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-183">Успешности</span><span class="sxs-lookup"><span data-stu-id="5562a-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5562a-184">Тип MIME документа Frame определяется браузером.</span><span class="sxs-lookup"><span data-stu-id="5562a-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="5562a-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="5562a-185">FrameTree</span></span> `object`

<span data-ttu-id="5562a-186">Сведения о иерархии рамок.</span><span class="sxs-lookup"><span data-stu-id="5562a-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5562a-187">Свойства</span><span class="sxs-lookup"><span data-stu-id="5562a-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5562a-188">интервал</span><span class="sxs-lookup"><span data-stu-id="5562a-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="5562a-189">Сведения о кадре для этого элемента дерева.</span><span class="sxs-lookup"><span data-stu-id="5562a-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5562a-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="5562a-190">childFrames</span></span> <br/> <i><span data-ttu-id="5562a-191">необязательные</span><span class="sxs-lookup"><span data-stu-id="5562a-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="5562a-192">Дочерние кадры.</span><span class="sxs-lookup"><span data-stu-id="5562a-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

---
description: Ссылка на домен страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools версии 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 688cc1fcfce0b81c5eed0c858a4a60b4754c49a4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571668"
---
# <span data-ttu-id="6f5e6-104">Page</span><span class="sxs-lookup"><span data-stu-id="6f5e6-104">Page</span></span>
<span data-ttu-id="6f5e6-105">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="6f5e6-106">Методы</span><span class="sxs-lookup"><span data-stu-id="6f5e6-106">Methods</span></span>**](#methods) | <span data-ttu-id="6f5e6-107">[Включение](#enable), [Отключение](#disable), [Навигация](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="6f5e6-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="6f5e6-108">События</span><span class="sxs-lookup"><span data-stu-id="6f5e6-108">Events</span></span>**](#events) | <span data-ttu-id="6f5e6-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="6f5e6-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="6f5e6-110">Типы</span><span class="sxs-lookup"><span data-stu-id="6f5e6-110">Types</span></span>**](#types) | <span data-ttu-id="6f5e6-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="6f5e6-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="6f5e6-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6f5e6-112">Methods</span></span>

### <span data-ttu-id="6f5e6-113">"Включить"</span><span class="sxs-lookup"><span data-stu-id="6f5e6-113">enable</span></span>
<span data-ttu-id="6f5e6-114">Включение уведомлений домена на странице.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="6f5e6-115">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="6f5e6-115">disable</span></span>
<span data-ttu-id="6f5e6-116">Отключение уведомлений домена на странице.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="6f5e6-117">переход</span><span class="sxs-lookup"><span data-stu-id="6f5e6-117">navigate</span></span>
<span data-ttu-id="6f5e6-118">Переход на текущую страницу по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f5e6-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-120">url</span><span class="sxs-lookup"><span data-stu-id="6f5e6-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6f5e6-121">URL-адрес для перемещения по странице.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-122">frameId</span><span class="sxs-lookup"><span data-stu-id="6f5e6-122">frameId</span></span> <br/> <i><span data-ttu-id="6f5e6-123">необязательные</span><span class="sxs-lookup"><span data-stu-id="6f5e6-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="6f5e6-124">Код кадра для навигации.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-124">Frame id to navigate.</span></span> <span data-ttu-id="6f5e6-125">Если он не указан, переходим к верхней странице.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-126">Дает</span><span class="sxs-lookup"><span data-stu-id="6f5e6-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-127">frameId</span><span class="sxs-lookup"><span data-stu-id="6f5e6-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="6f5e6-128">Код кадра, который будет использоваться для навигации.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="6f5e6-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="6f5e6-129">getFrameTree</span></span>
<span data-ttu-id="6f5e6-130">Возвращает структуру дерева кадров.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-131">Дает</span><span class="sxs-lookup"><span data-stu-id="6f5e6-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="6f5e6-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="6f5e6-133">Показать древовидную структуру фреймов.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="6f5e6-134">События</span><span class="sxs-lookup"><span data-stu-id="6f5e6-134">Events</span></span>

### <span data-ttu-id="6f5e6-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="6f5e6-135">frameAttached</span></span>
<span data-ttu-id="6f5e6-136">Срабатывает, если кадр присоединен к родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-137">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f5e6-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-138">frameId</span><span class="sxs-lookup"><span data-stu-id="6f5e6-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="6f5e6-139">Идентификатор присоединенного кадра.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="6f5e6-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="6f5e6-141">Идентификатор родительского фрейма.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-142">стека</span><span class="sxs-lookup"><span data-stu-id="6f5e6-142">stack</span></span> <br/> <i><span data-ttu-id="6f5e6-143">необязательные</span><span class="sxs-lookup"><span data-stu-id="6f5e6-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="6f5e6-144">Трассировка стека JavaScript для вложенного кадра задается только в том случае, если кадр инициирован из сценария.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="6f5e6-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="6f5e6-145">frameDetached</span></span>
<span data-ttu-id="6f5e6-146">Срабатывает, если кадр отсоединен от родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-147">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f5e6-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-148">frameId</span><span class="sxs-lookup"><span data-stu-id="6f5e6-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="6f5e6-149">Идентификатор отсоединенного кадра.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="6f5e6-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="6f5e6-150">frameNavigated</span></span>
<span data-ttu-id="6f5e6-151">Срабатывает после завершения навигации кадра.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-152">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f5e6-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-153">интервал</span><span class="sxs-lookup"><span data-stu-id="6f5e6-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="6f5e6-154">Объект Frame.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="6f5e6-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="6f5e6-155">loadEventFired</span></span>
<span data-ttu-id="6f5e6-156">Соответствует событию Window. OnLoad.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-157">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f5e6-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-158">штамп</span><span class="sxs-lookup"><span data-stu-id="6f5e6-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="6f5e6-159">Количество миллисекунд, прошедшее с момента создания эпохи.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="6f5e6-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="6f5e6-160">domContentEventFired</span></span>
<span data-ttu-id="6f5e6-161">Соответствует событию Document. onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f5e6-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-163">штамп</span><span class="sxs-lookup"><span data-stu-id="6f5e6-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="6f5e6-164">Количество миллисекунд, прошедшее с момента создания эпохи.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="6f5e6-165">Типы</span><span class="sxs-lookup"><span data-stu-id="6f5e6-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="6f5e6-166">FrameId</span><span class="sxs-lookup"><span data-stu-id="6f5e6-166">FrameId</span></span> `string`

<span data-ttu-id="6f5e6-167">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="6f5e6-168">Кадр</span><span class="sxs-lookup"><span data-stu-id="6f5e6-168">Frame</span></span> `object`

<span data-ttu-id="6f5e6-169">Сведения о кадре на странице.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-170">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f5e6-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-171">id</span><span class="sxs-lookup"><span data-stu-id="6f5e6-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="6f5e6-172">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-173">parentId</span><span class="sxs-lookup"><span data-stu-id="6f5e6-173">parentId</span></span> <br/> <i><span data-ttu-id="6f5e6-174">необязательные</span><span class="sxs-lookup"><span data-stu-id="6f5e6-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="6f5e6-175">Уникальный идентификатор родительского фрейма.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-176">name</span><span class="sxs-lookup"><span data-stu-id="6f5e6-176">name</span></span> <br/> <i><span data-ttu-id="6f5e6-177">необязательные</span><span class="sxs-lookup"><span data-stu-id="6f5e6-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6f5e6-178">Имя кадра, указанное в теге.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-179">url</span><span class="sxs-lookup"><span data-stu-id="6f5e6-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6f5e6-180">URL-адрес документа в рамке.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="6f5e6-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6f5e6-182">Источник защиты документа фрейма.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-183">Успешности</span><span class="sxs-lookup"><span data-stu-id="6f5e6-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6f5e6-184">Тип MIME документа Frame определяется браузером.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="6f5e6-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="6f5e6-185">FrameTree</span></span> `object`

<span data-ttu-id="6f5e6-186">Сведения о иерархии рамок.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6f5e6-187">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f5e6-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6f5e6-188">интервал</span><span class="sxs-lookup"><span data-stu-id="6f5e6-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="6f5e6-189">Сведения о кадре для этого элемента дерева.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6f5e6-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="6f5e6-190">childFrames</span></span> <br/> <i><span data-ttu-id="6f5e6-191">необязательные</span><span class="sxs-lookup"><span data-stu-id="6f5e6-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="6f5e6-192">Дочерние кадры.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

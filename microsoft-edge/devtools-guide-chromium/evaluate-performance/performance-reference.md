---
title: Ссылка на событие временной шкалы
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: e5f0807204877ce034fd52ea4535795ea80ba394
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611722"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="c2999-103">Ссылка на событие временной шкалы</span><span class="sxs-lookup"><span data-stu-id="c2999-103">Timeline Event Reference</span></span>   




<span data-ttu-id="c2999-104">В режиме событий временной шкалы отображаются все события, инициированные во время создания записи.</span><span class="sxs-lookup"><span data-stu-id="c2999-104">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="c2999-105">Чтобы узнать больше о каждом типе событий временной шкалы, воспользуйтесь ссылкой на событие временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="c2999-105">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="c2999-106">Общие свойства событий временной шкалы</span><span class="sxs-lookup"><span data-stu-id="c2999-106">Common timeline event properties</span></span>  

<span data-ttu-id="c2999-107">Некоторые сведения представлены в событиях всех типов, в то время как некоторые применимы только к определенным типам событий.</span><span class="sxs-lookup"><span data-stu-id="c2999-107">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="c2999-108">В этом разделе перечислены свойства, которые являются общими для различных типов событий.</span><span class="sxs-lookup"><span data-stu-id="c2999-108">This section lists properties common to different event types.</span></span>  <span data-ttu-id="c2999-109">Свойства, специфичные для определенных типов событий, перечислены в ссылках на следующие типы событий.</span><span class="sxs-lookup"><span data-stu-id="c2999-109">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="c2999-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="c2999-110">Property</span></span> | <span data-ttu-id="c2999-111">Когда оно отображается</span><span class="sxs-lookup"><span data-stu-id="c2999-111">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-112">Агрегированное время</span><span class="sxs-lookup"><span data-stu-id="c2999-112">Aggregated time</span></span> | <span data-ttu-id="c2999-113">Для событий с **вложенными событиями**— время, затраченное на каждую категорию событий.</span><span class="sxs-lookup"><span data-stu-id="c2999-113">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="c2999-114">Стек вызовов</span><span class="sxs-lookup"><span data-stu-id="c2999-114">Call Stack</span></span> | <span data-ttu-id="c2999-115">Для событий с **дочерними событиями**— время, затраченное на каждую категорию событий.</span><span class="sxs-lookup"><span data-stu-id="c2999-115">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="c2999-116">Время ЦП</span><span class="sxs-lookup"><span data-stu-id="c2999-116">CPU time</span></span> | <span data-ttu-id="c2999-117">Сколько времени ЦП потратило на записанное событие.</span><span class="sxs-lookup"><span data-stu-id="c2999-117">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="c2999-118">Сведения</span><span class="sxs-lookup"><span data-stu-id="c2999-118">Details</span></span> | <span data-ttu-id="c2999-119">Другие сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="c2999-119">Other details about the event.</span></span> |  
| <span data-ttu-id="c2999-120">Duration \ (в заметках времени \)</span><span class="sxs-lookup"><span data-stu-id="c2999-120">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="c2999-121">Сколько времени занимает событие со всеми дочерними элементами; timestamp — время возникновения события, относительно момента начала записи.</span><span class="sxs-lookup"><span data-stu-id="c2999-121">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="c2999-122">Собственное время</span><span class="sxs-lookup"><span data-stu-id="c2999-122">Self time</span></span> | <span data-ttu-id="c2999-123">Время, в течение которого событие не дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="c2999-123">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="c2999-124">Размер использованной кучи</span><span class="sxs-lookup"><span data-stu-id="c2999-124">Used Heap Size</span></span> | <span data-ttu-id="c2999-125">Объем памяти, используемой приложением, когда событие было записано, а дельта \ (+/-) изменяется в используемом размере кучи с момента последнего выборки.</span><span class="sxs-lookup"><span data-stu-id="c2999-125">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="c2999-126">Загрузка событий</span><span class="sxs-lookup"><span data-stu-id="c2999-126">Loading events</span></span>  

<span data-ttu-id="c2999-127">В этом разделе перечислены события, которые относятся к загрузке категории и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="c2999-127">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="c2999-128">Событие</span><span class="sxs-lookup"><span data-stu-id="c2999-128">Event</span></span> | <span data-ttu-id="c2999-129">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-129">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-130">Анализ HTML-кода</span><span class="sxs-lookup"><span data-stu-id="c2999-130">Parse HTML</span></span> |  <span data-ttu-id="c2999-131">Microsoft Edge запустил алгоритм синтаксического анализа HTML.</span><span class="sxs-lookup"><span data-stu-id="c2999-131">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="c2999-132">Завершить загрузку</span><span class="sxs-lookup"><span data-stu-id="c2999-132">Finish Loading</span></span> |  <span data-ttu-id="c2999-133">Сетевой запрос выполнен.</span><span class="sxs-lookup"><span data-stu-id="c2999-133">A network request completed.</span></span> |  
| <span data-ttu-id="c2999-134">Получение данных</span><span class="sxs-lookup"><span data-stu-id="c2999-134">Receive Data</span></span> |  <span data-ttu-id="c2999-135">Получены данные для запроса.</span><span class="sxs-lookup"><span data-stu-id="c2999-135">Data for a request was received.</span></span>  <span data-ttu-id="c2999-136">Одно или несколько событий приема данных.</span><span class="sxs-lookup"><span data-stu-id="c2999-136">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="c2999-137">Получение ответа</span><span class="sxs-lookup"><span data-stu-id="c2999-137">Receive Response</span></span> |  <span data-ttu-id="c2999-138">Первоначальный ответ HTTP из запроса.</span><span class="sxs-lookup"><span data-stu-id="c2999-138">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="c2999-139">Отправить запрос</span><span class="sxs-lookup"><span data-stu-id="c2999-139">Send Request</span></span> |  <span data-ttu-id="c2999-140">Сетевой запрос отправлен.</span><span class="sxs-lookup"><span data-stu-id="c2999-140">A network request has been sent.</span></span> |  

### <span data-ttu-id="c2999-141">Загрузка свойств событий</span><span class="sxs-lookup"><span data-stu-id="c2999-141">Loading event properties</span></span>  

| <span data-ttu-id="c2999-142">Свойство</span><span class="sxs-lookup"><span data-stu-id="c2999-142">Property</span></span> | <span data-ttu-id="c2999-143">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-143">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-144">Ресурс</span><span class="sxs-lookup"><span data-stu-id="c2999-144">Resource</span></span> | <span data-ttu-id="c2999-145">URL-адрес запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2999-145">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="c2999-146">Preview</span><span class="sxs-lookup"><span data-stu-id="c2999-146">Preview</span></span> | <span data-ttu-id="c2999-147">Предварительный просмотр запрашиваемого ресурса \ (только изображения \).</span><span class="sxs-lookup"><span data-stu-id="c2999-147">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="c2999-148">Метод запроса</span><span class="sxs-lookup"><span data-stu-id="c2999-148">Request Method</span></span> | <span data-ttu-id="c2999-149">Метод HTTP, используемый для запроса ( `GET` `POST` например, "\").</span><span class="sxs-lookup"><span data-stu-id="c2999-149">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="c2999-150">Код состояния</span><span class="sxs-lookup"><span data-stu-id="c2999-150">Status Code</span></span> | <span data-ttu-id="c2999-151">Код ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="c2999-151">HTTP response code.</span></span> |  
| <span data-ttu-id="c2999-152">Тип MIME</span><span class="sxs-lookup"><span data-stu-id="c2999-152">MIME Type</span></span> | <span data-ttu-id="c2999-153">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2999-153">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="c2999-154">Длина закодированных данных</span><span class="sxs-lookup"><span data-stu-id="c2999-154">Encoded Data Length</span></span> | <span data-ttu-id="c2999-155">Длина запрашиваемого ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="c2999-155">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="c2999-156">События сценария</span><span class="sxs-lookup"><span data-stu-id="c2999-156">Scripting events</span></span>  

<span data-ttu-id="c2999-157">В этом разделе перечислены события, которые относятся к категории сценариев и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="c2999-157">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="c2999-158">Событие</span><span class="sxs-lookup"><span data-stu-id="c2999-158">Event</span></span> | <span data-ttu-id="c2999-159">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-159">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-160">Кадр анимации, срабатывающий</span><span class="sxs-lookup"><span data-stu-id="c2999-160">Animation Frame Fired</span></span> | <span data-ttu-id="c2999-161">Назначенный кадр анимации, а также его обработчик обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c2999-161">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="c2999-162">Отмена анимации кадра</span><span class="sxs-lookup"><span data-stu-id="c2999-162">Cancel Animation Frame</span></span> |  <span data-ttu-id="c2999-163">Запланированный кадр анимации был отменен.</span><span class="sxs-lookup"><span data-stu-id="c2999-163">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="c2999-164">Событие GC</span><span class="sxs-lookup"><span data-stu-id="c2999-164">GC Event</span></span> |  <span data-ttu-id="c2999-165">Произошел сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="c2999-165">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="c2999-166">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="c2999-166">DOMContentLoaded</span></span> |  <span data-ttu-id="c2999-167">[Событие DOMContentLoaded][MDNWindowDOMContentLoadedEvent] было инициировано браузером.</span><span class="sxs-lookup"><span data-stu-id="c2999-167">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="c2999-168">Это событие возникает, когда все содержимое модели DOM страницы загружено и проанализировано.</span><span class="sxs-lookup"><span data-stu-id="c2999-168">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="c2999-169">Оценка сценария</span><span class="sxs-lookup"><span data-stu-id="c2999-169">Evaluate Script</span></span> | <span data-ttu-id="c2999-170">Вычислен сценарий.</span><span class="sxs-lookup"><span data-stu-id="c2999-170">A script was evaluated.</span></span> |  
| <span data-ttu-id="c2999-171">Событие</span><span class="sxs-lookup"><span data-stu-id="c2999-171">Event</span></span> | <span data-ttu-id="c2999-172">Событие JavaScript \ (например, `mousedown` или `key` \).</span><span class="sxs-lookup"><span data-stu-id="c2999-172">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="c2999-173">Вызов функции</span><span class="sxs-lookup"><span data-stu-id="c2999-173">Function Call</span></span> | <span data-ttu-id="c2999-174">Сделан вызов функции JavaScript верхнего уровня (появляется только в том случае, если браузер входит в ядро JavaScript).</span><span class="sxs-lookup"><span data-stu-id="c2999-174">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="c2999-175">Установка таймера</span><span class="sxs-lookup"><span data-stu-id="c2999-175">Install Timer</span></span> | <span data-ttu-id="c2999-176">Таймер создан с помощью [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] или [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="c2999-176">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="c2999-177">Кадр анимации запроса</span><span class="sxs-lookup"><span data-stu-id="c2999-177">Request Animation Frame</span></span> | <span data-ttu-id="c2999-178">`requestAnimationFrame()`Звонок, запланированный новым кадром.</span><span class="sxs-lookup"><span data-stu-id="c2999-178">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="c2999-179">Удалить таймер</span><span class="sxs-lookup"><span data-stu-id="c2999-179">Remove Timer</span></span> | <span data-ttu-id="c2999-180">Ранее созданный таймер был очищен.</span><span class="sxs-lookup"><span data-stu-id="c2999-180">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="c2999-181">Время</span><span class="sxs-lookup"><span data-stu-id="c2999-181">Time</span></span> |  <span data-ttu-id="c2999-182">Сценарий, именуемый [Console. Time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="c2999-182">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="c2999-183">Время окончания</span><span class="sxs-lookup"><span data-stu-id="c2999-183">Time End</span></span> | <span data-ttu-id="c2999-184">Сценарий, именуемый [Console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="c2999-184">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="c2999-185">Таймер запущен</span><span class="sxs-lookup"><span data-stu-id="c2999-185">Timer Fired</span></span> | <span data-ttu-id="c2999-186">Таймер, который был запланирован с помощью `setInterval()` или `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="c2999-186">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="c2999-187">Изменение состояния XHR Ready</span><span class="sxs-lookup"><span data-stu-id="c2999-187">XHR Ready State Change</span></span> | <span data-ttu-id="c2999-188">Состояние готовности XMLHTTPRequest изменилось.</span><span class="sxs-lookup"><span data-stu-id="c2999-188">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="c2999-189">Загрузка XHR</span><span class="sxs-lookup"><span data-stu-id="c2999-189">XHR Load</span></span> | <span data-ttu-id="c2999-190">`XMLHTTPRequest`Загрузка завершена.</span><span class="sxs-lookup"><span data-stu-id="c2999-190">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="c2999-191">Свойства событий в сценариях</span><span class="sxs-lookup"><span data-stu-id="c2999-191">Scripting event properties</span></span>  

| <span data-ttu-id="c2999-192">Свойство</span><span class="sxs-lookup"><span data-stu-id="c2999-192">Property</span></span> | <span data-ttu-id="c2999-193">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-193">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-194">КОД таймера</span><span class="sxs-lookup"><span data-stu-id="c2999-194">Timer ID</span></span> | <span data-ttu-id="c2999-195">Идентификатор таймера.</span><span class="sxs-lookup"><span data-stu-id="c2999-195">The timer ID.</span></span> |  
| <span data-ttu-id="c2999-196">Превышено время ожидания</span><span class="sxs-lookup"><span data-stu-id="c2999-196">Timeout</span></span> | <span data-ttu-id="c2999-197">Время ожидания, указанное в таймере.</span><span class="sxs-lookup"><span data-stu-id="c2999-197">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="c2999-198">Повторяет</span><span class="sxs-lookup"><span data-stu-id="c2999-198">Repeats</span></span> | <span data-ttu-id="c2999-199">Логическое значение, определяющее, повторяется ли таймер.</span><span class="sxs-lookup"><span data-stu-id="c2999-199">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="c2999-200">Вызов функции</span><span class="sxs-lookup"><span data-stu-id="c2999-200">Function Call</span></span> | <span data-ttu-id="c2999-201">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="c2999-201">A function that was invoked.</span></span> |  

## <span data-ttu-id="c2999-202">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="c2999-202">Rendering events</span></span>  

<span data-ttu-id="c2999-203">В этом разделе перечислены события, которые относятся к категории отрисовки и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="c2999-203">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="c2999-204">Событие</span><span class="sxs-lookup"><span data-stu-id="c2999-204">Event</span></span> | <span data-ttu-id="c2999-205">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-205">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-206">Недействительный макет</span><span class="sxs-lookup"><span data-stu-id="c2999-206">Invalidate layout</span></span> | <span data-ttu-id="c2999-207">Макет страницы был аннулирован при изменении модели DOM.</span><span class="sxs-lookup"><span data-stu-id="c2999-207">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="c2999-208">Макет</span><span class="sxs-lookup"><span data-stu-id="c2999-208">Layout</span></span> | <span data-ttu-id="c2999-209">Макет страницы завершен.</span><span class="sxs-lookup"><span data-stu-id="c2999-209">A page layout was completed.</span></span> |  
| <span data-ttu-id="c2999-210">Пересчитать стиль</span><span class="sxs-lookup"><span data-stu-id="c2999-210">Recalculate style</span></span> | <span data-ttu-id="c2999-211">Стили элементов, пересчитанные Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c2999-211">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="c2999-212">Scroll</span><span class="sxs-lookup"><span data-stu-id="c2999-212">Scroll</span></span> | <span data-ttu-id="c2999-213">Содержимое вложенного представления было прокручено.</span><span class="sxs-lookup"><span data-stu-id="c2999-213">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="c2999-214">Свойства событий отрисовки</span><span class="sxs-lookup"><span data-stu-id="c2999-214">Rendering event properties</span></span>  

| <span data-ttu-id="c2999-215">Свойство</span><span class="sxs-lookup"><span data-stu-id="c2999-215">Property</span></span> | <span data-ttu-id="c2999-216">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-216">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-217">Макет "недействителен"</span><span class="sxs-lookup"><span data-stu-id="c2999-217">Layout invalidated</span></span> | <span data-ttu-id="c2999-218">Для записей макета трассировка стека кода, который привел к недействительности макета.</span><span class="sxs-lookup"><span data-stu-id="c2999-218">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="c2999-219">Узлы, для которых нужен макет</span><span class="sxs-lookup"><span data-stu-id="c2999-219">Nodes that need layout</span></span> | <span data-ttu-id="c2999-220">Для записей макета — количество узлов, которые были помечены как нужные макеты до начала перекомпоновки.</span><span class="sxs-lookup"><span data-stu-id="c2999-220">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="c2999-221">Обычно это узлы, которые были аннулированы кодом разработчика, и путь вверх, чтобы переадресовать корневой макет.</span><span class="sxs-lookup"><span data-stu-id="c2999-221">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="c2999-222">Размер дерева макета</span><span class="sxs-lookup"><span data-stu-id="c2999-222">Layout tree size</span></span> | <span data-ttu-id="c2999-223">Для записей макета — общее количество узлов в корне перемакета (узел, на котором Microsoft Edge запускает перекомпоновку).</span><span class="sxs-lookup"><span data-stu-id="c2999-223">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="c2999-224">Область макета</span><span class="sxs-lookup"><span data-stu-id="c2999-224">Layout scope</span></span> | <span data-ttu-id="c2999-225">Возможные значения: `Partial` \ (граница макета — часть DOM \) или `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="c2999-225">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="c2999-226">Затронутые элементы</span><span class="sxs-lookup"><span data-stu-id="c2999-226">Elements affected</span></span> | <span data-ttu-id="c2999-227">Для пересчета записей стилей — количество элементов, затронутых с помощью пересчета стилей.</span><span class="sxs-lookup"><span data-stu-id="c2999-227">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="c2999-228">Недействительные стили</span><span class="sxs-lookup"><span data-stu-id="c2999-228">Styles invalidated</span></span> | <span data-ttu-id="c2999-229">Для пересчета записей стилей — трассировка стека кода, который вызвал недействительность стиля.</span><span class="sxs-lookup"><span data-stu-id="c2999-229">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="c2999-230">События рисования</span><span class="sxs-lookup"><span data-stu-id="c2999-230">Painting events</span></span>  

<span data-ttu-id="c2999-231">В этом разделе перечислены события, которые относятся к категории "раскрасить" и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="c2999-231">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="c2999-232">Событие</span><span class="sxs-lookup"><span data-stu-id="c2999-232">Event</span></span> | <span data-ttu-id="c2999-233">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-233">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-234">Составные слои</span><span class="sxs-lookup"><span data-stu-id="c2999-234">Composite Layers</span></span> | <span data-ttu-id="c2999-235">Составные слои изображений для модуля отрисовки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c2999-235">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="c2999-236">Декодирование изображений</span><span class="sxs-lookup"><span data-stu-id="c2999-236">Image Decode</span></span> | <span data-ttu-id="c2999-237">Перекодировано ресурс изображения.</span><span class="sxs-lookup"><span data-stu-id="c2999-237">An image resource was decoded.</span></span> |  
| <span data-ttu-id="c2999-238">Изменение размера изображения</span><span class="sxs-lookup"><span data-stu-id="c2999-238">Image Resize</span></span> | <span data-ttu-id="c2999-239">Размер изображения был изменен с помощью собственных размеров.</span><span class="sxs-lookup"><span data-stu-id="c2999-239">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="c2999-240">Paint</span><span class="sxs-lookup"><span data-stu-id="c2999-240">Paint</span></span> | <span data-ttu-id="c2999-241">Составные слои были окрашены в область экрана.</span><span class="sxs-lookup"><span data-stu-id="c2999-241">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="c2999-242">При наведении указателя мыши на запись Paint выделена область экрана, которая была обновлена.</span><span class="sxs-lookup"><span data-stu-id="c2999-242">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="c2999-243">Свойства событий рисования</span><span class="sxs-lookup"><span data-stu-id="c2999-243">Painting event properties</span></span>  

| <span data-ttu-id="c2999-244">Свойство</span><span class="sxs-lookup"><span data-stu-id="c2999-244">Property</span></span> | <span data-ttu-id="c2999-245">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-245">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c2999-246">Местоположение</span><span class="sxs-lookup"><span data-stu-id="c2999-246">Location</span></span> | <span data-ttu-id="c2999-247">Для событий Paint координаты x и y прямоугольника рисования.</span><span class="sxs-lookup"><span data-stu-id="c2999-247">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="c2999-248">Кодов</span><span class="sxs-lookup"><span data-stu-id="c2999-248">Dimensions</span></span> | <span data-ttu-id="c2999-249">Для событий рисования — высота и Ширина закрашиваемой области.</span><span class="sxs-lookup"><span data-stu-id="c2999-249">For Paint events, the height and width of the painted region.</span></span> |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Справочник по API для консоли времени"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "Справочник по API для timeEnd-Console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Окно: DOMContentLoaded событие | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="c2999-255">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c2999-255">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c2999-256">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) и [Meggin Kearney][MegginKearney] \ (технический редактор \) и [Flavioной][FlavioCopes] — для разработчиков с полным комплектом.</span><span class="sxs-lookup"><span data-stu-id="c2999-256">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c2999-258">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c2999-258">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  

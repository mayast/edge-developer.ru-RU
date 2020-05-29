---
description: Функции, добавленные в Microsoft Edge DevTools в обновлении Windows 10 для дизайнеров (EdgeHTML 16)
title: DevTools в EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, edgehtml 16
ms.custom: seodec18
ms.openlocfilehash: 78ede81e022cc8f0f623ecd33fd2303314ec9cb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571706"
---
# <span data-ttu-id="df529-104">DevTools в обновлении Windows 10 для дизайнеров (EdgeHTML 16)</span><span class="sxs-lookup"><span data-stu-id="df529-104">DevTools in the Windows 10 Fall Creators Update (EdgeHTML 16)</span></span>

<span data-ttu-id="df529-105">В этом выпуске мы начали DevTools рефакторинга, чтобы улучшить надежность и производительность, а также добавили целый ряд новых функций, которые можно приступить к работе сегодня!</span><span class="sxs-lookup"><span data-stu-id="df529-105">With this release we started a major DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today!</span></span> 

<span data-ttu-id="df529-106">Ниже указаны функции Microsoft Edge DevTools, которые поставлялись вместе с [обновлением для дизайнеров Windows 10](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span><span class="sxs-lookup"><span data-stu-id="df529-106">Here are the Microsoft Edge DevTools features that shipped with the [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span></span>

## <span data-ttu-id="df529-107">Прослушиватели событий предков</span><span class="sxs-lookup"><span data-stu-id="df529-107">Ancestor event listeners</span></span> 

<span data-ttu-id="df529-108">Теперь область **событий** добавляет параметр для просмотра прослушивателей событий, зарегистрированных на любом предке выделенного элемента (на панели **элементы** ) в дополнение к тем, которые находятся в самом элементе.</span><span class="sxs-lookup"><span data-stu-id="df529-108">The **Events** pane now adds the option to view event listeners registered on any ancestor of the currently selected element (in the **Elements** panel), in addition to those on the element itself.</span></span> <span data-ttu-id="df529-109">Кроме того, теперь можно сгруппировать прослушиватель событий в виде *события* или *элемента*.</span><span class="sxs-lookup"><span data-stu-id="df529-109">Additionally, you can now group the event listener display by either *Event* or *Element*.</span></span> 

![Область проверки прослушивателя событий](../media/elements_ancestor_events.png)

## <span data-ttu-id="df529-111">Контрольные точки изменений DOM</span><span class="sxs-lookup"><span data-stu-id="df529-111">DOM mutation breakpoints</span></span>

<span data-ttu-id="df529-112">Теперь вы можете настроить точки останова для изменений DOM, чтобы при каждом изменении выбранного узла элемента прерывать работу отладчика.</span><span class="sxs-lookup"><span data-stu-id="df529-112">You can now set DOM mutation breakpoints to break into the Debugger whenever a selected element node changes.</span></span> <span data-ttu-id="df529-113">На панели **элементы** с помощью команды RT щелкните любой элемент в представлении дерева DOM и выберите один или несколько из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="df529-113">From the **Elements** panel, rt-click on any element in the DOM tree view and select one or more of the following:</span></span>

 - <span data-ttu-id="df529-114">Прерывание на удаленном узле</span><span class="sxs-lookup"><span data-stu-id="df529-114">Break on Node removed</span></span>
 - <span data-ttu-id="df529-115">Прерывать на поддереве изменено</span><span class="sxs-lookup"><span data-stu-id="df529-115">Break on Subtree modified</span></span>
 - <span data-ttu-id="df529-116">Прерывать на измененных атрибутах</span><span class="sxs-lookup"><span data-stu-id="df529-116">Break on Attribute modified</span></span>

<span data-ttu-id="df529-117">Вы можете управлять контрольными точками для изменений из области **точки останова DOM** на панелях **элементы** или **отладчик** .</span><span class="sxs-lookup"><span data-stu-id="df529-117">You can manage your mutation breakpoints from the **DOM breakpoints** pane in the **Elements** or **Debugger** panels.</span></span>

![Область точек останова DOM](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="df529-119">Поддержка правил CSS в правилах</span><span class="sxs-lookup"><span data-stu-id="df529-119">CSS at-rule support</span></span>

<span data-ttu-id="df529-120">Правила CSS "at" (@) теперь представлены среди других объявлений правил CSS в области " **стили** ", включая `@keyframes` правила анимации (в данный момент только для чтения), `@supports` запросы функций и `@media` запросы.</span><span class="sxs-lookup"><span data-stu-id="df529-120">CSS "at" (@) rules are now represented among other CSS rule declarations on the **Styles** pane, including animation `@keyframes` rules (currently limited to read-only), `@supports` feature queries, and `@media` queries.</span></span>

![Проверка правил CSS из области "стиль DevTools"](../media/elements_at_rules.png)

## <span data-ttu-id="df529-122">Область «шрифты CSS»</span><span class="sxs-lookup"><span data-stu-id="df529-122">CSS fonts pane</span></span>

<span data-ttu-id="df529-123">`@font-face`Правила CSS теперь содержат собственную выделенную область **шрифтов** , которая показывает, где загружается шрифт (*Локальная* или *сеть*) и сколько знаков используется.</span><span class="sxs-lookup"><span data-stu-id="df529-123">CSS `@font-face` rules now have their own dedicated **Fonts** pane that displays where the font is loaded from (*Local* or *Network*) and how many characters are using it.</span></span> <span data-ttu-id="df529-124">Если шрифт загружен из сети, DevTools отобразит правило, которое его импортировало вместе с его псевдонимом и типом шрифта.</span><span class="sxs-lookup"><span data-stu-id="df529-124">If a font is loaded from the network,  DevTools will display the rule that imported it along with its alias and font type.</span></span>

![Сведения о шрифтах CSS](../media/elements_fonts.png)

## <span data-ttu-id="df529-126">Поддержка псевдо-элементов CSS</span><span class="sxs-lookup"><span data-stu-id="df529-126">CSS pseudo-element support</span></span>

<span data-ttu-id="df529-127">Область **стили** теперь группирует псевдо-элементы в своих заголовках и больше не отображает их содержимое как перечеркнутым.</span><span class="sxs-lookup"><span data-stu-id="df529-127">The **Styles** pane now groups pseudo-elements under their own headings and no longer displays their content as crossed out.</span></span>

**<span data-ttu-id="df529-128">До:</span><span class="sxs-lookup"><span data-stu-id="df529-128">Before:</span></span>**
<br>
![Ранее созданное содержимое было перепутано](../media/gc_before.png)

**<span data-ttu-id="df529-130">После:</span><span class="sxs-lookup"><span data-stu-id="df529-130">After:</span></span>**
<br>
![Сгенерированный контент больше не отображается с зачеркиванием](../media/gc_after.png)

## <span data-ttu-id="df529-132">Улучшенная консоль</span><span class="sxs-lookup"><span data-stu-id="df529-132">Console improvements</span></span>

<span data-ttu-id="df529-133">**Консольная** панель получила пересмотренное средство для повышения удобства использования и более быстрой и более функциональной функции IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="df529-133">The **Console** panel got a UX overhaul for improved usability and a faster, richer Intellisense experience.</span></span>

<span data-ttu-id="df529-134">**До:** 
![ Предыдущая консоль</span><span class="sxs-lookup"><span data-stu-id="df529-134">**Before:**
![Previous console</span></span>](../media/console_old.png)

<span data-ttu-id="df529-135">**После:** 
![ Новая консоль</span><span class="sxs-lookup"><span data-stu-id="df529-135">**After:**
![New console</span></span>](../media/console_new.png)

<span data-ttu-id="df529-136">Кроме того, добавлены следующие улучшения:</span><span class="sxs-lookup"><span data-stu-id="df529-136">We also added these improvements:</span></span>

 -  <span data-ttu-id="df529-137">Используйте `Shift + Enter` для добавления к команде дополнительной строки перед ее выполнением `Enter` .</span><span class="sxs-lookup"><span data-stu-id="df529-137">Use `Shift + Enter` to add an additional line to a command before executing it with `Enter`.</span></span> <span data-ttu-id="df529-138">(Ранее был *переключен на выключатель многострочного и однострочного режима* .)</span><span class="sxs-lookup"><span data-stu-id="df529-138">(Formerly there was a *Switch to multiline/single-line mode* toggle button.)</span></span>

 - <span data-ttu-id="df529-139">Поддерживаются следующие новые API:</span><span class="sxs-lookup"><span data-stu-id="df529-139">The following new APIs are supported:</span></span>
    - <span data-ttu-id="df529-140">метод [**Console. Table (***объект***)**](../console/console-api.md#organizing-log-output)</span><span class="sxs-lookup"><span data-stu-id="df529-140">[**console.table(***object***)**](../console/console-api.md#organizing-log-output) method</span></span>
    - <span data-ttu-id="df529-141">[**getEventListeners (***объект***)**](../console/command-line.md#event-listeners) , команда</span><span class="sxs-lookup"><span data-stu-id="df529-141">[**getEventListeners(***object***)**](../console/command-line.md#event-listeners) command</span></span>
    - <span data-ttu-id="df529-142">[**клавиша (***объект***)**](../console/command-line.md#object-inspection) , команда</span><span class="sxs-lookup"><span data-stu-id="df529-142">[**keys(***object***)**](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="df529-143">Команда [**"значения (***объект***)"**](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="df529-143">[**values(***object***)**](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="df529-144">Выбор [**$x (***выражение XPath***)**](../console/command-line.md#dom-selectors)</span><span class="sxs-lookup"><span data-stu-id="df529-144">[**$x(***xpath expression***)**](../console/command-line.md#dom-selectors) selector</span></span>

 - <span data-ttu-id="df529-145">Параметр форматирования [**% c ()**](../console/console-api.md#logging-custom-messages) теперь поддерживается</span><span class="sxs-lookup"><span data-stu-id="df529-145">The [**%c()**](../console/console-api.md#logging-custom-messages) formatting parameter is now supported</span></span>

## <span data-ttu-id="df529-146">Улучшенная Отладка</span><span class="sxs-lookup"><span data-stu-id="df529-146">Debugging improvements</span></span>

<span data-ttu-id="df529-147">В дополнение к набору новых функций для отладки [рабочих процессов и кэша служб PWA](#progressive-web-app-debugging)отладчик добавил следующие функции:</span><span class="sxs-lookup"><span data-stu-id="df529-147">In addition to a suite of new features for debugging your [PWA service workers and cache](#progressive-web-app-debugging), the Debugger added these features:</span></span>

### <span data-ttu-id="df529-148">Консолидированная Отладка для общих ресурсов</span><span class="sxs-lookup"><span data-stu-id="df529-148">Consolidated debugging for shared resources</span></span>

<span data-ttu-id="df529-149">Даже если ресурс (например, загруженный из сети CDN) упоминается в вашем коде несколько моментов времени, DevTools предоставит один экземпляр отладки для этого файла, в котором затем можно задать общие точки останова, которые будут выполняться вне зависимости от того, где он указан.</span><span class="sxs-lookup"><span data-stu-id="df529-149">Even when a resource, such as a file loaded from CDN, is referenced multiple times throughout your code,  DevTools will now provide a single debugging instance for that file where you can then set common breakpoints which will be hit regardless of where that file is referenced.</span></span> <span data-ttu-id="df529-150">(Ранее каждая ссылка на сценарий рассматривается как уникальный ресурс, который будет сопоставлен отдельному набору точек останова.)</span><span class="sxs-lookup"><span data-stu-id="df529-150">(Previously each script reference was considered a unique resource would map to a separate set of breakpoints.)</span></span>

### <span data-ttu-id="df529-151">Динамическое редактирование JavaScript с *неактивным редактированием*</span><span class="sxs-lookup"><span data-stu-id="df529-151">Live edit JavaScript with *Edit-on-idle*</span></span>

<span data-ttu-id="df529-152">Теперь вы можете редактировать JavaScript в течение сеанса отладки.</span><span class="sxs-lookup"><span data-stu-id="df529-152">You can now edit your JavaScript live during a debugging session.</span></span> <span data-ttu-id="df529-153">Эта функция была поэкспериментна (за пометкой) в [предыдущем](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) выпуске (*Windows 10 Creators Update*), и теперь она является постоянной функцией.</span><span class="sxs-lookup"><span data-stu-id="df529-153">This feature was experimentally available (behind a flag) in the [previous](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) release and now its a permanent feature.</span></span> <span data-ttu-id="df529-154">Просто выберите любой файл сценария на панели **отладчик** , нажмите кнопку изменить, а затем — **сохранить** (или `Ctrl+S` ), чтобы протестировать изменения при следующем запуске раздела кода.</span><span class="sxs-lookup"><span data-stu-id="df529-154">Simply select any script file from the **Debugger** panel, edit, then click **Save** (or `Ctrl+S`) to test your changes next time that section of code runs.</span></span> 

![Отладчик позволяет выполнять сценарий динамического редактирования и вносить в него изменения.](../media/debugger_edit_buttons.png) 

<span data-ttu-id="df529-156">Нажмите кнопку **сравнить документ с оригиналом** , чтобы просмотреть сведения о том, что вы изменили.</span><span class="sxs-lookup"><span data-stu-id="df529-156">Click the **Compare document to original** button to view the diff of what you changed.</span></span>

![Представление изменения кода в отладчике](../media/debugger_edit_code.png) 

<span data-ttu-id="df529-158">Обратите внимание на перечисленные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="df529-158">Please be aware of the following constraints:</span></span>

- <span data-ttu-id="df529-159">Редактирование сценария работает только во внешних *JS* -файлах (и не внедряется `<script>` в *Формат HTML*).</span><span class="sxs-lookup"><span data-stu-id="df529-159">Script editing only works in external *.js* files (and not embedded `<script>` within *.html*)</span></span>
- <span data-ttu-id="df529-160">Изменения сохраняются в памяти и удаляются при повторной загрузке документа, поэтому вы не сможете выполнять изменения внутри `DOMContentLoaded` обработчика, например</span><span class="sxs-lookup"><span data-stu-id="df529-160">Edits are saved in memory and flushed when the document is reloaded, thus you won’t be able to run edits inside a `DOMContentLoaded` handler, for example</span></span>
- <span data-ttu-id="df529-161">В настоящее время ни один из вариантов (например, " **Сохранить как** ") не позволяет сохранять изменения на диске из DevTools</span><span class="sxs-lookup"><span data-stu-id="df529-161">Currently there’s no way (such as a **Save As** option) to save your edits to disk from  DevTools</span></span>

## <span data-ttu-id="df529-162">Горячие</span><span class="sxs-lookup"><span data-stu-id="df529-162">Shortcuts</span></span>

<span data-ttu-id="df529-163">Теперь вы можете запустить DevTools на последней панели просмотра ( `Ctrl+Shift+I` ) или непосредственно на консоли ( `Ctrl+Shift+J` ) так же, как и в других крупных браузерах.</span><span class="sxs-lookup"><span data-stu-id="df529-163">You can now launch DevTools to the last viewed panel (`Ctrl+Shift+I`) or directly to the Console (`Ctrl+Shift+J`) just like you would on other major browsers.</span></span>

## <span data-ttu-id="df529-164">Отладка последовательного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="df529-164">Progressive Web App debugging</span></span>

<span data-ttu-id="df529-165">Протестируйте экспериментальную поддержку для последовательного веб-приложения (PWAs) в Microsoft EDGE и DevTools, выбрав параметр **включить сотрудников службы** `about:flags` (и перезапустить Microsoft EDGE).</span><span class="sxs-lookup"><span data-stu-id="df529-165">Test out the experimental support for Progressive Web Apps (PWAs) in Microsoft Edge and  DevTools by selecting the **Enable service workers** option from `about:flags` (and restarting Microsoft Edge).</span></span> <span data-ttu-id="df529-166">Если на сайте используются **Служебные сотрудники** и (или) API **кэша** , они будут заполнены на панели **отладчика** для каждого происхождения, как в веб-хранилище и проверки файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="df529-166">If a site makes use of **Service Workers** and/or the **Cache** API,  will populate entries in the **Debugger** panel for each origin, similar to how web storage and cookie inspection work.</span></span>

<span data-ttu-id="df529-167">Если щелкнуть определенную запись сотрудника службы, откроется **Обзор рабочего процесса**, в котором можно управлять регистрацией рабочего процесса для заданной области и принудительно инициировать принудительное извещение.</span><span class="sxs-lookup"><span data-stu-id="df529-167">Clicking on a specific service worker entry will open up the **Service Worker Overview**, where you can manage the service worker registration for the given scope and force a test push notification.</span></span> <span data-ttu-id="df529-168">Вы также можете **остановить** / **Запуск** отдельных сотрудников службы и **Просмотреть** их в отдельном окне отладчика:</span><span class="sxs-lookup"><span data-stu-id="df529-168">You can also **Stop**/**Start** individual service workers and **Inspect** them from a separate debugger window:</span></span>

![Область "Общие сведения о сотруднике службы"](../media/debugger_sw_overview.png)

<span data-ttu-id="df529-170">Обратите внимание на следующие сведения об отладке рабочих процессов службы.</span><span class="sxs-lookup"><span data-stu-id="df529-170">Please note the following about service worker debugging:</span></span>

 - <span data-ttu-id="df529-171">При отладке сотрудника службы будет запущен новый экземпляр DevTools отдельно от инструментов страницы, так как работники служб могут совместно работать на нескольких вкладках.</span><span class="sxs-lookup"><span data-stu-id="df529-171">Debugging a service worker will launch a new instance of the DevTools separate from the page's tools because service workers can be shared across multiple tabs.</span></span> 
 - <span data-ttu-id="df529-172">[Элементы](../elements.md) и панели [эмуляции](../emulation.md) отсутствуют в отладчике рабочих процессов служб, если сотрудники служб работают в фоновом режиме и не управляют непосредственно интерфейсом приложения.</span><span class="sxs-lookup"><span data-stu-id="df529-172">The [Elements](../elements.md) and [Emulation](../emulation.md) panels are absent from the service worker debugger, given that service workers run in the background and do not directly control the front-end of your app.</span></span>
 - <span data-ttu-id="df529-173">Сетевой трафик для сотрудника службы сообщается только из экземпляра отладки DevTools для этого работника, а не из центрального экземпляра самой страницы.</span><span class="sxs-lookup"><span data-stu-id="df529-173">Currently network traffic for a service worker is only reported from the DevTools debugging instance for that worker, and not from the central instance for the page itself.</span></span>

<span data-ttu-id="df529-174">При нажатии на определенную запись кэша откроется диспетчер **кэша** , в котором можно проверить и при необходимости удалить записи кэша (пары ключ-значение для*запроса* и *ответа* ).</span><span class="sxs-lookup"><span data-stu-id="df529-174">Clicking on a specific cache entry will open up the **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs).</span></span>
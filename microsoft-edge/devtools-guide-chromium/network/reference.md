---
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: ec8969fbf7b54512f00120ac4a253b952c55768f
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844021"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="e340a-103">Справочник по анализу сети</span><span class="sxs-lookup"><span data-stu-id="e340a-103">Network Analysis Reference</span></span>  

<span data-ttu-id="e340a-104">Ознакомьтесь с новыми способами для анализа того, как страница загружается в этой полной версии справочника по функциям сетевого анализа Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e340a-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="e340a-105">Запись сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="e340a-105">Record network requests</span></span>  

<span data-ttu-id="e340a-106">По умолчанию DevTools записывает все сетевые запросы на панели "сеть", пока не откроете DevTools.</span><span class="sxs-lookup"><span data-stu-id="e340a-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель "сеть"" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="e340a-108">Рисунок 1: панель " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="e340a-108">Figure 1:  The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-109">Прекращение записи сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="e340a-109">Stop recording network requests</span></span>  

<span data-ttu-id="e340a-110">Чтобы остановить запись запросов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-110">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="e340a-111">Выберите **остановить запись** остановка записи сетевого журнала ![ ][ImageRecordOnIcon] на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="e340a-111">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="e340a-112">Оно превращается в серый, чтобы показать, что DevTools больше не записывает запросы.</span><span class="sxs-lookup"><span data-stu-id="e340a-112">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="e340a-113">Нажимайте клавиши `Control` + `E` \ (Windows \) или `Command` + `E` \ (macOS \), пока фокус находится на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="e340a-113">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="e340a-114">Очистка запросов</span><span class="sxs-lookup"><span data-stu-id="e340a-114">Clear requests</span></span>  

<span data-ttu-id="e340a-115">**Clear** ![ ][ImageClearIcon] Чтобы очистить все запросы из таблицы "запросы", на панели "сеть" нажмите кнопку Clear Clear.</span><span class="sxs-lookup"><span data-stu-id="e340a-115">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка "очистить"" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="e340a-117">Рисунок 2: кнопка " **очистить** "</span><span class="sxs-lookup"><span data-stu-id="e340a-117">Figure 2:  The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-118">Сохранение запросов на загрузку страниц</span><span class="sxs-lookup"><span data-stu-id="e340a-118">Save requests across page loads</span></span>  

<span data-ttu-id="e340a-119">Для сохранения запросов на страницах загрузок на панели "сеть" установите флажок **сохранить журнал** .</span><span class="sxs-lookup"><span data-stu-id="e340a-119">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="e340a-120">DevTools сохраняет все запросы, пока не отключайте параметр **сохранить журнал**.</span><span class="sxs-lookup"><span data-stu-id="e340a-120">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Флажок "сохранить журнал"" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="e340a-122">Рисунок 3: флажок " **сохранить журнал** "</span><span class="sxs-lookup"><span data-stu-id="e340a-122">Figure 3:  The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-123">Захват снимков экрана при загрузке страницы</span><span class="sxs-lookup"><span data-stu-id="e340a-123">Capture screenshots during page load</span></span>  

<span data-ttu-id="e340a-124">Выведите снимки экрана, чтобы проанализировать, какие пользователи видят при ожидании загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="e340a-124">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="e340a-125">Чтобы включить снимки экрана, нажмите кнопку **Параметры сети** и выберите команду **захватить снимки экрана** на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="e340a-125">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="e340a-126">Обновите страницу, когда фокус находится на панели " **сеть** ", чтобы захватить снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="e340a-126">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="e340a-127">После захвата снимка экрана вы взаимодействуете с ним следующими способами.</span><span class="sxs-lookup"><span data-stu-id="e340a-127">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="e340a-128">Наведите указатель мыши на снимок экрана, чтобы просмотреть точку, в которой был записан снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="e340a-128">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="e340a-129">На панели **обзора** появится желтая линия.</span><span class="sxs-lookup"><span data-stu-id="e340a-129">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="e340a-130">Щелкните эскиз экрана, чтобы отфильтровать все запросы, произошедшие после захвата снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="e340a-130">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="e340a-131">Дважды щелкните эскиз, чтобы увеличить его.</span><span class="sxs-lookup"><span data-stu-id="e340a-131">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведение указателя на снимок экрана" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="e340a-133">Рисунок 4: наведение указателя на снимок экрана</span><span class="sxs-lookup"><span data-stu-id="e340a-133">Figure 4:  Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="e340a-134">Изменение поведения при загрузке</span><span class="sxs-lookup"><span data-stu-id="e340a-134">Change loading behavior</span></span>  

### <span data-ttu-id="e340a-135">Эмуляция первого времени посетителя с помощью отключения кэша браузера</span><span class="sxs-lookup"><span data-stu-id="e340a-135">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="e340a-136">Чтобы эмулировать, как пользователь попытается получить доступ к сайту, установите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="e340a-136">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="e340a-137">DevTools отключает кэш браузера.</span><span class="sxs-lookup"><span data-stu-id="e340a-137">DevTools disables the browser cache.</span></span>  <span data-ttu-id="e340a-138">Это более точно эмулирует взаимодействие с пользователем при первом запуске, так как запросы размещаются из кэша браузера на повторных посещениях.</span><span class="sxs-lookup"><span data-stu-id="e340a-138">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Флажок "отключить кэш"" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="e340a-140">Рисунок 5: флажок **отключения кэша**</span><span class="sxs-lookup"><span data-stu-id="e340a-140">Figure 5:  The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="e340a-141">Отключение кэша браузера из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="e340a-141">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="e340a-142">Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте денежные ящики условия сети.</span><span class="sxs-lookup"><span data-stu-id="e340a-142">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="e340a-143">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="e340a-143">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e340a-144">Установите или снимите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="e340a-144">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="e340a-145">Очистка кэша браузера вручную</span><span class="sxs-lookup"><span data-stu-id="e340a-145">Manually clear the browser cache</span></span>  

<span data-ttu-id="e340a-146">Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши в любом месте таблицы запросов и выберите пункт **очистить кэш браузера**).</span><span class="sxs-lookup"><span data-stu-id="e340a-146">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор очистки кэша браузера" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="e340a-148">Рисунок 6: выбор **очистки кэша браузера**</span><span class="sxs-lookup"><span data-stu-id="e340a-148">Figure 6:  Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-149">Эмуляция в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="e340a-149">Emulate offline</span></span>  

<span data-ttu-id="e340a-150">Новый класс веб-приложений, именуемых [прогрессивными веб-приложениями][DevtoolsProgressiveWebApps], не будет работать в автономном режиме с помощью **обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="e340a-150">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="e340a-151">Возможно, вам будет удобно быстро смоделировать устройство, которое не имеет подключения к данным, при построении такого типа приложения.</span><span class="sxs-lookup"><span data-stu-id="e340a-151">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="e340a-152">Щелкните раскрывающееся меню **онлайн** , выполните поиск в разделе " **стили**", а затем выберите пункт в **автономном режиме** , чтобы имитировать полностью автономный режим работы сети.</span><span class="sxs-lookup"><span data-stu-id="e340a-152">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Раскрывающееся меню "автономный режим"" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="e340a-154">Рисунок 7: раскрывающийся список в **автономном режиме**</span><span class="sxs-lookup"><span data-stu-id="e340a-154">Figure 7:  The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-155">Эмуляция медленных сетевых подключений</span><span class="sxs-lookup"><span data-stu-id="e340a-155">Emulate slow network connections</span></span>  

<span data-ttu-id="e340a-156">Эмуляция медленной сети 3G, Fast 3G и других скоростей соединения из раскрывающегося меню **Online** .</span><span class="sxs-lookup"><span data-stu-id="e340a-156">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Раскрывающееся меню регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="e340a-158">Рисунок 8: раскрывающееся меню **регулирования**</span><span class="sxs-lookup"><span data-stu-id="e340a-158">Figure 8:  The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="e340a-159">Вы можете выбрать один из самых разнообразных наборов параметров, например медленной или скорости 3G.</span><span class="sxs-lookup"><span data-stu-id="e340a-159">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="e340a-160">Вы также можете добавить собственные пользовательские стили, открыв меню регулирования и выбрав пункт **настраиваемое**  >  **Добавление**.</span><span class="sxs-lookup"><span data-stu-id="e340a-160">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="e340a-161">DevTools отображает значок предупреждения рядом с вкладкой **сеть** , чтобы напомнить вам, что регулирование разрешено.</span><span class="sxs-lookup"><span data-stu-id="e340a-161">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="e340a-162">Эмуляция медленных сетевых подключений из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="e340a-162">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="e340a-163">Если вы хотите регулировать сетевое соединение при работе с другими панелями DevTools, используйте денежные ящики условий сети.</span><span class="sxs-lookup"><span data-stu-id="e340a-163">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="e340a-164">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="e340a-164">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e340a-165">Выберите нужную скорость соединения в меню **регулирования** .</span><span class="sxs-lookup"><span data-stu-id="e340a-165">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="e340a-166">Очистка файлов cookie браузера вручную</span><span class="sxs-lookup"><span data-stu-id="e340a-166">Manually clear browser cookies</span></span>  

<span data-ttu-id="e340a-167">Чтобы вручную удалить cookie-файлы браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши, где угодно в таблице запросов и выберите команду **Очистить cookie-файлы браузера**).</span><span class="sxs-lookup"><span data-stu-id="e340a-167">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выбор очистки cookie-файлов браузера" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="e340a-169">Рисунок 9: выбор пункта **"Удалить cookie-файлы браузера"**</span><span class="sxs-lookup"><span data-stu-id="e340a-169">Figure 9:  Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-170">Переопределение агента пользователя</span><span class="sxs-lookup"><span data-stu-id="e340a-170">Override the user agent</span></span>  

<span data-ttu-id="e340a-171">Чтобы вручную переопределить агент пользователя, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-171">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="e340a-172">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="e340a-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e340a-173">Снимите флажок **автоматически**.</span><span class="sxs-lookup"><span data-stu-id="e340a-173">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="e340a-174">Выберите в меню пункт агента пользователя или введите его в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="e340a-174">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="e340a-175">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="e340a-175">Filter requests</span></span>  

### <span data-ttu-id="e340a-176">Фильтрация запросов по свойствам</span><span class="sxs-lookup"><span data-stu-id="e340a-176">Filter requests by properties</span></span>  

<span data-ttu-id="e340a-177">С помощью текстового поля **Фильтр** можно отфильтровать запросы по свойствам, таким как домен или размер запроса.</span><span class="sxs-lookup"><span data-stu-id="e340a-177">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="e340a-178">Если надпись не отображается, возможно, область Фильтры скрыта.</span><span class="sxs-lookup"><span data-stu-id="e340a-178">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="e340a-179">Посмотрите [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="e340a-179">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле "фильтр"" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="e340a-181">Рисунок 10: текстовое поле " **Фильтр** "</span><span class="sxs-lookup"><span data-stu-id="e340a-181">Figure 10:  The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="e340a-182">Вы можете использовать несколько свойств одновременно, разделяя каждое свойство пробелами.</span><span class="sxs-lookup"><span data-stu-id="e340a-182">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="e340a-183">Например, `mime-type:image/png larger-than:1K` отображает все PNGs, размер которых больше 1 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="e340a-183">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="e340a-184">Эти фильтры с несколькими свойствами эквивалентны `AND` операциям.</span><span class="sxs-lookup"><span data-stu-id="e340a-184">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="e340a-185">операции в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e340a-185">operations are currently not supported.</span></span>  

<span data-ttu-id="e340a-186">Полный список поддерживаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="e340a-186">The complete list of supported properties.</span></span>  

| <span data-ttu-id="e340a-187">Свойство</span><span class="sxs-lookup"><span data-stu-id="e340a-187">Property</span></span> | <span data-ttu-id="e340a-188">Сведения</span><span class="sxs-lookup"><span data-stu-id="e340a-188">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="e340a-189">Отображать только ресурсы из указанного домена.</span><span class="sxs-lookup"><span data-stu-id="e340a-189">Only display resources from the specified domain.</span></span>  <span data-ttu-id="e340a-190">Вы можете использовать подстановочный знак "\ `*` ", чтобы включить несколько доменов.</span><span class="sxs-lookup"><span data-stu-id="e340a-190">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="e340a-191">Например, `*.com` отображаются ресурсы из всех доменных имен, которые заканчиваются на `.com` .</span><span class="sxs-lookup"><span data-stu-id="e340a-191">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="e340a-192">DevTools заполняет раскрывающееся меню автозаполнения всеми найденными доменами.</span><span class="sxs-lookup"><span data-stu-id="e340a-192">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="e340a-193">Показать ресурсы, содержащие указанный заголовок HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="e340a-193">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="e340a-194">DevTools заполняет раскрывающийся список автозавершения всеми найденными заголовками ответов.</span><span class="sxs-lookup"><span data-stu-id="e340a-194">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="e340a-195">Используется `is:running` для поиска `WebSocket` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e340a-195">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="e340a-196">Показать ресурсы, размер которых больше указанного (в байтах).</span><span class="sxs-lookup"><span data-stu-id="e340a-196">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="e340a-197">Установка значения эквивалентно значению свойства `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="e340a-197">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="e340a-198">Показать ресурсы, полученные с помощью указанного типа метода HTTP.</span><span class="sxs-lookup"><span data-stu-id="e340a-198">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="e340a-199">DevTools заполнит раскрывающийся список всех обнаруженных методов HTTP.</span><span class="sxs-lookup"><span data-stu-id="e340a-199">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="e340a-200">Показать ресурсы указанного типа MIME.</span><span class="sxs-lookup"><span data-stu-id="e340a-200">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="e340a-201">DevTools наполняет в раскрывающемся списке все обнаруженные типы MIME.</span><span class="sxs-lookup"><span data-stu-id="e340a-201">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="e340a-202">Показать все смешанные ресурсы контента \ ( `mixed-content:all` \) или только те из них, которые в данный момент отображаются \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="e340a-202">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="e340a-203">Показать ресурсы, полученные через незащищенные HTTP \ ( `scheme:http` \) или защищенные HTTPS \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="e340a-203">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="e340a-204">Показать ресурсы с `Set-Cookie` заголовком с `Domain` атрибутом, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="e340a-204">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="e340a-205">DevTools заполняет Автозаполнение всеми обнаруженными ими доменами cookie.</span><span class="sxs-lookup"><span data-stu-id="e340a-205">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="e340a-206">Показать ресурсы с `Set-Cookie` заголовком с именем, которое соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="e340a-206">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="e340a-207">DevTools заполняет Автозаполнение всеми именами cookie-файлов, которые были обнаружены.</span><span class="sxs-lookup"><span data-stu-id="e340a-207">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="e340a-208">Показать ресурсы с `Set-Cookie` заголовком со значением, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="e340a-208">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="e340a-209">DevTools заполняет Автозаполнение всеми обнаруженными значениями cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="e340a-209">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="e340a-210">Показать только ресурсы, для которых код состояния HTTP соответствует указанному коду.</span><span class="sxs-lookup"><span data-stu-id="e340a-210">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="e340a-211">DevTools заполнит раскрывающееся меню автозаполнения, содержащее все найденные коды состояния.</span><span class="sxs-lookup"><span data-stu-id="e340a-211">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="e340a-212">Фильтрация запросов по типу</span><span class="sxs-lookup"><span data-stu-id="e340a-212">Filter requests by type</span></span>  

<span data-ttu-id="e340a-213">Чтобы отфильтровать запросы по типу запроса, выберите один из указанных ниже кнопок: **XHR**, **JS**, **CSS**, **img**, **Media**, **Font**, **doc**, **WS** \ (WebSocket \), **Манифест**или **другой** \ (любой другой тип, не указанный здесь) на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e340a-213">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="e340a-214">Если эти кнопки не отображаются, возможно, область фильтров скрыта.</span><span class="sxs-lookup"><span data-stu-id="e340a-214">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="e340a-215">Посмотрите [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="e340a-215">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="e340a-216">Чтобы включить множественные фильтры типов одновременно, удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и выберите.</span><span class="sxs-lookup"><span data-stu-id="e340a-216">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров типов для отображения ресурсов JS, CSS и документов" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="e340a-218">На рисунке 11: использование фильтров типов для отображения ресурсов JS, CSS и документов</span><span class="sxs-lookup"><span data-stu-id="e340a-218">Figure 11:  Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-219">Фильтрация запросов по времени</span><span class="sxs-lookup"><span data-stu-id="e340a-219">Filter requests by time</span></span>  

<span data-ttu-id="e340a-220">Чтобы отобразить только те запросы, которые были активны в течение этого времени, выберите и перетащите его влево или вправо в области "Обзор".</span><span class="sxs-lookup"><span data-stu-id="e340a-220">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="e340a-221">Фильтр является инклюзивным.</span><span class="sxs-lookup"><span data-stu-id="e340a-221">The filter is inclusive.</span></span>  <span data-ttu-id="e340a-222">Отображается любой запрос, который был активен в течение выбранного периода времени.</span><span class="sxs-lookup"><span data-stu-id="e340a-222">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация запросов, которые неактивны вокруг 300ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="e340a-224">Рис. 12: Фильтрация запросов, которые неактивны вокруг 300ms</span><span class="sxs-lookup"><span data-stu-id="e340a-224">Figure 12:  Filtering out any requests that were inactive around 300ms</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-225">Скрыть URL-адреса данных</span><span class="sxs-lookup"><span data-stu-id="e340a-225">Hide data URLs</span></span>  

<span data-ttu-id="e340a-226">[URL-адреса данных][MDNHTTPDataURIs] — это небольшие файлы, внедренные в другие документы.</span><span class="sxs-lookup"><span data-stu-id="e340a-226">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="e340a-227">Любой запрос, который начинается с адреса в таблице запросов, `data:` — это URL-адрес данных.</span><span class="sxs-lookup"><span data-stu-id="e340a-227">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="e340a-228">Установите флажок **скрыть URL-адреса данных** , чтобы скрыть запросы.</span><span class="sxs-lookup"><span data-stu-id="e340a-228">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Флажок "скрыть URL-адреса данных"" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="e340a-230">Рисунок 13: флажок **скрыть URL-адреса данных**</span><span class="sxs-lookup"><span data-stu-id="e340a-230">Figure 13:  The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="e340a-231">Запросы сортировки</span><span class="sxs-lookup"><span data-stu-id="e340a-231">Sort requests</span></span>  

<span data-ttu-id="e340a-232">По умолчанию запросы в таблице запросов сортируются по времени запуска, но вы можете отсортировать таблицу с помощью других условий.</span><span class="sxs-lookup"><span data-stu-id="e340a-232">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="e340a-233">Сортировка по столбцам</span><span class="sxs-lookup"><span data-stu-id="e340a-233">Sort by column</span></span>  

<span data-ttu-id="e340a-234">Выберите верхний колонтитул любого столбца в списке запросы для сортировки запросов по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="e340a-234">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="e340a-235">Этап сортировки по действию</span><span class="sxs-lookup"><span data-stu-id="e340a-235">Sort by activity phase</span></span>  

<span data-ttu-id="e340a-236">Чтобы изменить способ сортировки запросов, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню, наведите указатель мыши на пункт **Каскад**и выберите один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="e340a-236">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="e340a-237">**Время начала**.</span><span class="sxs-lookup"><span data-stu-id="e340a-237">**Start Time**.</span></span>  <span data-ttu-id="e340a-238">Первый инициированный запрос находится наверху.</span><span class="sxs-lookup"><span data-stu-id="e340a-238">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="e340a-239">**Время отклика**.</span><span class="sxs-lookup"><span data-stu-id="e340a-239">**Response Time**.</span></span>  <span data-ttu-id="e340a-240">Первый запрос, загруженный в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="e340a-240">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="e340a-241">**Время окончания**.</span><span class="sxs-lookup"><span data-stu-id="e340a-241">**End Time**.</span></span>  <span data-ttu-id="e340a-242">Первый завершенный запрос вверху.</span><span class="sxs-lookup"><span data-stu-id="e340a-242">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="e340a-243">**Общая длительность**.</span><span class="sxs-lookup"><span data-stu-id="e340a-243">**Total Duration**.</span></span>  <span data-ttu-id="e340a-244">Запрос с наиболее короткой установкой подключения и запросом и ответом в начале.</span><span class="sxs-lookup"><span data-stu-id="e340a-244">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="e340a-245">**Задержка**.</span><span class="sxs-lookup"><span data-stu-id="e340a-245">**Latency**.</span></span>  <span data-ttu-id="e340a-246">Запрос, который ожидает наиболее короткий момент ответа, находится наверху.</span><span class="sxs-lookup"><span data-stu-id="e340a-246">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="e340a-247">В этих описаниях предполагается, что каждый из вариантов имеет приоритет от кратчайшего к наиболее продолжительному.</span><span class="sxs-lookup"><span data-stu-id="e340a-247">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="e340a-248">Если выбрать верхний колонтитул столбца **каскадом** , порядок будет изменен на противоположный.</span><span class="sxs-lookup"><span data-stu-id="e340a-248">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка каскадом по общей длительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="e340a-250">Рисунок 14: Сортировка каскадом по общей длительности \ (светлая часть каждого элемента обходуется временем ожидания, а темная часть — это время, затраченное на загрузку байтов)</span><span class="sxs-lookup"><span data-stu-id="e340a-250">Figure 14:  Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="e340a-251">Анализ запросов</span><span class="sxs-lookup"><span data-stu-id="e340a-251">Analyze requests</span></span>  

<span data-ttu-id="e340a-252">Пока открыто окно DevTools, все запросы будут регистрироваться на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e340a-252">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="e340a-253">Проанализируйте запросы с помощью панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e340a-253">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="e340a-254">Просмотр журнала запросов</span><span class="sxs-lookup"><span data-stu-id="e340a-254">View a log of requests</span></span>  

<span data-ttu-id="e340a-255">С помощью таблицы запросы можно просмотреть журнал всех запросов, выполненных, когда DevTools открыт.</span><span class="sxs-lookup"><span data-stu-id="e340a-255">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="e340a-256">При выборе или наведении указателя мыши на запросы открывается больше сведений о каждом элементе.</span><span class="sxs-lookup"><span data-stu-id="e340a-256">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица запросов" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="e340a-258">Рис. 15: таблица запросы</span><span class="sxs-lookup"><span data-stu-id="e340a-258">Figure 15:  The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="e340a-259">По умолчанию в таблице запросов отображаются следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="e340a-259">The Requests table displays the following columns by default.</span></span>  

*   <span data-ttu-id="e340a-260">**Имя**.</span><span class="sxs-lookup"><span data-stu-id="e340a-260">**Name**.</span></span>  <span data-ttu-id="e340a-261">Имя или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e340a-261">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="e340a-262">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="e340a-262">**Status**.</span></span>  <span data-ttu-id="e340a-263">Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="e340a-263">The HTTP status code.</span></span>  
*   <span data-ttu-id="e340a-264">**Тип**.</span><span class="sxs-lookup"><span data-stu-id="e340a-264">**Type**.</span></span>  <span data-ttu-id="e340a-265">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="e340a-265">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="e340a-266">**Инициатор**.</span><span class="sxs-lookup"><span data-stu-id="e340a-266">**Initiator**.</span></span>  <span data-ttu-id="e340a-267">Следующие объекты или процессы инициируют запросы:</span><span class="sxs-lookup"><span data-stu-id="e340a-267">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="e340a-268">**Средство синтаксического анализа**.</span><span class="sxs-lookup"><span data-stu-id="e340a-268">**Parser**.</span></span>  <span data-ttu-id="e340a-269">Средство синтаксического анализа HTML для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e340a-269">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="e340a-270">**Redirect (перенаправление**).</span><span class="sxs-lookup"><span data-stu-id="e340a-270">**Redirect**.</span></span>  <span data-ttu-id="e340a-271">Переадресация HTTP.</span><span class="sxs-lookup"><span data-stu-id="e340a-271">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="e340a-272">**Сценарий**.</span><span class="sxs-lookup"><span data-stu-id="e340a-272">**Script**.</span></span>  <span data-ttu-id="e340a-273">Функция JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e340a-273">A JavaScript function.</span></span>  
    *   <span data-ttu-id="e340a-274">**Другие**.</span><span class="sxs-lookup"><span data-stu-id="e340a-274">**Other**.</span></span>  <span data-ttu-id="e340a-275">Другие процессы или действия, например переход на страницу с помощью ссылки или ввод URL-адреса в адресную строку.</span><span class="sxs-lookup"><span data-stu-id="e340a-275">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="e340a-276">**Размер**.</span><span class="sxs-lookup"><span data-stu-id="e340a-276">**Size**.</span></span>  <span data-ttu-id="e340a-277">Объединенный размер заголовков ответа и текст ответа, доставленный сервером.</span><span class="sxs-lookup"><span data-stu-id="e340a-277">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="e340a-278">**Time (время**).</span><span class="sxs-lookup"><span data-stu-id="e340a-278">**Time**.</span></span>  <span data-ttu-id="e340a-279">Общая продолжительность от начала запроса до получения последнего байта в ответе.</span><span class="sxs-lookup"><span data-stu-id="e340a-279">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="e340a-280">[**Каскадом**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="e340a-280">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="e340a-281">Визуальная декомпозиция мероприятия для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="e340a-281">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="e340a-282">Добавление и удаление столбцов</span><span class="sxs-lookup"><span data-stu-id="e340a-282">Add or remove columns</span></span>  

<span data-ttu-id="e340a-283">Наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите один из вариантов, чтобы скрыть или отобразить его.</span><span class="sxs-lookup"><span data-stu-id="e340a-283">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="e340a-284">Параметры, отображаемые в данный момент, отмечены флажками рядом с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="e340a-284">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу "запросы"" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="e340a-286">Рисунок 16: Добавление столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="e340a-286">Figure 16:  Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="e340a-287">Добавление настраиваемых столбцов</span><span class="sxs-lookup"><span data-stu-id="e340a-287">Add custom columns</span></span>  

<span data-ttu-id="e340a-288">Чтобы добавить настраиваемый столбец в таблицу запросы, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите **заголовки ответов**  >  .**Управление столбцами заголовков**.</span><span class="sxs-lookup"><span data-stu-id="e340a-288">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемого столбца в таблицу "запросы"" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="e340a-290">Рисунок 17: Добавление настраиваемого столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="e340a-290">Figure 17:  Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-291">Просмотр времени связи между запросами друг на друга</span><span class="sxs-lookup"><span data-stu-id="e340a-291">View the timing of requests in relation to one another</span></span>  

<span data-ttu-id="e340a-292">Используйте Каскад, чтобы просмотреть время связи между запросами друг с другом.</span><span class="sxs-lookup"><span data-stu-id="e340a-292">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="e340a-293">По умолчанию каскадом упорядочиваются по времени начала запросов.</span><span class="sxs-lookup"><span data-stu-id="e340a-293">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="e340a-294">Таким образом, запросы, которые раньше приступили к началу, чем те, которые находятся дальше по правому краю.</span><span class="sxs-lookup"><span data-stu-id="e340a-294">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="e340a-295">Чтобы увидеть различные способы сортировки каскадов, просмотрите [фазу сортировки по действию](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="e340a-295">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец "Каскад" на панели "запросы"" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="e340a-297">Рисунок 18: столбец "Каскад" на панели " **запросы** "</span><span class="sxs-lookup"><span data-stu-id="e340a-297">Figure 18:  The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   Old Figure 20:  The **Frames** tab  
:::image-end:::  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="e340a-298">Предварительный просмотр тела ответа</span><span class="sxs-lookup"><span data-stu-id="e340a-298">View a preview of a response body</span></span>  

<span data-ttu-id="e340a-299">Чтобы предварительно просмотреть текст ответа, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-299">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="e340a-300">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e340a-300">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e340a-301">Откройте вкладку **Предварительный просмотр** .</span><span class="sxs-lookup"><span data-stu-id="e340a-301">Select the **Preview** tab.</span></span>  

<span data-ttu-id="e340a-302">Эта вкладка особенно полезна для просмотра изображений.</span><span class="sxs-lookup"><span data-stu-id="e340a-302">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Вкладка "предварительный просмотр"" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="e340a-304">На рисунке 19: вкладка " **Предварительный просмотр** "</span><span class="sxs-lookup"><span data-stu-id="e340a-304">Figure 19:  The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-305">Просмотр текста ответа</span><span class="sxs-lookup"><span data-stu-id="e340a-305">View a response body</span></span>  

<span data-ttu-id="e340a-306">Чтобы просмотреть текст ответа на запрос, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-306">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="e340a-307">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e340a-307">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e340a-308">Откройте вкладку **ответ** .</span><span class="sxs-lookup"><span data-stu-id="e340a-308">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Вкладка "ответ"" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="e340a-310">Рисунок 20. Вкладка " **ответ** "</span><span class="sxs-lookup"><span data-stu-id="e340a-310">Figure 20:  The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-311">Просмотр заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="e340a-311">View HTTP headers</span></span>  

<span data-ttu-id="e340a-312">Чтобы просмотреть данные заголовка HTTP для запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-312">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="e340a-313">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e340a-313">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e340a-314">Откройте вкладку **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="e340a-314">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Вкладка "заголовки"" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="e340a-316">Рисунок 21: вкладка " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="e340a-316">Figure 21:  The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="e340a-317">Просмотр источника заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="e340a-317">View HTTP header source</span></span>  

<span data-ttu-id="e340a-318">По умолчанию на вкладке заголовки отображаются имена заголовков в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="e340a-318">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="e340a-319">Чтобы просмотреть имена HTTP-заголовков в том порядке, в котором они были получены:</span><span class="sxs-lookup"><span data-stu-id="e340a-319">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="e340a-320">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="e340a-320">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="e340a-321">См.: [Просмотр заголовков HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="e340a-321">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="e340a-322">Нажмите кнопку **источник**, рядом с разделом **заголовок запроса** или **заголовок ответа** .</span><span class="sxs-lookup"><span data-stu-id="e340a-322">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="e340a-323">Просмотр параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="e340a-323">View query string parameters</span></span>  

<span data-ttu-id="e340a-324">Чтобы просмотреть параметры строки запроса URL-адреса в удобочитаемом формате, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-324">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="e340a-325">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="e340a-325">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="e340a-326">См.: [Просмотр заголовков HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="e340a-326">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="e340a-327">Перейдите к разделу **Параметры строки запроса** .</span><span class="sxs-lookup"><span data-stu-id="e340a-327">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел "параметры строки запроса"" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="e340a-329">Рис. 22: раздел " **Параметры строки запроса** "</span><span class="sxs-lookup"><span data-stu-id="e340a-329">Figure 22:  The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="e340a-330">Просмотр источника параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="e340a-330">View query string parameters source</span></span>  

<span data-ttu-id="e340a-331">Чтобы просмотреть источник параметра строки запроса для запроса:</span><span class="sxs-lookup"><span data-stu-id="e340a-331">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="e340a-332">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="e340a-332">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="e340a-333">Просмотрите [Параметры строки запроса на просмотр](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="e340a-333">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="e340a-334">Нажмите кнопку **Просмотр источника**.</span><span class="sxs-lookup"><span data-stu-id="e340a-334">Select **view source**.</span></span>  

#### <span data-ttu-id="e340a-335">Просмотр строковых параметров запроса в кодировке URL</span><span class="sxs-lookup"><span data-stu-id="e340a-335">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="e340a-336">Чтобы просмотреть параметры строки запроса в удобочитаемом формате, но с сохранением кодировки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-336">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="e340a-337">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="e340a-337">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="e340a-338">Просмотрите [Параметры строки запроса на просмотр](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="e340a-338">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="e340a-339">Выберите команду **Просмотреть закодированный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="e340a-339">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="e340a-340">Просмотр файлов cookie</span><span class="sxs-lookup"><span data-stu-id="e340a-340">View cookies</span></span>  

<span data-ttu-id="e340a-341">Чтобы просмотреть cookie-файлы, отправленные в заголовке HTTP запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-341">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="e340a-342">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e340a-342">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e340a-343">Перейдите на вкладку " **cookie** ".</span><span class="sxs-lookup"><span data-stu-id="e340a-343">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Вкладка "cookie"" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="e340a-345">Рис. 23: вкладка "cookie"</span><span class="sxs-lookup"><span data-stu-id="e340a-345">Figure 23:  The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-346">Просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="e340a-346">View the timing breakdown of a request</span></span>  

<span data-ttu-id="e340a-347">Чтобы просмотреть межвременную разбивку запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-347">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="e340a-348">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e340a-348">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e340a-349">Откройте вкладку **время** .</span><span class="sxs-lookup"><span data-stu-id="e340a-349">Select the **Timing** tab.</span></span>  

<span data-ttu-id="e340a-350">Дополнительные сведения можно найти в разделе [Предварительный просмотр разбивки времени](#preview-a-timing-breakdown) для доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="e340a-350">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="e340a-351">Дополнительные сведения о каждой из фаз, которые можно увидеть на вкладке время, приведены в разделе [этапы разбиения по времени](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="e340a-351">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Вкладка время" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="e340a-353">Рисунок 24: вкладка **время**</span><span class="sxs-lookup"><span data-stu-id="e340a-353">Figure 24:  The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="e340a-354">Дополнительные сведения о каждой из фаз.</span><span class="sxs-lookup"><span data-stu-id="e340a-354">More information about each of the phases.</span></span>  

<span data-ttu-id="e340a-355">Другие способы доступа к этому представлению можно найти в разделе [Просмотр временных интервалов](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="e340a-355">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="e340a-356">Предварительный просмотр разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="e340a-356">Preview a timing breakdown</span></span>  

<span data-ttu-id="e340a-357">Чтобы просмотреть сведения о разбиении по времени для запроса, наведите указатель мыши на запись запроса в столбце **Каскад** таблицы запросы.</span><span class="sxs-lookup"><span data-stu-id="e340a-357">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="e340a-358">Ознакомьтесь [со](#view-the-timing-breakdown-of-a-request) сведениями о том, как получить доступ к данным, которые не требуют наведения мыши, в запросе.</span><span class="sxs-lookup"><span data-stu-id="e340a-358">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбиения по времени для запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="e340a-360">Рис. 25: предварительный просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="e340a-360">Figure 25:  Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="e340a-361">Описание этапов разделения времени</span><span class="sxs-lookup"><span data-stu-id="e340a-361">Timing breakdown phases explained</span></span>  

<span data-ttu-id="e340a-362">Дополнительные сведения о каждой из фаз, которые можно увидеть на вкладке **время** .</span><span class="sxs-lookup"><span data-stu-id="e340a-362">More information about each of the phases you may see in the **Timing** tab.</span></span>  

*   <span data-ttu-id="e340a-363">**Очереди**.</span><span class="sxs-lookup"><span data-stu-id="e340a-363">**Queueing**.</span></span>  <span data-ttu-id="e340a-364">Браузер помещает запросы в очередь в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="e340a-364">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="e340a-365">Существуют запросы с более высокими приоритетами.</span><span class="sxs-lookup"><span data-stu-id="e340a-365">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="e340a-366">Для этого происхождения уже открыто шесть подключений TCP, что является ограничением.</span><span class="sxs-lookup"><span data-stu-id="e340a-366">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="e340a-367">Применимо только к HTTP/1.0 и HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="e340a-367">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="e340a-368">Браузер временно выделяет место в кэше на диске.</span><span class="sxs-lookup"><span data-stu-id="e340a-368">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="e340a-369">**Ожидание**.</span><span class="sxs-lookup"><span data-stu-id="e340a-369">**Stalled**.</span></span>  <span data-ttu-id="e340a-370">Запрос может быть остановлен в любой из причин, описанных в разделе **очереди**.</span><span class="sxs-lookup"><span data-stu-id="e340a-370">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="e340a-371">**Поиск DNS**.</span><span class="sxs-lookup"><span data-stu-id="e340a-371">**DNS Lookup**.</span></span>  <span data-ttu-id="e340a-372">Браузер разрешает IP-адрес запроса.</span><span class="sxs-lookup"><span data-stu-id="e340a-372">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="e340a-373">**Начальное соединение**.</span><span class="sxs-lookup"><span data-stu-id="e340a-373">**Initial connection**.</span></span>  <span data-ttu-id="e340a-374">Браузер устанавливает подключение, в том числе подтверждения TCP, повторы TCP и согласование SSL.</span><span class="sxs-lookup"><span data-stu-id="e340a-374">The browser is establishing a connection including TCP handshakes, TCP retries, and negotiating an SSL.</span></span>
*   <span data-ttu-id="e340a-375">**Согласование прокси-сервера**.</span><span class="sxs-lookup"><span data-stu-id="e340a-375">**Proxy negotiation**.</span></span>  <span data-ttu-id="e340a-376">Браузер согласовывает запрос с [прокси-сервером][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="e340a-376">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="e340a-377">**Запрос отправлен**.</span><span class="sxs-lookup"><span data-stu-id="e340a-377">**Request sent**.</span></span>  <span data-ttu-id="e340a-378">Запрос отправляется.</span><span class="sxs-lookup"><span data-stu-id="e340a-378">The request is being sent.</span></span>  
*   <span data-ttu-id="e340a-379">**Подготовка ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="e340a-379">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="e340a-380">Браузер запускает сервисный рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="e340a-380">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="e340a-381">**Запросите ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="e340a-381">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="e340a-382">Запрос отправляется сотруднику службы.</span><span class="sxs-lookup"><span data-stu-id="e340a-382">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="e340a-383">**Ожидание \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="e340a-383">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="e340a-384">Браузер ожидает первый байт ответа.</span><span class="sxs-lookup"><span data-stu-id="e340a-384">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="e340a-385">TTFB означает время для первого байта.</span><span class="sxs-lookup"><span data-stu-id="e340a-385">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="e340a-386">Это время включает 1 круговый путь задержки и время, затраченное сервером на подготовку ответа.</span><span class="sxs-lookup"><span data-stu-id="e340a-386">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="e340a-387">**Загрузка содержимого**.</span><span class="sxs-lookup"><span data-stu-id="e340a-387">**Content Download**.</span></span>  <span data-ttu-id="e340a-388">Браузер получает ответ.</span><span class="sxs-lookup"><span data-stu-id="e340a-388">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="e340a-389">**Получение push-уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="e340a-389">**Receiving Push**.</span></span>  <span data-ttu-id="e340a-390">Браузер получает данные для этого ответа через HTTP/2 серверную извещающую передачу.</span><span class="sxs-lookup"><span data-stu-id="e340a-390">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="e340a-391">**Чтение push-уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="e340a-391">**Reading Push**.</span></span>  <span data-ttu-id="e340a-392">Браузер читает локальные данные, полученные ранее.</span><span class="sxs-lookup"><span data-stu-id="e340a-392">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="e340a-393">Просмотр инициаторов и зависимостей</span><span class="sxs-lookup"><span data-stu-id="e340a-393">View initiators and dependencies</span></span>  

<span data-ttu-id="e340a-394">Чтобы просмотреть инициаторы и зависимости запроса, удерживайте `Shift` и наведите указатель мыши на запрос в таблице запросы.</span><span class="sxs-lookup"><span data-stu-id="e340a-394">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="e340a-395">DevTools цвета: инициаторы отображаются зеленым цветом, а зависимости — красным.</span><span class="sxs-lookup"><span data-stu-id="e340a-395">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Просмотр инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="e340a-397">Рис. 26: Просмотр инициаторов и зависимостей запроса</span><span class="sxs-lookup"><span data-stu-id="e340a-397">Figure 26:  Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="e340a-398">Когда таблица запросов упорядочивается в хронологическом порядке, первым зеленым запросом над ним, который вы наводите, является инициатор зависимости.</span><span class="sxs-lookup"><span data-stu-id="e340a-398">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="e340a-399">Если над ним появится еще один зеленый запрос, этот более высокий запрос является инициатором инициатора.</span><span class="sxs-lookup"><span data-stu-id="e340a-399">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="e340a-400">И так далее.</span><span class="sxs-lookup"><span data-stu-id="e340a-400">And so on.</span></span>  

### <span data-ttu-id="e340a-401">Просмотр событий загрузки</span><span class="sxs-lookup"><span data-stu-id="e340a-401">View load events</span></span>  

<span data-ttu-id="e340a-402">DevTools отображает время показа `DOMContentLoaded` `load` событий в нескольких местах на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e340a-402">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="e340a-403">`DOMContentLoaded`Событие окрашивается синим цветом, а `load` событие — красным.</span><span class="sxs-lookup"><span data-stu-id="e340a-403">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположение событий DOMContentLoaded и Load на панели "сеть"" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="e340a-405">На рисунке 27 показано расположение событий " `DOMContentLoaded` и" `load` на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e340a-405">Figure 27:  The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-406">Просмотр общего числа запросов</span><span class="sxs-lookup"><span data-stu-id="e340a-406">View the total number of requests</span></span>  

<span data-ttu-id="e340a-407">Общее количество запросов можно найти в области сводки в нижней части панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e340a-407">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e340a-408">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="e340a-408">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="e340a-409">Если при открытии DevTools возникли другие запросы, эти запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="e340a-409">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее количество запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="e340a-411">Рис. 28: общее количество запросов с момента открытия DevTools</span><span class="sxs-lookup"><span data-stu-id="e340a-411">Figure 28:  The total number of requests since DevTools was opened</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-412">Просмотр общего объема загружаемого файла</span><span class="sxs-lookup"><span data-stu-id="e340a-412">View the total download size</span></span>  

<span data-ttu-id="e340a-413">Общий объем загруженных запросов отображается в области Сводка в нижней части панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e340a-413">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e340a-414">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="e340a-414">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="e340a-415">Если при открытии DevTools возникли другие запросы, предыдущие запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="e340a-415">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий объем загруженных запросов" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="e340a-417">Рис. 29: общий размер загружаемого запроса.</span><span class="sxs-lookup"><span data-stu-id="e340a-417">Figure 29:  The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="e340a-418">[Просмотр несжатого размера ресурса](#view-the-uncompressed-size-of-a-resource) для просмотра больших ресурсов после того, как браузер распаковывает каждый элемент.</span><span class="sxs-lookup"><span data-stu-id="e340a-418">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="e340a-419">Просмотр трассировки стека, которая привела к запросу</span><span class="sxs-lookup"><span data-stu-id="e340a-419">View the stack trace that caused a request</span></span>  

<span data-ttu-id="e340a-420">После того, как инструкция JavaScript запрашивает ресурс, наведите указатель мыши на столбец **инициатора** , чтобы просмотреть трассировку стека, выступающей в запрос.</span><span class="sxs-lookup"><span data-stu-id="e340a-420">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Трассировка стека, ведущая к запросу ресурсов" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="e340a-422">На рисунке 30 показана трассировка стека, ведущая к запросу ресурсов</span><span class="sxs-lookup"><span data-stu-id="e340a-422">Figure 30:  The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-423">Просмотр несжатого размера ресурса</span><span class="sxs-lookup"><span data-stu-id="e340a-423">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="e340a-424">Установите флажок **использовать строки большого запроса** , а затем посмотрите на нижнее значение столбца **Размер** .</span><span class="sxs-lookup"><span data-stu-id="e340a-424">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример несжатых ресурсов" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="e340a-426">Рисунок 31: пример несжатых ресурсов \ (сжатый размер `jquery-3.3.1.min.js` файла, отправленного по сети `29.9 KB` , в то время как несжатый размер `84.9 KB` )</span><span class="sxs-lookup"><span data-stu-id="e340a-426">Figure 31:  An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="e340a-427">Данные запросов на экспорт</span><span class="sxs-lookup"><span data-stu-id="e340a-427">Export requests data</span></span>  

### <span data-ttu-id="e340a-428">Сохранение всех сетевых запросов в файле HAR</span><span class="sxs-lookup"><span data-stu-id="e340a-428">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="e340a-429">Чтобы сохранить все сетевые запросы в файле HAR, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e340a-429">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="e340a-430">Наведите указатель мыши на любой запрос в таблице запросов и откройте контекстное меню (щелкните правой кнопкой мыши \).</span><span class="sxs-lookup"><span data-stu-id="e340a-430">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="e340a-431">Выберите команду **Сохранить как HAR с содержимым**.</span><span class="sxs-lookup"><span data-stu-id="e340a-431">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="e340a-432">DevTools сохраняет все запросы, произошедшие после того, как вы открыли DevTools в файл HAR.</span><span class="sxs-lookup"><span data-stu-id="e340a-432">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="e340a-433">Невозможно отфильтровать запросы или сохранить только один запрос.</span><span class="sxs-lookup"><span data-stu-id="e340a-433">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="e340a-434">После того как вы сохраните файл HAR, вы можете импортировать его обратно в DevTools для анализа.</span><span class="sxs-lookup"><span data-stu-id="e340a-434">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="e340a-435">Просто перетащите файл HAR в таблицу запросы.</span><span class="sxs-lookup"><span data-stu-id="e340a-435">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Выбор команды "Сохранить как HAR с контентом"" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="e340a-437">Рисунок 32: выбор команды " **Сохранить как HAR с контентом** "</span><span class="sxs-lookup"><span data-stu-id="e340a-437">Figure 32:  Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-438">Копирование одного или нескольких запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="e340a-438">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="e340a-439">В столбце **имя** таблицы запросы наведите указатель мыши на запрос, откройте контекстное меню (щелкните правой кнопкой мыши \), наведите указатель на пункт **Копировать**и выберите один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="e340a-439">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

*   <span data-ttu-id="e340a-440">**Копировать адрес ссылки**.</span><span class="sxs-lookup"><span data-stu-id="e340a-440">**Copy Link Address**.</span></span>  <span data-ttu-id="e340a-441">Скопируйте URL-адрес запроса в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="e340a-441">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="e340a-442">**Копирование ответа**.</span><span class="sxs-lookup"><span data-stu-id="e340a-442">**Copy Response**.</span></span>  <span data-ttu-id="e340a-443">Скопировать текст ответа в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="e340a-443">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="e340a-444">**Копировать как выборку**.</span><span class="sxs-lookup"><span data-stu-id="e340a-444">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="e340a-445">**Копировать как фигуру**.</span><span class="sxs-lookup"><span data-stu-id="e340a-445">**Copy as cURL**.</span></span>  <span data-ttu-id="e340a-446">Копирование запроса в виде текстовой команды.</span><span class="sxs-lookup"><span data-stu-id="e340a-446">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="e340a-447">**Копировать все как выборку**.</span><span class="sxs-lookup"><span data-stu-id="e340a-447">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="e340a-448">**Скопировать все как фигуру**.</span><span class="sxs-lookup"><span data-stu-id="e340a-448">**Copy All as cURL**.</span></span>  <span data-ttu-id="e340a-449">Копирование всех запросов в виде последовательности команд с фигурой.</span><span class="sxs-lookup"><span data-stu-id="e340a-449">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="e340a-450">**Копировать все как HAR**.</span><span class="sxs-lookup"><span data-stu-id="e340a-450">**Copy All as HAR**.</span></span>  <span data-ttu-id="e340a-451">Скопируйте все запросы как данные HAR.</span><span class="sxs-lookup"><span data-stu-id="e340a-451">Copy all requests as HAR data.</span></span>  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выбор пункта "Копировать ответ"" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="e340a-453">Рисунок 33: выбор пункта " **Копировать ответ** "</span><span class="sxs-lookup"><span data-stu-id="e340a-453">Figure 33:  Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="e340a-454">Изменение макета панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="e340a-454">Change the layout of the Network panel</span></span>  

<span data-ttu-id="e340a-455">Вы можете развернуть или свернуть разделы пользовательского интерфейса панели "сеть", чтобы сосредоточиться на важных сведениях.</span><span class="sxs-lookup"><span data-stu-id="e340a-455">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="e340a-456">Скрытие области фильтров</span><span class="sxs-lookup"><span data-stu-id="e340a-456">Hide the Filters pane</span></span>  

<span data-ttu-id="e340a-457">По умолчанию в DevTools отображается **область фильтров**.</span><span class="sxs-lookup"><span data-stu-id="e340a-457">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="e340a-458">Щелкните фильтр **фильтра** ![ ][ImageFilterIcon] , чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="e340a-458">Select **Filter** ![Filter][ImageFilterIcon] to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка "скрыть фильтры"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="e340a-460">Рисунок 34: кнопка "скрыть фильтры"</span><span class="sxs-lookup"><span data-stu-id="e340a-460">Figure 34:  The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-461">Использование строк большого запроса</span><span class="sxs-lookup"><span data-stu-id="e340a-461">Use large request rows</span></span>  

<span data-ttu-id="e340a-462">Используйте большие строки, если вы хотите, чтобы в таблице сетевых запросов больше пробелов.</span><span class="sxs-lookup"><span data-stu-id="e340a-462">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="e340a-463">Некоторые столбцы также содержат дополнительные сведения при использовании больших строк.</span><span class="sxs-lookup"><span data-stu-id="e340a-463">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="e340a-464">Например, минимальное значение столбца « **Размер** » — это несжатый размер запроса.</span><span class="sxs-lookup"><span data-stu-id="e340a-464">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример строк большого запроса в области "запросы"" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="e340a-466">Рисунок 35: пример строк большого запроса в области " **запросы** "</span><span class="sxs-lookup"><span data-stu-id="e340a-466">Figure 35:  An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="e340a-467">Установите флажок **использовать строки большого запроса** , чтобы включить большие строки.</span><span class="sxs-lookup"><span data-stu-id="e340a-467">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Флажок "использовать строки большого запроса"" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="e340a-469">Рисунок 36: флажок " **использовать строки большого запроса** "</span><span class="sxs-lookup"><span data-stu-id="e340a-469">Figure 36:  The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="e340a-470">Скрытие области обзора</span><span class="sxs-lookup"><span data-stu-id="e340a-470">Hide the Overview pane</span></span>  

<span data-ttu-id="e340a-471">По умолчанию в DevTools отображается **область "Общие сведения**".</span><span class="sxs-lookup"><span data-stu-id="e340a-471">By default, DevTools shows the **Overview pane**.</span></span>  <span data-ttu-id="e340a-472">Снимите флажок **Показать общие сведения** , чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="e340a-472">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Флажок "Показать общие сведения"" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="e340a-474">Рисунок 37: флажок **Показать общие сведения**</span><span class="sxs-lookup"><span data-stu-id="e340a-474">Figure 37:  The **Show Overview** checkbox</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Отладка последовательного веб-приложения"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедии"  

> [!NOTE]
> <span data-ttu-id="e340a-478">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e340a-478">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e340a-479">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e340a-479">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e340a-481">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e340a-481">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Полный справочник по функциям панели DevTools сети Microsoft Edge.
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 38570e6d196314aa6315a34f0b8b1b0b0d740c91
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993620"
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

# <span data-ttu-id="e9183-104">Справочник по анализу сети</span><span class="sxs-lookup"><span data-stu-id="e9183-104">Network Analysis Reference</span></span>  

<span data-ttu-id="e9183-105">Ознакомьтесь с новыми способами для анализа того, как страница загружается в этой полной версии справочника по функциям сетевого анализа Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e9183-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="e9183-106">Запись сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="e9183-106">Record network requests</span></span>  

<span data-ttu-id="e9183-107">По умолчанию DevTools записывает все сетевые запросы на панели "сеть", пока не откроете DevTools.</span><span class="sxs-lookup"><span data-stu-id="e9183-107">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель "сеть"" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="e9183-109">Рисунок 1: панель " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="e9183-109">Figure 1:  The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-110">Прекращение записи сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="e9183-110">Stop recording network requests</span></span>  

<span data-ttu-id="e9183-111">Чтобы остановить запись запросов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="e9183-112">Выберите **остановить запись** остановка записи сетевого журнала ![ ][ImageRecordOnIcon] на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="e9183-112">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="e9183-113">Оно превращается в серый, чтобы показать, что DevTools больше не записывает запросы.</span><span class="sxs-lookup"><span data-stu-id="e9183-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="e9183-114">Нажимайте клавиши `Control` + `E` \ (Windows \) или `Command` + `E` \ (macOS \), пока фокус находится на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="e9183-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="e9183-115">Очистка запросов</span><span class="sxs-lookup"><span data-stu-id="e9183-115">Clear requests</span></span>  

<span data-ttu-id="e9183-116">**Clear** ![ ][ImageClearIcon] Чтобы очистить все запросы из таблицы "запросы", на панели "сеть" нажмите кнопку Clear Clear.</span><span class="sxs-lookup"><span data-stu-id="e9183-116">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка "очистить"" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="e9183-118">Рисунок 2: кнопка " **очистить** "</span><span class="sxs-lookup"><span data-stu-id="e9183-118">Figure 2:  The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-119">Сохранение запросов на загрузку страниц</span><span class="sxs-lookup"><span data-stu-id="e9183-119">Save requests across page loads</span></span>  

<span data-ttu-id="e9183-120">Для сохранения запросов на страницах загрузок на панели "сеть" установите флажок **сохранить журнал** .</span><span class="sxs-lookup"><span data-stu-id="e9183-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="e9183-121">DevTools сохраняет все запросы, пока не отключайте параметр **сохранить журнал**.</span><span class="sxs-lookup"><span data-stu-id="e9183-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Флажок "сохранить журнал"" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="e9183-123">Рисунок 3: флажок " **сохранить журнал** "</span><span class="sxs-lookup"><span data-stu-id="e9183-123">Figure 3:  The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-124">Захват снимков экрана при загрузке страницы</span><span class="sxs-lookup"><span data-stu-id="e9183-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="e9183-125">Выведите снимки экрана, чтобы проанализировать, какие пользователи видят при ожидании загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="e9183-125">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="e9183-126">Чтобы включить снимки экрана, нажмите кнопку **Параметры сети** и выберите команду **захватить снимки экрана** на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="e9183-126">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="e9183-127">Обновите страницу, когда фокус находится на панели " **сеть** ", чтобы захватить снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="e9183-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="e9183-128">После захвата снимка экрана вы взаимодействуете с ним следующими способами.</span><span class="sxs-lookup"><span data-stu-id="e9183-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="e9183-129">Наведите указатель мыши на снимок экрана, чтобы просмотреть точку, в которой был записан снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="e9183-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="e9183-130">На панели **обзора** появится желтая линия.</span><span class="sxs-lookup"><span data-stu-id="e9183-130">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="e9183-131">Щелкните эскиз экрана, чтобы отфильтровать все запросы, произошедшие после захвата снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="e9183-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="e9183-132">Дважды щелкните эскиз, чтобы увеличить его.</span><span class="sxs-lookup"><span data-stu-id="e9183-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведение указателя на снимок экрана" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="e9183-134">Рисунок 4: наведение указателя на снимок экрана</span><span class="sxs-lookup"><span data-stu-id="e9183-134">Figure 4:  Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="e9183-135">Изменение поведения при загрузке</span><span class="sxs-lookup"><span data-stu-id="e9183-135">Change loading behavior</span></span>  

### <span data-ttu-id="e9183-136">Эмуляция первого времени посетителя с помощью отключения кэша браузера</span><span class="sxs-lookup"><span data-stu-id="e9183-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="e9183-137">Чтобы эмулировать, как пользователь попытается получить доступ к сайту, установите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="e9183-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="e9183-138">DevTools отключает кэш браузера.</span><span class="sxs-lookup"><span data-stu-id="e9183-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="e9183-139">Это более точно эмулирует взаимодействие с пользователем при первом запуске, так как запросы размещаются из кэша браузера на повторных посещениях.</span><span class="sxs-lookup"><span data-stu-id="e9183-139">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Флажок "отключить кэш"" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="e9183-141">Рисунок 5: флажок **отключения кэша**</span><span class="sxs-lookup"><span data-stu-id="e9183-141">Figure 5:  The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="e9183-142">Отключение кэша браузера из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="e9183-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="e9183-143">Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте денежные ящики условия сети.</span><span class="sxs-lookup"><span data-stu-id="e9183-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="e9183-144">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="e9183-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e9183-145">Установите или снимите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="e9183-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="e9183-146">Очистка кэша браузера вручную</span><span class="sxs-lookup"><span data-stu-id="e9183-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="e9183-147">Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши в любом месте таблицы запросов и выберите пункт **очистить кэш браузера**).</span><span class="sxs-lookup"><span data-stu-id="e9183-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор очистки кэша браузера" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="e9183-149">Рисунок 6: выбор **очистки кэша браузера**</span><span class="sxs-lookup"><span data-stu-id="e9183-149">Figure 6:  Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-150">Эмуляция в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="e9183-150">Emulate offline</span></span>  

<span data-ttu-id="e9183-151">Новый класс веб-приложений, именуемых [прогрессивными веб-приложениями][DevtoolsProgressiveWebApps], не будет работать в автономном режиме с помощью **обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="e9183-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="e9183-152">Возможно, вам будет удобно быстро смоделировать устройство, которое не имеет подключения к данным, при построении такого типа приложения.</span><span class="sxs-lookup"><span data-stu-id="e9183-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="e9183-153">Щелкните раскрывающееся меню **онлайн** , выполните поиск в разделе " **стили**", а затем выберите пункт в **автономном режиме** , чтобы имитировать полностью автономный режим работы сети.</span><span class="sxs-lookup"><span data-stu-id="e9183-153">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Раскрывающееся меню "автономный режим"" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="e9183-155">Рисунок 7: раскрывающийся список в **автономном режиме**</span><span class="sxs-lookup"><span data-stu-id="e9183-155">Figure 7:  The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-156">Эмуляция медленных сетевых подключений</span><span class="sxs-lookup"><span data-stu-id="e9183-156">Emulate slow network connections</span></span>  

<span data-ttu-id="e9183-157">Эмуляция медленной сети 3G, Fast 3G и других скоростей соединения из раскрывающегося меню **Online** .</span><span class="sxs-lookup"><span data-stu-id="e9183-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Раскрывающееся меню регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="e9183-159">Рисунок 8: раскрывающееся меню **регулирования**</span><span class="sxs-lookup"><span data-stu-id="e9183-159">Figure 8:  The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="e9183-160">Вы можете выбрать один из самых разнообразных наборов параметров, например медленной или скорости 3G.</span><span class="sxs-lookup"><span data-stu-id="e9183-160">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="e9183-161">Вы также можете добавить собственные пользовательские стили, открыв меню регулирования и выбрав пункт **настраиваемое**  >  **Добавление**.</span><span class="sxs-lookup"><span data-stu-id="e9183-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="e9183-162">DevTools отображает значок предупреждения рядом с вкладкой **сеть** , чтобы напомнить вам, что регулирование разрешено.</span><span class="sxs-lookup"><span data-stu-id="e9183-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="e9183-163">Эмуляция медленных сетевых подключений из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="e9183-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="e9183-164">Если вы хотите регулировать сетевое соединение при работе с другими панелями DevTools, используйте денежные ящики условий сети.</span><span class="sxs-lookup"><span data-stu-id="e9183-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="e9183-165">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="e9183-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e9183-166">Выберите нужную скорость соединения в меню **регулирования** .</span><span class="sxs-lookup"><span data-stu-id="e9183-166">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="e9183-167">Очистка файлов cookie браузера вручную</span><span class="sxs-lookup"><span data-stu-id="e9183-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="e9183-168">Чтобы вручную удалить cookie-файлы браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши, где угодно в таблице запросов и выберите команду **Очистить cookie-файлы браузера**).</span><span class="sxs-lookup"><span data-stu-id="e9183-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выбор очистки cookie-файлов браузера" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="e9183-170">Рисунок 9: выбор пункта **"Удалить cookie-файлы браузера"**</span><span class="sxs-lookup"><span data-stu-id="e9183-170">Figure 9:  Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-171">Переопределение агента пользователя</span><span class="sxs-lookup"><span data-stu-id="e9183-171">Override the user agent</span></span>  

<span data-ttu-id="e9183-172">Чтобы вручную переопределить агент пользователя, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-172">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="e9183-173">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="e9183-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e9183-174">Снимите флажок **автоматически**.</span><span class="sxs-lookup"><span data-stu-id="e9183-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="e9183-175">Выберите в меню пункт агента пользователя или введите его в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="e9183-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="e9183-176">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="e9183-176">Filter requests</span></span>  

### <span data-ttu-id="e9183-177">Фильтрация запросов по свойствам</span><span class="sxs-lookup"><span data-stu-id="e9183-177">Filter requests by properties</span></span>  

<span data-ttu-id="e9183-178">С помощью текстового поля **Фильтр** можно отфильтровать запросы по свойствам, таким как домен или размер запроса.</span><span class="sxs-lookup"><span data-stu-id="e9183-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="e9183-179">Если надпись не отображается, возможно, область Фильтры скрыта.</span><span class="sxs-lookup"><span data-stu-id="e9183-179">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="e9183-180">Посмотрите [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="e9183-180">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле "фильтр"" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="e9183-182">Рисунок 10: текстовое поле " **Фильтр** "</span><span class="sxs-lookup"><span data-stu-id="e9183-182">Figure 10:  The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="e9183-183">Вы можете использовать несколько свойств одновременно, разделяя каждое свойство пробелами.</span><span class="sxs-lookup"><span data-stu-id="e9183-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="e9183-184">Например, `mime-type:image/png larger-than:1K` отображает все PNGs, размер которых больше 1 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="e9183-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="e9183-185">Эти фильтры с несколькими свойствами эквивалентны `AND` операциям.</span><span class="sxs-lookup"><span data-stu-id="e9183-185">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="e9183-186">операции в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e9183-186">operations are currently not supported.</span></span>  

<span data-ttu-id="e9183-187">Полный список поддерживаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="e9183-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="e9183-188">Свойство</span><span class="sxs-lookup"><span data-stu-id="e9183-188">Property</span></span> | <span data-ttu-id="e9183-189">Сведения</span><span class="sxs-lookup"><span data-stu-id="e9183-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="e9183-190">Отображать только ресурсы из указанного домена.</span><span class="sxs-lookup"><span data-stu-id="e9183-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="e9183-191">Вы можете использовать подстановочный знак "\ `*` ", чтобы включить несколько доменов.</span><span class="sxs-lookup"><span data-stu-id="e9183-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="e9183-192">Например, `*.com` отображаются ресурсы из всех доменных имен, которые заканчиваются на `.com` .</span><span class="sxs-lookup"><span data-stu-id="e9183-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="e9183-193">DevTools заполняет раскрывающееся меню автозаполнения всеми найденными доменами.</span><span class="sxs-lookup"><span data-stu-id="e9183-193">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="e9183-194">Показать ресурсы, содержащие указанный заголовок HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="e9183-194">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="e9183-195">DevTools заполняет раскрывающийся список автозавершения всеми найденными заголовками ответов.</span><span class="sxs-lookup"><span data-stu-id="e9183-195">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="e9183-196">Используется `is:running` для поиска `WebSocket` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9183-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="e9183-197">Показать ресурсы, размер которых больше указанного (в байтах).</span><span class="sxs-lookup"><span data-stu-id="e9183-197">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="e9183-198">Установка значения эквивалентно значению свойства `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="e9183-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="e9183-199">Показать ресурсы, полученные с помощью указанного типа метода HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9183-199">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="e9183-200">DevTools заполнит раскрывающийся список всех обнаруженных методов HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9183-200">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="e9183-201">Показать ресурсы указанного типа MIME.</span><span class="sxs-lookup"><span data-stu-id="e9183-201">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="e9183-202">DevTools наполняет в раскрывающемся списке все обнаруженные типы MIME.</span><span class="sxs-lookup"><span data-stu-id="e9183-202">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="e9183-203">Показать все смешанные ресурсы контента \ ( `mixed-content:all` \) или только те из них, которые в данный момент отображаются \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="e9183-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="e9183-204">Показать ресурсы, полученные через незащищенные HTTP \ ( `scheme:http` \) или защищенные HTTPS \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="e9183-204">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="e9183-205">Показать ресурсы с `Set-Cookie` заголовком с `Domain` атрибутом, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="e9183-205">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="e9183-206">DevTools заполняет Автозаполнение всеми обнаруженными ими доменами cookie.</span><span class="sxs-lookup"><span data-stu-id="e9183-206">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="e9183-207">Показать ресурсы с `Set-Cookie` заголовком с именем, которое соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="e9183-207">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="e9183-208">DevTools заполняет Автозаполнение всеми именами cookie-файлов, которые были обнаружены.</span><span class="sxs-lookup"><span data-stu-id="e9183-208">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="e9183-209">Показать ресурсы с `Set-Cookie` заголовком со значением, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="e9183-209">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="e9183-210">DevTools заполняет Автозаполнение всеми обнаруженными значениями cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="e9183-210">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="e9183-211">Показать только ресурсы, для которых код состояния HTTP соответствует указанному коду.</span><span class="sxs-lookup"><span data-stu-id="e9183-211">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="e9183-212">DevTools заполнит раскрывающееся меню автозаполнения, содержащее все найденные коды состояния.</span><span class="sxs-lookup"><span data-stu-id="e9183-212">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="e9183-213">Фильтрация запросов по типу</span><span class="sxs-lookup"><span data-stu-id="e9183-213">Filter requests by type</span></span>  

<span data-ttu-id="e9183-214">Чтобы отфильтровать запросы по типу запроса, выберите один из указанных ниже кнопок: **XHR**, **JS**, **CSS**, **img**, **Media**, **Font**, **doc**, **WS** \ (WebSocket \), **Манифест**или **другой** \ (любой другой тип, не указанный здесь) на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e9183-214">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="e9183-215">Если эти кнопки не отображаются, возможно, область фильтров скрыта.</span><span class="sxs-lookup"><span data-stu-id="e9183-215">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="e9183-216">Посмотрите [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="e9183-216">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="e9183-217">Чтобы включить множественные фильтры типов одновременно, удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и выберите.</span><span class="sxs-lookup"><span data-stu-id="e9183-217">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров типов для отображения ресурсов JS, CSS и документов" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="e9183-219">На рисунке 11: использование фильтров типов для отображения ресурсов JS, CSS и документов</span><span class="sxs-lookup"><span data-stu-id="e9183-219">Figure 11:  Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-220">Фильтрация запросов по времени</span><span class="sxs-lookup"><span data-stu-id="e9183-220">Filter requests by time</span></span>  

<span data-ttu-id="e9183-221">Чтобы отобразить только те запросы, которые были активны в течение этого времени, выберите и перетащите его влево или вправо в области "Обзор".</span><span class="sxs-lookup"><span data-stu-id="e9183-221">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="e9183-222">Фильтр является инклюзивным.</span><span class="sxs-lookup"><span data-stu-id="e9183-222">The filter is inclusive.</span></span>  <span data-ttu-id="e9183-223">Отображается любой запрос, который был активен в течение выбранного периода времени.</span><span class="sxs-lookup"><span data-stu-id="e9183-223">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация запросов, которые неактивны вокруг 300ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="e9183-225">Рис. 12: Фильтрация запросов, которые неактивны вокруг 300ms</span><span class="sxs-lookup"><span data-stu-id="e9183-225">Figure 12:  Filtering out any requests that were inactive around 300ms</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-226">Скрыть URL-адреса данных</span><span class="sxs-lookup"><span data-stu-id="e9183-226">Hide data URLs</span></span>  

<span data-ttu-id="e9183-227">[URL-адреса данных][MDNHTTPDataURIs] — это небольшие файлы, внедренные в другие документы.</span><span class="sxs-lookup"><span data-stu-id="e9183-227">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="e9183-228">Любой запрос, который начинается с адреса в таблице запросов, `data:` — это URL-адрес данных.</span><span class="sxs-lookup"><span data-stu-id="e9183-228">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="e9183-229">Установите флажок **скрыть URL-адреса данных** , чтобы скрыть запросы.</span><span class="sxs-lookup"><span data-stu-id="e9183-229">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Флажок "скрыть URL-адреса данных"" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="e9183-231">Рисунок 13: флажок **скрыть URL-адреса данных**</span><span class="sxs-lookup"><span data-stu-id="e9183-231">Figure 13:  The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="e9183-232">Запросы сортировки</span><span class="sxs-lookup"><span data-stu-id="e9183-232">Sort requests</span></span>  

<span data-ttu-id="e9183-233">По умолчанию запросы в таблице запросов сортируются по времени запуска, но вы можете отсортировать таблицу с помощью других условий.</span><span class="sxs-lookup"><span data-stu-id="e9183-233">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="e9183-234">Сортировка по столбцам</span><span class="sxs-lookup"><span data-stu-id="e9183-234">Sort by column</span></span>  

<span data-ttu-id="e9183-235">Выберите верхний колонтитул любого столбца в списке запросы для сортировки запросов по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="e9183-235">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="e9183-236">Этап сортировки по действию</span><span class="sxs-lookup"><span data-stu-id="e9183-236">Sort by activity phase</span></span>  

<span data-ttu-id="e9183-237">Чтобы изменить способ сортировки запросов, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню, наведите указатель мыши на пункт **Каскад**и выберите один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="e9183-237">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="e9183-238">**Время начала**.</span><span class="sxs-lookup"><span data-stu-id="e9183-238">**Start Time**.</span></span>  <span data-ttu-id="e9183-239">Первый инициированный запрос находится наверху.</span><span class="sxs-lookup"><span data-stu-id="e9183-239">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="e9183-240">**Время отклика**.</span><span class="sxs-lookup"><span data-stu-id="e9183-240">**Response Time**.</span></span>  <span data-ttu-id="e9183-241">Первый запрос, загруженный в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="e9183-241">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="e9183-242">**Время окончания**.</span><span class="sxs-lookup"><span data-stu-id="e9183-242">**End Time**.</span></span>  <span data-ttu-id="e9183-243">Первый завершенный запрос вверху.</span><span class="sxs-lookup"><span data-stu-id="e9183-243">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="e9183-244">**Общая длительность**.</span><span class="sxs-lookup"><span data-stu-id="e9183-244">**Total Duration**.</span></span>  <span data-ttu-id="e9183-245">Запрос с наиболее короткой установкой подключения и запросом и ответом в начале.</span><span class="sxs-lookup"><span data-stu-id="e9183-245">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="e9183-246">**Задержка**.</span><span class="sxs-lookup"><span data-stu-id="e9183-246">**Latency**.</span></span>  <span data-ttu-id="e9183-247">Запрос, который ожидает наиболее короткий момент ответа, находится наверху.</span><span class="sxs-lookup"><span data-stu-id="e9183-247">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="e9183-248">В этих описаниях предполагается, что каждый из вариантов имеет приоритет от кратчайшего к наиболее продолжительному.</span><span class="sxs-lookup"><span data-stu-id="e9183-248">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="e9183-249">Если выбрать верхний колонтитул столбца **каскадом** , порядок будет изменен на противоположный.</span><span class="sxs-lookup"><span data-stu-id="e9183-249">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка каскадом по общей длительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="e9183-251">Рисунок 14: Сортировка каскадом по общей длительности \ (светлая часть каждого элемента обходуется временем ожидания, а темная часть — это время, затраченное на загрузку байтов)</span><span class="sxs-lookup"><span data-stu-id="e9183-251">Figure 14:  Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="e9183-252">Анализ запросов</span><span class="sxs-lookup"><span data-stu-id="e9183-252">Analyze requests</span></span>  

<span data-ttu-id="e9183-253">Пока открыто окно DevTools, все запросы будут регистрироваться на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e9183-253">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="e9183-254">Проанализируйте запросы с помощью панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e9183-254">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="e9183-255">Просмотр журнала запросов</span><span class="sxs-lookup"><span data-stu-id="e9183-255">View a log of requests</span></span>  

<span data-ttu-id="e9183-256">С помощью таблицы запросы можно просмотреть журнал всех запросов, выполненных, когда DevTools открыт.</span><span class="sxs-lookup"><span data-stu-id="e9183-256">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="e9183-257">При выборе или наведении указателя мыши на запросы открывается больше сведений о каждом элементе.</span><span class="sxs-lookup"><span data-stu-id="e9183-257">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица запросов" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="e9183-259">Рис. 15: таблица запросы</span><span class="sxs-lookup"><span data-stu-id="e9183-259">Figure 15:  The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="e9183-260">По умолчанию в таблице запросов отображаются следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="e9183-260">The Requests table displays the following columns by default.</span></span>  

*   <span data-ttu-id="e9183-261">**Имя**.</span><span class="sxs-lookup"><span data-stu-id="e9183-261">**Name**.</span></span>  <span data-ttu-id="e9183-262">Имя или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e9183-262">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="e9183-263">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="e9183-263">**Status**.</span></span>  <span data-ttu-id="e9183-264">Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9183-264">The HTTP status code.</span></span>  
*   <span data-ttu-id="e9183-265">**Тип**.</span><span class="sxs-lookup"><span data-stu-id="e9183-265">**Type**.</span></span>  <span data-ttu-id="e9183-266">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="e9183-266">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="e9183-267">**Инициатор**.</span><span class="sxs-lookup"><span data-stu-id="e9183-267">**Initiator**.</span></span>  <span data-ttu-id="e9183-268">Следующие объекты или процессы инициируют запросы:</span><span class="sxs-lookup"><span data-stu-id="e9183-268">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="e9183-269">**Средство синтаксического анализа**.</span><span class="sxs-lookup"><span data-stu-id="e9183-269">**Parser**.</span></span>  <span data-ttu-id="e9183-270">Средство синтаксического анализа HTML для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e9183-270">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="e9183-271">**Redirect (перенаправление**).</span><span class="sxs-lookup"><span data-stu-id="e9183-271">**Redirect**.</span></span>  <span data-ttu-id="e9183-272">Переадресация HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9183-272">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="e9183-273">**Сценарий**.</span><span class="sxs-lookup"><span data-stu-id="e9183-273">**Script**.</span></span>  <span data-ttu-id="e9183-274">Функция JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9183-274">A JavaScript function.</span></span>  
    *   <span data-ttu-id="e9183-275">**Другие**.</span><span class="sxs-lookup"><span data-stu-id="e9183-275">**Other**.</span></span>  <span data-ttu-id="e9183-276">Другие процессы или действия, например переход на страницу с помощью ссылки или ввод URL-адреса в адресную строку.</span><span class="sxs-lookup"><span data-stu-id="e9183-276">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="e9183-277">**Размер**.</span><span class="sxs-lookup"><span data-stu-id="e9183-277">**Size**.</span></span>  <span data-ttu-id="e9183-278">Объединенный размер заголовков ответа и текст ответа, доставленный сервером.</span><span class="sxs-lookup"><span data-stu-id="e9183-278">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="e9183-279">**Time (время**).</span><span class="sxs-lookup"><span data-stu-id="e9183-279">**Time**.</span></span>  <span data-ttu-id="e9183-280">Общая продолжительность от начала запроса до получения последнего байта в ответе.</span><span class="sxs-lookup"><span data-stu-id="e9183-280">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="e9183-281">[**Каскадом**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="e9183-281">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="e9183-282">Визуальная декомпозиция мероприятия для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="e9183-282">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="e9183-283">Добавление и удаление столбцов</span><span class="sxs-lookup"><span data-stu-id="e9183-283">Add or remove columns</span></span>  

<span data-ttu-id="e9183-284">Наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите один из вариантов, чтобы скрыть или отобразить его.</span><span class="sxs-lookup"><span data-stu-id="e9183-284">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="e9183-285">Параметры, отображаемые в данный момент, отмечены флажками рядом с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="e9183-285">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу "запросы"" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="e9183-287">Рисунок 16: Добавление столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="e9183-287">Figure 16:  Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="e9183-288">Добавление настраиваемых столбцов</span><span class="sxs-lookup"><span data-stu-id="e9183-288">Add custom columns</span></span>  

<span data-ttu-id="e9183-289">Чтобы добавить настраиваемый столбец в таблицу запросы, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите **заголовки ответов**  >  .**Управление столбцами заголовков**.</span><span class="sxs-lookup"><span data-stu-id="e9183-289">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемого столбца в таблицу "запросы"" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="e9183-291">Рисунок 17: Добавление настраиваемого столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="e9183-291">Figure 17:  Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-292">Просмотр времени связи между запросами друг на друга</span><span class="sxs-lookup"><span data-stu-id="e9183-292">View the timing of requests in relation to one another</span></span>  

<span data-ttu-id="e9183-293">Используйте Каскад, чтобы просмотреть время связи между запросами друг с другом.</span><span class="sxs-lookup"><span data-stu-id="e9183-293">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="e9183-294">По умолчанию каскадом упорядочиваются по времени начала запросов.</span><span class="sxs-lookup"><span data-stu-id="e9183-294">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="e9183-295">Таким образом, запросы, которые раньше приступили к началу, чем те, которые находятся дальше по правому краю.</span><span class="sxs-lookup"><span data-stu-id="e9183-295">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="e9183-296">Чтобы увидеть различные способы сортировки каскадов, просмотрите [фазу сортировки по действию](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="e9183-296">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец "Каскад" на панели "запросы"" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="e9183-298">Рисунок 18: столбец "Каскад" на панели " **запросы** "</span><span class="sxs-lookup"><span data-stu-id="e9183-298">Figure 18:  The Waterfall column of the **Requests** pane</span></span>  
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

### <span data-ttu-id="e9183-299">Предварительный просмотр тела ответа</span><span class="sxs-lookup"><span data-stu-id="e9183-299">View a preview of a response body</span></span>  

<span data-ttu-id="e9183-300">Чтобы предварительно просмотреть текст ответа, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-300">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="e9183-301">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e9183-301">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e9183-302">Откройте вкладку **Предварительный просмотр** .</span><span class="sxs-lookup"><span data-stu-id="e9183-302">Select the **Preview** tab.</span></span>  

<span data-ttu-id="e9183-303">Эта вкладка особенно полезна для просмотра изображений.</span><span class="sxs-lookup"><span data-stu-id="e9183-303">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Вкладка "предварительный просмотр"" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="e9183-305">На рисунке 19: вкладка " **Предварительный просмотр** "</span><span class="sxs-lookup"><span data-stu-id="e9183-305">Figure 19:  The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-306">Просмотр текста ответа</span><span class="sxs-lookup"><span data-stu-id="e9183-306">View a response body</span></span>  

<span data-ttu-id="e9183-307">Чтобы просмотреть текст ответа на запрос, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-307">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="e9183-308">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e9183-308">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e9183-309">Откройте вкладку **ответ** .</span><span class="sxs-lookup"><span data-stu-id="e9183-309">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Вкладка "ответ"" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="e9183-311">Рисунок 20. Вкладка " **ответ** "</span><span class="sxs-lookup"><span data-stu-id="e9183-311">Figure 20:  The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-312">Просмотр заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="e9183-312">View HTTP headers</span></span>  

<span data-ttu-id="e9183-313">Чтобы просмотреть данные заголовка HTTP для запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-313">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="e9183-314">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e9183-314">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e9183-315">Откройте вкладку **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="e9183-315">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Вкладка "заголовки"" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="e9183-317">Рисунок 21: вкладка " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="e9183-317">Figure 21:  The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="e9183-318">Просмотр источника заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="e9183-318">View HTTP header source</span></span>  

<span data-ttu-id="e9183-319">По умолчанию на вкладке заголовки отображаются имена заголовков в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="e9183-319">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="e9183-320">Чтобы просмотреть имена HTTP-заголовков в том порядке, в котором они были получены:</span><span class="sxs-lookup"><span data-stu-id="e9183-320">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="e9183-321">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="e9183-321">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="e9183-322">См.: [Просмотр заголовков HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="e9183-322">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="e9183-323">Нажмите кнопку **источник**, рядом с разделом **заголовок запроса** или **заголовок ответа** .</span><span class="sxs-lookup"><span data-stu-id="e9183-323">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="e9183-324">Просмотр параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="e9183-324">View query string parameters</span></span>  

<span data-ttu-id="e9183-325">Чтобы просмотреть параметры строки запроса URL-адреса в удобочитаемом формате, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-325">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="e9183-326">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="e9183-326">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="e9183-327">См.: [Просмотр заголовков HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="e9183-327">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="e9183-328">Перейдите к разделу **Параметры строки запроса** .</span><span class="sxs-lookup"><span data-stu-id="e9183-328">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел "параметры строки запроса"" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="e9183-330">Рис. 22: раздел " **Параметры строки запроса** "</span><span class="sxs-lookup"><span data-stu-id="e9183-330">Figure 22:  The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="e9183-331">Просмотр источника параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="e9183-331">View query string parameters source</span></span>  

<span data-ttu-id="e9183-332">Чтобы просмотреть источник параметра строки запроса для запроса:</span><span class="sxs-lookup"><span data-stu-id="e9183-332">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="e9183-333">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="e9183-333">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="e9183-334">Просмотрите [Параметры строки запроса на просмотр](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="e9183-334">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="e9183-335">Нажмите кнопку **Просмотр источника**.</span><span class="sxs-lookup"><span data-stu-id="e9183-335">Select **view source**.</span></span>  

#### <span data-ttu-id="e9183-336">Просмотр строковых параметров запроса в кодировке URL</span><span class="sxs-lookup"><span data-stu-id="e9183-336">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="e9183-337">Чтобы просмотреть параметры строки запроса в удобочитаемом формате, но с сохранением кодировки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-337">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="e9183-338">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="e9183-338">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="e9183-339">Просмотрите [Параметры строки запроса на просмотр](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="e9183-339">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="e9183-340">Выберите команду **Просмотреть закодированный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="e9183-340">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="e9183-341">Просмотр файлов cookie</span><span class="sxs-lookup"><span data-stu-id="e9183-341">View cookies</span></span>  

<span data-ttu-id="e9183-342">Чтобы просмотреть cookie-файлы, отправленные в заголовке HTTP запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-342">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="e9183-343">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e9183-343">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e9183-344">Перейдите на вкладку " **cookie** ".</span><span class="sxs-lookup"><span data-stu-id="e9183-344">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Вкладка "cookie"" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="e9183-346">Рис. 23: вкладка "cookie"</span><span class="sxs-lookup"><span data-stu-id="e9183-346">Figure 23:  The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-347">Просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="e9183-347">View the timing breakdown of a request</span></span>  

<span data-ttu-id="e9183-348">Чтобы просмотреть межвременную разбивку запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-348">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="e9183-349">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="e9183-349">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e9183-350">Откройте вкладку **время** .</span><span class="sxs-lookup"><span data-stu-id="e9183-350">Select the **Timing** tab.</span></span>  

<span data-ttu-id="e9183-351">Дополнительные сведения можно найти в разделе [Предварительный просмотр разбивки времени](#preview-a-timing-breakdown) для доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="e9183-351">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="e9183-352">Дополнительные сведения о каждой из фаз, которые можно увидеть на вкладке время, приведены в разделе [этапы разбиения по времени](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="e9183-352">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Вкладка время" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="e9183-354">Рисунок 24: вкладка **время**</span><span class="sxs-lookup"><span data-stu-id="e9183-354">Figure 24:  The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="e9183-355">Дополнительные сведения о каждой из фаз.</span><span class="sxs-lookup"><span data-stu-id="e9183-355">More information about each of the phases.</span></span>  

<span data-ttu-id="e9183-356">Другие способы доступа к этому представлению можно найти в разделе [Просмотр временных интервалов](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="e9183-356">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="e9183-357">Предварительный просмотр разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="e9183-357">Preview a timing breakdown</span></span>  

<span data-ttu-id="e9183-358">Чтобы просмотреть сведения о разбиении по времени для запроса, наведите указатель мыши на запись запроса в столбце **Каскад** таблицы запросы.</span><span class="sxs-lookup"><span data-stu-id="e9183-358">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="e9183-359">Ознакомьтесь [со](#view-the-timing-breakdown-of-a-request) сведениями о том, как получить доступ к данным, которые не требуют наведения мыши, в запросе.</span><span class="sxs-lookup"><span data-stu-id="e9183-359">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбиения по времени для запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="e9183-361">Рис. 25: предварительный просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="e9183-361">Figure 25:  Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="e9183-362">Описание этапов разделения времени</span><span class="sxs-lookup"><span data-stu-id="e9183-362">Timing breakdown phases explained</span></span>  

<span data-ttu-id="e9183-363">Дополнительные сведения о каждой из фаз, которые можно увидеть на вкладке **время** .</span><span class="sxs-lookup"><span data-stu-id="e9183-363">More information about each of the phases you may see in the **Timing** tab.</span></span>  

*   <span data-ttu-id="e9183-364">**Очереди**.</span><span class="sxs-lookup"><span data-stu-id="e9183-364">**Queueing**.</span></span>  <span data-ttu-id="e9183-365">Браузер помещает запросы в очередь в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="e9183-365">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="e9183-366">Существуют запросы с более высокими приоритетами.</span><span class="sxs-lookup"><span data-stu-id="e9183-366">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="e9183-367">Для этого происхождения уже открыто шесть подключений TCP, что является ограничением.</span><span class="sxs-lookup"><span data-stu-id="e9183-367">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="e9183-368">Применимо только к HTTP/1.0 и HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="e9183-368">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="e9183-369">Браузер временно выделяет место в кэше на диске.</span><span class="sxs-lookup"><span data-stu-id="e9183-369">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="e9183-370">**Ожидание**.</span><span class="sxs-lookup"><span data-stu-id="e9183-370">**Stalled**.</span></span>  <span data-ttu-id="e9183-371">Запрос может быть остановлен в любой из причин, описанных в разделе **очереди**.</span><span class="sxs-lookup"><span data-stu-id="e9183-371">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="e9183-372">**Поиск DNS**.</span><span class="sxs-lookup"><span data-stu-id="e9183-372">**DNS Lookup**.</span></span>  <span data-ttu-id="e9183-373">Браузер разрешает IP-адрес запроса.</span><span class="sxs-lookup"><span data-stu-id="e9183-373">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="e9183-374">**Начальное соединение**.</span><span class="sxs-lookup"><span data-stu-id="e9183-374">**Initial connection**.</span></span>  <span data-ttu-id="e9183-375">Браузер устанавливает подключение, в том числе подтверждения TCP, повторы TCP и согласование SSL.</span><span class="sxs-lookup"><span data-stu-id="e9183-375">The browser is establishing a connection including TCP handshakes, TCP retries, and negotiating an SSL.</span></span>
*   <span data-ttu-id="e9183-376">**Согласование прокси-сервера**.</span><span class="sxs-lookup"><span data-stu-id="e9183-376">**Proxy negotiation**.</span></span>  <span data-ttu-id="e9183-377">Браузер согласовывает запрос с [прокси-сервером][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="e9183-377">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="e9183-378">**Запрос отправлен**.</span><span class="sxs-lookup"><span data-stu-id="e9183-378">**Request sent**.</span></span>  <span data-ttu-id="e9183-379">Запрос отправляется.</span><span class="sxs-lookup"><span data-stu-id="e9183-379">The request is being sent.</span></span>  
*   <span data-ttu-id="e9183-380">**Подготовка ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="e9183-380">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="e9183-381">Браузер запускает сервисный рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="e9183-381">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="e9183-382">**Запросите ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="e9183-382">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="e9183-383">Запрос отправляется сотруднику службы.</span><span class="sxs-lookup"><span data-stu-id="e9183-383">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="e9183-384">**Ожидание \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="e9183-384">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="e9183-385">Браузер ожидает первый байт ответа.</span><span class="sxs-lookup"><span data-stu-id="e9183-385">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="e9183-386">TTFB означает время для первого байта.</span><span class="sxs-lookup"><span data-stu-id="e9183-386">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="e9183-387">Это время включает 1 круговый путь задержки и время, затраченное сервером на подготовку ответа.</span><span class="sxs-lookup"><span data-stu-id="e9183-387">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="e9183-388">**Загрузка содержимого**.</span><span class="sxs-lookup"><span data-stu-id="e9183-388">**Content Download**.</span></span>  <span data-ttu-id="e9183-389">Браузер получает ответ.</span><span class="sxs-lookup"><span data-stu-id="e9183-389">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="e9183-390">**Получение push-уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="e9183-390">**Receiving Push**.</span></span>  <span data-ttu-id="e9183-391">Браузер получает данные для этого ответа через HTTP/2 серверную извещающую передачу.</span><span class="sxs-lookup"><span data-stu-id="e9183-391">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="e9183-392">**Чтение push-уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="e9183-392">**Reading Push**.</span></span>  <span data-ttu-id="e9183-393">Браузер читает локальные данные, полученные ранее.</span><span class="sxs-lookup"><span data-stu-id="e9183-393">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="e9183-394">Просмотр инициаторов и зависимостей</span><span class="sxs-lookup"><span data-stu-id="e9183-394">View initiators and dependencies</span></span>  

<span data-ttu-id="e9183-395">Чтобы просмотреть инициаторы и зависимости запроса, удерживайте `Shift` и наведите указатель мыши на запрос в таблице запросы.</span><span class="sxs-lookup"><span data-stu-id="e9183-395">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="e9183-396">DevTools цвета: инициаторы отображаются зеленым цветом, а зависимости — красным.</span><span class="sxs-lookup"><span data-stu-id="e9183-396">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Просмотр инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="e9183-398">Рис. 26: Просмотр инициаторов и зависимостей запроса</span><span class="sxs-lookup"><span data-stu-id="e9183-398">Figure 26:  Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="e9183-399">Когда таблица запросов упорядочивается в хронологическом порядке, первым зеленым запросом над ним, который вы наводите, является инициатор зависимости.</span><span class="sxs-lookup"><span data-stu-id="e9183-399">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="e9183-400">Если над ним появится еще один зеленый запрос, этот более высокий запрос является инициатором инициатора.</span><span class="sxs-lookup"><span data-stu-id="e9183-400">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="e9183-401">И так далее.</span><span class="sxs-lookup"><span data-stu-id="e9183-401">And so on.</span></span>  

### <span data-ttu-id="e9183-402">Просмотр событий загрузки</span><span class="sxs-lookup"><span data-stu-id="e9183-402">View load events</span></span>  

<span data-ttu-id="e9183-403">DevTools отображает время показа `DOMContentLoaded` `load` событий в нескольких местах на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e9183-403">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="e9183-404">`DOMContentLoaded`Событие окрашивается синим цветом, а `load` событие — красным.</span><span class="sxs-lookup"><span data-stu-id="e9183-404">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположение событий DOMContentLoaded и Load на панели "сеть"" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="e9183-406">На рисунке 27 показано расположение событий " `DOMContentLoaded` и" `load` на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e9183-406">Figure 27:  The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-407">Просмотр общего числа запросов</span><span class="sxs-lookup"><span data-stu-id="e9183-407">View the total number of requests</span></span>  

<span data-ttu-id="e9183-408">Общее количество запросов можно найти в области сводки в нижней части панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e9183-408">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e9183-409">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="e9183-409">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="e9183-410">Если при открытии DevTools возникли другие запросы, эти запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="e9183-410">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее количество запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="e9183-412">Рис. 28: общее количество запросов с момента открытия DevTools</span><span class="sxs-lookup"><span data-stu-id="e9183-412">Figure 28:  The total number of requests since DevTools was opened</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-413">Просмотр общего объема загружаемого файла</span><span class="sxs-lookup"><span data-stu-id="e9183-413">View the total download size</span></span>  

<span data-ttu-id="e9183-414">Общий объем загруженных запросов отображается в области Сводка в нижней части панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="e9183-414">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e9183-415">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="e9183-415">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="e9183-416">Если при открытии DevTools возникли другие запросы, предыдущие запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="e9183-416">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий объем загруженных запросов" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="e9183-418">Рис. 29: общий размер загружаемого запроса.</span><span class="sxs-lookup"><span data-stu-id="e9183-418">Figure 29:  The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="e9183-419">[Просмотр несжатого размера ресурса](#view-the-uncompressed-size-of-a-resource) для просмотра больших ресурсов после того, как браузер распаковывает каждый элемент.</span><span class="sxs-lookup"><span data-stu-id="e9183-419">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="e9183-420">Просмотр трассировки стека, которая привела к запросу</span><span class="sxs-lookup"><span data-stu-id="e9183-420">View the stack trace that caused a request</span></span>  

<span data-ttu-id="e9183-421">После того, как инструкция JavaScript запрашивает ресурс, наведите указатель мыши на столбец **инициатора** , чтобы просмотреть трассировку стека, выступающей в запрос.</span><span class="sxs-lookup"><span data-stu-id="e9183-421">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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
   <span data-ttu-id="e9183-423">На рисунке 30 показана трассировка стека, ведущая к запросу ресурсов</span><span class="sxs-lookup"><span data-stu-id="e9183-423">Figure 30:  The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-424">Просмотр несжатого размера ресурса</span><span class="sxs-lookup"><span data-stu-id="e9183-424">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="e9183-425">Установите флажок **использовать строки большого запроса** , а затем посмотрите на нижнее значение столбца **Размер** .</span><span class="sxs-lookup"><span data-stu-id="e9183-425">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример несжатых ресурсов" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="e9183-427">Рисунок 31: пример несжатых ресурсов \ (сжатый размер `jquery-3.3.1.min.js` файла, отправленного по сети `29.9 KB` , в то время как несжатый размер `84.9 KB` )</span><span class="sxs-lookup"><span data-stu-id="e9183-427">Figure 31:  An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="e9183-428">Данные запросов на экспорт</span><span class="sxs-lookup"><span data-stu-id="e9183-428">Export requests data</span></span>  

### <span data-ttu-id="e9183-429">Сохранение всех сетевых запросов в файле HAR</span><span class="sxs-lookup"><span data-stu-id="e9183-429">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="e9183-430">Чтобы сохранить все сетевые запросы в файле HAR, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e9183-430">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="e9183-431">Наведите указатель мыши на любой запрос в таблице запросов и откройте контекстное меню (щелкните правой кнопкой мыши \).</span><span class="sxs-lookup"><span data-stu-id="e9183-431">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="e9183-432">Выберите команду **Сохранить как HAR с содержимым**.</span><span class="sxs-lookup"><span data-stu-id="e9183-432">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="e9183-433">DevTools сохраняет все запросы, произошедшие после того, как вы открыли DevTools в файл HAR.</span><span class="sxs-lookup"><span data-stu-id="e9183-433">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="e9183-434">Невозможно отфильтровать запросы или сохранить только один запрос.</span><span class="sxs-lookup"><span data-stu-id="e9183-434">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="e9183-435">После того как вы сохраните файл HAR, вы можете импортировать его обратно в DevTools для анализа.</span><span class="sxs-lookup"><span data-stu-id="e9183-435">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="e9183-436">Просто перетащите файл HAR в таблицу запросы.</span><span class="sxs-lookup"><span data-stu-id="e9183-436">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Выбор команды "Сохранить как HAR с контентом"" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="e9183-438">Рисунок 32: выбор команды " **Сохранить как HAR с контентом** "</span><span class="sxs-lookup"><span data-stu-id="e9183-438">Figure 32:  Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-439">Копирование одного или нескольких запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="e9183-439">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="e9183-440">В столбце **имя** таблицы запросы наведите указатель мыши на запрос, откройте контекстное меню (щелкните правой кнопкой мыши \), наведите указатель на пункт **Копировать**и выберите один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="e9183-440">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

*   <span data-ttu-id="e9183-441">**Копировать адрес ссылки**.</span><span class="sxs-lookup"><span data-stu-id="e9183-441">**Copy Link Address**.</span></span>  <span data-ttu-id="e9183-442">Скопируйте URL-адрес запроса в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="e9183-442">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="e9183-443">**Копирование ответа**.</span><span class="sxs-lookup"><span data-stu-id="e9183-443">**Copy Response**.</span></span>  <span data-ttu-id="e9183-444">Скопировать текст ответа в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="e9183-444">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="e9183-445">**Копировать как выборку**.</span><span class="sxs-lookup"><span data-stu-id="e9183-445">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="e9183-446">**Копировать как фигуру**.</span><span class="sxs-lookup"><span data-stu-id="e9183-446">**Copy as cURL**.</span></span>  <span data-ttu-id="e9183-447">Копирование запроса в виде текстовой команды.</span><span class="sxs-lookup"><span data-stu-id="e9183-447">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="e9183-448">**Копировать все как выборку**.</span><span class="sxs-lookup"><span data-stu-id="e9183-448">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="e9183-449">**Скопировать все как фигуру**.</span><span class="sxs-lookup"><span data-stu-id="e9183-449">**Copy All as cURL**.</span></span>  <span data-ttu-id="e9183-450">Копирование всех запросов в виде последовательности команд с фигурой.</span><span class="sxs-lookup"><span data-stu-id="e9183-450">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="e9183-451">**Копировать все как HAR**.</span><span class="sxs-lookup"><span data-stu-id="e9183-451">**Copy All as HAR**.</span></span>  <span data-ttu-id="e9183-452">Скопируйте все запросы как данные HAR.</span><span class="sxs-lookup"><span data-stu-id="e9183-452">Copy all requests as HAR data.</span></span>  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выбор пункта "Копировать ответ"" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="e9183-454">Рисунок 33: выбор пункта " **Копировать ответ** "</span><span class="sxs-lookup"><span data-stu-id="e9183-454">Figure 33:  Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="e9183-455">Изменение макета панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="e9183-455">Change the layout of the Network panel</span></span>  

<span data-ttu-id="e9183-456">Вы можете развернуть или свернуть разделы пользовательского интерфейса панели "сеть", чтобы сосредоточиться на важных сведениях.</span><span class="sxs-lookup"><span data-stu-id="e9183-456">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="e9183-457">Скрытие области фильтров</span><span class="sxs-lookup"><span data-stu-id="e9183-457">Hide the Filters pane</span></span>  

<span data-ttu-id="e9183-458">По умолчанию в DevTools отображается **область фильтров**.</span><span class="sxs-lookup"><span data-stu-id="e9183-458">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="e9183-459">Щелкните фильтр **фильтра** ![ ][ImageFilterIcon] , чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="e9183-459">Select **Filter** ![Filter][ImageFilterIcon] to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка "скрыть фильтры"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="e9183-461">Рисунок 34: кнопка "скрыть фильтры"</span><span class="sxs-lookup"><span data-stu-id="e9183-461">Figure 34:  The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-462">Использование строк большого запроса</span><span class="sxs-lookup"><span data-stu-id="e9183-462">Use large request rows</span></span>  

<span data-ttu-id="e9183-463">Используйте большие строки, если вы хотите, чтобы в таблице сетевых запросов больше пробелов.</span><span class="sxs-lookup"><span data-stu-id="e9183-463">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="e9183-464">Некоторые столбцы также содержат дополнительные сведения при использовании больших строк.</span><span class="sxs-lookup"><span data-stu-id="e9183-464">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="e9183-465">Например, минимальное значение столбца « **Размер** » — это несжатый размер запроса.</span><span class="sxs-lookup"><span data-stu-id="e9183-465">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример строк большого запроса в области "запросы"" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="e9183-467">Рисунок 35: пример строк большого запроса в области " **запросы** "</span><span class="sxs-lookup"><span data-stu-id="e9183-467">Figure 35:  An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="e9183-468">Установите флажок **использовать строки большого запроса** , чтобы включить большие строки.</span><span class="sxs-lookup"><span data-stu-id="e9183-468">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Флажок "использовать строки большого запроса"" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="e9183-470">Рисунок 36: флажок " **использовать строки большого запроса** "</span><span class="sxs-lookup"><span data-stu-id="e9183-470">Figure 36:  The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="e9183-471">Скрытие области обзора</span><span class="sxs-lookup"><span data-stu-id="e9183-471">Hide the Overview pane</span></span>  

<span data-ttu-id="e9183-472">По умолчанию в DevTools отображается **область "Общие сведения**".</span><span class="sxs-lookup"><span data-stu-id="e9183-472">By default, DevTools shows the **Overview pane**.</span></span>  <span data-ttu-id="e9183-473">Снимите флажок **Показать общие сведения** , чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="e9183-473">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Флажок "Показать общие сведения"" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="e9183-475">Рисунок 37: флажок **Показать общие сведения**</span><span class="sxs-lookup"><span data-stu-id="e9183-475">Figure 37:  The **Show Overview** checkbox</span></span>  
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
> <span data-ttu-id="e9183-479">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e9183-479">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e9183-480">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e9183-480">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e9183-482">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e9183-482">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
